---
description: Следующая функция используется с анонимными каналами.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Функции канала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0ef895fe8b987f19f025b6a21ef4c3a5dc3cb24db5458595c25708066e8a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481608"
---
# <a name="pipe-functions"></a>Функции канала

Следующая функция используется с анонимными каналами.



| Функция                         | Описание                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Создает анонимный канал. |



 

С именованными каналами используются следующие функции.



| Функция                                                                 | Описание                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**каллнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Подключается к каналу типа сообщений, выполняет запись в канал и считывает из него, а затем закрывает канал.                                                                                                                                       |
| [**коннектнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Позволяет процессу сервера именованных каналов ожидать подключения клиентского процесса к экземпляру именованного канала.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Создает экземпляр именованного канала и возвращает маркер для последующих операций канала. Клиентский процесс подключается к именованному каналу с помощью функции [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) или [**каллнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . |
| [**дисконнектнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Отключает серверный экземпляр именованного канала от клиентского процесса.                                                                                                                                                          |
| [**жетнамедпипеклиенткомпутернаме**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Возвращает имя клиентского компьютера для указанного именованного канала.                                                                                                                                                                    |
| [**жетнамедпипеклиентпроцессид**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Получает идентификатор клиентского процесса для указанного именованного канала.                                                                                                                                                               |
| [**жетнамедпипеклиентсессионид**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Получает идентификатор сеанса клиента для указанного именованного канала.                                                                                                                                                               |
| [**жетнамедпипехандлестате**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Извлекает сведения об указанном именованном канале.                                                                                                                                                                                 |
| [**жетнамедпипеинфо**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Извлекает сведения об указанном именованном канале.                                                                                                                                                                               |
| [**жетнамедпипесерверпроцессид**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Возвращает идентификатор серверного процесса для указанного именованного канала.                                                                                                                                                               |
| [**жетнамедпипесерверсессионид**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Возвращает идентификатор сеанса сервера для указанного именованного канала.                                                                                                                                                               |
| [**имперсонатенамедпипеклиент**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Олицетворяет клиентское приложение именованного канала.                                                                                                                                                                                       |
| [**пикнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Копирует данные из именованного или анонимного канала в буфер, не удаляя его из канала.                                                                                                                                         |
| [**сетнамедпипехандлестате**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Задает режим чтения и режим блокировки указанного именованного канала.                                                                                                                                                               |
| [**трансактнамедпипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Объединяет функции, которые записывают сообщение в и считывают сообщение из указанного именованного канала в одну сетевую операцию.                                                                                                    |
| [**ваитнамедпипе**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Ожидает, пока не истечет интервал времени ожидания или не будет доступен экземпляр указанного именованного канала для соединения.                                                                                                            |



 

 

 
