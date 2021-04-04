---
description: С функциями Сетупинсталлфиле, Сетупинсталлфиликс и Сетупинсталлфроминфсектион используются следующие уведомления. Дополнительные сведения о форматировании и использовании уведомлений см. в разделе уведомления.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Уведомления INF-файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998619"
---
# <a name="inf-file-notifications"></a>Уведомления INF-файлов

С функциями [**сетупинсталлфиле**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**сетупинсталлфиликс**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)и [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) используются следующие уведомления. Дополнительные сведения о форматировании и использовании уведомлений см. в разделе [уведомления](notifications.md).



| Уведомление                                                      | Описание                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**СПФИЛЕНОТИФИ \_ филеопделайед**](spfilenotify-fileopdelayed.md) | Файл используется, и текущая операция откладывается до перезагрузки системы. |
| [**СПФИЛЕНОТИФИ \_ лангмисматч**](spfilenotify-langmismatch.md)   | Язык текущего файла не соответствует языку системы.                   |
| [**СПФИЛЕНОТИФИ \_ таржетексистс**](spfilenotify-targetexists.md)   | Копия указанного файла уже существует на целевом объекте.                             |
| [**СПФИЛЕНОТИФИ \_ таржетневер**](spfilenotify-targetnewer.md)     | На целевом компьютере существует более новая версия указанного файла.                            |



 

> [!Note]  
> Так как [**сетупинсталлфроминфсектион**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) создает и фиксирует внутреннюю очередь файлов, она также использует [уведомления об очереди файлов](file-queue-notifications.md).

 

 

 



