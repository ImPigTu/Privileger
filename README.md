# Privileger

## RU
Privileger позволяет вам максимально просто работать с привилегиями в ОС Windows. Присутствуют следующие режимы:

1. Добавить привилегии аккаунту. Реализовано через взаимодействие с LSA посредством функции LSA `LsaAddAccountRights()`:

2. Запустить процесс, добавив в его токен конкретную привилегию. Реализовано с помощью функций `ImpersonateSelf()`, `OpenThreadToken()`. `AdjustTokenPrivileges()`, `CreateProcessWithTokenW()`:



3. Удалить у пользователя привилегию. Осуществляется через взаимодействие с LSA посредством функции LSA `LsaRemoveAccountRights()`:


4. Режим поиска. Позволяет обнаруживать на конкретном компьютере объекты, обладающие какой-либо привилегией. Делается через `LsaEnumerateAccountsWithUserRight()`:


5. С помощью данного режима вы сможете перечислить все привилегии, которые назначены конкретному аккаунту. Реализовано через `LsaEnumerateAccountRights()`:



## EN
Privileger allows you to work with privileges in Windows as easily as possible. There are different modes:
1. Add privileges to an account. Implemented through interaction with the LSA via the LSA function `LsaAddAccountRights()`:

2. Start a process by adding a specific privilege to its token. Implemented by `ImpersonateSelf()`, `OpenThreadToken()`. `AdjustTokenPrivileges()`, `CreateProcessWithTokenW()`:


3. Remove privilege from the user. Performed through interaction with the LSA via the LSA `LsaRemoveAccountRights()` function:


4. Search mode. Allows to detect objects with some privileges on a particular computer. This is done through `LsaEnumerateAccountsWithUserRight()`:


5. With this mode you can list all the privileges that are assigned to a particular account. Implemented through `LsaEnumerateAccountRights()`:
