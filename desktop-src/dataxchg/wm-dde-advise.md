---
title: Сообщение WM_DDE_ADVISE (DDE. h)
description: клиентское приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение об ошибке WM DDE в приложение сервера DDE, чтобы запрашивать сервер предоставлять обновление для элемента данных при каждом изменении элемента.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c651144b4f09cf53f07c0f1860625cab8277e5c8a9532ee864b9ec1b1c927323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636224"
---
# <a name="wm_dde_advise-message"></a>\_ \_ Сообщение об исходе DDE WM

клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение об ошибке **WM \_ DDE \_** в приложение сервера DDE, чтобы запрашивать сервер предоставлять обновление для элемента данных при каждом изменении элемента.

Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик, помещая сообщение в клиентское окно.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово низкого порядка является маркером глобального объекта памяти, содержащего структуру [**ддеадвисе**](/windows/desktop/api/Dde/ns-dde-ddeadvise) , указывающую способ отправки данных.

Слово высокого порядка содержит объект Atom, который идентифицирует запрошенный элемент данных.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если клиентское приложение поддерживает несколько форматов буфера обмена для одного раздела и элемента, оно может отправлять несколько сообщений с рекомендацией **WM \_ DDE \_** для раздела и элемента, указывая другой формат буфера обмена для каждого сообщения. Обратите внимание, что сервер может поддерживать несколько форматов только для ссылок на горячие данные, а не для горячих ссылок на данные.

### <a name="posting"></a>Товаров

Клиентское приложение отправляет сообщение с рекомендацией **WM \_ DDE \_** с помощью вызова функции [**onmessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , а не функции [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

Клиентское приложение выделяет объект глобальной памяти с помощью функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Он выделяет Atom с помощью функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Клиентское приложение должно создать или повторно использовать **параметр \_ WM DDE \_ advise** *lParam* , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Если принимающее (серверное) приложение получает ответ с отрицательным сообщением [**WM \_ DDE \_**](wm-dde-ack.md) , оно должно удалить объект.

Флаг **фрелеасе** не используется в сообщениях с рекомендацией **WM \_ DDE \_** , но их поведение при освобождении данных аналогично поведению [**\_ \_ данных WM DDE**](wm-dde-data.md) , и сообщения [**WM \_ DDE \_**](wm-dde-poke.md) , где **фрелеасе** имеет **значение true**.

### <a name="receiving"></a>Получение

Серверное приложение отправляет сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа. При отправке приложения **WM \_ DDE \_ ACK** приложение может повторно использовать Atom или удалить его и создать новый. Если сообщение **WM \_ DDE \_** имеет положительное значение, приложение должно удалить объект глобальной памяти; в противном случае приложение не должно удалять объект.

Сервер должен создать или повторно использовать параметр *lParam* в [**WM \_ DDE \_**](wm-dde-ack.md) , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

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

[**ддеадвисе**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[**фридделпарам**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**\_Вставка DDE \_ WM**](wm-dde-poke.md)
</dt> <dt>

[**\_запрос DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения о платформа динамических данных Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

