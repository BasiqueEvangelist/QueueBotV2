# QueueBotV2
Refactored version of SimpleQueueBot, which now can be used normally.

# Документация
Префикс бота - '!'.

Ниже обязательные аргументы будут обозначаться как `<argument>`, а опциональные - как `{argument}`.

При написании команд НЕ нужно писать символы `<>{}`, они будут игнорированы/интерпретированы неверно!

`!help` - помощь по командам (перенаправляет сюда).

`!ping` - выводит текущую задержку бота.

`!version` - выводит текущую версию бота (или любую не особо важную информацию, которую я туда прописал).

`!create <name>` - создаёт очередь с именем name, если это имя ещё не занято.

`!delete <name>` - удаляет очередь с именем name, если очередь с таким именем существует и отправитель имеет права создателя этой очереди.

`!rename <name> <new_name>` - изменяет имя очереди name на new_name, если очередь с таким именем существует и отправитель имеет права создателя этой очереди.

`!transfer <name> <candidate>` - передаёт права создателя очереди name пользователю candidate, если очередь с таким именем существует и отправитель имеет права создателя этой очереди.

`!promote <name> <candidate>` - выдаёт права администратора очереди name пользователю candidate, если очередь с таким именем существует, отправитель имеет права создателя этой очереди и candidate ещё не является администратором этой очереди.

`!demote <name> <candidate>` - забирает права администратора очереди name у пользователя candidate, если очередь с таким именем существует, отправитель имеет права создателя этой очереди и candidate является администратором этой очереди.

`!join <name> {candidate}` - если candidate не указан, присоединяет отправителя в конец очереди name. Если candidate указано и отправитель имеет права администратора в очереди name, присоединяет candidate в конец очереди name.

`!leave <name> {candidate}` - если candidate не указан, удаляет отправителя из очереди name. Если candidate указано и отправитель имеет права администратора в очереди name, удаляет candidate из очереди name.

`!next <name>` - если очередь name не пуста и отправитель имеет права администратора очереди name, вызывает на сдачу первого человека в очереди name.

`!clear <name>` - если отправитель имеет права администратора очереди name, очищает очередь name.

`!all {page}` - выводит краткую информацию по всем существующим очередям (дефолтное значение page - 0, выводит по 10 очередей на каждой странице).

`!info <name>` - выводит подробную информацию об очереди name.

# Контакты
По всем вопросам писать в Discord: `tiom4eg#1219`.
