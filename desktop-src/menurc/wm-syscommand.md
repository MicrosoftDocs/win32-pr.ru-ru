---
title: Сообщение WM_SYSCOMMAND (Winuser. h)
description: Окно получает это сообщение, когда пользователь выбирает команду из меню «окно» (прежнее название — система или меню «Управление») или когда пользователь нажимает кнопку развернуть, кнопку сворачивания, кнопку восстановить или кнопку Закрыть.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698822"
---
# <a name="wm_syscommand-message"></a><span data-ttu-id="b14e9-104">\_Сообщение СИСКОММАНД WM</span><span class="sxs-lookup"><span data-stu-id="b14e9-104">WM\_SYSCOMMAND message</span></span>

<span data-ttu-id="b14e9-105">Окно получает это сообщение, когда пользователь выбирает команду из меню « **окно»** (прежнее название — система или меню «Управление») или когда пользователь нажимает кнопку развернуть, кнопку сворачивания, кнопку восстановить или кнопку Закрыть.</span><span class="sxs-lookup"><span data-stu-id="b14e9-105">A window receives this message when the user chooses a command from the **Window** menu (formerly known as the system or control menu) or when the user chooses the maximize button, minimize button, restore button, or close button.</span></span>


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a><span data-ttu-id="b14e9-106">Пример</span><span class="sxs-lookup"><span data-stu-id="b14e9-106">Example</span></span>

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
<span data-ttu-id="b14e9-107">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="b14e9-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) on GitHub.</span></span>

## <a name="parameters"></a><span data-ttu-id="b14e9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b14e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14e9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b14e9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b14e9-110">Тип запрашиваемой системной команды.</span><span class="sxs-lookup"><span data-stu-id="b14e9-110">The type of system command requested.</span></span> <span data-ttu-id="b14e9-111">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="b14e9-111">This parameter can be one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b14e9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b14e9-112">Value</span></span></th>
<th><span data-ttu-id="b14e9-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b14e9-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <span data-ttu-id="b14e9-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-115">Закрывает окно.</span><span class="sxs-lookup"><span data-stu-id="b14e9-115">Closes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <span data-ttu-id="b14e9-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-117">Изменяет курсор на вопросительный знак с помощью указателя.</span><span class="sxs-lookup"><span data-stu-id="b14e9-117">Changes the cursor to a question mark with a pointer.</span></span> <span data-ttu-id="b14e9-118">Если пользователь щелкает элемент управления в диалоговом окне, элемент управления получает <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> сообщение.</span><span class="sxs-lookup"><span data-stu-id="b14e9-118">If the user then clicks a control in the dialog box, the control receives a <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <span data-ttu-id="b14e9-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-120">Выбирает элемент по умолчанию; пользователь дважды щелкнул меню окно.</span><span class="sxs-lookup"><span data-stu-id="b14e9-120">Selects the default item; the user double-clicked the window menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <span data-ttu-id="b14e9-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-122">Активирует окно, связанное с заданной приложением горячей клавишей.</span><span class="sxs-lookup"><span data-stu-id="b14e9-122">Activates the window associated with the application-specified hot key.</span></span> <span data-ttu-id="b14e9-123">Параметр <em>lParam</em> определяет окно для активации.</span><span class="sxs-lookup"><span data-stu-id="b14e9-123">The <em>lParam</em> parameter identifies the window to activate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <span data-ttu-id="b14e9-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-125">Выполняет прокрутку по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="b14e9-125">Scrolls horizontally.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <span data-ttu-id="b14e9-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-127">Указывает, является ли экранная заставка безопасной.</span><span class="sxs-lookup"><span data-stu-id="b14e9-127">Indicates whether the screen saver is secure.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <span data-ttu-id="b14e9-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-129">Извлекает меню окна в результате нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="b14e9-129">Retrieves the window menu as a result of a keystroke.</span></span> <span data-ttu-id="b14e9-130">Дополнительные сведения см. в разделе "Замечания".</span><span class="sxs-lookup"><span data-stu-id="b14e9-130">For more information, see the Remarks section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <span data-ttu-id="b14e9-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-132">Разворачивает окно.</span><span class="sxs-lookup"><span data-stu-id="b14e9-132">Maximizes the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <span data-ttu-id="b14e9-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-134">Сворачивает окно.</span><span class="sxs-lookup"><span data-stu-id="b14e9-134">Minimizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <span data-ttu-id="b14e9-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-136">Задает состояние отображения.</span><span class="sxs-lookup"><span data-stu-id="b14e9-136">Sets the state of the display.</span></span> <span data-ttu-id="b14e9-137">Эта команда поддерживает устройства с функциями энергосбережения, такими как персональный компьютер с питанием от аккумулятора.</span><span class="sxs-lookup"><span data-stu-id="b14e9-137">This command supports devices that have power-saving features, such as a battery-powered personal computer.</span></span> <br/> <span data-ttu-id="b14e9-138">Параметр <em>lParam</em> может иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b14e9-138">The <em>lParam</em> parameter can have the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="b14e9-139">-1 (при включении дисплея)</span><span class="sxs-lookup"><span data-stu-id="b14e9-139">-1 (the display is powering on)</span></span></li>
<li><span data-ttu-id="b14e9-140">1 (дисплей переходит в низкую степень)</span><span class="sxs-lookup"><span data-stu-id="b14e9-140">1 (the display is going to low power)</span></span></li>
<li><span data-ttu-id="b14e9-141">2 (отображение завершается)</span><span class="sxs-lookup"><span data-stu-id="b14e9-141">2 (the display is being shut off)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <span data-ttu-id="b14e9-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-143">Извлекает меню окна в результате щелчка мышью.</span><span class="sxs-lookup"><span data-stu-id="b14e9-143">Retrieves the window menu as a result of a mouse click.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <span data-ttu-id="b14e9-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-145">Перемещает окно.</span><span class="sxs-lookup"><span data-stu-id="b14e9-145">Moves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <span data-ttu-id="b14e9-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-147">Переход к следующему окну.</span><span class="sxs-lookup"><span data-stu-id="b14e9-147">Moves to the next window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <span data-ttu-id="b14e9-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-149">Переход к предыдущему окну.</span><span class="sxs-lookup"><span data-stu-id="b14e9-149">Moves to the previous window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <span data-ttu-id="b14e9-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-151">Восстанавливает нормальное расположение и размер окна.</span><span class="sxs-lookup"><span data-stu-id="b14e9-151">Restores the window to its normal position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <span data-ttu-id="b14e9-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-153">Выполняет приложение экранной заставки, указанное в разделе [boot] файла System.ini.</span><span class="sxs-lookup"><span data-stu-id="b14e9-153">Executes the screen saver application specified in the [boot] section of the System.ini file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <span data-ttu-id="b14e9-154"><dt><strong>SC_SIZE</strong></dt> <dt>число 0xF000 не</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-155">Изменяет размер окна.</span><span class="sxs-lookup"><span data-stu-id="b14e9-155">Sizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <span data-ttu-id="b14e9-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-157">Активирует меню " <strong>Пуск</strong> ".</span><span class="sxs-lookup"><span data-stu-id="b14e9-157">Activates the <strong>Start</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <span data-ttu-id="b14e9-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span><span class="sxs-lookup"><span data-stu-id="b14e9-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span></span></dl></td>
<td><span data-ttu-id="b14e9-159">Прокрутка по вертикали.</span><span class="sxs-lookup"><span data-stu-id="b14e9-159">Scrolls vertically.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="b14e9-160">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b14e9-160">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b14e9-161">Слово нижнего порядка задает горизонтальное расположение курсора в экранных координатах, если команда меню окна выбрана с мышью.</span><span class="sxs-lookup"><span data-stu-id="b14e9-161">The low-order word specifies the horizontal position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="b14e9-162">В противном случае этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="b14e9-162">Otherwise, this parameter is not used.</span></span>

