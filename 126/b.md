# B: YYMM or MMYY
まず、与えられる入力を長さ 4 の文字列とみなしたとき、前半 2 文字から 2 桁の整数と後半 2 文字から 2 桁の整数に変換してみましょう。例えば前半 2 文字から 2 桁の整数に変換するのは、 `(s[0]-’0’)*10+s[1]-’0’` などと計算することで得られます。  
First, let us consider the input as a string of length 4. Then we can convert first half 2 characters to a 2-digit number and convert the second half 2 characters as well. For example, conversion of first half 2 characters to a 2-digit number can be done by calculating `(s[0] - '0')*10 + s[1] - '0'`.

代わりの手段として、入力が数字列であるため、これを整数とみなし、4 桁の整数から 2 桁の整数を 2 つ取り出すこともできます。この場合では、前半の 2 桁の整数は例えば `a/100` 、後半の 2 桁の整数は `a%100` となります。  
Plan B(As an alternative), since the input is an array of numbers, considering it as an integer, we can extract 2 of 2-digit number from the input. In this case, the first half 2-digit number is converted by `a/100`, and the second half is by `a%100`.

その後、各種フォーマットの条件を満たすかを判定します。  
After that, we judge whether numbers satisfy conditions of formats.
* YYMM フォーマットであるためには、後半の 2 桁の整数が 1 以上 12 以下である必要があります。  
To be YYMM format, the second half 2-digit integer must be between 1 and 12.
* MMYY フォーマットであるためには、前半の 2 桁の整数が 1 以上 12 以下である必要があります。    
To be MMYY format,  the first half 2-digit integer must be between 1 and 12.

上の 2 つを判定することで、4 つの答えのうちどれであるかが決まります。  
By checking the above two conditions, we can decide the answer from four possible answers.

C++ での実装例は以下の通りです。  
The sample code in C++ is as follows.
