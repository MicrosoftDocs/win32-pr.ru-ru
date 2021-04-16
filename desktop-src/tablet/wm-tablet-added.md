---
description: Сообщение, \_ добавленное планшетом WM, отправляется \_ при добавлении планшетного устройства в Windows.
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: Сообщение WM_TABLET_ADDED (Тпкшрд. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692237"
---
# <a name="wm_tablet_added-message"></a>\_Сообщение, \_ добавленное ПЛАНШЕТом WM

Сообщение **, \_ \_ добавленное планшетом WM** , отправляется при добавлении планшетного устройства в Windows.


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Индекс добавляемого устройства планшета

</dd> <dt>

*lParam* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это сообщение отправляется всем окнам верхнего уровня в системе, включая отключенные или невидимые ненадлежащие окна, перекрывающиеся окна и всплывающие окна; но сообщение не отправляется в дочерние окна.

Индексы, переданные в параметре *wParam* , связаны с индексом, используемым методом [**Итаблетманажер:: DataTable**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                        |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                            |
| Header<br/>                   | <dl> <dt>Тпкшрд. h</dt> </dl> |



 

 
