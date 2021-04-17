---
UID: ''
title: Функция обратного вызова Шеллпрок
description: Функция получает уведомления о событиях оболочки от системы.
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
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "105700835"
---
# <a name="shellproc-function"></a>Функция Шеллпрок

## <a name="description"></a>Описание

Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Функция получает уведомления о событиях оболочки от системы.

Тип **хукпрок** определяет указатель на эту функцию обратного вызова.
**Шеллпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Параметры

### <a name="ncode-in"></a>Нкоде [in]

Тип: **int**

Код обработчика.
Если *нкоде* меньше нуля, процедура-обработчик должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.
Этот параметр может принимать одно из указанных ниже значений.

| Значение | Значение |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** 11 | Состояние доступности изменилось. |
| **HSHELL_ACTIVATESHELLWINDOW** 3 | Оболочка должна активировать свое главное окно. |
| **HSHELL_APPCOMMAND** 12 | Пользователь завершил событие ввода (например, нажал кнопку команды приложения на клавиатуре или клавишу команды приложения), и приложение не обработало [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) сообщение, созданное этими входными данными. Если процедура оболочки обрабатывает сообщение [WM_COMMAND](/windows/desktop/menurc/wm-command) , оно не должно вызывать **каллнекссукекс**. Дополнительные сведения см. в разделе возвращаемое значение. |
| **HSHELL_GETMINRECT** 5 | Окно уменьшается или разворачивается. Системе требуются координаты сворачивания прямоугольника для окна. |
| **HSHELL_LANGUAGE** 8 | Язык клавиатуры был изменен или была загружена новая раскладка клавиатуры. |
| **HSHELL_REDRAW** 6 | Заголовок окна на панели задач был перерисован. |
| **HSHELL_TASKMAN** 7 | Пользователь выбрал список задач. Приложение оболочки, предоставляющее список задач, должно возвращать **значение true** , чтобы предотвратить запуск списка задач в Windows. |
| **HSHELL_WINDOWACTIVATED** 4 | Активация была изменена на другое, ненадлежащее окно верхнего уровня. |
| **HSHELL_WINDOWCREATED** 1 | Создано ненадлежащее окно верхнего уровня. Это окно существует, когда система вызывает этот обработчик. |
| **HSHELL_WINDOWDESTROYED** 2 | Будет уничтожено ненадлежащее окно верхнего уровня. Окно по-прежнему существует, когда система вызывает этот обработчик. |
| **HSHELL_WINDOWREPLACED** 13 | Заменяется окно верхнего уровня. Это окно существует, когда система вызывает этот обработчик. |

### <a name="wparam-in"></a>wParam [вход]

Тип: **wParam**

Этот параметр зависит от значения параметра *нкоде* , как показано в следующей таблице.

| нкоде | wParam |
|-------|---------|
| **HSHELL_ACCESSIBILITYSTATE** | Указывает, какая функция специальных возможностей изменила состояние. Это значение может быть одним из следующих: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** или **ACCESS_STICKYKEYS**. |
| **HSHELL_APPCOMMAND** | Указывает, куда было первоначально отправлено сообщение **WM_APPCOMMAND** . Например, маркер для окна. Дополнительные сведения см. в разделе параметр cmd в **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Маркер для сворачивания или развернутого окна. |
| **HSHELL_LANGUAGE** | Маркер окна. |
| **HSHELL_REDRAW** | Маркер перевыписанного окна. |
| **HSHELL_WINDOWACTIVATED** | Маркер для активированного окна. |
| **HSHELL_WINDOWCREATED** | Маркер для созданного окна. |
| **HSHELL_WINDOWDESTROYED** | Маркер для уничтоженного окна. |
| **HSHELL_WINDOWREPLACED** | Описатель для заменяемого окна. Windows 2000: не поддерживается. |

### <a name="lparam-in"></a>lParam [in]

Тип: **lParam** .

Этот параметр зависит от значения параметра *нкоде* , как показано в следующей таблице.

| нкоде | lParam |
|-------|---------|
| **HSHELL_APPCOMMAND** | `GET_APPCOMMAND_LPARAM(lParam)` Команда приложения, соответствующая входному событию. `GET_DEVICE_LPARAM(lParam)` Указывает, что создало событие ввода. Например, мышь или клавиатура. Дополнительные сведения см. в описании параметра *удевице* в разделе **WM_APPCOMMAND**. `GET_FLAGS_LPARAM(lParam)` зависит от значения *cmd* в **WM_APPCOMMAND**. Например, он может указать, какие виртуальные ключи были заблокированы при первоначальной отправке сообщения **WM_APPCOMMAND** . Дополнительные сведения см. в описании параметра *двкмдфлагс* Description в разделе **WM_APPCOMMAND**. |
| **HSHELL_GETMINRECT** | Указатель на структуру [Rect](/previous-versions/dd162897(v=vs.85)) . |
| **HSHELL_LANGUAGE** | Маркер раскладки клавиатуры. |
| **HSHELL_MONITORCHANGED** | Маркер окна, который перемещается на другой монитор. |
| **HSHELL_REDRAW** | Значение равно **true** , если окно мигает, или **false** в противном случае. |
| **HSHELL_WINDOWACTIVATED** | Значение TRUE, если окно находится в полноэкранном режиме, или **false** в противном случае. |
| **HSHELL_WINDOWREPLACED** | Маркер нового окна. Windows 2000: не поддерживается. |

## <a name="returns"></a>Возвращаемое значение

Тип: **lResult**

Возвращаемое значение должно равняться нулю, если значение Нкоде не **HSHELL_APPCOMMAND** и процедура оболочки обрабатывает сообщение **WM_COMMAND** .
В этом случае возвращаемое значение должно быть ненулевым.

## <a name="remarks"></a>Комментарии

Установите эту процедуру-обработчик, указав тип обработчика [WH_SHELL](about-hooks.md) и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .

## <a name="see-also"></a>См. также раздел

[каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SendMessage](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand)

[WM_COMMAND](/windows/desktop/menurc/wm-command)

[Обработчики](hooks.md)
