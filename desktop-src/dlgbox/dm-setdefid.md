---
title: Сообщение DM_SETDEFID (Winuser. h)
description: Изменяет идентификатор кнопки отправки по умолчанию для диалогового окна.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- DM_SETDEFID диалоговых окон сообщений
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92749cc7eca569b57d239a36bb6559e59a6a7ebc31c63787a93d0720b334d1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741754"
---
# <a name="dm_setdefid-message"></a>\_Сообщение СЕТДЕФИД DM

Изменяет идентификатор кнопки отправки по умолчанию для диалогового окна.


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Идентификатор элемента управления "Кнопка", который станет значением по умолчанию.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение всегда равно **true**.

## <a name="remarks"></a>Remarks

Это сообщение обрабатывается функцией [**дефдлгпрок**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) . Чтобы задать кнопку по умолчанию, функция может отправлять сообщения [**WM \_ Жетдлгкоде**](wm-getdlgcode.md) и [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) в указанный элемент управления и текущую кнопку по умолчанию.

Использование сообщения **DM \_ сетдефид** может привести к тому, что несколько кнопок будут иметь состояние кнопки отправки по умолчанию. Когда система открывает диалоговое окно, она рисует первую кнопку отправки в шаблоне диалогового окна с границей состояния по умолчанию. Отправка сообщения **\_ сетдефид DM** для изменения кнопки по умолчанию не всегда приведет к удалению границы состояния по умолчанию из первой кнопки отправки. В таких случаях приложение должно отправить сообщение [**BM \_ SETSTYLE**](../controls/bm-setstyle.md) , чтобы изменить стиль границы первой кнопки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                     |
| Заголовок<br/>                   | <dl> <dt>Winuser. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**дефдлгпрок**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[**\_ЖЕТДЕФИД DM**](dm-getdefid.md)
</dt> <dt>

[**WM \_ жетдлгкоде**](wm-getdlgcode.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Диалоговые окна](dialog-boxes.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[**BM \_ SETSTYLE**](../controls/bm-setstyle.md)
</dt> <dt>

[**EM \_ сетлимиттекст**](../controls/em-setlimittext.md)
</dt> </dl>

 

