---
title: Код уведомления LBN_ERRSPACE (Winuser. h)
description: Уведомляет приложение о том, что список не может выделить достаточно памяти для удовлетворения конкретного запроса. Родительское окно списка получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- LBN_ERRSPACE кода уведомления Windows элементы управления
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
ms.openlocfilehash: 4161cf750995bca3755f11ab45148fd184e2bc13a127909a256333549b1e9258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085304"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Другие ресурсы**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_команда WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

