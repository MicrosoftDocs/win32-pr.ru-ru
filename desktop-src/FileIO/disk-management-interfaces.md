---
description: Интерфейсы, используемые в управлении дисками.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Интерфейсы управления дисками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a7314de976b1a5228a8b537da5d09be3df66936ed57915d86d78b0a84c4361e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823214"
---
# <a name="disk-management-interfaces"></a>Интерфейсы управления дисками

В оснастке «Управление дисками» используются следующие интерфейсы.

## <a name="in-this-section"></a>Содержание раздела



| Интерфейс                                                     | Описание                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**идисккуотаконтрол**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | Управляет дисковыми квотами для одного тома файловой системы NTFS.<br/>                             |
| [**идисккуотаевентс**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | Получает уведомления о событиях, связанных с квотами.<br/>                                                         |
| [**идисккуотаусер**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | Представляет одну запись пользовательской квоты в файле сведений о квотах тома.<br/>                          |
| [**идисккуотаусербатч**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | Добавляет несколько пользовательских объектов квоты в контейнер, который затем отправляется для обновления в одном вызове.<br/> |
| [**иенумдисккуотаусерс**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | Перечисляет записи квоты пользователя на томе.<br/>                                                        |



 

 

