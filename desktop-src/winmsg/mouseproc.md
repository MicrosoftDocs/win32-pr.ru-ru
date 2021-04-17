---
UID: ''
title: Функция обратного вызова Маусепрок
description: Система вызывает эту функцию, когда приложение вызывает функцию сообщения и имеется сообщение, которое необходимо обработать.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "105700833"
---
# <a name="mouseproc-function"></a>Функция Маусепрок

## <a name="description"></a>Описание

Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Система вызывает эту функцию всякий [раз, когда](/windows/desktop/api/winuser/nf-winuser-getmessage) приложение вызывает функцию [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) и для обработки сообщений мыши.

Тип **хукпрок** определяет указатель на эту функцию обратного вызова.
**Маусепрок** — это заполнитель для определяемого приложением или библиотечного имени функции.

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Параметры

### <a name="ncode-in"></a>Нкоде [in]

Тип: **int**

Код, используемый процедурой-обработчиком для определения способа обработки сообщения.
Если *нкоде* меньше нуля, процедура-обработчик должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.
Этот параметр может принимать одно из указанных ниже значений.

| Значение | Значение |
|-------|---------|
| **HC_ACTION** 0 | Параметры *wParam* и *lParam* содержат сведения о сообщении мыши. |
| **HC_NOREMOVE** 3 | Параметры *wParam* и *lParam* содержат сведения о сообщении мыши, а сообщение мыши не было удалено из очереди сообщений. (Приложение, именуемое функцией **PeekMessage** , с указанием флага **PM_NOREMOVE** .) |

### <a name="wparam-in"></a>wParam [вход]

Тип: **wParam**

Идентификатор сообщения мыши.

### <a name="lparam-in"></a>lParam [in]

Тип: **lParam** .

Указатель на структуру [маусехукструкт](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .

## <a name="returns"></a>Возвращаемое значение

Тип: **lResult**

Если *нкоде* меньше нуля, процедура-обработчик должна возвращать значение, возвращенное **каллнекссукекс**.

Если *нкоде* больше или равен нулю и процедура обработчика не обработала сообщение, настоятельно рекомендуется вызвать метод **каллнекссукекс** и вернуть возвращаемое значение. в противном случае другие приложения, которые установили [WH_MOUSEные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.
Если процедура обработки сообщения обрабатывает сообщение, она может вернуть ненулевое значение, чтобы система не могла передать сообщение в целевую процедуру окна.

## <a name="remarks"></a>Комментарии

Приложение устанавливает процедуру-обработчик, указывая тип обработчика WH_MOUSE и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .

Процедура-обработчик не должна устанавливать [WH_JOURNALPLAYBACK](about-hooks.md) функцию обратного вызова.

Этот обработчик может быть вызван в контексте потока, установившего его.
Вызов осуществляется путем отправки сообщения в поток, устанавливающий обработчик.
Таким образом, поток, устанавливающий обработчик, должен иметь цикл обработки сообщений.

## <a name="see-also"></a>См. также раздел

[каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[маусехукструкт](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Обработчики](hooks.md)

[О обработчиках](about-hooks.md)
