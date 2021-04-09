---
UID: ''
title: Функция обратного вызова Ловлевелмаусепрок
description: Система вызывает эту функцию каждый раз, когда будет отправлено новое событие ввода-вывода мыши в очередь входных потоков.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2020
ms.locfileid: "104070807"
---
# <a name="lowlevelmouseproc-function"></a>Функция Ловлевелмаусепрок

## <a name="description"></a>Описание

Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Система вызывает эту функцию каждый раз, когда будет отправлено новое событие ввода-вывода мыши в очередь входных потоков.

Тип **хукпрок** определяет указатель на эту функцию обратного вызова.
**Ловлевелмаусепрок** — это заполнитель для определяемого приложением или библиотечного имени функции.

```cpp
LRESULT CALLBACK LowLevelMouseProc(
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

### <a name="wparam-in"></a>wParam [вход]

Тип: **wParam**

Идентификатор сообщения мыши.
Этот параметр может принимать одно из следующих сообщений: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) или [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).

### <a name="lparam-in"></a>lParam [in]

Тип: **lParam** .

Указатель на структуру [мсллхукструкт](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .

## <a name="returns"></a>Возвращаемое значение

Тип: **lResult**

Если *нкоде* меньше нуля, процедура-обработчик должна возвращать значение, возвращенное **каллнекссукекс**.

Если *нкоде* больше или равен нулю и процедура обработчика не обработала сообщение, настоятельно рекомендуется вызвать метод **каллнекссукекс** и вернуть возвращаемое значение. в противном случае другие приложения, которые установили [WH_MOUSE_LLные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.
Если процедура обработки сообщения обрабатывала сообщение, она может вернуть ненулевое значение, чтобы система не могла передать сообщение остальной части цепочки обработчиков или конечной процедуры окна.

## <a name="remarks"></a>Комментарии

Приложение устанавливает процедуру-обработчик, указывая тип обработчика **WH_MOUSE_LL** и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .

Этот обработчик вызывается в контексте потока, установившего его.
Вызов осуществляется путем отправки сообщения в поток, устанавливающий обработчик.
Таким образом, поток, устанавливающий обработчик, должен иметь цикл обработки сообщений.

Входные данные мыши могут поступать от локального драйвера мыши или из вызовов функции [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .
Если входные данные поступают из вызова функции **mouse_event**, входные данные были «добавлены».
Однако обработчик **WH_MOUSE_LL** не внедряется в другой процесс.
Вместо этого контекст переключается в процесс, который установил обработчик, и вызывается в исходном контексте.
Затем контекст переключается обратно в приложение, создавшее событие.

Процедура-ловушка должна обрабатывать сообщение меньше времени, чем запись данных, указанная в значении **ловлевелхукстимеаут** в следующем разделе реестра: **HKEY_CURRENT_USER\Control Panel\Desktop**.

Значение указывается в миллисекундах.
Если превышено время ожидания для процедуры-обработчика, система передает сообщение следующему обработчику.
Однако в Windows 7 и более поздних версиях обработчик автоматически удаляется без вызова.
Для приложения нет способа определить, удален ли обработчик.

**Примечание.**  Ловушки отладки не могут контролировать этот тип обработчиков мыши низкого уровня.
Если приложение должно использовать перехватчики низкого уровня, оно должно запускать обработчики в выделенном потоке, который передает работу в рабочий поток, а затем немедленно возвращает.
В большинстве случаев, когда приложению требуется использовать низкоуровневые обработчики, вместо него следует отслеживать необработанные данные.
Это обусловлено тем, что необработанные входные данные могут асинхронно отслеживать сообщения мыши и клавиатуры, предназначенные для других потоков более эффективно, чем низкоуровневые обработчики.
Дополнительные сведения о необработанных входных данных см. в разделе [необработанные входные](/windows/desktop/inputdev/raw-input)данные.

## <a name="see-also"></a>См. также раздел

[каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[кбдллхукструкт](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[мсллхукструкт](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown)

[WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup)

[WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove)

[WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel)

[WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown)

[WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup)

[Обработчики](hooks.md)

[О обработчиках](about-hooks.md)
