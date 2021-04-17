---
title: Функции управления сетью
description: Функции управления сетью можно группировать следующим образом.
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a169d097fbe86c95aa9aa3120c3f732a8edd2c0
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/21/2020
ms.locfileid: "105681712"
---
# <a name="network-management-functions"></a>Функции управления сетью

Функции управления сетью можно группировать следующим образом.

## <a name="alert-functions"></a>Функции предупреждений



| Функция                                   | Описание                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**неталертраисе**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Уведомляет всех зарегистрированных клиентов о том, что произошло определенное событие.                                                                                                                                  |
| [**неталертраисикс**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Упрощает уведомление зарегистрированных клиентов о том, что произошло определенное событие, поскольку, в отличие от **неталертраисе**, **Неталертраисикс** не требует стандартных структур [**\_ предупреждений**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) . |



 

## <a name="api-buffer-functions"></a>Функции буфера API



| Функция                                                 | Описание                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**нетапибуффераллокате**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Выделяет память из кучи. Вызывайте эту функцию, если требуется совместимость с функцией **нетапибуфферфри** . |
| [**нетапибуфферфри**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Освобождает память, выделенную функцией **нетапибуффераллокате** и другими функциями управления сетью.                   |
| [**нетапибуфферреаллокате**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Изменяет размер буфера, выделенного вызовом функции **нетапибуффераллокате** .                                |
| [**нетапибуфферсизе**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Возвращает размер (в байтах) буфера, выделенного путем вызова функции **нетапибуффераллокате** .                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Azure Active Directory функции присоединиться к информации



| Функция                                                       | Описание                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**нетфриааджоининформатион**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | Освобождает память, выделенную для указанной структуры [**\_ \_ сведений о соединении дсрег**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) , которая содержит сведения о соединении для клиента и, полученные путем вызова функции [**нетжетааджоининформатион**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) . |
| [**нетжетааджоининформатион**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | Извлекает сведения о соединении для указанного клиента. Эта функция проверяет сведения о соединении для Microsoft Azure Active Directory и рабочую учетную запись, добавленную текущим пользователем.                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>Функции службы каталогов и присоединение к домену



| Функция                                                                             | Описание                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**нетаддалтернатекомпутернаме**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | Добавляет альтернативное имя для указанного компьютера.                                                                                                                                                                                                                      |
| [**неткреатепровисионингпаккаже**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | Подготавливает учетную запись компьютера для последующего использования в операции присоединение к автономному домену.                                                                                                                                                                                        |
| [**нетенумератекомпутернамес**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | Перечисляет имена для указанного компьютера.                                                                                                                                                                                                                            |
| [**нетжетжоинаблеаус**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | Извлекает список подразделений (OU), в которых может быть создана учетная запись компьютера.                                                                                                                                                                              |
| [**нетжетжоининформатион**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | Возвращает сведения о состоянии присоединение для указанного компьютера.                                                                                                                                                                                                           |
| [**нетжоиндомаин**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | Присоединяет компьютер к Рабочей группе или домену.                                                                                                                                                                                                                              |
| [**нетпровисионкомпутераккаунт**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | Подготавливает учетную запись компьютера для последующего использования в операции присоединение к автономному домену.                                                                                                                                                                                       |
| [**нетремовеалтернатекомпутернаме**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | Удаляет альтернативное имя указанного компьютера.                                                                                                                                                                                                                   |
| [**нетренамемачинеиндомаин**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | Изменяет имя компьютера в домене.                                                                                                                                                                                                                             |
| [**нетрекуестоффлинедомаинжоин**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | Выполняется локально на компьютере для изменения образа операционной системы Windows, подключенного к тому. Реестр загружается для образа и подготовка данных большого двоичного объекта записывается там, где их можно получить на этапе завершения операции присоединения к автономному домену.     |
| [**нетрекуестпровисионингпаккажеинсталл**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | Выполняется локально на компьютере для изменения образа операционной системы Windows, подключенного к тому. Реестр загружается из образа, и данные пакета подготовки записываются там, где их можно получить на этапе завершения операции присоединения к автономному домену. |
| [**нетсетпримарикомпутернаме**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | Задает имя основного компьютера для указанного компьютера.                                                                                                                                                                                                              |
| [**нетунжоиндомаин**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Отсоединение компьютера от рабочей группы или домена.                                                                                                                                                                                                                        |
| [**нетвалидатенаме**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | Проверка допустимости имени компьютера, имени Рабочей группы или имени домена.                                                                                                                                                                                               |



 

## <a name="get-functions"></a>Получение функций



| Функция                                                               | Описание                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**нетжетанидкнаме**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Возвращает имя любого контроллера домена для домена, который напрямую является доверенным для указанного сервера.                                   |
| [**нетжетдкнаме**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Возвращает имя основного контроллера домена (PDC) для указанного домена.                                                        |
| [**нетжетдисплайинформатиониндекс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Возвращает индекс первой записи отображаемой информации, имя которой начинается с указанной строки или в алфавитном порядке за строкой. |
| [**неткуеридисплайинформатион**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Возвращает сведения об учетной записи пользователя, компьютера или глобальной группы.                                                                             |



 

## <a name="group-functions"></a>Групповые функции



| Функция                                     | Описание                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**нетграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Создает глобальную группу.                                                           |
| [**нетграупаддусер**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Добавляет одного пользователя в существующую глобальную группу.                                        |
| [**нетграупдел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Удаляет глобальную группу независимо от того, содержит ли группа какие-либо члены.                  |
| [**нетграупделусер**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Удаляет одно имя пользователя из глобальной группы.                                        |
| [**нетграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Список всех глобальных групп на сервере.                                              |
| [**нетграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Возвращает сведения о конкретной глобальной группе.                              |
| [**нетграупжетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Список всех членов определенной глобальной группы.                                   |
| [**нетграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Задает общие сведения о глобальной группе.                                    |
| [**нетграупсетусерс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Назначает члены новой глобальной группе; заменяет члены существующей группы. |



 

## <a name="local-group-functions"></a>Функции локальной группы



| Функция                                                   | Описание                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**нетлокалграупадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Создает локальную группу.                                                  |
| [**нетлокалграупаддмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Добавляет одного или нескольких пользователей или глобальные группы в существующую локальную группу.     |
| [**нетлокалграупдел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Удаляет локальную группу, удаляя все существующие члены группы.    |
| [**нетлокалграупделмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Удаляет один или несколько членов из существующей локальной группы.               |
| [**нетлокалграупенум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Возвращает сведения о каждой учетной записи локальной группы на сервере.         |
| [**нетлокалграупжетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Возвращает сведения об определенной учетной записи локальной группы на сервере. |
| [**нетлокалграупжетмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Список всех членов указанной локальной группы.                           |
| [**нетлокалграупсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Задает общие сведения о локальной группе.                           |
| [**нетлокалграупсетмемберс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Назначает члены локальной группе.                                       |



 

## <a name="message-functions"></a>Функции сообщений



| Функция                                               | Описание                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**нетмессажебуфферсенд**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Отправляет сообщение в псевдоним зарегистрированного сообщения.                                  |
| [**нетмессаженамеадд**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Регистрирует псевдоним сообщения в таблице имен сообщений.                            |
| [**нетмессаженамедел**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Удаляет псевдоним сообщения из таблицы имен сообщений.                            |
| [**нетмессаженаминум**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Список всех псевдонимов сообщений, хранящихся в таблице имен сообщений.                 |
| [**нетмессаженамежетинфо**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Возвращает сведения о конкретном псевдониме сообщения в таблице имен сообщений. |



 

## <a name="netfile-functions"></a>Функции Нетфиле



| Функция                                | Описание                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**нетфилеклосе**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Принудительное закрытие ресурса.                                          |
| [**нетфилинум**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Возвращает сведения об открытых файлах на сервере.                    |
| [**нетфилежетинфо**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Возвращает сведения об определенном открытии ресурса сервера. |



 

## <a name="remote-utility-functions"></a>Удаленные служебные функции



| Функция                                                       | Описание                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**нетремотекомпутерсуппортс**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | Запрашивает у перенаправителя получение дополнительных функций, поддерживаемых удаленной системой. |
| [**нетремотетод**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | Позволяет приложениям получать доступ к сведениям о времени суток на удаленном сервере.          |



 

## <a name="schedule-functions"></a>Функции планирования



| Функция                                                                     | Описание                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**нетсчедулежобадд**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Отправляет задание для выполнения в указанную будущую дату и время.        |
| [**нетсчедулежобдел**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Отменяет ряд заданий, поставленных в очередь для запуска на компьютере.             |
| [**нетсчедулежобенум**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Список заданий, поставленных в очередь на указанном компьютере.                   |
| [**нетсчедулежобжетинфо**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Возвращает сведения о конкретном задании, поставленном в очередь на компьютере. |
| [**жетнетсчедулеаккаунтинформатион**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Возвращает имя учетной записи службы AT.                           |
| [**сетнетсчедулеаккаунтинформатион**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Задает имя учетной записи службы AT и пароль.                   |



 

## <a name="server-functions"></a>Функции сервера



| Функция                                       | Описание                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**нетсервердискенум**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Возвращает список локальных дисков на сервере.                                   |
| [**нетсерверенум**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Список всех видимых серверов определенного типа (или типов) в указанном домене. |
| [**нетсервержетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Возвращает сведения о конфигурации указанного сервера.                        |
| [**нетсерверсетинфо**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Задает параметры операционной системы для сервера.                                        |



 

## <a name="server-and-workstation-transport-functions"></a>Транспортные функции сервера и рабочей станции



| Функция                                                     | Описание                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**нетсерверкомпутернамеадд**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Привязывает имя эмулированного сервера к каждому транспортному протоколу, на котором активен сервер. (Сочетает функциональные возможности функции [**нетсервертранспортенум**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) и функции [**нетсервертранспортаддекс**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) .)                                            |
| [**нетсерверкомпутернамедел**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Отключает каждый сетевой транспортный протокол из имени эмулированного сервера, установленного предыдущим вызовом функции **нетсерверкомпутернамеадд** .                                                                                                                                                                               |
| [**нетсервертранспортадд**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Привязывает указанный сервер к транспортному протоколу. (Эта функция поддерживает только уровень информации о [**\_ транспортном сервере \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) .)                                                                                                                                                |
| [**нетсервертранспортаддекс**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Привязывает указанный сервер к транспортному протоколу. (Эта расширенная функция поддерживает уровни информации о транспортном [**сервере \_ \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**сервере \_ \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)и [**\_ транспортном сервере \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) .) |
| [**нетсервертранспортдел**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Отключает транспортный протокол от сервера.                                                                                                                                                                                                                                                                         |
| [**нетсервертранспортенум**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Перечисляет транспортные протоколы, управляемые сервером.                                                                                                                                                                                                                                                                   |
| [**нетвкстатранспортенум**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | Список транспортных протоколов, управляемых перенаправитель.                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>Использование функций



| Функция                               | Описание                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**нетусеадд**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Создает подключение между локальным компьютером и сервером.                               |
| [**нетуседел**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Завершает подключение к общему ресурсу.                                                   |
| [**нетусинум**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Список всех текущих подключений между локальным компьютером и ресурсами на удаленных серверах. |
| [**нетусежетинфо**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Возвращает сведения о подключении к общему ресурсу.                              |



 

## <a name="user-functions"></a>Пользовательские функции



| Функция                                               | Описание                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**нетусерадд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Добавляет учетную запись пользователя и назначает пароль и уровень привилегий.     |
| [**нетусерчанжепассворд**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Изменяет пароль пользователя для указанного сетевого сервера или домена. |
| [**нетусердел**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Удаляет учетную запись пользователя с сервера.                             |
| [**нетусеренум**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Выводит список всех учетных записей пользователей на сервере.                                |
| [**нетусержетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Возвращает список имен глобальных групп, к которым принадлежит пользователь.       |
| [**нетусержетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Возвращает сведения об определенной учетной записи пользователя на сервере.    |
| [**нетусержетлокалграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Возвращает список имен локальных групп, к которым принадлежит пользователь.        |
| [**нетусерсетграупс**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Задает членство в глобальных группах для указанной учетной записи пользователя.         |
| [**нетусерсетинфо**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Задает пароль и другие элементы учетной записи пользователя.             |



 

## <a name="user-modals-functions"></a>Пользовательские функции модальных функций



| Функция                                     | Описание                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**нетусермодалсжет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Возвращает глобальные сведения для всех пользователей и глобальных групп в базе данных безопасности, которая является базой данных диспетчера учетных записей безопасности (SAM) или, в случае контроллеров домена, Active Directory. |
| [**нетусермодалссет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Задает глобальные сведения для всех пользователей и глобальных групп в базе данных безопасности.                                                                                                                       |



 

## <a name="validation-functions"></a>Функции проверки



| Функция                                                               | Описание                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**нетвалидатепассвордполицифри**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Освобождает память, выделенную функцией [**нетвалидатепассвордполици**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) для параметра *аутпутарг* ,                                                                                      |
| [**нетвалидатепассвордполици**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Позволяет приложению проверять соответствие паролей для базы данных учетных записей, предоставляемой приложением, и проверять, что пароли соответствуют сложности, сроку давности, минимальной длине и повторному использованию журналов, предъявляемым политикой паролей. |



 

## <a name="workstation-and-workstation-user-functions"></a>Пользовательские функции рабочих станций и рабочих станций



| Функция                                           | Описание                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**нетвкстажетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | Возвращает сведения об элементах конфигурации для рабочей станции.             |
| [**нетвкстасетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | Настраивает рабочую станцию.                                                           |
| [**нетвкстаусеренум**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Выводит сведения обо всех пользователях, которые в данный момент вошли на рабочую станцию.           |
| [**нетвкстаусержетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Возвращает сведения об одном пользователе, вошедшем в систему.                             |
| [**нетвкстаусерсетинфо**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Задает сведения об отдельных пользователях для элементов конфигурации рабочей станции. |



 

## <a name="obsolete-functions"></a>Устаревшие функции

-   [**нетакцессадд**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**нетакцессчекк**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**нетакцессдел**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**нетакцессенум**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**нетакцессжетинфо**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**нетакцессжетусерпермс**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**нетакцесссетинфо**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**нетаудитклеар**](netauditclear.md)
-   [**нетаудитреад**](netauditread.md)
-   [**нетаудитврите**](netauditwrite.md)
-   [**нетконфигжет**](netconfigget.md)
-   [**нетконфигжеталл**](netconfiggetall.md)
-   [**нетконфигсет**](netconfigset.md)
-   [**нетеррорлогклеар**](neterrorlogclear.md)
-   [**нетеррорлогреад**](neterrorlogread.md)
-   [**нетеррорлогврите**](neterrorlogwrite.md)
-   [**нетлокалграупаддмембер**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**нетлокалграупделмембер**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**нетсервицеконтрол**](netservicecontrol.md)
-   [**нетсервицеенум**](netserviceenum.md)
-   [**нетсервицежетинфо**](netservicegetinfo.md)
-   [**нетсервицеинсталл**](netserviceinstall.md)
-   [**нетвкстатранспортадд**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**нетвкстатранспортдел**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сетевые функции Windows](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 