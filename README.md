# .github
Правила работы с репозиториями

# Команды
Каждый разработчик для доступа к репозиторию должен находится в соответствующей команде. Если репозиторий для бэкенда, значит разработчик должен находиться в команде бэкендеров для написания нового кода. Аналогично с фронтэндерами. Здесь пока что только 2 команды. Можно состоять в обоих. Если необходимы какие-то изменения в командах - писать в телеграме @m1ker1n. 

# Репозитории
Изначально 2 репозитория: front, back. Если есть необходимость создать новый репозиторий - писать в телеграме @m1ker1n.

# Ветки
В каждом репозитории должно быть как минимум 2 ветки: main/master и develop. 

Семантика main/master: код, который уже используется на продуктовом сервере. Обычно редко обновляется. Если обновляется, то на новую <b>стабильную</b> версию. Обновляется <b>ТОЛЬКО</b> при помощи Pull Request'ов из ветки <b>develop</b> (в крайнем случае из ветки hotfix/\*). 

Семантика develop: код, который используется/будет использован на сервере для разработчиков. Обновляется по мере написания новых функций, исправления старых. Обновляется <b>ТОЛЬКО</b> при помощи Pull Request'ов из веток <b>feature/\*</b> и <b>fix/\*</b>.

Семантика feature/fix: код, который содержит реализацию/исправление <b>одной элементарной</b> функции. Обновляется путем обычных коммитов в эту ветку. Создаются разработчиками. Желательно иметь короткое название фичи или код фичи (если есть).

# Важно
Так как мы используем бесплатную версию организации в GitHub, а репозитории приватные, то нет возможности защитить ветки от пуша в main/master и develop. Поэтому, пожалуйста, смотрите правило выше и проверяйте перед написанием кода, в какой ветке находитесь.

# Pull Request'ы
Лаконичное название. Подробное описание: какую фичу сделали, что именно затронули, как эту фичу использовать. 

После создания Pull Request'а сообщаете своей команде/проверяющему: "Я сделал \*это\*. Ссылка: \*ссылка\*". Проверяющий проверяет и либо отправляет на доработку, либо одобряет и мерджит в develop.

Когда фича доделана, скорее всего ваша ветка будет позади от девелопа (как никак параллельная разработка). Вам нужно привести вашу ветку в порядок таким образом, чтобы можно было сразу замерджить в develop. Для этого обычно используется следующий алгоритм:

1) Скачать изменения develop'а из удаленного репозитория
2) Перенести свою ветку на последний коммит develop'а (который уже будет совпадать с последним коммитом удаленного репозитория)

Возможно потребуется разрешать конфликты, возникшие в результате переноса ветки. Предлагается заниматься этим каждый раз перед тем, как начинается писать код, чтобы через неделю не тратить целый день на разрешение конфликтов.

Если одной командой: 

``` bash
# Находясь в своей ветке
git  pull --rebase origin develop
``` 

Если есть сомнения - можно попробовать воссоздать свою ситуацию тут: https://learngitbranching.js.org

Или обратиться к кому-нибудь за помощью.

# Коммиты
Желательно много и поменьше, чтобы можно было зайти в ветку, посмотреть историю коммитов этой ветки и понять по названиям коммитов, что сделали. Если не получается описать кратко в названии, используйте описание коммита. 
