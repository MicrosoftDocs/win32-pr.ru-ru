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
# <a name="shellproc-function"></a><span data-ttu-id="6c4aa-103">Функция Шеллпрок</span><span class="sxs-lookup"><span data-stu-id="6c4aa-103">ShellProc function</span></span>

## <a name="description"></a><span data-ttu-id="6c4aa-104">Описание</span><span class="sxs-lookup"><span data-stu-id="6c4aa-104">Description</span></span>

<span data-ttu-id="6c4aa-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="6c4aa-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="6c4aa-106">Функция получает уведомления о событиях оболочки от системы.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-106">The function receives notifications of Shell events from the system.</span></span>

<span data-ttu-id="6c4aa-107">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="6c4aa-108">**Шеллпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-108">**ShellProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="6c4aa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c4aa-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="6c4aa-110">Нкоде [in]</span><span class="sxs-lookup"><span data-stu-id="6c4aa-110">nCode [in]</span></span>

<span data-ttu-id="6c4aa-111">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-111">Type: **int**</span></span>

<span data-ttu-id="6c4aa-112">Код обработчика.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-112">The hook code.</span></span>
<span data-ttu-id="6c4aa-113">Если *нкоде* меньше нуля, процедура-обработчик должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="6c4aa-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="6c4aa-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6c4aa-115">Value</span></span> | <span data-ttu-id="6c4aa-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6c4aa-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="6c4aa-117">**HSHELL_ACCESSIBILITYSTATE** 11</span><span class="sxs-lookup"><span data-stu-id="6c4aa-117">**HSHELL_ACCESSIBILITYSTATE** 11</span></span> | <span data-ttu-id="6c4aa-118">Состояние доступности изменилось.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-118">The accessibility state has changed.</span></span> |
| <span data-ttu-id="6c4aa-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span><span class="sxs-lookup"><span data-stu-id="6c4aa-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span></span> | <span data-ttu-id="6c4aa-120">Оболочка должна активировать свое главное окно.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-120">The shell should activate its main window.</span></span> |
| <span data-ttu-id="6c4aa-121">**HSHELL_APPCOMMAND** 12</span><span class="sxs-lookup"><span data-stu-id="6c4aa-121">**HSHELL_APPCOMMAND** 12</span></span> | <span data-ttu-id="6c4aa-122">Пользователь завершил событие ввода (например, нажал кнопку команды приложения на клавиатуре или клавишу команды приложения), и приложение не обработало [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) сообщение, созданное этими входными данными.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-122">The user completed an input event (for example, pressed an application command button on the mouse or an application command key on the keyboard), and the application did not handle the [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message generated by that input.</span></span> <span data-ttu-id="6c4aa-123">Если процедура оболочки обрабатывает сообщение [WM_COMMAND](/windows/desktop/menurc/wm-command) , оно не должно вызывать **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-123">If the Shell procedure handles the [WM_COMMAND](/windows/desktop/menurc/wm-command) message, it should not call **CallNextHookEx**.</span></span> <span data-ttu-id="6c4aa-124">Дополнительные сведения см. в разделе возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-124">See the Return Value section for more information.</span></span> |
| <span data-ttu-id="6c4aa-125">**HSHELL_GETMINRECT** 5</span><span class="sxs-lookup"><span data-stu-id="6c4aa-125">**HSHELL_GETMINRECT** 5</span></span> | <span data-ttu-id="6c4aa-126">Окно уменьшается или разворачивается.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-126">A window is being minimized or maximized.</span></span> <span data-ttu-id="6c4aa-127">Системе требуются координаты сворачивания прямоугольника для окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-127">The system needs the coordinates of the minimized rectangle for the window.</span></span> |
| <span data-ttu-id="6c4aa-128">**HSHELL_LANGUAGE** 8</span><span class="sxs-lookup"><span data-stu-id="6c4aa-128">**HSHELL_LANGUAGE** 8</span></span> | <span data-ttu-id="6c4aa-129">Язык клавиатуры был изменен или была загружена новая раскладка клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-129">Keyboard language was changed or a new keyboard layout was loaded.</span></span> |
| <span data-ttu-id="6c4aa-130">**HSHELL_REDRAW** 6</span><span class="sxs-lookup"><span data-stu-id="6c4aa-130">**HSHELL_REDRAW** 6</span></span> | <span data-ttu-id="6c4aa-131">Заголовок окна на панели задач был перерисован.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-131">The title of a window in the task bar has been redrawn.</span></span> |
| <span data-ttu-id="6c4aa-132">**HSHELL_TASKMAN** 7</span><span class="sxs-lookup"><span data-stu-id="6c4aa-132">**HSHELL_TASKMAN** 7</span></span> | <span data-ttu-id="6c4aa-133">Пользователь выбрал список задач.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-133">The user has selected the task list.</span></span> <span data-ttu-id="6c4aa-134">Приложение оболочки, предоставляющее список задач, должно возвращать **значение true** , чтобы предотвратить запуск списка задач в Windows.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-134">A shell application that provides a task list should return **TRUE** to prevent Windows from starting its task list.</span></span> |
| <span data-ttu-id="6c4aa-135">**HSHELL_WINDOWACTIVATED** 4</span><span class="sxs-lookup"><span data-stu-id="6c4aa-135">**HSHELL_WINDOWACTIVATED** 4</span></span> | <span data-ttu-id="6c4aa-136">Активация была изменена на другое, ненадлежащее окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-136">The activation has changed to a different top-level, unowned window.</span></span> |
| <span data-ttu-id="6c4aa-137">**HSHELL_WINDOWCREATED** 1</span><span class="sxs-lookup"><span data-stu-id="6c4aa-137">**HSHELL_WINDOWCREATED** 1</span></span> | <span data-ttu-id="6c4aa-138">Создано ненадлежащее окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-138">A top-level, unowned window has been created.</span></span> <span data-ttu-id="6c4aa-139">Это окно существует, когда система вызывает этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-139">The window exists when the system calls this hook.</span></span> |
| <span data-ttu-id="6c4aa-140">**HSHELL_WINDOWDESTROYED** 2</span><span class="sxs-lookup"><span data-stu-id="6c4aa-140">**HSHELL_WINDOWDESTROYED** 2</span></span> | <span data-ttu-id="6c4aa-141">Будет уничтожено ненадлежащее окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-141">A top-level, unowned window is about to be destroyed.</span></span> <span data-ttu-id="6c4aa-142">Окно по-прежнему существует, когда система вызывает этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-142">The window still exists when the system calls this hook.</span></span> |
| <span data-ttu-id="6c4aa-143">**HSHELL_WINDOWREPLACED** 13</span><span class="sxs-lookup"><span data-stu-id="6c4aa-143">**HSHELL_WINDOWREPLACED** 13</span></span> | <span data-ttu-id="6c4aa-144">Заменяется окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-144">A top-level window is being replaced.</span></span> <span data-ttu-id="6c4aa-145">Это окно существует, когда система вызывает этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-145">The window exists when the system calls this hook.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="6c4aa-146">wParam [вход]</span><span class="sxs-lookup"><span data-stu-id="6c4aa-146">wParam [in]</span></span>

