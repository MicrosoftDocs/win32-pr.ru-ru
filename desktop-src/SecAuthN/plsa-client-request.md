---
description: Непрозрачный тип данных.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Нтсекпкг. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264686"
---
# <a name="plsa_client_request"></a>\_запрос клиента \_ плса

Тип **данных \_ \_ запроса клиента плса** является непрозрачным типом данных.

[*Локальный центр безопасности*](../secgloss/l-gly.md) (LSA) использует его для внутренних целей, чтобы поддерживать клиентскую информацию, относящуюся к отдельным запросам.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Нтсекпкг. h</dt> </dl> |



 

 