<span data-ttu-id="b14e9-163">Слово в высоком порядке указывает вертикальное расположение курсора в экранных координатах, если команда меню окна выбрана с мышью.</span><span class="sxs-lookup"><span data-stu-id="b14e9-163">The high-order word specifies the vertical position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="b14e9-164">Этот параметр равен 1, если команда выбрана с помощью системного ускорителя, или нуль при использовании назначенной клавиши.</span><span class="sxs-lookup"><span data-stu-id="b14e9-164">This parameter is  1 if the command is chosen using a system accelerator, or zero if using a mnemonic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14e9-165">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b14e9-165">Return value</span></span>

<span data-ttu-id="b14e9-166">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="b14e9-166">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b14e9-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b14e9-167">Remarks</span></span>

<span data-ttu-id="b14e9-168">Чтобы получить координаты положения в координатах экрана, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="b14e9-168">To obtain the position coordinates in screen coordinates, use the following code:</span></span>


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



<span data-ttu-id="b14e9-169">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выполняет запрос меню окна для предопределенных действий, указанных в предыдущей таблице.</span><span class="sxs-lookup"><span data-stu-id="b14e9-169">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function carries out the window menu request for the predefined actions specified in the previous table.</span></span>

<span data-ttu-id="b14e9-170">В сообщениях **WM \_ сискомманд** четыре младшие биты параметра *wParam* используются системой внутри системы.</span><span class="sxs-lookup"><span data-stu-id="b14e9-170">In **WM\_SYSCOMMAND** messages, the four low-order bits of the *wParam* parameter are used internally by the system.</span></span> <span data-ttu-id="b14e9-171">Чтобы получить правильный результат при проверке значения *wParam*, приложение должно объединить значение 0xFFF0 с значением *wParam* с помощью побитового оператора и.</span><span class="sxs-lookup"><span data-stu-id="b14e9-171">To obtain the correct result when testing the value of *wParam*, an application must combine the value 0xFFF0 with the *wParam* value by using the bitwise AND operator.</span></span>

