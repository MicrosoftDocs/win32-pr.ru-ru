---
title: Сообщение WM_DDE_DATA (DDE. h)
description: серверное приложение платформа динамических данных Exchange (DDE) отправляет \_ \_ сообщение данных WM dde в клиентское приложение dde для передачи элемента данных клиенту или для уведомления клиента о доступности элемента данных.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA Exchange данных сообщений
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0200737a9b25a123954498941ad117e5465f58f5313daa8caf90674751355ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736281"
---
# <a name="wm_dde_data-message"></a>\_ \_ Сообщение данных DDE WM

серверное приложение платформа динамических данных Exchange (DDE) отправляет сообщение **\_ \_ данных WM dde** в клиентское приложение dde для передачи элемента данных клиенту или для уведомления клиента о доступности элемента данных.

Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер серверного окна, помещая сообщение.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово низкого порядка — это маркер глобального объекта памяти, содержащего структуру [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) с данными и дополнительные сведения. Если сервер уведомляет клиента о том, что значение элемента данных изменилось во время канала горячего передачи данных, этот обработчик должен иметь значение **null** . Горячий канал устанавливается клиентом, отправляющей сообщение [**WM \_ DDE \_ advise**](wm-dde-advise.md) с установленным битом **фдеферупд** .

Слово высокого порядка содержит объект Atom, который определяет элемент данных, для которого отправляются данные или уведомление.

</dd> </dl>

## <a name="remarks"></a>Remarks

### <a name="posting"></a>Товаров

Серверное приложение выделяет объект глобальной памяти с помощью функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Он выделяет Atom с помощью функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Сервер должен создать или повторно использовать параметр *lParam* для **\_ \_ данных WM DDE** , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Если принимающее (клиентское) приложение реагирует на отрицательное [**сообщение \_ WM \_ DDE**](wm-dde-ack.md) , приложение, выполняющее разноски (сервер), должно удалить объект глобальной памяти. в противном случае клиент должен удалить объект после извлечения его содержимого, вызвав функцию [**унпаккдделпарам**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .

Если серверное приложение устанавливает для элемента **фрелеасе** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) **значение false**, сервер несет ответственность за удаление объекта при получении положительного или отрицательного подтверждения.

Серверному приложению не следует задавать значения **false** для членов **факкрек** и **фрелеасе** структуры [**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata) . Если для обоих членов задано **значение false**, сервер не может определить, когда следует удалить объект.

### <a name="receiving"></a>Получение

Если **факкрек** имеет **значение true**, клиентское приложение должно отправлять ответное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа. При размещении **WM \_ DDE \_ ACK** клиент может либо повторно использовать Atom, либо удалить его и создать новый.

Клиент должен создать или повторно использовать параметр *lParam* в [**WM \_ DDE \_**](wm-dde-ack.md) , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Если **факкрек** имеет **значение false**, клиентское приложение должно удалить Atom.

Если в приложении, указанном в параметре Global Memory, задано **значение NULL**, принимающее приложение может запросить у сервера отправить данные путем отправки сообщения [**\_ \_ запроса DDE WM**](wm-dde-request.md) .

После обработки сообщения **\_ \_ данных WM DDE** , в котором объект глобальной памяти не имеет **значение NULL**, клиент должен освободить объект, если не выполняется одно из следующих условий.

-   Член **фрелеасе** имеет **значение false**.
-   Член **фрелеасе** имеет **значение true**, но клиентское приложение реагирует на сообщение о неотрицательном сообщении [**WM \_ DDE \_**](wm-dde-ack.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                 |
| Заголовок<br/>                   | <dl> <dt>Dde. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Ссылки**
</dt> <dt>

[**ддедата**](/windows/desktop/api/Dde/ns-dde-ddedata)
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

[**Протокол WM \_ DDE \_ advise**](wm-dde-advise.md)
</dt> <dt>

[**\_Вставка DDE \_ WM**](wm-dde-poke.md)
</dt> <dt>

[**\_запрос DDE \_ WM**](wm-dde-request.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения о платформа динамических данных Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

