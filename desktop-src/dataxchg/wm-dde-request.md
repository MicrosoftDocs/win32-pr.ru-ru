---
title: Сообщение WM_DDE_REQUEST (DDE. h)
description: клиентское приложение платформа динамических данных Exchange (dde) отправляет \_ \_ сообщение запроса WM dde в приложение сервера DDE для запроса значения элемента данных. Чтобы опубликовать это сообщение, вызовите функцию почтовых сообщений со следующими параметрами.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c58877b15f39d2de907688972905e98007658981bcc57df62655634bafe8be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811355"
---
# <a name="wm_dde_request-message"></a>\_ \_ Сообщение запроса DDE WM

клиентское приложение платформа динамических данных Exchange (dde) отправляет сообщение **\_ \_ запроса WM dde** в приложение сервера DDE для запроса значения элемента данных.

Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер клиентского окна, отправляющего сообщение.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка указывает формат стандартного или зарегистрированного буфера обмена.

Слово высокого порядка содержит объект Atom, который определяет элемент данных, запрошенный с сервера.

</dd> </dl>

## <a name="remarks"></a>Remarks

### <a name="posting"></a>Товаров

Клиентское приложение выделяет Atom, вызывая функцию [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

### <a name="receiving"></a>Получение

Если принимающее (серверное) приложение может удовлетворить запрос, оно реагирует на сообщение [**данных WM \_ DDE \_**](wm-dde-data.md) , содержащее запрошенные данные. В противном случае он реагирует на отрицательное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .

При ответе с помощью [**\_ \_ данных в формате WM DDE**](wm-dde-data.md) или сообщения [**WM \_ DDE \_ ACK**](wm-dde-ack.md) серверное приложение может либо повторно использовать Atom, либо удалить Atom и создать новый.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Dde. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

**Ссылки**
</dt> <dt>

[**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**унпаккдделпарам**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**\_данные DDE \_ WM**](wm-dde-data.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения о платформа динамических данных Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

