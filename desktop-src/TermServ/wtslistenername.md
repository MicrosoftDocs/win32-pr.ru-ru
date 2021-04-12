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
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415828"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>WtsApi32. h</dt> </dl> |



 

 





