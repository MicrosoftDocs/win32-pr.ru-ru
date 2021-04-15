---
description: Интерфейсы, используемые с квотами диска.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Интерфейсы дисковой квоты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497970"
---
# <a name="disk-quota-interfaces"></a>Интерфейсы дисковой квоты

С дисковой квотой используются следующие интерфейсы.



| Интерфейс                                          | Описание                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**идисккуотаконтрол**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | Управляет дисковыми квотами для одного тома файловой системы NTFS.<br/>                             |
| [**идисккуотаевентс**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | Получает уведомления о событиях, связанных с квотами.<br/>                                                         |
| [**идисккуотаусер**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | Представляет одну запись пользовательской квоты в файле сведений о квотах тома.<br/>                          |
| [**идисккуотаусербатч**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | Добавляет несколько пользовательских объектов квоты в контейнер, который затем отправляется для обновления в одном вызове.<br/> |
| [**иенумдисккуотаусерс**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | Перечисляет записи квоты пользователя на томе.<br/>                                                        |



 

 

