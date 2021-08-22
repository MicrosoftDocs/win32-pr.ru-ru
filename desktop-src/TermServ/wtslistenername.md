---
title: ВТСЛИСТЕНЕРНАМЕ (WtsApi32. h)
description: Представляет имя службы удаленных рабочих столов прослушивателей на сервере узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- втслистенернамев
- втслистенернамеа
- втслистенернаме
- пвтслистенернаме
- втслистенернаме
- пвтслистенернаме
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce0df52229670cd090dd900dda3c2284437297bedc25c69f12c980b9cc40d92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513844"
---
# <a name="wtslistenername"></a>втслистенернаме

Представляет имя службы удаленных рабочих столов прослушивателей на сервере узла сеансов удаленный рабочий стол (узел сеанса удаленных рабочих столов).


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

**втслистенернамев**
</dt> <dd>

Имя в Юникоде прослушивателя.

</dd> <dt>

**втслистенернамеа**
</dt> <dd>

Указатель на имя в формате ANSI прослушивателя.

</dd> <dt>

**втслистенернаме**
</dt> <dd>

Имя прослушивателя.

</dd> <dt>

**пвтслистенернаме**
</dt> <dd>

Указатель на имя прослушивателя.

</dd> <dt>

**втслистенернаме**
</dt> <dd>

Имя прослушивателя.

</dd> <dt>

**пвтслистенернаме**
</dt> <dd>

Указатель на имя прослушивателя.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>WtsApi32. h</dt> </dl> |



 

 





