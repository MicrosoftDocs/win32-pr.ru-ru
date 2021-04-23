---
title: Использование ввода с клавиатуры
description: В этом разделе рассматриваются задачи, связанные с вводом с клавиатуры.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- Ввод данных пользователем, ввод с клавиатуры
- запись вводимых пользователем данных, ввод с клавиатуры
- ввод с клавиатуры
- сообщения о нажатии клавиш
- Символьные сообщения
- крышки, ввод с клавиатуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76b3f90a626506430b91e7539069c6ecdf634c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710281"
---
# <a name="using-keyboard-input"></a><span data-ttu-id="dc474-109">Использование ввода с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="dc474-109">Using Keyboard Input</span></span>

<span data-ttu-id="dc474-110">Окно получает ввод с клавиатуры в виде сообщений о нажатиях клавиш и символьных сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc474-110">A window receives keyboard input in the form of keystroke messages and character messages.</span></span> <span data-ttu-id="dc474-111">В цикле сообщений, присоединенном к окну, должен быть указан код для преобразования сообщений о нажатии клавиш в соответствующие символьные сообщения.</span><span class="sxs-lookup"><span data-stu-id="dc474-111">The message loop attached to the window must include code to translate keystroke messages into the corresponding character messages.</span></span> <span data-ttu-id="dc474-112">Если окно отображает ввод с клавиатуры в клиентской области, он должен создать и отобразить курсор, указывающий позицию, в которой будет введен следующий символ.</span><span class="sxs-lookup"><span data-stu-id="dc474-112">If the window displays keyboard input in its client area, it should create and display a caret to indicate the position where the next character will be entered.</span></span> <span data-ttu-id="dc474-113">В следующих разделах описывается код, связанный с получением, обработкой и отображением ввода с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="dc474-113">The following sections describe the code involved in receiving, processing, and displaying keyboard input:</span></span>

