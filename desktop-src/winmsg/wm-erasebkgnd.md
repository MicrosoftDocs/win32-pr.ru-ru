---
description: Посылается, когда фон окна должен быть стерт (например, при изменении размера окна). Сообщение отправляется для подготовки недействительной части окна для рисования.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Сообщение WM_ERASEBKGND (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265438"
---
# <a name="wm_erasebkgnd-message"></a>\_Сообщение ЕРАСЕБКГНД WM

Посылается, когда фон окна должен быть стерт (например, при изменении размера окна). Сообщение отправляется для подготовки недействительной части окна для рисования.


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер контекста устройства.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **lResult**

Приложение должно вернуть ненулевое значение, если удаляет фон. в противном случае он должен вернуть ноль.

## <a name="remarks"></a>Комментарии

Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) удаляет фон, используя кисть фона класса, заданную элементом **хбрбаккграунд** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Если **хбрбаккграунд** имеет **значение NULL**, приложение должно обработать сообщение **WM \_ ерасебкгнд** и стереть фон.

Приложение должно вернуть ненулевое значение в ответ на **\_ ерасебкгнд WM** , если оно обрабатывает сообщение и стирает фон. Это означает, что дальнейшая очистка не требуется. Если приложение возвращает ноль, окно остается помеченным для стирания. (Как правило, это означает, что элемент **ферасе** структуры [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) будет иметь **значение true**.)

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

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Зрения**
</dt> <dt>

[Значки](../menurc/icons.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**бегинпаинт**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
