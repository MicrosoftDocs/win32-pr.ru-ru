---
description: Интерфейсы, используемые в управлении дисками.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Интерфейсы управления дисками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266135"
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



 

 

