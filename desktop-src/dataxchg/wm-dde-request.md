---
title: Сообщение WM_DDE_REQUEST (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение запроса WM DDE в приложение сервера DDE для запроса значения элемента данных. Чтобы опубликовать это сообщение, вызовите функцию почтовых сообщений со следующими параметрами.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Обмен данными с сообщениями WM_DDE_REQUEST
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
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801966"
---
# <a name="wm_dde_request-message"></a>\_ \_ Сообщение запроса DDE WM

Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **\_ \_ запроса WM DDE** в приложение сервера DDE для запроса значения элемента данных.

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

## <a name="remarks"></a>Комментарии

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
| Заголовок<br/>                   | <dl> <dt>DDE. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

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

 

