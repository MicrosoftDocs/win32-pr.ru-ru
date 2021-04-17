---
description: Для файловых очередей используются следующие функции.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Функции очереди файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663784"
---
# <a name="file-queue-functions"></a>Функции очереди файлов

Для файловых очередей используются следующие функции.



| Функция                                                             | Описание                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**сетупклосефилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Завершает очередь. Все оставшиеся транзакции не фиксируются.                                   |
| [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Фиксирует все транзакции в очереди.                                                                      |
| [**сетупопенфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Инициализирует и возвращает маркер в файловую очередь.                                                   |
| [**сетуппромптребут**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | При необходимости предлагает пользователю перезагрузить свой компьютер.                                         |
| [**сетупкуеуекопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Ставит в очередь копию файла.                                                                                   |
| [**сетупкуеуекописектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Ставит в очередь файлы в разделе файлы копирования INF.                                                        |
| [**сетупкуеуедефаулткопи**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Ставит в очередь файлы в разделе INF-файлов копирования, используя сведения по умолчанию, указанные в INF-файле. |
| [**сетупкуеуеделете**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Ставит в очередь удаление файлов.                                                                               |
| [**сетупкуеуеделетесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Ставит в очередь файлы в разделе Удаление файлов INF.                                                      |
| [**сетупкуеуеренаме**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Ставит в очередь переименование файлов.                                                                                 |
| [**сетупкуеуеренамесектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Ставит в очередь файлы в разделе "переименованные файлы" INF.                                                      |
| [**сетупсканфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Сканирует очередь файлов.                                                                                 |
| [**сетупсетплатформпасоверриде**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Задает переопределение пути платформы.                                                                      |



 

 

 