<span data-ttu-id="6c4aa-147">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-147">Type: **WPARAM**</span></span>

<span data-ttu-id="6c4aa-148">Этот параметр зависит от значения параметра *нкоде* , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-148">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="6c4aa-149">нкоде</span><span class="sxs-lookup"><span data-stu-id="6c4aa-149">nCode</span></span> | <span data-ttu-id="6c4aa-150">wParam</span><span class="sxs-lookup"><span data-stu-id="6c4aa-150">wParam</span></span> |
|-------|---------|
| <span data-ttu-id="6c4aa-151">**HSHELL_ACCESSIBILITYSTATE**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-151">**HSHELL_ACCESSIBILITYSTATE**</span></span> | <span data-ttu-id="6c4aa-152">Указывает, какая функция специальных возможностей изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-152">Indicates which accessibility feature has changed state.</span></span> <span data-ttu-id="6c4aa-153">Это значение может быть одним из следующих: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** или **ACCESS_STICKYKEYS**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-153">This value is one of the following: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS**, or **ACCESS_STICKYKEYS**.</span></span> |
| <span data-ttu-id="6c4aa-154">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-154">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="6c4aa-155">Указывает, куда было первоначально отправлено сообщение **WM_APPCOMMAND** . Например, маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-155">Indicates where the **WM_APPCOMMAND** message was originally sent; for example, the handle to a window.</span></span> <span data-ttu-id="6c4aa-156">Дополнительные сведения см. в разделе параметр cmd в **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-156">For more information, see cmd parameter in **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="6c4aa-157">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-157">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="6c4aa-158">Маркер для сворачивания или развернутого окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-158">A handle to the minimized or maximized window.</span></span> |
| <span data-ttu-id="6c4aa-159">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-159">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="6c4aa-160">Маркер окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-160">A handle to the window.</span></span> |
| <span data-ttu-id="6c4aa-161">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-161">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="6c4aa-162">Маркер перевыписанного окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-162">A handle to the redrawn window.</span></span> |
| <span data-ttu-id="6c4aa-163">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-163">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="6c4aa-164">Маркер для активированного окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-164">A handle to the activated window.</span></span> |
| <span data-ttu-id="6c4aa-165">**HSHELL_WINDOWCREATED**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-165">**HSHELL_WINDOWCREATED**</span></span> | <span data-ttu-id="6c4aa-166">Маркер для созданного окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-166">A handle to the created window.</span></span> |
| <span data-ttu-id="6c4aa-167">**HSHELL_WINDOWDESTROYED**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-167">**HSHELL_WINDOWDESTROYED**</span></span> | <span data-ttu-id="6c4aa-168">Маркер для уничтоженного окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-168">A handle to the destroyed window.</span></span> |
| <span data-ttu-id="6c4aa-169">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-169">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="6c4aa-170">Описатель для заменяемого окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-170">A handle to the window being replaced.</span></span> <span data-ttu-id="6c4aa-171">Windows 2000: не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-171">Windows 2000:  Not supported.</span></span> |

