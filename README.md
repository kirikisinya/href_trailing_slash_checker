##概要##
href属税の末尾のスラッシュの有無をチェックするツール。
レンダリング後のHTMLを解析するのではなく、ソースファイル中のhref属性を探し、
検索条件に合うものを洗い出す。

##実行方法##

`sh href_trailing_slash_checker.sh '/path/to/dir(=>ココで指定したディレクトリ以下を検索対象とします)'`

##オプション##

*-c: ヒットした行数のみを表示します
（href属性の数ではなく、それらが含まれる行数であることに注意。1行に2つ含まれていた場合は1つにカウントされる）

*-s: 末尾スラッシュ有り/無しを指定  
　　-s0:末尾スラッシュ無し  
　　-s1:末尾スラッシュ有り  
　　このオプションを指定しない場合、末尾スラッシュ有り/無し両方を検索します。
　　
*-h: ヘルプを表示


###実行例###

`sh href_trailing_slash_checker.sh -s1 /home/kiriki/flowers`
/home/kiriki/flowersディレクトリ以下で末尾がスラッシュ有りのhref属性がある行を表示

`sh href_trailing_slash_checker.sh -c -s0 /home/kiriki/animals`
/home/kiriki/animalsディレクトリ以下で末尾がスラッシュ無しのhref属性を含む件数を表示


##テストコード##

    cd tests
    sh href_trailing_slash_check.test.sh

エラーが起きなければ（何も表示されなければ）大丈夫。エラー起きたら教えてください。
