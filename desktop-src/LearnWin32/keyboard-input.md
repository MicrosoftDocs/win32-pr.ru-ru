---
title: Ввод с клавиатуры (начало работы с Win32 и C++)
description: Ввод с клавиатуры
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "105674517"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a><span data-ttu-id="adcb4-103">Ввод с клавиатуры (начало работы с Win32 и C++)</span><span class="sxs-lookup"><span data-stu-id="adcb4-103">Keyboard Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="adcb4-104">Клавиатура используется для нескольких различных типов входных данных, включая:</span><span class="sxs-lookup"><span data-stu-id="adcb4-104">The keyboard is used for several distinct types of input, including:</span></span>

-   <span data-ttu-id="adcb4-105">Ввод символов.</span><span class="sxs-lookup"><span data-stu-id="adcb4-105">Character input.</span></span> <span data-ttu-id="adcb4-106">Текст, который пользователь вводит в документ или поле редактирования.</span><span class="sxs-lookup"><span data-stu-id="adcb4-106">Text that the user types into a document or edit box.</span></span>
-   <span data-ttu-id="adcb4-107">Сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="adcb4-107">Keyboard shortcuts.</span></span> <span data-ttu-id="adcb4-108">Ключевые черты, которые вызывают функции приложения; Например, CTRL + O, чтобы открыть файл.</span><span class="sxs-lookup"><span data-stu-id="adcb4-108">Key strokes that invoke application functions; for example, CTRL + O to open a file.</span></span>
-   <span data-ttu-id="adcb4-109">Системные команды.</span><span class="sxs-lookup"><span data-stu-id="adcb4-109">System commands.</span></span> <span data-ttu-id="adcb4-110">Ключевые черты, вызывающие системные функции; Например, ALT + TAB для переключения окон.</span><span class="sxs-lookup"><span data-stu-id="adcb4-110">Key strokes that invoke system functions; for example, ALT + TAB to switch windows.</span></span>

<span data-ttu-id="adcb4-111">При обдумывании ввода с клавиатуры важно помнить, что сочетание клавиш не совпадает с символом.</span><span class="sxs-lookup"><span data-stu-id="adcb4-111">When thinking about keyboard input, it is important to remember that a key stroke is not the same as a character.</span></span> <span data-ttu-id="adcb4-112">Например, при нажатии клавиши может появиться любой из следующих символов.</span><span class="sxs-lookup"><span data-stu-id="adcb4-112">For example, pressing the A key could result in any of the following characters.</span></span>

-   <span data-ttu-id="adcb4-113">а</span><span class="sxs-lookup"><span data-stu-id="adcb4-113">a</span></span>
-   <span data-ttu-id="adcb4-114">Объект</span><span class="sxs-lookup"><span data-stu-id="adcb4-114">A</span></span>
-   <span data-ttu-id="adcb4-115">б (если клавиатура поддерживает сочетание диакритических знаков)</span><span class="sxs-lookup"><span data-stu-id="adcb4-115">á (if the keyboard supports combining diacritics)</span></span>

<span data-ttu-id="adcb4-116">Кроме того, если клавиша ALT удерживается, нажатие клавиши вызывает ALT + A, который система не обрабатывает как символ, а вместо системной команды.</span><span class="sxs-lookup"><span data-stu-id="adcb4-116">Further, if the ALT key is held down, pressing the A key produces ALT+A, which the system does not treat as a character at all, but rather as a system command.</span></span>

## <a name="key-codes"></a><span data-ttu-id="adcb4-117">Коды клавиш</span><span class="sxs-lookup"><span data-stu-id="adcb4-117">Key Codes</span></span>

<span data-ttu-id="adcb4-118">При нажатии клавиши оборудование создает *код сканирования*.</span><span class="sxs-lookup"><span data-stu-id="adcb4-118">When you press a key, the hardware generates a *scan code*.</span></span> <span data-ttu-id="adcb4-119">Коды сканирования меняются от одной клавиатуры к следующей, и для событий ключа и нажатия клавиш существуют отдельные коды проверки.</span><span class="sxs-lookup"><span data-stu-id="adcb4-119">Scan codes vary from one keyboard to the next, and there are separate scan codes for key-up and key-down events.</span></span> <span data-ttu-id="adcb4-120">Вы почти не будете заботиться о кодах проверки.</span><span class="sxs-lookup"><span data-stu-id="adcb4-120">You will almost never care about scan codes.</span></span> <span data-ttu-id="adcb4-121">Драйвер клавиатуры преобразует коды проверки в *коды виртуальных клавиш*.</span><span class="sxs-lookup"><span data-stu-id="adcb4-121">The keyboard driver translates scan codes into *virtual-key codes*.</span></span> <span data-ttu-id="adcb4-122">Коды виртуальных клавиш не зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="adcb4-122">Virtual-key codes are device-independent.</span></span> <span data-ttu-id="adcb4-123">При нажатии клавиши на любой клавиатуре создается тот же код виртуального ключа.</span><span class="sxs-lookup"><span data-stu-id="adcb4-123">Pressing the A key on any keyboard generates the same virtual-key code.</span></span>

