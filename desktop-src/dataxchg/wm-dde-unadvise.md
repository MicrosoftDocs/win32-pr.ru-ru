---
title: Сообщение WM_DDE_UNADVISE (DDE. h)
description: Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение WM \_ DDE \_ Unadvise для информирования серверного приложения DDE о том, что указанный элемент или определенный формат буфера обмена для элемента больше не должны обновляться.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Обмен данными с сообщениями WM_DDE_UNADVISE
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492198"
---
# <a name="wm_dde_unadvise-message"></a>\_ \_ Сообщение об исходе DDE WM

Клиентское приложение платформа динамических данных Exchange (DDE) отправляет сообщение **WM \_ DDE \_ unadvise** для информирования серверного приложения DDE о том, что указанный элемент или определенный формат буфера обмена для элемента больше не должны обновляться. В результате горячий или горячий канал данных для указанного элемента завершается.

Чтобы опубликовать это сообщение, вызовите функцию почтовых [**сообщений**](/windows/desktop/api/winuser/nf-winuser-postmessagea) со следующими параметрами.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*wParam* 
</dt> <dd>

Маркер клиентского окна, отправляющего сообщение.

</dd> <dt>

*lParam* 
</dt> <dd>

Слово нижнего порядка указывает формат буфера обмена элемента, для которого отозван запрос на обновление. Если это **значение равно NULL**, все активные диалоги диалога [**WM \_ DDE \_**](wm-dde-advise.md) для элемента должны быть завершены.

Слово высокого порядка содержит глобальный объект Atom, который определяет элемент, для которого отозван запрос на обновление. Если это **значение равно NULL**, все активные ссылки на предложение [**WM \_ DDE \_**](wm-dde-advise.md) , связанные с диалогом, должны быть завершены.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Клиентское приложение выделяет большое слово *lParam* с помощью вызова функции [**глобаладдатом**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Серверное приложение отправляет сообщение [**WM \_ DDE \_ ACK**](wm-dde-ack.md) для положительного или отрицательного ответа. При публикации **WM \_ DDE \_ ACK** сервер может либо повторно использовать Atom, либо удалить Atom и создать новый.

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

[**Протокол WM \_ DDE \_ advise**](wm-dde-advise.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Сведения о платформа динамических данных Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

