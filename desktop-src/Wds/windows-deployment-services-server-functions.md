---
title: Функции сервера служб развертывания Windows
description: В API-интерфейсе PXE-сервера служб развертывания Windows используются следующие функции.
ms.assetid: b6089ff9-4d74-4f5d-957f-4a741c09f4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3852ecfd3e51d6375ca8d566f78d019e733808ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411295"
---
# <a name="windows-deployment-services-server-functions"></a>Функции сервера служб развертывания Windows

В API-интерфейсе PXE-сервера служб развертывания Windows используются следующие функции.



| Функция                                                           | Описание                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**пксеасинкреквдоне**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone)                       | Возвращает асинхронные результаты запроса клиента.                                                                                |
| [**пкседхкпаппендоптион**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoption)                 | Добавляет параметр DHCP к ответному пакету.                                                                                     |
| [**пкседхкпаппендоптионрав**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpappendoptionraw)           | Добавляет параметр DHCP к ответному пакету.                                                                                     |
| [**пкседхкпжетоптионвалуе**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetoptionvalue)             | Извлекает значение параметра из пакета DHCP.                                                                                  |
| [**пкседхкпжетвендороптионвалуе**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpgetvendoroptionvalue) | Извлекает значение параметра из поля сведений об определенном поставщике (43) пакета DHCP.                                    |
| [**пкседхкпинитиализе**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpinitialize)                     | Инициализирует ответный пакет как пакет ответа DHCP.                                                                          |
| [**пкседхкписвалид**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpisvalid)                           | Проверяет, является пакет DHCP-пакетом.                                                                                      |
| [**пксежетсерверинфо**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfo)                       | Возвращает сведения о PXE-сервере.                                                                                      |
| [**пксепаккеталлокате**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate)                     | Выделяет пакет для отправки с помощью функции [**пксесендрепли**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) .                                          |
| [**пксепаккетфри**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketfree)                             | Освобождает пакет, выделенный функцией [**пксепаккеталлокате**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxepacketallocate) .                                       |
| [**пксепровидеренумклосе**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumclose)               | Закрывает перечисление поставщиков, открытых функцией [**пксепровидеренумфирст**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst) .               |
| [**пксепровидеренумфирст**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumfirst)               | Запускает перечисление зарегистрированных поставщиков.                                                                                 |
| [**пксепровидеренумнекст**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext)                 | Перечисляет зарегистрированные поставщики.                                                                                               |
| [**пксепровидерфриинфо**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderfreeinfo)                 | Освобождает память, выделенную функцией [**пксепровидеренумнекст**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderenumnext) .                                     |
| [*пксепровидеринитиализе*](pxeproviderinitialize.md)               | Экспорт из библиотеки динамической компоновки (DLL) поставщика, которая инициализирует поставщик и подготавливает его для получения запросов клиентов. |
| [**пксепровидеркуериндекс**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderqueryindex)             | Возвращает индекс указанного поставщика в списке зарегистрированных поставщиков.                                               |
| [*пксепровидеррекврекуест*](pxeproviderrecvrequest.md)             | Вызывается при получении запроса от клиента.                                                                               |
| [**пксепровидеррегистер**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderregister)                 | Регистрирует поставщик в системе.                                                                                          |
| [*пксепровидерсервицеконтрол*](pxeproviderservicecontrol.md)       | Вызывается, когда служба WDS получает код управления службой.                                                             |
| [**пксепровидерсетаттрибуте**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)         | Задает атрибуты для поставщика.                                                                                         |
| [*пксепровидершутдовн*](pxeprovidershutdown.md)                   | Вызывается для завершения работы поставщика.                                                                                               |
| [**пксепровидерунрегистер**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeproviderunregister)             | Удаляет поставщик из списка зарегистрированных поставщиков.                                                                      |
| [**пксерегистеркаллбакк**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)                 | Регистрирует функции обратного вызова для различных событий уведомления.                                                                |
| [**пксесендрепли**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)                               | Отправляет пакет в клиентский запрос.                                                                                            |
| [**пксетраце**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxetrace)                                       | Добавляет запись трассировки в журнал PXE.                                                                                             |



 

Доступны следующие возможности, начиная с Windows 8 и Windows Server 2012.

| Функция                                                               | Описание                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**PxeDhcpv6AppendOption**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoption)                 | Добавляет параметр DHCPv6 к ответному пакету.                                                  |
| [**PxeDhcpv6AppendOptionRaw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6appendoptionraw)           | Добавляет параметр DHCPv6 к ответному пакету.                                                  |
| [**PxeDhcpv6GetOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getoptionvalue)             | Извлекает значение параметра из DHCPv6-пакета.                                               |
| [**PxeDhcpv6GetVendorOptionValue**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6getvendoroptionvalue) | Извлекает значения параметров из поля "параметр \_ поставщика" \_ (17) пакета DHCPv6.          |
| [**PxeDhcpv6Initialize**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6initialize)                     | Инициализирует ответный пакет как ответный пакет DHCPv6.                                       |
| [**PxeDhcpv6IsValid**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6isvalid)                           | Проверяет, что пакет является допустимым пакетом DHCPv6.                                             |
| [**пксежетсерверинфоекс**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxegetserverinfoex)                       | Возвращает сведения о PXE-сервере.                                                     |
| [**PxeDhcpv6ParseRelayForw**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6parserelayforw)             | Позволяет поставщику анализировать сообщения РЕТРАНСЛЯТОРа-ФОРВ и их вложенные сообщения о ПАРАМЕТРах \_ ретранслятора \_ . |
| [**PxeDhcpv6CreateRelayRepl**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxedhcpv6createrelayrepl)           | Создает сообщение RELAY-REPL.                                                               |



 

 

 




