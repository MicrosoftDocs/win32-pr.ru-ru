---
title: Основные функции API оболочки клиента
description: В следующей таблице представлен обзор основных функций для API-интерфейса клиентской оболочки служба удаленного управления Windows (WinRM).
ms.assetid: cd0e6b55-03e8-4ebe-aea8-35d268cdb18c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebfe3390b3808cd0abbe9d6bf4ea83ccb0a92338
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411013"
---
# <a name="client-shell-api-core-functions"></a>Основные функции API оболочки клиента

В следующей таблице представлен обзор основных функций для API-интерфейса клиентской оболочки служба удаленного управления Windows (WinRM).



| Базовые функции                                                   | Описание                                                                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**всманклосекомманд**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosecommand)                   | Закрывает команду.                                                                                                                                                               |
| [**всманклосеоператион**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseoperation)               | Закрывает операцию.                                                                                                                                                            |
| [**всманклосесессион**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosesession)                   | Закрывает сеанс WinRM.                                                                                                                                                         |
| [**всманклосешелл**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseshell)                       | Закрывает объект оболочки.                                                                                                                                                          |
| [**всманконнектшелл**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshell)                   | Подключается к существующему сеансу сервера.                                                                                                                                         |
| [**всманконнектшеллкомманд**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshellcommand)     | Подключается к существующей команде, выполняемой в оболочке.                                                                                                                             |
| [**всманкреатесессион**](/windows/desktop/api/Wsman/nf-wsman-wsmancreatesession)                 | Создает сеанс WinRM.                                                                                                                                                        |
| [**всманкреатешелл**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell)                     | Создает объект оболочки.                                                                                                                                                         |
| [**всманкреатешеллекс**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshellex)                 | Создает объект оболочки с использованием тех же функций, что и функция [**всманкреатешелл**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) , с добавлением идентификатора оболочки, заданной клиентом.          |
| [**всмандеинитиализе**](/windows/desktop/api/Wsman/nf-wsman-wsmandeinitialize)                   | Деинициализирует клиентский стек WinRM.                                                                                                                                           |
| [**всмандисконнектшелл**](/windows/desktop/api/Wsman/nf-wsman-wsmandisconnectshell)             | Отключает сетевое подключение активной оболочки и связанных с ней команд.                                                                                              |
| [**всманинитиализе**](/windows/desktop/api/Wsman/nf-wsman-wsmaninitialize)                       | Инициализирует WinRM.                                                                                                                                                              |
| [**всманрецеивешеллаутпут**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)       | Получает выходные данные оболочки.                                                                                                                                                          |
| [**всманреконнектшелл**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshell)               | Повторно подключает ранее отключенный сеанс оболочки. Чтобы повторно подключить связанные команды сеанса оболочки, используйте [**всманреконнектшеллкомманд**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand). |
| [**всманреконнектшеллкомманд**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand) | Повторно подключает ранее отключенную команду.                                                                                                                                   |
| [**всманруншеллкомманд**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand)             | Выполняет команду оболочки.                                                                                                                                                           |
| [**всманруншеллкоммандекс**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommandex)         | Предоставляет те же функциональные возможности, что и функция [**всманруншеллкомманд**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand) , с добавлением параметра идентификатора команды.                                 |
| [**всмансендшеллинпут**](/windows/desktop/api/Wsman/nf-wsman-wsmansendshellinput)               | Отправляет входные данные в оболочку.                                                                                                                                                         |
| [**всмансигналшелл**](/windows/desktop/api/Wsman/nf-wsman-wsmansignalshell)                     | Сигнализирует оболочке.                                                                                                                                                                |



 

 

 




