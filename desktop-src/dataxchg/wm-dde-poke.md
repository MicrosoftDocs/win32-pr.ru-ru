---
title: Сообщение WM_DDE_POKE (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение WM \_ DDE \_ в приложение сервера DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Обмен данными с сообщениями WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803922"
---
# <a name="wm_dde_poke-message"></a>\_Сообщение о \_ выводится DDE WM

Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **WM \_ DDE \_** в приложение сервера DDE. Клиент использует это сообщение, чтобы запросить сервер на прием незапрошенного элемента данных. Ожидается, что сервер отвечает с сообщением [**WM \_ DDE \_ ACK**](wm-dde-ack.md) , указывающим, принял ли он элемент данных.

Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Обработчик, помещая сообщение в клиентское окно.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово низкого порядка — это маркер глобального объекта памяти, содержащего структуру [**ддепоке**](/windows/desktop/api/Dde/ns-dde-ddepoke) с данными и дополнительные сведения.

Слово высокого порядка содержит глобальный объект Atom, который определяет элемент данных, для которого отправляются данные или уведомление.

</dd> </dl>

## <a name="remarks"></a>Комментарии

### <a name="posting"></a>Товаров

Клиентское приложение должно выделить память для объекта глобальной памяти с помощью функции [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Клиентское приложение должно удалить объект, если выполняется одно из следующих условий.

-   Серверное приложение реагирует на отрицательное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) .
-   Член **фрелеасе** имеет **значение false**, но серверное приложение реагирует на положительный или отрицательный ответ [**WM \_ DDE \_**](wm-dde-ack.md).

Клиентское приложение должно создать Atom с помощью функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Клиентское приложение должно создать или повторно использовать **параметр \_ WM \_ DDE** с параметрами *lParam* , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

### <a name="receiving"></a>Получение

Серверное приложение должно отправлять ответное сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа. При размещении **WM \_ DDE \_ ACK** сервер может либо повторно использовать Atom, либо удалить его и создать новый.

Сервер должен создать или повторно использовать параметр *lParam* в [**WM \_ DDE \_**](wm-dde-ack.md) , вызвав функцию [**паккдделпарам**](/windows/desktop/api/Dde/nf-dde-packddelparam) или функцию [**реуседделпарам**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Чтобы освободить объект глобальной памяти, сервер должен вызвать функцию [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Кроме того, если формат данных — [**CF \_ Дспметафилепикт**](clipboard-formats.md) или **CF \_ метафилепикт**, сервер также должен вызвать [**делетеметафиле**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) с помощью внедренного метафайла. Эти два формата имеют дополнительный уровень косвенного обращения. то есть приложение должно заблокировать объект для получения указателя на маркер, а затем заблокировать этот обработчик для получения указателя на структуру [**метафилепикт**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) и, наконец, вызвать **делетеметафиле** с помощью маркера из **ХМФ** элемента структуры **метафилепикт** .

Чтобы освободить объект, сервер должен вызвать функцию [**фридделпарам**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

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

[**ддепоке**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**фридделпарам**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**метафилепикт**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
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

**Зрения**
</dt> <dt>

[Сведения о платформа динамических данных Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