<span data-ttu-id="adcb4-124">В общем случае коды виртуальных клавиш не соответствуют кодам ASCII или любому другому стандарту кодировки символов.</span><span class="sxs-lookup"><span data-stu-id="adcb4-124">In general, virtual-key codes do not correspond to ASCII codes or any other character-encoding standard.</span></span> <span data-ttu-id="adcb4-125">Это очевидно, если вы думаете о нем, так как один и тот же ключ может создавать разные символы (a, б), а некоторые ключи, такие как функциональные клавиши, не соответствуют какому-либо символу.</span><span class="sxs-lookup"><span data-stu-id="adcb4-125">This is obvious if you think about it, because the same key can generate different characters (a, A, á), and some keys, such as function keys, do not correspond to any character.</span></span>

<span data-ttu-id="adcb4-126">С другой стороны, следующие коды виртуальных клавиш соответствуют эквивалентам ASCII:</span><span class="sxs-lookup"><span data-stu-id="adcb4-126">That said, the following virtual-key codes do map to ASCII equivalents:</span></span>

-   <span data-ttu-id="adcb4-127">от 0 до 9 ключей = ASCII "0" – "9" (0x30 – 0x39)</span><span class="sxs-lookup"><span data-stu-id="adcb4-127">0 through 9 keys = ASCII '0' – '9' (0x30 – 0x39)</span></span>
-   <span data-ttu-id="adcb4-128">От A до Z клавиш = ASCII ' A ' – ' Z ' (0x41 влево – 0x5A)</span><span class="sxs-lookup"><span data-stu-id="adcb4-128">A through Z keys = ASCII 'A' – 'Z' (0x41 – 0x5A)</span></span>

<span data-ttu-id="adcb4-129">В некоторых отношениях это сопоставление относится к сожалению, поскольку в этом случае не следует думать о кодах виртуальных клавиш как символах, по указанным причинам.</span><span class="sxs-lookup"><span data-stu-id="adcb4-129">In some respects this mapping is unfortunate, because you should never think of virtual-key codes as characters, for the reasons discussed.</span></span>