### <a name="lparam-in"></a><span data-ttu-id="6c4aa-172">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="6c4aa-172">lParam [in]</span></span>

<span data-ttu-id="6c4aa-173">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="6c4aa-173">Type: **LPARAM**</span></span>

<span data-ttu-id="6c4aa-174">Этот параметр зависит от значения параметра *нкоде* , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-174">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="6c4aa-175">нкоде</span><span class="sxs-lookup"><span data-stu-id="6c4aa-175">nCode</span></span> | <span data-ttu-id="6c4aa-176">lParam</span><span class="sxs-lookup"><span data-stu-id="6c4aa-176">lParam</span></span> |
|-------|---------|
| <span data-ttu-id="6c4aa-177">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-177">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="6c4aa-178">`GET_APPCOMMAND_LPARAM(lParam)` Команда приложения, соответствующая входному событию.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-178">`GET_APPCOMMAND_LPARAM(lParam)` is the application command corresponding to the input event.</span></span> <span data-ttu-id="6c4aa-179">`GET_DEVICE_LPARAM(lParam)` Указывает, что создало событие ввода. Например, мышь или клавиатура.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-179">`GET_DEVICE_LPARAM(lParam)` indicates what generated the input event; for example, the mouse or keyboard.</span></span> <span data-ttu-id="6c4aa-180">Дополнительные сведения см. в описании параметра *удевице* в разделе **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-180">For more information, see the *uDevice* parameter description under **WM_APPCOMMAND**.</span></span> <span data-ttu-id="6c4aa-181">`GET_FLAGS_LPARAM(lParam)` зависит от значения *cmd* в **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-181">`GET_FLAGS_LPARAM(lParam)` depends on the value of *cmd* in **WM_APPCOMMAND**.</span></span> <span data-ttu-id="6c4aa-182">Например, он может указать, какие виртуальные ключи были заблокированы при первоначальной отправке сообщения **WM_APPCOMMAND** .</span><span class="sxs-lookup"><span data-stu-id="6c4aa-182">For example, it might indicate which virtual keys were held down when the **WM_APPCOMMAND** message was originally sent.</span></span> <span data-ttu-id="6c4aa-183">Дополнительные сведения см. в описании параметра *двкмдфлагс* Description в разделе **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-183">For more information, see the *dwCmdFlags* description parameter under **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="6c4aa-184">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-184">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="6c4aa-185">Указатель на структуру [Rect](/previous-versions/dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6c4aa-185">A pointer to a [RECT](/previous-versions/dd162897(v=vs.85)) structure.</span></span> |
| <span data-ttu-id="6c4aa-186">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-186">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="6c4aa-187">Маркер раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-187">A handle to a keyboard layout.</span></span> |
| <span data-ttu-id="6c4aa-188">**HSHELL_MONITORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-188">**HSHELL_MONITORCHANGED**</span></span> | <span data-ttu-id="6c4aa-189">Маркер окна, который перемещается на другой монитор.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-189">A handle to the window that moved to a different monitor.</span></span> |
| <span data-ttu-id="6c4aa-190">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-190">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="6c4aa-191">Значение равно **true** , если окно мигает, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-191">The value is **TRUE** if the window is flashing, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="6c4aa-192">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-192">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="6c4aa-193">Значение TRUE, если окно находится в полноэкранном режиме, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-193">The value is TRUE if the window is in full-screen mode, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="6c4aa-194">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-194">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="6c4aa-195">Маркер нового окна.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-195">A handle to the new window.</span></span> <span data-ttu-id="6c4aa-196">Windows 2000: не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-196">Windows 2000:  Not supported.</span></span> |

