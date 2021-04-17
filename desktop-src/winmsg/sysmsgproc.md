---
UID: ''
title: Функция обратного вызова Сисмсгпрок
description: Система вызывает эту функцию после возникновения события ввода в диалоговом окне, окне сообщения, меню или полосе прокрутки. | Функция обратного вызова Сисмсгпрок
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0d5c7fc116b74dada141e88116ba67209da4a103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703617"
---
# <a name="sysmsgproc-function"></a>Функция Сисмсгпрок

## <a name="description"></a>Описание

Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Система вызывает эту функцию после возникновения события ввода в диалоговом окне, окне сообщения, меню или полосе прокрутки, но до обработки сообщения, созданного событием ввода.
Функция может отслеживать сообщения для любого диалогового окна, окна сообщения, меню или полосы прокрутки в системе.

Тип **хукпрок** определяет указатель на эту функцию обратного вызова.
**Сисмсгпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.

```cpp
LRESULT CALLBACK SysMsgProc(
  _In_ int    nCode,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Параметры

### <a name="ncode-in"></a>Нкоде [in]

Тип: **int**

Тип события ввода, создавшего сообщение.
Если *нкоде* меньше нуля, процедура-обработчик должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.
Этот параметр может принимать одно из указанных ниже значений.

| Значение | Значение |
|-------|---------|
| **MSGF_DIALOGBOX** 0 | Входное событие, произошедшее в окне сообщения или в диалоговом окне. |
| **MSGF_MENU** 2 | Входное событие, произошедшее в меню. |
| **MSGF_SCROLLBAR** 5 | Входное событие произошло в полосе прокрутки. |

### <a name="wparam"></a>wParam

Тип: **wParam**

Этот параметр не используется.

### <a name="lparam-in"></a>lParam [in]

Тип: **lParam** .

Указатель на структуру сообщения [MSG](/windows/desktop/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Возвращаемое значение

Тип: **lResult**

Если *нкоде* меньше нуля, процедура-обработчик должна возвращать значение, возвращенное **каллнекссукекс**.

Если *нкоде* больше или равен нулю и процедура обработчика не обработала сообщение, настоятельно рекомендуется вызвать метод **каллнекссукекс** и вернуть возвращаемое значение. в противном случае другие приложения, которые установили [WH_SYSMSGFILTERные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.
Если процедура обработки сообщения обрабатывает сообщение, она может вернуть ненулевое значение, чтобы система не могла передать сообщение в целевую процедуру окна.

## <a name="remarks"></a>Комментарии

Приложение устанавливает процедуру-обработчик, указывая тип обработчика **WH_SYSMSGFILTER** и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .

## <a name="see-also"></a>См. также раздел

[каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[ОБ](/windows/desktop/api/winuser/ns-winuser-msg)

[сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Обработчики](hooks.md)
