---
description: Для файловых очередей используются следующие функции.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Функции очереди файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70087bfcc00f2c3d86c93cc62081adc9aa50705d248d79a524435c95f480562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887083"
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



 

 

 



