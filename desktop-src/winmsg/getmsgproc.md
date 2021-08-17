---
UID: ''
title: Функция обратного вызова Жетмсгпрок
description: Система вызывает эту функцию, когда функция сообщения получает сообщение из очереди сообщений приложения.
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
ms.openlocfilehash: e5c51f2abe8b3660ae40bae05c13428e0622fd4d5c4b8020fea8caa924a35681
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200796"
---
# <a name="getmsgproc-function"></a>Функция Жетмсгпрок

## <a name="-description"></a>-Описание

Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) . Система вызывает эту функцию при извлечении сообщения из очереди сообщений приложения функцией [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) или функции WITH [Message](/windows/desktop/api/winuser/nf-winuser-getmessage) .
Перед возвратом полученного сообщения вызывающему объекту система передает сообщение в процедуру-обработчик.

Тип **хукпрок** определяет указатель на эту функцию обратного вызова.
**Жетмсгпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-Parameters

### <a name="code-in"></a>код [в]

Тип: **int**

Указывает, должна ли процедура-обработчик обработать сообщение.
Если *код* **HC_ACTION**, процедура обработчика должна обработать сообщение.
Если *код* меньше нуля, процедура обработчика должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.

### <a name="wparam-in"></a>wParam [вход]

Тип: **wParam**

Указывает, было ли сообщение удалено из очереди.
Этот параметр может принимать одно из указанных ниже значений.

| Значение | Значение |
|-------|---------|
| **PM_NOREMOVE** Символ 0x0000 | Сообщение не было удалено из очереди. (Приложение, именуемое функцией **PeekMessage** , с указанием флага **PM_NOREMOVE** .) |
| **PM_REMOVE** 0x0001 | Сообщение было удалено из очереди. (Приложение **с именем или** функцией  **PeekMessage** , которое указывает флаг **PM_REMOVE** .)|

### <a name="lparam-in"></a>lParam [in]

Тип: **lParam** .

Указатель на структуру [MSG](/windows/desktop/api/winuser/ns-winuser-msg) , содержащую сведения о сообщении.

## <a name="-returns"></a>— Возвращает

Если *код* меньше нуля, процедура обработчика должна возвращать значение, возвращаемое функцией [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex).

Если *код* больше или равен нулю, настоятельно рекомендуется вызвать **каллнекссукекс** и возвратить возвращаемое значение. в противном случае другие приложения, которые установили [WH_GETMESSAGEные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.
Если процедура-обработчик не вызывает **каллнекссукекс**, возвращаемое значение должно быть равно нулю.

## <a name="-remarks"></a>-замечания

Процедура-обработчик **жетмсгпрок** может проверить или изменить сообщение.
После того как процедура-обработчик возвращает управление системе, функция **PeekMessage** и **Message** , а также любые изменения передаются в приложение, которое его вызвало.

Приложение устанавливает эту процедуру-обработчик, указывая тип обработчика **WH_GETMESSAGE** и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .

## <a name="see-also"></a>См. также раздел

[каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[ОБ](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Обработчики](hooks.md)
