1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea
_____________________________________________________________________________
-       отв:  aefead2207ef7e2aa5dc81a34aedf0cad4c32545 , Update CHANGELOG.md
-       Использовал команды: 
-       git log --pretty=format:"%H , %s" | grep ^aefea
-       git show aefea  
_____________________________________________________________________________

2. Какому тегу соответствует коммит 85024d3 ?
_____________________________________________
-       отв: v0.12.23
-       Использовал команду:"git show 85024d3 -s"
_______________________________________________________

3. Сколько родителей у коммита b8d720 ? Напишите их хеши.
_________________________________________________________
-       отв:    56cd7859e05c36c06b56d013b55a252d0bb7e158   9ea88f22fc6269854151c571162c5bcf958bee2b
-       Использовал команду: git log --pretty=%P -n 1 "b8d720"
___________________________________________________________________________________________ 
   
4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.
_____________________________________________________________________________________________________
-       отв:
-       33ff1c03bb960b332be3af2e333462dde88b279e (tag: v0.12.24) v0.12.24
-       b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links
-       3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md
-       6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable
-       5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location
-       06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md
-       d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows
-       4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md
-       dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md
-       225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release
+	Использовал команду: git log --pretty=oneline v0.12.23...v0.12.24
_____________________________________________________________________________________________________
    
5. Найдите коммит в котором была создана функция func providerSource, 
   ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).
_________________________________________________________________________________________________________
-       отв:
-       5af1e6234 main: Honor explicit provider_installation CLI config when present
-       8c928e835 main: Consult local directories as potential mirrors of providers
-       Использовал команды:
-       git show 5af1e6234
-       git show 8c928e835
____________________________________________________________________________________

6. Найдите все коммиты в которых была изменена функция globalPluginDirs.
________________________________________________________________________
-       отв "Будет состоять из Комитов и Хеш":
-       78b122055   78b12205587fe839f10d946ea3fdc06719decb05
-       52dbf9483   52dbf94834cb970b510f2fba853a5b49ad9b1a46 
-       41ab0aef7   41ab0aef7a0fe030e84018973a64135b11abcd70
-       66ebff90c   66ebff90cdfaa6938f26f908c7ebad8d547fea17
-       8364383c3   8364383c359a6b738a436d1b7745ccdce178df47
-       
-       Использовал команды:
-       git grep -e "globalPluginDirs"
-       git log -L :globalPluginDirs:plugins.go
____________________________________________________________

7. Кто автор функции synchronizedWriters?
_________________________________________
-       отв:
-       git log -S "func synchronizedWriters" --oneline
-       git show 5ac311e2a
-       Автором является: Martin Atkins <mart@degeneration.co.uk>