<span data-ttu-id="b14e9-172">Пункты меню в меню окно можно изменить с помощью функций [**жетсистеммену**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**аппендмену**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**инсертмену**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**модифимену**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**инсертменуитем**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)и [**сетменуитеминфо**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="b14e9-172">The menu items in a window menu can be modified by using the [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), and [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) functions.</span></span> <span data-ttu-id="b14e9-173">Приложения, изменяющие меню окна, должны обрабатывать сообщения **WM \_ сискомманд** .</span><span class="sxs-lookup"><span data-stu-id="b14e9-173">Applications that modify the window menu must process **WM\_SYSCOMMAND** messages.</span></span>

<span data-ttu-id="b14e9-174">Приложение может выполнять любую системную команду в любое время, передавая сообщение **WM \_ Сискомманд** в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="b14e9-174">An application can carry out any system command at any time by passing a **WM\_SYSCOMMAND** message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="b14e9-175">Все сообщения **WM \_ сискомманд** , не обрабатываемые приложением, должны передаваться в **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="b14e9-175">Any **WM\_SYSCOMMAND** messages not handled by the application must be passed to **DefWindowProc**.</span></span> <span data-ttu-id="b14e9-176">Все значения команд, добавленные приложением, должны обрабатываться приложением и не могут быть переданы в **дефвиндовпрок**.</span><span class="sxs-lookup"><span data-stu-id="b14e9-176">Any command values added by an application must be processed by the application and cannot be passed to **DefWindowProc**.</span></span>

<span data-ttu-id="b14e9-177">Если защита паролем включена политикой, экранная заставка запускается независимо от того, какое действие выполняет приложение с уведомлением **SC \_ скринсаве** , даже если оно не передается в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="b14e9-177">If password protection is enabled by policy, the screen saver is started regardless of what an application does with the **SC\_SCREENSAVE** notification even if fails to pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="b14e9-178">Сочетания клавиш, определенные для выбора элементов из меню "окно", преобразуются в сообщения **WM \_ сискомманд** . все остальные сочетания клавиш переводятся в [**\_ Командные сообщения WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="b14e9-178">Accelerator keys that are defined to choose items from the window menu are translated into **WM\_SYSCOMMAND** messages; all other accelerator keystrokes are translated into [**WM\_COMMAND**](wm-command.md) messages.</span></span>

<span data-ttu-id="b14e9-179">Если параметр *wParam* имеет значение **SC \_ кэймену**, то параметр *lParam* содержит код символа ключа, который используется с клавишей Alt для вывода всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="b14e9-179">If the *wParam* is **SC\_KEYMENU**, *lParam* contains the character code of the key that is used with the ALT key to display the popup menu.</span></span> <span data-ttu-id="b14e9-180">Например, если нажать клавиши ALT + F, чтобы отобразить всплывающее окно файла **, \_ сискомманд WM** с параметром *wParam* , равным **SC \_ кэймену** и *lParam* , равным "F".</span><span class="sxs-lookup"><span data-stu-id="b14e9-180">For example, pressing ALT+F to display the File popup will cause a **WM\_SYSCOMMAND** with *wParam* equal to **SC\_KEYMENU** and *lParam* equal to 'f'.</span></span>

## <a name="requirements"></a><span data-ttu-id="b14e9-181">Требования</span><span class="sxs-lookup"><span data-stu-id="b14e9-181">Requirements</span></span>



| <span data-ttu-id="b14e9-182">Требование</span><span class="sxs-lookup"><span data-stu-id="b14e9-182">Requirement</span></span> | <span data-ttu-id="b14e9-183">Значение</span><span class="sxs-lookup"><span data-stu-id="b14e9-183">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14e9-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b14e9-184">Minimum supported client</span></span><br/> | <span data-ttu-id="b14e9-185">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b14e9-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b14e9-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b14e9-186">Minimum supported server</span></span><br/> | <span data-ttu-id="b14e9-187">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b14e9-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b14e9-188">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b14e9-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="b14e9-189"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b14e9-189"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b14e9-190">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b14e9-190">See also</span></span>

<dl> <dt>

<span data-ttu-id="b14e9-191">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="b14e9-191">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b14e9-192">**аппендмену**</span><span class="sxs-lookup"><span data-stu-id="b14e9-192">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="b14e9-193">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="b14e9-193">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="b14e9-194">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="b14e9-194">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b14e9-195">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="b14e9-195">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b14e9-196">**жетсистеммену**</span><span class="sxs-lookup"><span data-stu-id="b14e9-196">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[<span data-ttu-id="b14e9-197">**инсертмену**</span><span class="sxs-lookup"><span data-stu-id="b14e9-197">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[<span data-ttu-id="b14e9-198">**модифимену**</span><span class="sxs-lookup"><span data-stu-id="b14e9-198">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[<span data-ttu-id="b14e9-199">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="b14e9-199">**WM\_COMMAND**</span></span>](wm-command.md)
</dt> <dt>

<span data-ttu-id="b14e9-200">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b14e9-200">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b14e9-201">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="b14e9-201">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

