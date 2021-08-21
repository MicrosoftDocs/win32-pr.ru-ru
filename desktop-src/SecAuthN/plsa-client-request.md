---
description: Непрозрачный тип данных.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Нтсекпкг. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792b81516e434469750b4ddd667bf6ddb82df31f4f13f82588d281f743bc8835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921043"
---
# <a name="plsa_client_request"></a>\_запрос клиента \_ плса

Тип **данных \_ \_ запроса клиента плса** является непрозрачным типом данных.

[*Локальный центр безопасности*](../secgloss/l-gly.md) (LSA) использует его для внутренних целей, чтобы поддерживать клиентскую информацию, относящуюся к отдельным запросам.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Заголовок<br/>                   | <dl> <dt>Нтсекпкг. h</dt> </dl> |



 

 
