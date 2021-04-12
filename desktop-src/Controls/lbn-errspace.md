---
title: Код уведомления LBN_ERRSPACE (Winuser. h)
description: Уведомляет приложение о том, что список не может выделить достаточно памяти для удовлетворения конкретного запроса. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- LBN_ERRSPACE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104262210"
---
# <a name="lbn_errspace-notification-code"></a>\_Код уведомления ЛБН еррспаце

Уведомляет приложение о том, что список не может выделить достаточно памяти для удовлетворения конкретного запроса. Родительское окно списка получает этот код уведомления через [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор поля списка. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.

</dd> <dt>

*lParam* 
</dt> <dd>

Обработайте с списком.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

