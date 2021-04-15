---
title: Функции API WebDAV
description: В API WebDAV используются следующие функции.
ms.assetid: 489cdc17-aca8-4621-bc61-f0f3b9ac22b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1917cd6ebb64470eec6fde9188cc39341142fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710137"
---
# <a name="webdav-api-functions"></a>Функции API WebDAV

В API WebDAV используются следующие функции.



| Функция                                                             | Описание                                                                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**даваддконнектион**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection)                         | Создает безопасное подключение к серверу WebDAV или к удаленному файлу или каталогу на сервере WebDAV.                                                                                                                                   |
| [*даваускаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback)                                | Клиент WebDAV вызывает функцию обратного вызова [*даваускаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) , определяемую приложением, чтобы запросить у пользователя учетные данные.                                                                                           |
| [**давканцелконнектионстосервер**](/windows/desktop/api/davclnt/nf-davclnt-davcancelconnectionstoserver) | Закрывает все подключения к серверу WebDAV или к удаленному файлу или каталогу на сервере WebDAV.                                                                                                                                        |
| [**давделетеконнектион**](/windows/desktop/api/davclnt/nf-davclnt-davdeleteconnection)                   | Закрывает соединение, созданное с помощью функции [**даваддконнектион**](/windows/desktop/api/davclnt/nf-davclnt-davaddconnection) .                                                                                                                              |
| [**давфлушфиле**](/windows/desktop/api/davclnt/nf-davclnt-davflushfile)                                 | Сбрасывает данные из локальной версии удаленного файла на сервер WebDAV.                                                                                                                                                        |
| [*давфрикредкаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred)                        | Клиент WebDAV вызывает функцию обратного вызова [*давфрикредкаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback_freecred) , определяемую приложением, чтобы освободить учетные данные, полученные функцией обратного вызова [*даваускаллбакк*](/windows/desktop/api/Davclnt/nc-davclnt-pfndavauthcallback) . |
| [**давжетекстендедеррор**](/windows/desktop/api/davclnt/nf-davclnt-davgetextendederror)                   | Возвращает сведения о расширенном коде ошибки, возвращенном сервером WebDAV для предыдущей неудачной операции ввода-вывода.                                                                                                                  |
| [**давжесттпфромункпас**](/windows/desktop/api/davclnt/nf-davclnt-davgethttpfromuncpath)               | Преобразует указанный UNC-путь в эквивалентный путь HTTP.                                                                                                                                                                           |
| [**давжетселокковнерофсефиле**](/windows/desktop/api/davclnt/nf-davclnt-davgetthelockownerofthefile)   | Возвращает владельца блокировки файла для файла, заблокированного на сервере WebDAV.                                                                                                                                                             |
| [**давжетункфромхттппас**](/windows/desktop/api/davclnt/nf-davclnt-davgetuncfromhttppath)               | Преобразует указанный путь HTTP в эквивалентный UNC-путь.                                                                                                                                                                           |
| [**давинвалидатекаче**](/windows/desktop/api/davclnt/nf-davclnt-davinvalidatecache)                     | Делает недействительным содержимое локального кэша для удаленного файла на сервере WebDAV.                                                                                                                                                     |
| [**даврегистераускаллбакк**](/windows/desktop/api/Davclnt/nf-davclnt-davregisterauthcallback)           | Регистрирует определяемую приложением функцию обратного вызова, которую клиент WebDAV может использовать для запроса учетных данных у пользователя.                                                                                                                 |
| [**давунрегистераускаллбакк**](/windows/desktop/api/Davclnt/nf-davclnt-davunregisterauthcallback)       | Отменяет регистрацию зарегистрированной функции обратного вызова, которую клиент WebDAV использует для запроса учетных данных пользователя.                                                                                                                            |



 

 

 




