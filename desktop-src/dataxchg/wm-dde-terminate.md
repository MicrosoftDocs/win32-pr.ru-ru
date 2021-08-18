---
title: Сообщение WM_DDE_TERMINATE (DDE. h)
description: приложение платформа динамических данных Exchange (DDE) (клиент или сервер) отправляет \_ \_ сообщение об увольнении WM DDE для завершения диалога. Чтобы опубликовать это сообщение, вызовите функцию почтовых сообщений со следующими параметрами.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98d9b4bf2120cb6daa08b6088a8dd39f8a17b8e28c37a3917936a9c49230487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736271"
---
# <a name="wm_dde_terminate-message"></a>\_Сообщение о \_ прекращении DDE в WM

приложение платформа динамических данных Exchange (DDE) (клиент или сервер) отправляет сообщение об **\_ \_ увольнении WM DDE** для завершения диалога.

Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер для клиентского или серверного окна, в котором разноски сообщения.

</dd> <dt>

*lParam* 
</dt> <dd>

Этот параметр не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

### <a name="posting"></a>Товаров

При ожидании подтверждения завершения приложение не должно отправлять другие сообщения в принимающее приложение. Если отправляющее приложение получает сообщения (отличные от **WM \_ DDE \_**) от принимающего приложения, то оно должно удалить все атомы или объекты общей памяти, сопровождающие сообщения, за исключением глобальных объектов памяти, связанных с сообщениями об ошибках в приложениях [**WM \_ DDE \_**](wm-dde-poke.md) или [**WM \_ \_**](wm-dde-data.md) DDE, не имеющих набора элементов **фрелеасе** .

### <a name="receiving"></a>Получение

Клиентское или серверное приложение должно отвечать, отправляя сообщение о **\_ \_ прекращении работы WM DDE** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Dde. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_данные DDE \_ WM**](wm-dde-data.md)
</dt> <dt>

[**\_Вставка DDE \_ WM**](wm-dde-poke.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения о платформа динамических данных Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