<span data-ttu-id="adcb4-130">Файл заголовка WinUser. h определяет константы для большинства кодов виртуальных клавиш.</span><span class="sxs-lookup"><span data-stu-id="adcb4-130">The header file WinUser.h defines constants for most of the virtual-key codes.</span></span> <span data-ttu-id="adcb4-131">Например, код виртуального ключа для клавиши со стрелкой влево — **VK \_ Left** (0x25).</span><span class="sxs-lookup"><span data-stu-id="adcb4-131">For example, the virtual-key code for the LEFT ARROW key is **VK\_LEFT** (0x25).</span></span> <span data-ttu-id="adcb4-132">Полный список кодов виртуальных ключей см. в разделе [**коды виртуальных ключей**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="adcb4-132">For the complete list of virtual-key codes, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="adcb4-133">Для кодов виртуальных клавиш, соответствующих значениям ASCII, константы не определены.</span><span class="sxs-lookup"><span data-stu-id="adcb4-133">No constants are defined for the virtual-key codes that match ASCII values.</span></span> <span data-ttu-id="adcb4-134">Например, код виртуального ключа для ключа — 0x41 влево, но нет константы с именем **VK \_ A**.</span><span class="sxs-lookup"><span data-stu-id="adcb4-134">For example, the virtual-key code for the A key is 0x41, but there is no constant named **VK\_A**.</span></span> <span data-ttu-id="adcb4-135">Вместо этого просто используйте числовое значение.</span><span class="sxs-lookup"><span data-stu-id="adcb4-135">Instead, just use the numeric value.</span></span>

## <a name="key-down-and-key-up-messages"></a><span data-ttu-id="adcb4-136">Сообщения Key-Down и Key-Up</span><span class="sxs-lookup"><span data-stu-id="adcb4-136">Key-Down and Key-Up Messages</span></span>

<span data-ttu-id="adcb4-137">При нажатии клавиши окно с фокусом клавиатуры получает одно из следующих сообщений.</span><span class="sxs-lookup"><span data-stu-id="adcb4-137">When you press a key, the window that has keyboard focus receives one of the following messages.</span></span>

-   [<span data-ttu-id="adcb4-138">**WM \_ сискэйдовн**</span><span class="sxs-lookup"><span data-stu-id="adcb4-138">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
-   [<span data-ttu-id="adcb4-139">**WM \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="adcb4-139">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)

<span data-ttu-id="adcb4-140">Сообщение [**WM \_ сискэйдовн**](/windows/desktop/inputdev/wm-syskeydown) указывает на *системный ключ*, который является ключевым росчерком, вызывающим системную команду.</span><span class="sxs-lookup"><span data-stu-id="adcb4-140">The [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message indicates a *system key*, which is a key stroke that invokes a system command.</span></span> <span data-ttu-id="adcb4-141">Существует два типа системного ключа:</span><span class="sxs-lookup"><span data-stu-id="adcb4-141">There are two types of system key:</span></span>

-   <span data-ttu-id="adcb4-142">ALT + любой ключ</span><span class="sxs-lookup"><span data-stu-id="adcb4-142">ALT + any key</span></span>
-   <span data-ttu-id="adcb4-143">F10</span><span class="sxs-lookup"><span data-stu-id="adcb4-143">F10</span></span>

<span data-ttu-id="adcb4-144">Клавиша F10 активирует строку меню окна.</span><span class="sxs-lookup"><span data-stu-id="adcb4-144">The F10 key activates the menu bar of a window.</span></span> <span data-ttu-id="adcb4-145">Различные сочетания ALT-клавиш вызывают системные команды.</span><span class="sxs-lookup"><span data-stu-id="adcb4-145">Various ALT-key combinations invoke system commands.</span></span> <span data-ttu-id="adcb4-146">Например, клавиши ALT + TAB переключились на новое окно.</span><span class="sxs-lookup"><span data-stu-id="adcb4-146">For example, ALT + TAB switches to a new window.</span></span> <span data-ttu-id="adcb4-147">Кроме того, если окно содержит меню, клавишу ALT можно использовать для активации пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="adcb4-147">In addition, if a window has a menu, the ALT key can be used to activate menu items.</span></span> <span data-ttu-id="adcb4-148">Некоторые сочетания клавиш ALT не выполняют никаких действий.</span><span class="sxs-lookup"><span data-stu-id="adcb4-148">Some ALT key combinations do not do anything.</span></span>

<span data-ttu-id="adcb4-149">Все остальные сочетания клавиш считаются несистемными ключами и создают сообщение [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="adcb4-149">All other key strokes are considered nonsystem keys and produce the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span> <span data-ttu-id="adcb4-150">Сюда входят функциональные клавиши, отличные от F10.</span><span class="sxs-lookup"><span data-stu-id="adcb4-150">This includes the function keys other than F10.</span></span>

<span data-ttu-id="adcb4-151">При освобождении ключа система отправляет соответствующее сообщение о ключе:</span><span class="sxs-lookup"><span data-stu-id="adcb4-151">When you release a key, the system sends a corresponding key-up message:</span></span>

-   [<span data-ttu-id="adcb4-152">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="adcb4-152">**WM\_KEYUP**</span></span>](/windows/desktop/inputdev/wm-keyup)
-   [<span data-ttu-id="adcb4-153">**WM \_ сискэйуп**</span><span class="sxs-lookup"><span data-stu-id="adcb4-153">**WM\_SYSKEYUP**</span></span>](/windows/desktop/inputdev/wm-syskeyup)

<span data-ttu-id="adcb4-154">Если удерживать ключ достаточно долго для запуска функции повтора клавиатуры, система отправляет несколько сообщений о ключах, за которыми следует одно сообщение о нажатии.</span><span class="sxs-lookup"><span data-stu-id="adcb4-154">If you hold down a key long enough to start the keyboard's repeat feature, the system sends multiple key-down messages, followed by a single key-up message.</span></span>

<span data-ttu-id="adcb4-155">Во всех четырех описанных выше сообщениях клавиатуры параметр *wParam* содержит код виртуального ключа.</span><span class="sxs-lookup"><span data-stu-id="adcb4-155">In all four of the keyboard messages discussed so far, the *wParam* parameter contains the virtual-key code of the key.</span></span> <span data-ttu-id="adcb4-156">Параметр *lParam* содержит некоторые прочие сведения, упакованные в 32 бит.</span><span class="sxs-lookup"><span data-stu-id="adcb4-156">The *lParam* parameter contains some miscellaneous information packed into 32 bits.</span></span> <span data-ttu-id="adcb4-157">Как правило, сведения не нужны в параметре *lParam*.</span><span class="sxs-lookup"><span data-stu-id="adcb4-157">You typically do not need the information in *lParam*.</span></span> <span data-ttu-id="adcb4-158">Одним из флагов, которые могут быть полезны, является бит 30, флаг "предыдущее состояние ключа" которого имеет значение 1 для повторяющихся сообщений о нажатии клавиш.</span><span class="sxs-lookup"><span data-stu-id="adcb4-158">One flag that might be useful is bit 30, the "previous key state" flag, which is set to 1 for repeated key-down messages.</span></span>

<span data-ttu-id="adcb4-159">Как следует из названия, системные клавиши обводки в основном предназначены для использования операционной системой.</span><span class="sxs-lookup"><span data-stu-id="adcb4-159">As the name implies, system key strokes are primarily intended for use by the operating system.</span></span> <span data-ttu-id="adcb4-160">Если вы перехватите сообщение [**WM \_ сискэйдовн**](/windows/desktop/inputdev/wm-syskeydown) , вызовите [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) позже.</span><span class="sxs-lookup"><span data-stu-id="adcb4-160">If you intercept the [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message, call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afterward.</span></span> <span data-ttu-id="adcb4-161">В противном случае операционная система будет заблокирована для обработки команды.</span><span class="sxs-lookup"><span data-stu-id="adcb4-161">Otherwise, you will block the operating system from handling the command.</span></span>

## <a name="character-messages"></a><span data-ttu-id="adcb4-162">Символьные сообщения</span><span class="sxs-lookup"><span data-stu-id="adcb4-162">Character Messages</span></span>

<span data-ttu-id="adcb4-163">При помощи функции [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , которую мы впервые видели в [модуле 1](your-first-windows-program.md), они преобразуются в символы.</span><span class="sxs-lookup"><span data-stu-id="adcb4-163">Key strokes are converted into characters by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function, which we first saw in [Module 1](your-first-windows-program.md).</span></span> <span data-ttu-id="adcb4-164">Эта функция проверяет сообщения о нажатии клавиш и преобразует их в символы.</span><span class="sxs-lookup"><span data-stu-id="adcb4-164">This function examines key-down messages and translates them into characters.</span></span> <span data-ttu-id="adcb4-165">Для каждого созданного символа функция **TranslateMessage** помещает сообщение [**WM \_ char**](/windows/desktop/inputdev/wm-char) или [**WM \_ сисчар**](/windows/desktop/menurc/wm-syschar) в очередь сообщений окна.</span><span class="sxs-lookup"><span data-stu-id="adcb4-165">For each character that is produced, the **TranslateMessage** function puts a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) or [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message on the message queue of the window.</span></span> <span data-ttu-id="adcb4-166">Параметр *wParam* сообщения содержит символ UTF-16.</span><span class="sxs-lookup"><span data-stu-id="adcb4-166">The *wParam* parameter of the message contains the UTF-16 character.</span></span>

<span data-ttu-id="adcb4-167">Как вы можете догадаться, сообщения [**WM \_ char**](/windows/desktop/inputdev/wm-char) формируются из сообщений [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) , а сообщения [**WM \_ сисчар**](/windows/desktop/menurc/wm-syschar) создаются из сообщений [**WM \_ сискэйдовн**](/windows/desktop/inputdev/wm-syskeydown) .</span><span class="sxs-lookup"><span data-stu-id="adcb4-167">As you might guess, [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages are generated from [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, while [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) messages are generated from [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) messages.</span></span> <span data-ttu-id="adcb4-168">Например, предположим, что пользователь нажимает клавишу SHIFT, а затем ключ.</span><span class="sxs-lookup"><span data-stu-id="adcb4-168">For example, suppose the user presses the SHIFT key followed by the A key.</span></span> <span data-ttu-id="adcb4-169">При условии стандартной раскладки клавиатуры вы получите следующую последовательность сообщений:</span><span class="sxs-lookup"><span data-stu-id="adcb4-169">Assuming a standard keyboard layout, you would get the following sequence of messages:</span></span>

<span data-ttu-id="adcb4-170">**WM \_ KEYDOWN**: Shift</span><span class="sxs-lookup"><span data-stu-id="adcb4-170">**WM\_KEYDOWN**: SHIFT</span></span>  
<span data-ttu-id="adcb4-171">**WM \_ KEYDOWN**: A</span><span class="sxs-lookup"><span data-stu-id="adcb4-171">**WM\_KEYDOWN**: A</span></span>  
<span data-ttu-id="adcb4-172">**WM \_ CHAR**: ' A '</span><span class="sxs-lookup"><span data-stu-id="adcb4-172">**WM\_CHAR**: 'A'</span></span>  


<span data-ttu-id="adcb4-173">С другой стороны, сочетание ALT + P создаст следующее:</span><span class="sxs-lookup"><span data-stu-id="adcb4-173">On the other hand, the combination ALT + P would generate:</span></span>

 <span data-ttu-id="adcb4-174">**WM \_ СИСКЭЙДОВН**: \_ меню VK</span><span class="sxs-lookup"><span data-stu-id="adcb4-174">**WM\_SYSKEYDOWN**: VK\_MENU</span></span>  
<span data-ttu-id="adcb4-175">**WM \_ СИСКЭЙДОВН**: 0x50</span><span class="sxs-lookup"><span data-stu-id="adcb4-175">**WM\_SYSKEYDOWN**: 0x50</span></span>  
<span data-ttu-id="adcb4-176">**WM \_ СИСЧАР**: "p"</span><span class="sxs-lookup"><span data-stu-id="adcb4-176">**WM\_SYSCHAR**: 'p'</span></span>  
<span data-ttu-id="adcb4-177">**WM \_ СИСКЭЙУП**: 0x50</span><span class="sxs-lookup"><span data-stu-id="adcb4-177">**WM\_SYSKEYUP**: 0x50</span></span>  
<span data-ttu-id="adcb4-178">**WM \_ Клавиша вверх**: VK \_ меню</span><span class="sxs-lookup"><span data-stu-id="adcb4-178">**WM\_KEYUP**: VK\_MENU</span></span>  


<span data-ttu-id="adcb4-179">(Код виртуального ключа для клавиши ALT называется VK \_ МЕНЮ по историческим причинам.)</span><span class="sxs-lookup"><span data-stu-id="adcb4-179">(The virtual-key code for the ALT key is named VK\_MENU for historical reasons.)</span></span>

<span data-ttu-id="adcb4-180">Сообщение [**WM \_ сисчар**](/windows/desktop/menurc/wm-syschar) указывает системный символ.</span><span class="sxs-lookup"><span data-stu-id="adcb4-180">The [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message indicates a system character.</span></span> <span data-ttu-id="adcb4-181">Как и в [**WM \_ сискэйдовн**](/windows/desktop/inputdev/wm-syskeydown), это сообщение обычно следует передавать непосредственно в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="adcb4-181">As with [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), you should generally pass this message directly to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="adcb4-182">В противном случае может возникнуть конфликт со стандартными системными командами.</span><span class="sxs-lookup"><span data-stu-id="adcb4-182">Otherwise, you may interfere with standard system commands.</span></span> <span data-ttu-id="adcb4-183">В частности, не следует рассматривать **WM \_ сисчар** как текст, вводимый пользователем.</span><span class="sxs-lookup"><span data-stu-id="adcb4-183">In particular, do not treat **WM\_SYSCHAR** as text that the user has typed.</span></span>

<span data-ttu-id="adcb4-184">Сообщение [**WM \_ char**](/windows/desktop/inputdev/wm-char) — это то, что обычно можно считать символьным вводом.</span><span class="sxs-lookup"><span data-stu-id="adcb4-184">The [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message is what you normally think of as character input.</span></span> <span data-ttu-id="adcb4-185">Тип данных для символа — **WCHAR \_ t**, представляющий символ Юникода UTF-16.</span><span class="sxs-lookup"><span data-stu-id="adcb4-185">The data type for the character is **wchar\_t**, representing a UTF-16 Unicode character.</span></span> <span data-ttu-id="adcb4-186">Символьные данные могут содержать символы за пределами диапазона ASCII, особенно с раскладками клавиатуры, которые обычно используются за пределами США.</span><span class="sxs-lookup"><span data-stu-id="adcb4-186">Character input can include characters outside the ASCII range, especially with keyboard layouts that are commonly used outside of the United States.</span></span> <span data-ttu-id="adcb4-187">Вы можете попробовать различные раскладки клавиатуры, установив региональную клавиатуру, а затем используя функцию экранной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="adcb4-187">You can try different keyboard layouts by installing a regional keyboard and then using the On-Screen Keyboard feature.</span></span>

<span data-ttu-id="adcb4-188">Пользователи также могут установить редактор метода ввода (IME) для ввода сложных наборов символов, таких как японские символы, с помощью стандартной клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="adcb4-188">Users can also install an Input Method Editor (IME) to enter complex scripts, such as Japanese characters, with a standard keyboard.</span></span> <span data-ttu-id="adcb4-189">Например, используя японский редактор IME для ввода символа катакана カ (ка), вы можете получить следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="adcb4-189">For example, using a Japanese IME to enter the katakana character カ (ka), you might get the following messages:</span></span>

<span data-ttu-id="adcb4-190">**WM \_ KEYDOWN**: VK \_ процесскэй (клавиша обработки IME)</span><span class="sxs-lookup"><span data-stu-id="adcb4-190">**WM\_KEYDOWN**: VK\_PROCESSKEY (the IME PROCESS key)</span></span>  
<span data-ttu-id="adcb4-191">**WM \_ Клавиша вверх**: 0x4B</span><span class="sxs-lookup"><span data-stu-id="adcb4-191">**WM\_KEYUP**: 0x4B</span></span>  
<span data-ttu-id="adcb4-192">**WM \_ KEYDOWN**: VK \_ процесскэй</span><span class="sxs-lookup"><span data-stu-id="adcb4-192">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="adcb4-193">**WM \_ Клавиша вверх**: 0x41 влево</span><span class="sxs-lookup"><span data-stu-id="adcb4-193">**WM\_KEYUP**: 0x41</span></span>  
<span data-ttu-id="adcb4-194">**WM \_ KEYDOWN**: VK \_ процесскэй</span><span class="sxs-lookup"><span data-stu-id="adcb4-194">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="adcb4-195">**WM \_ CHAR**: カ</span><span class="sxs-lookup"><span data-stu-id="adcb4-195">**WM\_CHAR**: カ</span></span>  
<span data-ttu-id="adcb4-196">**WM \_ Клавиша вверх**: VK \_ return</span><span class="sxs-lookup"><span data-stu-id="adcb4-196">**WM\_KEYUP**: VK\_RETURN</span></span>  


<span data-ttu-id="adcb4-197">Некоторые сочетания клавиш CTRL преобразуются в управляющие символы ASCII.</span><span class="sxs-lookup"><span data-stu-id="adcb4-197">Some CTRL key combinations are translated into ASCII control characters.</span></span> <span data-ttu-id="adcb4-198">Например, CTRL + A преобразуется в символ ASCII CTRL-A (SOH) (значение ASCII 0x01).</span><span class="sxs-lookup"><span data-stu-id="adcb4-198">For example, CTRL+A is translated to the ASCII ctrl-A (SOH) character (ASCII value 0x01).</span></span> <span data-ttu-id="adcb4-199">Для ввода текста обычно следует отфильтровывать управляющие символы.</span><span class="sxs-lookup"><span data-stu-id="adcb4-199">For text input, you should generally filter out the control characters.</span></span> <span data-ttu-id="adcb4-200">Кроме того, не следует использовать [**WM \_ char**](/windows/desktop/inputdev/wm-char) для реализации сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="adcb4-200">Also, avoid using [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) to implement keyboard shortcuts.</span></span> <span data-ttu-id="adcb4-201">Вместо этого используйте сообщения с помощью [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) или еще лучше, используя таблицу сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="adcb4-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span></span> <span data-ttu-id="adcb4-202">Таблицы ускорителей описаны в следующем разделе: [таблицы сочетаний клавиш](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="adcb4-202">Accelerator tables are described in the next topic, [Accelerator Tables](accelerator-tables.md).</span></span>

<span data-ttu-id="adcb4-203">В следующем коде отображаются основные сообщения клавиатуры в отладчике.</span><span class="sxs-lookup"><span data-stu-id="adcb4-203">The following code displays the main keyboard messages in the debugger.</span></span> <span data-ttu-id="adcb4-204">Попробуйте воспроизвести различные сочетания клавиш и посмотрите, какие сообщения создаются.</span><span class="sxs-lookup"><span data-stu-id="adcb4-204">Try playing with different keystroke combinations and see what messages are generated.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a><span data-ttu-id="adcb4-205">Различные сообщения клавиатуры</span><span class="sxs-lookup"><span data-stu-id="adcb4-205">Miscellaneous Keyboard Messages</span></span>

<span data-ttu-id="adcb4-206">Большинство приложений могут спокойно игнорировать некоторые другие сообщения клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="adcb4-206">Some other keyboard messages can safely be ignored by most applications.</span></span>

-   <span data-ttu-id="adcb4-207">Сообщение [**WM \_ деадчар**](/windows/desktop/inputdev/wm-deadchar) отправляется для комбинированного ключа, например диакритических знаков.</span><span class="sxs-lookup"><span data-stu-id="adcb4-207">The [**WM\_DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) message is sent for a combining key, such as a diacritic.</span></span> <span data-ttu-id="adcb4-208">Например, на клавиатуре для испанского языка при вводе диакритических знаков ('), за которыми следует буква «E».</span><span class="sxs-lookup"><span data-stu-id="adcb4-208">For example, on a Spanish language keyboard, typing accent (') followed by E produces the character é.</span></span> <span data-ttu-id="adcb4-209">Для символа ударения отправляется **\_ деадчар WM** .</span><span class="sxs-lookup"><span data-stu-id="adcb4-209">The **WM\_DEADCHAR** is sent for the accent character.</span></span>
-   <span data-ttu-id="adcb4-210">Сообщение [**WM \_ уничар**](/windows/desktop/inputdev/wm-unichar) устарело.</span><span class="sxs-lookup"><span data-stu-id="adcb4-210">The [**WM\_UNICHAR**](/windows/desktop/inputdev/wm-unichar) message is obsolete.</span></span> <span data-ttu-id="adcb4-211">Он позволяет программам ANSI принимать входные символы Юникода.</span><span class="sxs-lookup"><span data-stu-id="adcb4-211">It enables ANSI programs to receive Unicode character input.</span></span>
-   <span data-ttu-id="adcb4-212">Символ [**\_ IME редактора \_ WM**](/windows/desktop/Intl/wm-ime-char) ОТПРАВЛЯЕТСЯ, когда редактор IME преобразует последовательность нажатия клавиш в символы.</span><span class="sxs-lookup"><span data-stu-id="adcb4-212">The [**WM\_IME\_CHAR**](/windows/desktop/Intl/wm-ime-char) character is sent when an IME translates a keystroke sequence into characters.</span></span> <span data-ttu-id="adcb4-213">Он отправляется в дополнение к обычному сообщению [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="adcb4-213">It is sent in addition to the usual [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>

## <a name="keyboard-state"></a><span data-ttu-id="adcb4-214">Состояние клавиатуры</span><span class="sxs-lookup"><span data-stu-id="adcb4-214">Keyboard State</span></span>

<span data-ttu-id="adcb4-215">Сообщения клавиатуры управляются событиями.</span><span class="sxs-lookup"><span data-stu-id="adcb4-215">The keyboard messages are event-driven.</span></span> <span data-ttu-id="adcb4-216">То есть вы получаете сообщение, когда что-нибудь интересное, например нажатие клавиши, и сообщение сообщает о том, что произошло.</span><span class="sxs-lookup"><span data-stu-id="adcb4-216">That is, you get a message when something interesting happens, such as a key press, and the message tells you what just happened.</span></span> <span data-ttu-id="adcb4-217">Но вы также можете проверить состояние ключа в любое время, вызвав функцию [**жеткэйстате**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .</span><span class="sxs-lookup"><span data-stu-id="adcb4-217">But you can also test the state of a key at any time, by calling the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function.</span></span>

<span data-ttu-id="adcb4-218">Например, рассмотрим, как можно определить сочетание левой кнопки мыши + ALT.</span><span class="sxs-lookup"><span data-stu-id="adcb4-218">For example, consider how would you detect the combination of left mouse click + ALT key.</span></span> <span data-ttu-id="adcb4-219">Вы можете отвести состояние клавиши ALT, прослушивая сообщения о нажатии клавиш и сохранив флаг, но [**жеткэйстате**](/windows/desktop/api/winuser/nf-winuser-getkeystate) экономит проблемы.</span><span class="sxs-lookup"><span data-stu-id="adcb4-219">You could track the state of the ALT key by listening for key-stroke messages and storing a flag, but [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) saves you the trouble.</span></span> <span data-ttu-id="adcb4-220">При получении сообщения [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown) просто вызовите **жеткэйстате** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="adcb4-220">When you receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, just call **GetKeyState** as follows:</span></span>


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



<span data-ttu-id="adcb4-221">Сообщение [**жеткэйстате**](/windows/desktop/api/winuser/nf-winuser-getkeystate) принимает в качестве входных данных код виртуального ключа и возвращает набор битовых флагов (на самом деле только два флага).</span><span class="sxs-lookup"><span data-stu-id="adcb4-221">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) message takes a virtual-key code as input and returns a set of bit flags (actually just two flags).</span></span> <span data-ttu-id="adcb4-222">Значение 0x8000 содержит битовый флаг, который проверяет, нажата ли клавиша в данный момент.</span><span class="sxs-lookup"><span data-stu-id="adcb4-222">The value 0x8000 contains the bit flag that tests whether the key is currently pressed.</span></span>

<span data-ttu-id="adcb4-223">Большинство клавиатур имеют две клавиши ALT слева и справа.</span><span class="sxs-lookup"><span data-stu-id="adcb4-223">Most keyboards have two ALT keys, left and right.</span></span> <span data-ttu-id="adcb4-224">В предыдущем примере проверяется, была ли нажата одна из них.</span><span class="sxs-lookup"><span data-stu-id="adcb4-224">The previous example tests whether either of them of pressed.</span></span> <span data-ttu-id="adcb4-225">Можно также использовать [**жеткэйстате**](/windows/desktop/api/winuser/nf-winuser-getkeystate) для различения левого и правого экземпляров клавиш ALT, Shift или CTRL.</span><span class="sxs-lookup"><span data-stu-id="adcb4-225">You can also use [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) to distinguish between the left and right instances of the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="adcb4-226">Например, следующий код проверяет, нажата ли правая клавиша ALT.</span><span class="sxs-lookup"><span data-stu-id="adcb4-226">For example, the following code tests if the right ALT key is pressed.</span></span>


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



<span data-ttu-id="adcb4-227">Функция [**жеткэйстате**](/windows/desktop/api/winuser/nf-winuser-getkeystate) является интересной, так как она сообщает о состоянии *виртуальной* клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="adcb4-227">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function is interesting because it reports a *virtual* keyboard state.</span></span> <span data-ttu-id="adcb4-228">Это виртуальное состояние основано на содержимом очереди сообщений и обновляется при удалении сообщений из очереди.</span><span class="sxs-lookup"><span data-stu-id="adcb4-228">This virtual state is based on the contents of your message queue, and gets updated as you remove messages from the queue.</span></span> <span data-ttu-id="adcb4-229">По мере того как программа обрабатывает сообщения окна, **жеткэйстате** предоставляет моментальный снимок клавиатуры во время постановки каждого сообщения в очередь.</span><span class="sxs-lookup"><span data-stu-id="adcb4-229">As your program processes window messages, **GetKeyState** gives you a snapshot of the keyboard at the time that each message was queued.</span></span> <span data-ttu-id="adcb4-230">Например, если Последнее сообщение в очереди — [**WM \_ лбуттондовн**](/windows/desktop/inputdev/wm-lbuttondown), **жеткэйстате** сообщает о состоянии клавиатуры в момент нажатия пользователем кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="adcb4-230">For example, if the last message on the queue was [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** reports the keyboard state at the moment when the user clicked the mouse button.</span></span>

<span data-ttu-id="adcb4-231">Так как [**жеткэйстате**](/windows/desktop/api/winuser/nf-winuser-getkeystate) основан на очереди сообщений, она также игнорирует ввод с клавиатуры, отправленный в другую программу.</span><span class="sxs-lookup"><span data-stu-id="adcb4-231">Because [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) is based on your message queue, it also ignores keyboard input that was sent to another program.</span></span> <span data-ttu-id="adcb4-232">Если пользователь переключается на другую программу, любые нажатия клавиш, отправленные в эту программу, игнорируются **жеткэйстате**.</span><span class="sxs-lookup"><span data-stu-id="adcb4-232">If the user switches to another program, any key presses that are sent to that program are ignored by **GetKeyState**.</span></span> <span data-ttu-id="adcb4-233">Если вы действительно хотите получить немедленное физическое состояние клавиатуры, существует функция для этого: [**жетасинккэйстате**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="adcb4-233">If you really want to know the immediate physical state of the keyboard, there is a function for that: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span> <span data-ttu-id="adcb4-234">Однако для большинства кода пользовательского интерфейса правильная функция — **жеткэйстате**.</span><span class="sxs-lookup"><span data-stu-id="adcb4-234">For most UI code, however, the correct function is **GetKeyState**.</span></span>

## <a name="next"></a><span data-ttu-id="adcb4-235">Следующая</span><span class="sxs-lookup"><span data-stu-id="adcb4-235">Next</span></span>

[<span data-ttu-id="adcb4-236">Таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="adcb4-236">Accelerator Tables</span></span>](accelerator-tables.md)

 

 
