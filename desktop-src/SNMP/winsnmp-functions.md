---
title: Функции WinSNMP
description: Функции, используемые с функцией WinSNMP, делятся на следующие функциональные группы. Ниже приведен алфавитный список.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c5ebb49e8ec56c0d0b1174fd667d847c09d3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134175"
---
# <a name="winsnmp-functions"></a>Функции WinSNMP

\[Протокол SNMP доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого используйте [Служба удаленного управления Windows](/windows/desktop/WinRM/portal), который является реализацией Microsoft WS-Man.\]

Функции, используемые с функцией WinSNMP, делятся на следующие функциональные группы. Ниже приведен алфавитный список.

-   [Функции связи](#winsnmp-communications-functions)
-   [Функции сущностей и контекста](#winsnmp-entity-and-context-functions)
-   [Функции базы данных](#winsnmp-database-functions)
-   [Функции PDU](#winsnmp-pdu-functions)
-   [Служебные функции](#winsnmp-utility-functions)
-   [Функции привязки переменных](#winsnmp-variable-binding-functions)
-   [Функции WinSNMP, алфавитный список](/windows)

## <a name="winsnmp-communications-functions"></a>Функции WinSNMP Communications

Функции WinSNMP Communications предоставляют интерфейс между вызывающим приложением WinSNMP и реализацией Microsoft WinSNMP. Реализация обрабатывает взаимодействие между приложением и другими сущностями управления.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>снмпканцелмсг</strong></a></td>
<td>Запрашивает, что реализация Microsoft WinSNMP отменит попытки повторной передачи и уведомления о времени ожидания для сообщения запроса SNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>снмпклеануп</strong></a></td>
<td>Информирует реализацию о том, что приложение отключается и больше не требует выделения ресурсов.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>снмпклеанупекс</strong></a></td>
<td>Выполняет очистку при отсутствии невыполненных успешных вызовов <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>снмпстартуп</strong></a> или <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>Снмпстартупекс</strong></a> в приложении WinSNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>снмпклосе</strong></a></td>
<td>Включает реализацию для освобождения ресурсов, связанных с сеансом, и для закрытия механизмов связи.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>снмпкреатесессион</strong></a></td>
<td>Запрашивает реализацию для открытия сеанса WinSNMP и выделения ресурсов и механизмов связи. При разработке новых приложений WinSNMP рекомендуется вызвать функцию <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>снмпкреатесессион</strong></a> , чтобы открыть объект WinSNMP Session вместо вызова функции <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>снмпопен</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>снмплистен</strong></a></td>
<td>Регистрирует или отменяет регистрацию приложения WinSNMP в качестве агента SNMP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>снмпопен</strong></a></td>
<td>Запрашивает реализацию для открытия сеанса WinSNMP и выделения ресурсов и механизмов связи. При разработке новых приложений WinSNMP рекомендуется вызвать функцию <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>снмпкреатесессион</strong></a> , чтобы открыть объект WinSNMP Session вместо вызова функции <strong>снмпопен</strong> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>снмпреквмсг</strong></a></td>
<td>Возвращает сообщения SNMP и необработанные данные и уведомления о ловушках.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>снмпрегистер</strong></a></td>
<td>Информирует реализацию, которую приложение должно зарегистрировать или отменить регистрацию для ловушек и уведомлений.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>снмпсендмсг</strong></a></td>
<td>Запрашивает передачу блока данных протокола в реализации.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>снмпстартуп</strong></a></td>
<td>Уведомляет реализацию о необходимости выполнения процедур инициализации для приложения. Приложение должно успешно вызвать функцию <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>снмпстартуп</strong></a> перед вызовом любой другой функции WinSNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>снмпстартупекс</strong></a></td>
<td>Уведомляет реализацию Microsoft WinSNMP, что приложению WinSNMP требуются службы реализации. <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>Снмпстартупекс</strong></a> обеспечивает поддержку нескольких независимых программных модулей, использующих WinSNMP в одном приложении.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></td>
<td>Уведомляет сеанс WinSNMP о том, что доступно сообщение SNMP или асинхронное событие.
<blockquote>
[!Note]<br />
Эта функция обратного вызова применяется только к сеансам, открытым в результате вызова функции <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>снмпкреатесессион</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a>Функции WinSNMP Entity и context

Функции WinSNMP Entity и context позволяют приложению WinSNMP указывать понятные имена для объектов SNMP и контекстов. В реализации Microsoft WinSNMP имя преобразуется в компоненты со своей базой в SNMPv2C или в базе данных реализации.



| Функция                                     | Описание                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**снмпконтексттостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Возвращает строку, определяющую контекст SNMP (набор ресурсов управляемого объекта).                                  |
| [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Возвращает строку, идентифицирующую сущность управления SNMP.                                                            |
| [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Высвобождает ресурсы, выделенные функцией [**снмпстртоконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) для контекста SNMP.         |
| [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Высвобождает ресурсы, выделенные функцией [**снмпстртоентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) для СУЩНОСТИ управления SNMP. |
| [**снмпсетпорт**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Изменяет порт, назначенный целевой сущности SNMP.                                                               |
| [**снмпстртоконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Возвращает обработчик сведений о контексте SNMP, характерный для реализации.                                   |
| [**снмпстртоентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Возвращает маркер для сведений об объекте управления SNMP, характерном для реализации.                         |



 

## <a name="winsnmp-database-functions"></a>Функции WinSNMP базы данных

Функции WinSNMP Database предоставляют WinSNMP приложение с доступом к текущим параметрам в хранилище административной информации в реализации Microsoft WinSNMP. Эти функции допускают изменение режима повторной передачи и режима преобразования сущностей и контекста. Функции базы данных также предоставляют приложению возможность управлять значениями времени ожидания и числа повторных попыток.



| Функция                                               | Описание                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**снмпжетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Возвращает текущее значение режима повторной передачи.                                               |
| [**снмпжетретри**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Возвращает значение счетчика повторных попыток повторной передачи запросов сообщений SNMP.             |
| [**снмпжеттимеаут**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Возвращает значение времени ожидания в сотых долях секунды для передачи запросов сообщений SNMP. |
| [**снмпжеттранслатемоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Возвращает текущее значение режима преобразования объекта и контекста.                               |
| [**снмпжетвендоринфо**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Извлекает сведения, идентифицирующие поставщика WinSNMP.                                             |
| [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Изменяет режим повторной передачи.                                                                      |
| [**снмпсетретри**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Изменяет значение счетчика повторных попыток повторной передачи запросов сообщений SNMP.                        |
| [**снмпсеттимеаут**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Изменяет значение времени ожидания для передачи запросов сообщений SNMP.                             |
| [**снмпсеттранслатемоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Изменяет режим преобразования сущностей и контекста.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>Функции WinSNMP PDU

Функции WinSNMP PDU позволяют приложениям WinSNMP извлекать и обновлять элементы данных (или поля) PDU. Сюда входят устройства PDU, возвращенные вызовом функции [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) или функции [**снмпдекодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) . Функции PDU также создают устройства PDU для использования в функциях [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) и [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .



| Функция                                     | Описание                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Создает и инициализирует блок данных протокола SNMP.                                                                                                                               |
| [**снмпдупликатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Дублирует единицу данных протокола SNMP.                                                                                                                                            |
| [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Освобождает ресурсы, связанные с единицей данных протокола SNMP, созданной функцией [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) или [**снмпдупликатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) . |
| [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Возвращает выбранные элементы данных из указанной единицы данных протокола SNMP.                                                                                                          |
| [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Обновляет выбранные элементы данных в указанной единице данных протокола SNMP.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>Функции WinSNMP Utility

Служебные функции WinSNMP позволяют приложению WinSNMP управлять объектами и сообщениями SNMP через интерфейс WinSNMP.



| Функция                                         | Описание                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**снмпдекодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Декодирует закодированное или сериализованное сообщение SNMP в составляющие его компоненты.                                      |
| [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Создает закодированное сообщение SNMP.                                                                                    |
| [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Сигнализирует реализации Microsoft WinSNMP, что она должна освободить память, выделенную для определенного дескриптора. |
| [**снмпжетластеррор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Возвращает значение кода последней ошибки для последней операции SNMP.                                                      |
| [**снмпоидкомпаре**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Сравнивает два идентификатора объектов SNMP.                                                                               |
| [**снмпоидкопи**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Копирует идентификатор объекта SNMP.                                                                                   |
| [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Преобразует внутреннее двоичное представление идентификатора объекта SNMP в формат числовой строки с точками.       |
| [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Преобразует формат числовых строк с точками для идентификатора объекта SNMP в его внутреннее двоичное представление.       |



 

## <a name="winsnmp-variable-binding-functions"></a>Функции привязки WinSNMP Variable

Функции привязки WinSNMP Variable позволяют приложениям WinSNMP создавать списки привязок переменных и управлять ими, а также включать их в устройства PDU.



| Функция                                     | Описание                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**снмпкаунтвбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Перечисляет записи привязки переменных в указанном списке привязок переменных.                                                                                                   |
| [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Создает новый список привязок переменных.                                                                                                                                            |
| [**снмпделетевб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Удаляет запись привязки переменной из списка привязок переменных.                                                                                                                  |
| [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Копирует список привязок переменных.                                                                                                                                                 |
| [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Высвобождает ресурсы для списка привязок переменных, выделенного ранее функцией [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) или [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . |
| [**снмпжетвб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Извлекает сведения из указанной записи привязки переменной.                                                                                                                  |
| [**снмпсетвб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Изменяет записи привязки переменных в списке привязок переменных; добавляет новые записи привязки переменных в существующий список привязок переменных.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Функции WinSNMP, алфавитный список

-   [**\_обратный вызов снмпапи**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**снмпканцелмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**снмпклеануп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**снмпклосе**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**снмпконтексттостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**снмпкаунтвбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**снмпкреатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**снмпкреатесессион**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**снмпкреатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**снмпдекодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**снмпделетевб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**снмпдупликатепду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**снмпдупликатевбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**снмпенкодемсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**снмпентититостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**снмпжетластеррор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**снмпжетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**снмпжетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**снмпжетретри**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**снмпжеттимеаут**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**снмпжеттранслатемоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**снмпжетвб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**снмпжетвендоринфо**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**снмплистен**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**снмпоидкомпаре**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**снмпоидкопи**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**снмпоидтостр**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**снмпопен**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**снмпреквмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**снмпрегистер**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**снмпсендмсг**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**снмпсетпдудата**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**снмпсетпорт**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**снмпсетретрансмитмоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**снмпсетретри**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**снмпсеттимеаут**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**снмпсеттранслатемоде**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**снмпсетвб**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**снмпстартуп**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**снмпстртоконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**снмпстртоентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**снмпстртуид**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

