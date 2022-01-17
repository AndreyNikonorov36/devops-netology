     <<Домашнее задание к лекции №5
  < 1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.
Решение:
git show aefea 
aefead220 Update CHANGELOG.md
Ответ:
aefead220
Update CHANGELOG.md

   < 2. Какому тегу соответствует коммит 85024d3?
Решение:
git show 85024
commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)
   < 3. Сколько родителей у коммита b8d720? Напишите их хеши.
Решение:
1 вариант:
git show --pretty=format:' %P' b8d720
 56cd7859e05c36c06b56d013b55a252d0bb7e158 9ea88f22fc6269854151c571162c5bcf958bee2b

    < 4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.
Решение:
git log  v0.12.23..v0.12.24  --oneline
33ff1c03b (tag: v0.12.24) v0.12.24
b14b74c49 [Website] vmc provider links
3f235065b Update CHANGELOG.md
6ae64e247 registry: Fix panic when server is unreachable
5c619ca1b website: Remove links to the getting started guide's old location
06275647e Update CHANGELOG.md
d5f9411f5 command: Fix bug when using terraform login on Windows
4b6d06cc5 Update CHANGELOG.md
dd01a3507 Update CHANGELOG.md
225466bc3 Cleanup after v0.12.23 release
    < 5. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).
Решение:
git log -S'func providerSource' --oneline
5af1e6234 main: Honor explicit provider_installation CLI config when present
8c928e835 main: Consult local directories as potential mirrors of providers

   < 6. Кто автор функции synchronizedWriters?
Решение:
git log -S'func synchronizedWriters' --pretty=format:'%h - %an %ae'
bdfea50cc - James Bardin j.bardin@gmail.com
5ac311e2a - Martin Atkins mart@degeneration.co.uk