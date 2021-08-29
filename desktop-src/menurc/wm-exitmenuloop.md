---
title: Сообщение WM_EXITMENULOOP (Winuser. h)
description: Сообщает процедуре главного окна приложения о том, что был завершен модальный цикл меню.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6d2cfb8457a748b7bb7bbdda481a0a1f73e5331891d45bd1bf1cabdfe0c5c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886384"
---
# <a name="wm_exitmenuloop-message"></a>\_Сообщение ЕКСИТМЕНУЛУП WM

Сообщает процедуре главного окна приложения о том, что был завершен модальный цикл меню.


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Указывает, является ли меню контекстным меню. Этот параметр имеет значение **true** , если это контекстное меню, и **false** в противном случае.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Приложение должно вернуть нуль, если оно обрабатывает это сообщение.

## <a name="remarks"></a>Remarks

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) возвращает ноль.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ентерменулуп**](wm-entermenuloop.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Меню](menus.md)
</dt> </dl>

 