## <a name="returns"></a><span data-ttu-id="6c4aa-197">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c4aa-197">Returns</span></span>

<span data-ttu-id="6c4aa-198">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="6c4aa-198">Type: **LRESULT**</span></span>

<span data-ttu-id="6c4aa-199">Возвращаемое значение должно равняться нулю, если значение Нкоде не **HSHELL_APPCOMMAND** и процедура оболочки обрабатывает сообщение **WM_COMMAND** .</span><span class="sxs-lookup"><span data-stu-id="6c4aa-199">The return value should be zero unless the value of nCode is **HSHELL_APPCOMMAND** and the shell procedure handles the **WM_COMMAND** message.</span></span>
<span data-ttu-id="6c4aa-200">В этом случае возвращаемое значение должно быть ненулевым.</span><span class="sxs-lookup"><span data-stu-id="6c4aa-200">In this case, the return should be nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c4aa-201">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c4aa-201">Remarks</span></span>

<span data-ttu-id="6c4aa-202">Установите эту процедуру-обработчик, указав тип обработчика [WH_SHELL](about-hooks.md) и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="6c4aa-202">Install this hook procedure by specifying the [WH_SHELL](about-hooks.md) hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c4aa-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c4aa-203">See also</span></span>

[<span data-ttu-id="6c4aa-204">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="6c4aa-204">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="6c4aa-205">SendMessage</span><span class="sxs-lookup"><span data-stu-id="6c4aa-205">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[<span data-ttu-id="6c4aa-206">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="6c4aa-206">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="6c4aa-207">WM_APPCOMMAND</span><span class="sxs-lookup"><span data-stu-id="6c4aa-207">WM_APPCOMMAND</span></span>](/windows/desktop/inputdev/wm-appcommand)

[<span data-ttu-id="6c4aa-208">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="6c4aa-208">WM_COMMAND</span></span>](/windows/desktop/menurc/wm-command)

[<span data-ttu-id="6c4aa-209">Обработчики</span><span class="sxs-lookup"><span data-stu-id="6c4aa-209">Hooks</span></span>](hooks.md)
