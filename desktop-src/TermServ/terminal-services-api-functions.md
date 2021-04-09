---
title: Функции API службы удаленных рабочих столов
description: Для службы удаленных рабочих столов используются следующие функции.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94a2168f5ad4501b9725b72923c98ea97cc707c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792133"
---
# <a name="remote-desktop-services-api-functions"></a>Функции API службы удаленных рабочих столов

Для службы удаленных рабочих столов используются следующие функции.

## <a name="in-this-section"></a>Содержание раздела

<dl> <dt>

[**процессидтосессионид**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Извлекает службы удаленных рабочих столов сеанс, связанный с указанным процессом.

</dd> <dt>

[**тлсконнекттолссервер**](tlsconnecttolsserver.md)
</dt> <dd>

Открывает маркер указанного сервера лицензий удаленный рабочий стол.

</dd> <dt>

[**тлсдисконнектфромсервер**](tlsdisconnectfromserver.md)
</dt> <dd>

Закрывает открытый маркер для сервера лицензий удаленный рабочий стол.

</dd> <dt>

[**тлсжетсерверцертификате**](tlsgetservercertificate.md)
</dt> <dd>

Возвращает сертификат сервера лицензирования удаленный рабочий стол.

</dd> <dt>

[**тлскэйпаккенумбегин**](tlskeypackenumbegin.md)
</dt> <dd>

Начинает перечисление всех ключевых пакетов, установленных на сервере лицензий удаленный рабочий стол на основе условий поиска.

</dd> <dt>

[**тлскэйпаккенуменд**](tlskeypackenumend.md)
</dt> <dd>

Переходит от предыдущего вызова функции [**тлскэйпаккенумбегин**](tlskeypackenumbegin.md) и завершает перечисление.

</dd> <dt>

[**тлскэйпаккенумнекст**](tlskeypackenumnext.md)
</dt> <dd>

Переходит от предыдущего вызова функции [**тлскэйпаккенумбегин**](tlskeypackenumbegin.md) и возвращает следующий пакет ключей, установленный на сервере лицензирования удаленный рабочий стол, который соответствует условиям поиска.

</dd> <dt>

[**тлслиценсинумбегин**](tlslicenseenumbegin.md)
</dt> <dd>

Начинает перечисление лицензий, выданных сервером лицензий удаленный рабочий стол на основе условий поиска.

</dd> <dt>

[**тлслиценсинуменд**](tlslicenseenumend.md)
</dt> <dd>

Переходит от предыдущего вызова функции [**тлслиценсинумбегин**](tlslicenseenumbegin.md) и завершает перечисление.

</dd> <dt>

[**тлслиценсинумнекст**](tlslicenseenumnext.md)
</dt> <dd>

Продолжение предыдущего вызова функции [**тлслиценсинумбегин**](tlslicenseenumbegin.md) и возврат следующей лицензии, установленной на сервере лицензирования удаленный рабочий стол, соответствующем условиям поиска.

</dd> <dt>

[**виртуалчаннелклосе**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Закрывает клиентский узел виртуального канала.

</dd> <dt>

[**виртуалчаннелентри**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Определяемая приложением точка входа для клиентской библиотеки DLL приложения, использующего службы удаленных рабочих столов виртуальные каналы.

</dd> <dt>

[**виртуалчаннелинит**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Инициализирует доступ клиентской библиотеки DLL к службы удаленных рабочих столов виртуальным каналам.

</dd> <dt>

[*виртуалчаннелинитевент*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Определяемая приложением функция обратного вызова, службы удаленных рабочих столов вызовов для уведомления клиентской библиотеки о событиях виртуального канала.

</dd> <dt>

[**виртуалчаннелопен**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Открывает клиентский узел виртуального канала.

</dd> <dt>

[*виртуалчаннелопеневент*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Определяемая приложением функция обратного вызова, которая службы удаленных рабочих столов вызовы для уведомления клиентской библиотеки событий для определенного виртуального канала.

</dd> <dt>

[**виртуалчаннелврите**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Отправляет данные с клиентской стороны виртуального канала в приложение-партнер на стороне сервера.

</dd> <dt>

[**втсклосесервер**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Закрывает открытый маркер на сервере узла сеансов удаленный рабочий стол.

</dd> <dt>

[**втсконнектсессион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Подключает сеанс службы удаленных рабочих столов к существующему сеансу на локальном компьютере.

</dd> <dt>

[**втскреателистенер**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Создает новый прослушиватель службы удаленных рабочих столов или настраивает существующий прослушиватель.

</dd> <dt>

[**втсдисконнектсессион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Отключает вошедшего в систему пользователя из указанного сеанса службы удаленных рабочих столов, не закрывая сеанс.

</dd> <dt>

[**втсенаблечилдсессионс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Включает или отключает [дочерние сеансы](child-sessions.md).

</dd> <dt>

[**втсенумерателистенерс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Перечисление всех прослушивателей службы удаленных рабочих столов на сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втсенумератепроцессес**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Извлекает сведения об активных процессах на указанном сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втсенумератепроцессесекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Извлекает сведения об активных процессах на указанном сервере узла сеансов удаленных рабочих столов или на сервере узла виртуализации удаленных рабочих столов (Узел виртуализации удаленных рабочих столов).

</dd> <dt>

[**втсенумератесерверс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Возвращает список всех серверов узлов сеансов удаленных рабочих столов в указанном домене.

</dd> <dt>

[**втсенумератесессионс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Получает список сеансов на сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втсенумератесессионсекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Получает список сеансов на указанном сервере узла сеансов удаленных рабочих столов или сервере узла виртуализации удаленных рабочих столов.

</dd> <dt>

[**втсфримемори**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Освобождает память, выделенную функцией службы удаленных рабочих столов.

</dd> <dt>

[**втсфримеморекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

Освобождает память, содержащую [**сведения о \_ процессе \_ \_ ВТС**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) , а также структуры [**\_ сеанса \_ \_ 1 ВТС**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) , выделенные функцией службы удаленных рабочих столов.

</dd> <dt>

[**втсжетактивеконсолесессионид**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Возвращает идентификатор сеанса консоли.

</dd> <dt>

[**втсжетчилдсессионид**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Возвращает идентификатор дочернего сеанса, если он есть.

</dd> <dt>

[**втсжетлистенерсекурити**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Возвращает дескриптор безопасности прослушивателя службы удаленных рабочих столов.

</dd> <dt>

[**втсисчилдсессионсенаблед**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

Определяет, включены ли дочерние сеансы.

</dd> <dt>

[**втслогоффсессион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

Записывает в журнал указанный сеанс службы удаленных рабочих столов.

</dd> <dt>

[**втсопенсервер**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

Открывает обработчик для указанного сервера узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втсопенсерверекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Открывает обработчик для указанного сервера узла сеансов удаленных рабочих столов или сервера узла виртуализации удаленных рабочих столов.

</dd> <dt>

[**втскуерилистенерконфиг**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Извлекает сведения о конфигурации для прослушивателя службы удаленных рабочих столов.

</dd> <dt>

[**втскуерисессионинформатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Извлекает сведения о сеансе для указанного сеанса на указанном сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втскуерюсерконфиг**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Извлекает сведения о конфигурации указанного пользователя на указанном контроллере домена или сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втскуерюсертокен**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

Получает основной маркер доступа пользователя, выполнившего вход в систему, заданный ИДЕНТИФИКАТОРом сеанса.

</dd> <dt>

[**втсрегистерсессионнотификатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

Регистрирует указанное окно для получения уведомлений об изменениях сеанса.

</dd> <dt>

[**втсрегистерсессионнотификатионекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

Регистрирует указанное окно для получения уведомлений об изменениях сеанса.

</dd> <dt>

[**втссендмессаже**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

Отображает окно сообщения на клиентском компьютере указанного сеанса службы удаленных рабочих столов.

</dd> <dt>

[**втссетлистенерсекурити**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Настраивает дескриптор безопасности прослушивателя службы удаленных рабочих столов.

</dd> <dt>

[**втссетусерконфиг**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Изменяет сведения о конфигурации для указанного пользователя на указанном контроллере домена или на сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втсшутдовнсистем**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Завершает работу (и при необходимости перезапускает) указанного сервера узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втсстартремотеконтролсессион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Запускает Удаленное управление другим сеансом службы удаленных рабочих столов. Эту функцию необходимо вызывать из удаленного сеанса.

</dd> <dt>

[**втсстопремотеконтролсессион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Останавливает сеанс удаленного управления.

</dd> <dt>

[**втстерминатепроцесс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Завершает указанный процесс на указанном сервере узла сеансов удаленных рабочих столов.

</dd> <dt>

[**втсунрегистерсессионнотификатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

Отменяет регистрацию указанного окна, чтобы он не получал дальнейшие уведомления об изменении сеанса.

</dd> <dt>

[**втсунрегистерсессионнотификатионекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Отменяет регистрацию указанного окна, чтобы он не получал дальнейшие уведомления об изменении сеанса.

</dd> <dt>

[**втсвиртуалчаннелклосе**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Закрывает открытый маркер виртуального канала.

</dd> <dt>

[**втсвиртуалчаннелопен**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Открывает обработчик для указанного виртуального канала на сервере.

</dd> <dt>

[**втсвиртуалчаннелопенекс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Создает виртуальный канал таким же образом, как и [**втсвиртуалчаннелопен**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).

</dd> <dt>

[**втсвиртуалчаннелпуржеинпут**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Удаляет из указанного виртуального канала все входные данные очереди, отправленные с клиента на сервер.

</dd> <dt>

[**втсвиртуалчаннелпуржеаутпут**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Удаляет из указанного виртуального канала все выходные данные в очереди, отправленные с сервера клиенту.

</dd> <dt>

[**втсвиртуалчаннелкуери**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Возвращает сведения об указанном виртуальном канале.

</dd> <dt>

[**втсвиртуалчаннелреад**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Считывает данные с конца виртуального канала на сервере.

</dd> <dt>

[**втсвиртуалчаннелврите**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Записывает данные на серверный конец виртуального канала.

</dd> <dt>

[**втсваитсистемевент**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Ожидает события службы удаленных рабочих столов перед возвратом вызывающему объекту.

</dd> </dl>

 

 