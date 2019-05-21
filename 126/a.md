A: Changing a Character
問題文のとおりに文字列の K 番目の文字を小文字に変換すればよいです。
As the statement says, the problem can be solved by just converting the K-th character of the string to lower case.

A, B, C の 3 文字のみが入力に含まれるので if 文を 3 個書いてもよいですし、アルファベットの大文字と小文字の文字コードが 32 異なるということを利用して char 型の該当する文字に 32 を加えても良いです。
Since only 3 kinds of letters are included in the input, you can convert the letter by writing 'if' statement 3 times, or adding 32 to the letter using the fact that ASCII codes of lower and upper case characters are different by 32.
C++ での実装例は以下の通りです (include 等は省いています)。
A code examples in C++ is as follows.
char in[55];
int main(){
int a,b;scanf("%d%d",&a,&b);
scanf("%s",in);
in[b-1]+=32;
printf("%s\n",in);
}

