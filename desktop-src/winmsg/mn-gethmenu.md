---
description: Получает маркер меню для текущего окна.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Сообщение MN_GETHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cfc1eb6086f94f64e1a0e152e6f86fe89a0ea0278a6c4cc25a487edb6f93ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089934"
---
# <a name="mn_gethmenu-message"></a>\_Сообщение ЖЕСМЕНУ MN

Получает маркер меню для текущего окна.


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Этот параметр не используется.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HMENU**

В случае успеха возвращаемое значение является **HMENU** для текущего окна. В случае сбоя возвращается значение **null**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



 

 




