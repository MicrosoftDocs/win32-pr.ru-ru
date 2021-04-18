---
title: Сообщение WM_ENTERMENULOOP (Winuser. h)
description: Сообщает процедуре главного окна приложения о том, что был введен модальный цикл меню.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710459"
---
# <a name="wm_entermenuloop-message"></a>\_Сообщение ЕНТЕРМЕНУЛУП WM

Сообщает процедуре главного окна приложения о том, что был введен модальный цикл меню.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, было ли указано меню "окно" с помощью функции [**метод TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) . Этот параметр имеет значение **true** , если меню окна было указано с помощью **метод TrackPopupMenu**, и **false** в противном случае.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Комментарии

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает ноль.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ екситменулуп**](wm-exitmenuloop.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Меню](menus.md)
</dt> </dl>

 