-   [<span data-ttu-id="dc474-114">Обработка сообщений с нажатием клавиши</span><span class="sxs-lookup"><span data-stu-id="dc474-114">Processing Keystroke Messages</span></span>](#processing-keystroke-messages)
-   [<span data-ttu-id="dc474-115">Преобразование символьных сообщений</span><span class="sxs-lookup"><span data-stu-id="dc474-115">Translating Character Messages</span></span>](#translating-character-messages)
-   [<span data-ttu-id="dc474-116">Обработка сообщений с символами</span><span class="sxs-lookup"><span data-stu-id="dc474-116">Processing Character Messages</span></span>](#processing-character-messages)
-   [<span data-ttu-id="dc474-117">Использование курсора</span><span class="sxs-lookup"><span data-stu-id="dc474-117">Using the Caret</span></span>](#using-the-caret)
-   [<span data-ttu-id="dc474-118">Отображение ввода с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="dc474-118">Displaying Keyboard Input</span></span>](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a><span data-ttu-id="dc474-119">Обработка сообщений с нажатием клавиши</span><span class="sxs-lookup"><span data-stu-id="dc474-119">Processing Keystroke Messages</span></span>

<span data-ttu-id="dc474-120">Оконная процедура окна с фокусом клавиатуры получает сообщения о нажатии клавиш, когда пользователь вводит клавиатуру.</span><span class="sxs-lookup"><span data-stu-id="dc474-120">The window procedure of the window that has the keyboard focus receives keystroke messages when the user types at the keyboard.</span></span> <span data-ttu-id="dc474-121">Сообщения о нажатии клавиши: [**WM \_ KeyDown**](wm-keydown.md), [**WM \_ KEYUP**](wm-keyup.md), [**WM \_ сискэйдовн**](wm-syskeydown.md)и [**WM \_ сискэйуп**](wm-syskeyup.md).</span><span class="sxs-lookup"><span data-stu-id="dc474-121">The keystroke messages are [**WM\_KEYDOWN**](wm-keydown.md), [**WM\_KEYUP**](wm-keyup.md), [**WM\_SYSKEYDOWN**](wm-syskeydown.md), and [**WM\_SYSKEYUP**](wm-syskeyup.md).</span></span> <span data-ttu-id="dc474-122">Типичная процедура окна игнорирует все сообщения с нажатием клавиши, за исключением **WM \_ KeyDown**.</span><span class="sxs-lookup"><span data-stu-id="dc474-122">A typical window procedure ignores all keystroke messages except **WM\_KEYDOWN**.</span></span> <span data-ttu-id="dc474-123">Система отправляет сообщение **WM \_ KeyDown** , когда пользователь нажимает клавишу.</span><span class="sxs-lookup"><span data-stu-id="dc474-123">The system posts the **WM\_KEYDOWN** message when the user presses a key.</span></span>

<span data-ttu-id="dc474-124">Когда процедура окна получает сообщение [**WM \_ KeyDown**](wm-keydown.md) , она должна изучить код виртуального ключа, сопровождающего сообщение, чтобы определить, как обрабатывать нажатие клавиши.</span><span class="sxs-lookup"><span data-stu-id="dc474-124">When the window procedure receives the [**WM\_KEYDOWN**](wm-keydown.md) message, it should examine the virtual-key code that accompanies the message to determine how to process the keystroke.</span></span> <span data-ttu-id="dc474-125">Код виртуального ключа находится в параметре *wParam* сообщения.</span><span class="sxs-lookup"><span data-stu-id="dc474-125">The virtual-key code is in the message's *wParam* parameter.</span></span> <span data-ttu-id="dc474-126">Как правило, приложение обрабатывает только нажатия клавиш, созданные несимвольными ключами, включая функциональные клавиши, клавиши перемещения курсора и специальные сочетания клавиш, такие как INS, DEL, HOME и END.</span><span class="sxs-lookup"><span data-stu-id="dc474-126">Typically, an application processes only keystrokes generated by noncharacter keys, including the function keys, the cursor movement keys, and the special purpose keys such as INS, DEL, HOME, and END.</span></span>

<span data-ttu-id="dc474-127">В следующем примере показана структура оконной процедуры, используемая обычным приложением для получения и обработки сообщений о нажатии клавиш.</span><span class="sxs-lookup"><span data-stu-id="dc474-127">The following example shows the window procedure framework that a typical application uses to receive and process keystroke messages.</span></span>


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a><span data-ttu-id="dc474-128">Преобразование символьных сообщений</span><span class="sxs-lookup"><span data-stu-id="dc474-128">Translating Character Messages</span></span>

<span data-ttu-id="dc474-129">Любой поток, принимающий символьные данные от пользователя, должен включать функцию [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) в свой цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc474-129">Any thread that receives character input from the user must include the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function in its message loop.</span></span> <span data-ttu-id="dc474-130">Эта функция проверяет код виртуального ключа сообщения о нажатии клавиши и, если код соответствует символу, помещает в очередь сообщений символьное сообщение.</span><span class="sxs-lookup"><span data-stu-id="dc474-130">This function examines the virtual-key code of a keystroke message and, if the code corresponds to a character, places a character message into the message queue.</span></span> <span data-ttu-id="dc474-131">Символьное сообщение удаляется и отправляется при следующей итерации цикла обработки сообщений. параметр *wParam* сообщения содержит код символа.</span><span class="sxs-lookup"><span data-stu-id="dc474-131">The character message is removed and dispatched on the next iteration of the message loop; the *wParam* parameter of the message contains the character code.</span></span>

<span data-ttu-id="dc474-132">Как правило, цикл обработки сообщений потока должен использовать функцию [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) для преобразования каждого сообщения, а не только для сообщений с виртуальным ключом.</span><span class="sxs-lookup"><span data-stu-id="dc474-132">In general, a thread's message loop should use the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function to translate every message, not just virtual-key messages.</span></span> <span data-ttu-id="dc474-133">Хотя **TranslateMessage** не влияет на другие типы сообщений, это гарантирует, что ввод с клавиатуры будет преобразован правильно.</span><span class="sxs-lookup"><span data-stu-id="dc474-133">Although **TranslateMessage** has no effect on other types of messages, it guarantees that keyboard input is translated correctly.</span></span> <span data-ttu-id="dc474-134">В следующем примере показано, как включить функцию **TranslateMessage** в типичный цикл обработки сообщений потока.</span><span class="sxs-lookup"><span data-stu-id="dc474-134">The following example shows how to include the **TranslateMessage** function in a typical thread message loop.</span></span>


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a><span data-ttu-id="dc474-135">Обработка сообщений с символами</span><span class="sxs-lookup"><span data-stu-id="dc474-135">Processing Character Messages</span></span>

<span data-ttu-id="dc474-136">Оконная процедура получает символьное сообщение, когда функция [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) преобразует код виртуальной клавиши, соответствующий символьной клавише.</span><span class="sxs-lookup"><span data-stu-id="dc474-136">A window procedure receives a character message when the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function translates a virtual-key code corresponding to a character key.</span></span> <span data-ttu-id="dc474-137">Символьные сообщения имеют [**\_ тип WM char**](wm-char.md), [**WM \_ Деадчар**](wm-deadchar.md), [**WM \_ сисчар**](/windows/desktop/menurc/wm-syschar)и [**WM \_ сисдеадчар**](wm-sysdeadchar.md).</span><span class="sxs-lookup"><span data-stu-id="dc474-137">The character messages are [**WM\_CHAR**](wm-char.md), [**WM\_DEADCHAR**](wm-deadchar.md), [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar), and [**WM\_SYSDEADCHAR**](wm-sysdeadchar.md).</span></span> <span data-ttu-id="dc474-138">Типичная процедура окна игнорирует все символьные сообщения, кроме **WM \_ char**.</span><span class="sxs-lookup"><span data-stu-id="dc474-138">A typical window procedure ignores all character messages except **WM\_CHAR**.</span></span> <span data-ttu-id="dc474-139">Функция **TranslateMessage** создает сообщение **WM \_ char** , когда пользователь нажимает любой из следующих клавиш:</span><span class="sxs-lookup"><span data-stu-id="dc474-139">The **TranslateMessage** function generates a **WM\_CHAR** message when the user presses any of the following keys:</span></span>

-   <span data-ttu-id="dc474-140">Любой ключ символа</span><span class="sxs-lookup"><span data-stu-id="dc474-140">Any character key</span></span>
-   <span data-ttu-id="dc474-141">BACKSPACE</span><span class="sxs-lookup"><span data-stu-id="dc474-141">BACKSPACE</span></span>
-   <span data-ttu-id="dc474-142">Ввод (возврат каретки)</span><span class="sxs-lookup"><span data-stu-id="dc474-142">ENTER (carriage return)</span></span>
-   <span data-ttu-id="dc474-143">ESC</span><span class="sxs-lookup"><span data-stu-id="dc474-143">ESC</span></span>
-   <span data-ttu-id="dc474-144">SHIFT + ВВОД (перевод строки)</span><span class="sxs-lookup"><span data-stu-id="dc474-144">SHIFT+ENTER (linefeed)</span></span>
-   <span data-ttu-id="dc474-145">TAB</span><span class="sxs-lookup"><span data-stu-id="dc474-145">TAB</span></span>

<span data-ttu-id="dc474-146">Когда процедура окна получает сообщение [**WM \_ char**](wm-char.md) , она должна проверить код символа, сопровождающего сообщение, чтобы определить способ обработки символа.</span><span class="sxs-lookup"><span data-stu-id="dc474-146">When a window procedure receives the [**WM\_CHAR**](wm-char.md) message, it should examine the character code that accompanies the message to determine how to process the character.</span></span> <span data-ttu-id="dc474-147">Код символа находится в параметре *wParam* сообщения.</span><span class="sxs-lookup"><span data-stu-id="dc474-147">The character code is in the message's *wParam* parameter.</span></span>

<span data-ttu-id="dc474-148">В следующем примере показана структура оконной процедуры, используемая обычным приложением для получения и обработки символьных сообщений.</span><span class="sxs-lookup"><span data-stu-id="dc474-148">The following example shows the window procedure framework that a typical application uses to receive and process character messages.</span></span>


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a><span data-ttu-id="dc474-149">Использование курсора</span><span class="sxs-lookup"><span data-stu-id="dc474-149">Using the Caret</span></span>

<span data-ttu-id="dc474-150">Окно, получающее ввод с клавиатуры, обычно отображает символы, которые пользователь вводит в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="dc474-150">A window that receives keyboard input typically displays the characters the user types in the window's client area.</span></span> <span data-ttu-id="dc474-151">Окно должно использовать курсор, чтобы указать позицию в клиентской области, где будет отображаться следующий символ.</span><span class="sxs-lookup"><span data-stu-id="dc474-151">A window should use a caret to indicate the position in the client area where the next character will appear.</span></span> <span data-ttu-id="dc474-152">Окно также должно создавать и отображать курсор при получении фокуса клавиатуры, а также скрывать и уничтожать курсор при потере фокуса.</span><span class="sxs-lookup"><span data-stu-id="dc474-152">The window should also create and display the caret when it receives the keyboard focus, and hide and destroy the caret when it loses the focus.</span></span> <span data-ttu-id="dc474-153">Окно может выполнять эти операции при обработке сообщений [**WM \_ SETFOCUS**](wm-setfocus.md) и [**WM \_ киллфокус**](wm-killfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="dc474-153">A window can perform these operations in the processing of the [**WM\_SETFOCUS**](wm-setfocus.md) and [**WM\_KILLFOCUS**](wm-killfocus.md) messages.</span></span> <span data-ttu-id="dc474-154">Дополнительные сведения о параметре крышки см. в разделе символы [крышки](/windows/desktop/menurc/carets).</span><span class="sxs-lookup"><span data-stu-id="dc474-154">For more information about carets, see [Carets](/windows/desktop/menurc/carets).</span></span>

## <a name="displaying-keyboard-input"></a><span data-ttu-id="dc474-155">Отображение ввода с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="dc474-155">Displaying Keyboard Input</span></span>

<span data-ttu-id="dc474-156">В примере в этом разделе показано, как приложение может принимать символы с клавиатуры, отображать их в клиентской области окна и обновлять позиции курсора с каждым введенным символом.</span><span class="sxs-lookup"><span data-stu-id="dc474-156">The example in this section shows how an application can receive characters from the keyboard, display them in the client area of a window, and update the position of the caret with each character typed.</span></span> <span data-ttu-id="dc474-157">Здесь также показано, как переместить курсор в ответ на стрелку влево, стрелку вправо, домой и завершить нажатия клавиш и показать, как выделить выделенный текст в ответ на сочетание клавиш SHIFT + стрелка вправо.</span><span class="sxs-lookup"><span data-stu-id="dc474-157">It also demonstrates how to move the caret in response to the LEFT ARROW, RIGHT ARROW, HOME, and END keystrokes, and shows how to highlight selected text in response to the SHIFT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="dc474-158">При обработке сообщения, [**\_ созданного**](/windows/desktop/winmsg/wm-create) с помощью WM, процедура Window, показанная в примере, выделяет буфер размером 64 КБ для хранения ввода с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="dc474-158">During processing of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure shown in the example allocates a 64K buffer for storing keyboard input.</span></span> <span data-ttu-id="dc474-159">Он также извлекает метрики текущего загруженного шрифта, сохраняя высоту и среднюю ширину символов в шрифте.</span><span class="sxs-lookup"><span data-stu-id="dc474-159">It also retrieves the metrics of the currently loaded font, saving the height and average width of characters in the font.</span></span> <span data-ttu-id="dc474-160">Высота и ширина используются при обработке сообщения [**\_ размера WM**](/windows/desktop/winmsg/wm-size) для вычисления длины строки и максимального количества строк в зависимости от размера клиентской области.</span><span class="sxs-lookup"><span data-stu-id="dc474-160">The height and width are used in processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to calculate the line length and maximum number of lines, based on the size of the client area.</span></span>

<span data-ttu-id="dc474-161">Процедура окна создает и отображает курсор при обработке сообщения [**WM \_ SETFOCUS**](wm-setfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="dc474-161">The window procedure creates and displays the caret when processing the [**WM\_SETFOCUS**](wm-setfocus.md) message.</span></span> <span data-ttu-id="dc474-162">Он скрывает и удаляет курсор при обработке сообщения [**WM \_ киллфокус**](wm-killfocus.md) .</span><span class="sxs-lookup"><span data-stu-id="dc474-162">It hides and deletes the caret when processing the [**WM\_KILLFOCUS**](wm-killfocus.md) message.</span></span>

<span data-ttu-id="dc474-163">При обработке сообщения [**WM \_ char**](wm-char.md) процедура Window отображает символы, сохраняет их во входном буфере и обновляет позиции курсора.</span><span class="sxs-lookup"><span data-stu-id="dc474-163">When processing the [**WM\_CHAR**](wm-char.md) message, the window procedure displays characters, stores them in the input buffer, and updates the caret position.</span></span> <span data-ttu-id="dc474-164">Процедура окна также преобразует символы табуляции в четыре последовательных символа пробела.</span><span class="sxs-lookup"><span data-stu-id="dc474-164">The window procedure also converts tab characters to four consecutive space characters.</span></span> <span data-ttu-id="dc474-165">Символы Backspace, перевода строки и экранирования создают звуковой сигнал, но не обрабатываются иным образом.</span><span class="sxs-lookup"><span data-stu-id="dc474-165">Backspace, linefeed, and escape characters generate a beep, but are not otherwise processed.</span></span>

<span data-ttu-id="dc474-166">При обработке сообщения [**WM \_ KeyDown**](wm-keydown.md) в процедуре Window выполняются перемещения влево, вправо, конечных и домашних курсоров.</span><span class="sxs-lookup"><span data-stu-id="dc474-166">The window procedure performs the left, right, end, and home caret movements when processing the [**WM\_KEYDOWN**](wm-keydown.md) message.</span></span> <span data-ttu-id="dc474-167">При обработке действия клавиши со стрелкой вправо процедура окна проверяет состояние клавиши SHIFT и, если она не работает, выбирает символ справа от курсора при перемещении курсора.</span><span class="sxs-lookup"><span data-stu-id="dc474-167">While processing the action of the RIGHT ARROW key, the window procedure checks the state of the SHIFT key and, if it is down, selects the character to the right of the caret as the caret is moved.</span></span>

<span data-ttu-id="dc474-168">Обратите внимание, что следующий код написан таким образом, чтобы его можно было скомпилировать как в Юникоде, так и в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="dc474-168">Note that the following code is written so that it can be compiled either as Unicode or as ANSI.</span></span> <span data-ttu-id="dc474-169">Если исходный код определяет Юникод, строки обрабатываются как символы Юникода. в противном случае они обрабатываются как символы ANSI.</span><span class="sxs-lookup"><span data-stu-id="dc474-169">If the source code defines UNICODE, strings are handled as Unicode characters; otherwise, they are handled as ANSI characters.</span></span>


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 