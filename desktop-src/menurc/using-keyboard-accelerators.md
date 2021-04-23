---
title: Использование сочетаний клавиш
description: В этом разделе рассматриваются задачи, связанные с сочетаниями клавиш.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- Ввод данных пользователем, сочетания клавиш
- захват вводимых пользователем данных, сочетания клавиш
- сочетания клавиш
- Accelerator
- таблицы сочетаний клавиш
- ресурсы таблицы ускорителя
- Функция сочетания клавиш для преобразования
- Сообщение WM_COMMAND
- Сообщение команды WM_SYS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069991"
---
# <a name="using-keyboard-accelerators"></a><span data-ttu-id="7bbbe-112">Использование сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="7bbbe-112">Using Keyboard Accelerators</span></span>

<span data-ttu-id="7bbbe-113">В этом разделе рассматриваются задачи, связанные с сочетаниями клавиш.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-113">This section covers tasks that are associated with keyboard accelerators.</span></span>

-   [<span data-ttu-id="7bbbe-114">Использование ресурса таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="7bbbe-114">Using an Accelerator Table Resource</span></span>](#using-an-accelerator-table-resource)
    -   [<span data-ttu-id="7bbbe-115">Создание ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-115">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
    -   [<span data-ttu-id="7bbbe-116">Загрузка ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-116">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
    -   [<span data-ttu-id="7bbbe-117">Вызов функции ускорителя преобразования</span><span class="sxs-lookup"><span data-stu-id="7bbbe-117">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
    -   [<span data-ttu-id="7bbbe-118">Обработка \_ командных сообщений WM</span><span class="sxs-lookup"><span data-stu-id="7bbbe-118">Processing WM\_COMMAND Messages</span></span>](/windows)
    -   [<span data-ttu-id="7bbbe-119">Уничтожение ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-119">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
    -   [<span data-ttu-id="7bbbe-120">Создание ускорителей для атрибутов шрифта</span><span class="sxs-lookup"><span data-stu-id="7bbbe-120">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)
-   [<span data-ttu-id="7bbbe-121">Использование таблицы сочетаний клавиш, созданной во время выполнения</span><span class="sxs-lookup"><span data-stu-id="7bbbe-121">Using an Accelerator Table Created at Run Time</span></span>](#using-an-accelerator-table-created-at-run-time)
    -   [<span data-ttu-id="7bbbe-122">Создание Run-Time таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="7bbbe-122">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
    -   [<span data-ttu-id="7bbbe-123">Ускорители обработки</span><span class="sxs-lookup"><span data-stu-id="7bbbe-123">Processing Accelerators</span></span>](#processing-accelerators)
    -   [<span data-ttu-id="7bbbe-124">Уничтожение таблицы Run-Time Accelerator</span><span class="sxs-lookup"><span data-stu-id="7bbbe-124">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
    -   [<span data-ttu-id="7bbbe-125">Создание пользовательских ускорителей редактирования</span><span class="sxs-lookup"><span data-stu-id="7bbbe-125">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a><span data-ttu-id="7bbbe-126">Использование ресурса таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="7bbbe-126">Using an Accelerator Table Resource</span></span>

<span data-ttu-id="7bbbe-127">Наиболее распространенным способом добавления поддержки ускорителя в приложение является включение ресурса таблицы ускорителя в исполняемый файл приложения, а затем Загрузка ресурса во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-127">The most common way to add accelerator support to an application is to include an accelerator-table resource with the application's executable file and then load the resource at run time.</span></span>

<span data-ttu-id="7bbbe-128">В этом разделе рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-128">This section covers the following topics.</span></span>

-   [<span data-ttu-id="7bbbe-129">Создание ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-129">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
-   [<span data-ttu-id="7bbbe-130">Загрузка ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-130">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
-   [<span data-ttu-id="7bbbe-131">Вызов функции ускорителя преобразования</span><span class="sxs-lookup"><span data-stu-id="7bbbe-131">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
-   [<span data-ttu-id="7bbbe-132">Обработка \_ командных сообщений WM</span><span class="sxs-lookup"><span data-stu-id="7bbbe-132">Processing WM\_COMMAND Messages</span></span>](/windows)
-   [<span data-ttu-id="7bbbe-133">Уничтожение ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-133">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
-   [<span data-ttu-id="7bbbe-134">Создание ускорителей для атрибутов шрифта</span><span class="sxs-lookup"><span data-stu-id="7bbbe-134">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a><span data-ttu-id="7bbbe-135">Создание ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-135">Creating the Accelerator Table Resource</span></span>

<span data-ttu-id="7bbbe-136">Ресурс-таблица ускорителя создается с помощью оператора [ускорителей](./accelerators-resource.md) в файле определения ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-136">You create an accelerator-table resource by using the [ACCELERATORS](./accelerators-resource.md) statement in your application's resource-definition file.</span></span> <span data-ttu-id="7bbbe-137">Необходимо назначить имя или идентификатор ресурса для таблицы сочетаний клавиш, желательно в отличие от других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-137">You must assign a name or resource identifier to the accelerator table, preferably unlike that of any other resource.</span></span> <span data-ttu-id="7bbbe-138">Система использует этот идентификатор для загрузки ресурса во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-138">The system uses this identifier to load the resource at run time.</span></span>

<span data-ttu-id="7bbbe-139">Для каждого определяемого сочетания клавиш требуется отдельная запись в таблице сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-139">Each accelerator you define requires a separate entry in the accelerator table.</span></span> <span data-ttu-id="7bbbe-140">В каждой записи определяется нажатие клавиши (либо код символа ASCII, либо код виртуального ключа), который создает ускоритель и идентификатор ускорителя.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-140">In each entry, you define the keystroke (either an ASCII character code or virtual-key code) that generates the accelerator and the accelerator's identifier.</span></span> <span data-ttu-id="7bbbe-141">Необходимо также указать, следует ли использовать нажатие клавиши в сочетании с клавишами ALT, SHIFT или CTRL.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-141">You must also specify whether the keystroke must be used in some combination with the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="7bbbe-142">Дополнительные сведения о виртуальных ключах см. в разделе [Ввод с клавиатуры](/windows/desktop/inputdev/keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="7bbbe-142">For more information about virtual keys, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="7bbbe-143">Клавиша ASCII указывается либо путем заключения символа ASCII в двойные кавычки, либо с помощью целочисленного значения символа в сочетании с флагом ASCII.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-143">An ASCII keystroke is specified either by enclosing the ASCII character in double quotation marks or by using the integer value of the character in combination with the ASCII flag.</span></span> <span data-ttu-id="7bbbe-144">В следующих примерах показано, как определить ускорители ASCII.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-144">The following examples show how to define ASCII accelerators.</span></span>

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

<span data-ttu-id="7bbbe-145">Нажатие клавиши с помощью виртуального ключа определяется по-разному в зависимости от того, является ли клавиша буквенно-цифровым или ключом, отличным от букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-145">A virtual-key code keystroke is specified differently depending on whether the keystroke is an alphanumeric key or a non-alphanumeric key.</span></span> <span data-ttu-id="7bbbe-146">Для буквенно-цифрового ключа буква или номер ключа, заключенные в двойные кавычки, комбинируется с флагом **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-146">For an alphanumeric key, the key's letter or number, enclosed in double quotation marks, is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="7bbbe-147">Для ключа, не являющегося буквенно-цифровым, код виртуального ключа для конкретного ключа объединяется с флагом **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-147">For a non-alphanumeric key, the virtual-key code for the specific key is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="7bbbe-148">В следующих примерах показано, как определить сочетания клавиш для работы с виртуальными ключами.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-148">The following examples show how to define virtual-key code accelerators.</span></span>

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

<span data-ttu-id="7bbbe-149">В следующем примере показан ресурс таблицы ускорителя, определяющий ускорители для файловых операций.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-149">The following example shows an accelerator-table resource that defines accelerators for file operations.</span></span> <span data-ttu-id="7bbbe-150">Имя ресурса — *филеакцел*.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-150">The name of the resource is *FileAccel*.</span></span>

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

<span data-ttu-id="7bbbe-151">Если вы хотите, чтобы пользователь нажмет клавиши ALT, SHIFT или CTRL в некоторой комбинации с нажатием клавиши быстрого вызова, укажите ALT, SHIFT и УПРАВЛЯЮЩие флаги в определении ускорителя.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-151">If you want the user to press the ALT, SHIFT, or CTRL keys in some combination with the accelerator keystroke, specify the ALT, SHIFT, and CONTROL flags in the accelerator's definition.</span></span> <span data-ttu-id="7bbbe-152">Ниже приводятся некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-152">Following are some examples.</span></span>

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

<span data-ttu-id="7bbbe-153">По умолчанию, когда сочетание клавиш соответствует пункту меню, система выделяет элемент меню.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-153">By default, when an accelerator key corresponds to a menu item, the system highlights the menu item.</span></span> <span data-ttu-id="7bbbe-154">Для предотвращения выделения отдельных сочетаний клавиш можно использовать флаг **инверсии** .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-154">You can use the **NOINVERT** flag to prevent highlighting for an individual accelerator.</span></span> <span data-ttu-id="7bbbe-155">В следующем примере показано, как использовать флаг **инверсии** :</span><span class="sxs-lookup"><span data-stu-id="7bbbe-155">The following example shows how to use the **NOINVERT** flag:</span></span>

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

<span data-ttu-id="7bbbe-156">Чтобы определить ускорители, соответствующие элементам меню в приложении, включите ускорители в текст пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-156">To define accelerators that correspond to menu items in your application, include the accelerators in the text of the menu items.</span></span> <span data-ttu-id="7bbbe-157">В следующем примере показано, как включить ускорители в текст элемента меню в файле определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-157">The following example shows how to include accelerators in menu-item text in a resource-definition file.</span></span>

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a><span data-ttu-id="7bbbe-158">Загрузка ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-158">Loading the Accelerator Table Resource</span></span>

<span data-ttu-id="7bbbe-159">Приложение загружает ресурс-таблицу ускорителя, вызывая функцию [**лоадакцелераторс**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) и указывая для приложения обработчик экземпляра, исполняемый файл которого содержит ресурс, а также имя или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-159">An application loads an accelerator-table resource by calling the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function and specifying the instance handle to the application whose executable file contains the resource and the name or identifier of the resource.</span></span> <span data-ttu-id="7bbbe-160">**Лоадакцелераторс** загружает указанную таблицу сочетаний клавиш в память и возвращает маркер в таблицу сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-160">**LoadAccelerators** loads the specified accelerator table into memory and returns the handle to the accelerator table.</span></span>

<span data-ttu-id="7bbbe-161">Приложение может загрузить ресурс таблицы ускорителя в любое время.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-161">An application can load an accelerator-table resource at any time.</span></span> <span data-ttu-id="7bbbe-162">Как правило, приложение с одним потоком загружает свою таблицу сочетаний клавиш перед входом в основной цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-162">Usually, a single-threaded application loads its accelerator table before entering its main message loop.</span></span> <span data-ttu-id="7bbbe-163">Приложение, использующее несколько потоков, обычно загружает ресурс-таблицу ускорителя для потока перед входом в цикл обработки сообщений для потока.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-163">An application that uses multiple threads typically loads the accelerator-table resource for a thread before entering the message loop for the thread.</span></span> <span data-ttu-id="7bbbe-164">Приложение или поток может также использовать несколько таблиц сочетаний клавиш, каждый из которых связан с определенным окном в приложении.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-164">An application or thread might also use multiple accelerator tables, each associated with a particular window in the application.</span></span> <span data-ttu-id="7bbbe-165">Такое приложение загрузит таблицу сочетаний клавиш для окна каждый раз, когда пользователь активировал окно.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-165">Such an application would load the accelerator table for the window each time the user activated the window.</span></span> <span data-ttu-id="7bbbe-166">Дополнительные сведения о потоках см. в разделе [процессы и потоки](/windows/desktop/ProcThread/processes-and-threads).</span><span class="sxs-lookup"><span data-stu-id="7bbbe-166">For more information about threads, see [Processes and Threads](/windows/desktop/ProcThread/processes-and-threads).</span></span>

### <a name="calling-the-translate-accelerator-function"></a><span data-ttu-id="7bbbe-167">Вызов функции ускорителя преобразования</span><span class="sxs-lookup"><span data-stu-id="7bbbe-167">Calling the Translate Accelerator Function</span></span>

<span data-ttu-id="7bbbe-168">Чтобы обработать ускорители, цикл обработки сообщений приложения (или потока) должен содержать вызов функции [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-168">To process accelerators, an application's (or thread's) message loop must contain a call to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function.</span></span> <span data-ttu-id="7bbbe-169">**TranslateAccelerator** сравнивает нажатия клавиш с таблицей сочетаний клавиш и, если находит совпадение, преобразует нажатия клавиш в сообщение [**\_ Command WM**](wm-command.md) (или [**WM \_ сискомманд**](wm-syscommand.md)).</span><span class="sxs-lookup"><span data-stu-id="7bbbe-169">**TranslateAccelerator** compares keystrokes to an accelerator table and, if it finds a match, translates the keystrokes into a [**WM\_COMMAND**](wm-command.md) (or [**WM\_SYSCOMMAND**](wm-syscommand.md)) message.</span></span> <span data-ttu-id="7bbbe-170">Затем функция отправляет сообщение в процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-170">The function then sends the message to a window procedure.</span></span> <span data-ttu-id="7bbbe-171">Параметры функции **TranslateAccelerator** включают в себя маркер окна, который получает сообщения **\_ команды WM** , обработчик для таблицы сочетаний клавиш, используемый для преобразования ускорителей, и указатель на структуру [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) , содержащую сообщение из очереди.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-171">The parameters of the **TranslateAccelerator** function include the handle to the window that is to receive the **WM\_COMMAND** messages, the handle to the accelerator table used to translate accelerators, and a pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure containing a message from the queue.</span></span> <span data-ttu-id="7bbbe-172">В следующем примере показано, как вызвать **TranslateAccelerator** из цикла обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-172">The following example shows how to call **TranslateAccelerator** from within a message loop.</span></span>


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a><span data-ttu-id="7bbbe-173">Обработка \_ командных сообщений WM</span><span class="sxs-lookup"><span data-stu-id="7bbbe-173">Processing WM\_COMMAND Messages</span></span>

<span data-ttu-id="7bbbe-174">При использовании сочетания клавиш окно, указанное в функции [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , получает [**\_ команду WM**](wm-command.md) или сообщение [**\_ сискомманд WM**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-174">When an accelerator is used, the window specified in the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function receives a [**WM\_COMMAND**](wm-command.md) or [**WM\_SYSCOMMAND**](wm-syscommand.md) message.</span></span> <span data-ttu-id="7bbbe-175">Слово низкого порядка параметра *wParam* содержит идентификатор ускорителя.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-175">The low-order word of the *wParam* parameter contains the identifier of the accelerator.</span></span> <span data-ttu-id="7bbbe-176">Процедура окна проверяет идентификатор, чтобы определить источник сообщения **\_ команды WM** и обработать сообщение соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-176">The window procedure examines the identifier to determine the source of the **WM\_COMMAND** message and process the message accordingly.</span></span>

<span data-ttu-id="7bbbe-177">Как правило, если ускоритель соответствует пункту меню в приложении, элементу сочетания клавиш и пункта меню назначается один и тот же идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-177">Typically, if an accelerator corresponds to a menu item in the application, the accelerator and menu item are assigned the same identifier.</span></span> <span data-ttu-id="7bbbe-178">Если необходимо узнать, было ли [**\_ командное сообщение WM**](wm-command.md) создано ускорителем или пунктом меню, можно проверить слово в высоком порядке в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-178">If you need to know whether a [**WM\_COMMAND**](wm-command.md) message was generated by an accelerator or by a menu item, you can examine the high-order word of the *wParam* parameter.</span></span> <span data-ttu-id="7bbbe-179">Если сообщение создано ускорителем, то его значение в высоком порядке равно 1. Если сообщение создано элементом меню, то его значение в верхнем порядке равно 0.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-179">If an accelerator generated the message, the high-order word is 1; if a menu item generated the message, the high-order word is 0.</span></span>

### <a name="destroying-the-accelerator-table-resource"></a><span data-ttu-id="7bbbe-180">Уничтожение ресурса таблицы ускорителя</span><span class="sxs-lookup"><span data-stu-id="7bbbe-180">Destroying the Accelerator Table Resource</span></span>

<span data-ttu-id="7bbbe-181">Система автоматически уничтожает ресурсы таблицы ускорителя, загруженные функцией [**лоадакцелераторс**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , удаляя ресурс из памяти после закрытия приложения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-181">The system automatically destroys accelerator-table resources loaded by the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function, removing the resource from memory after the application closes.</span></span>

### <a name="creating-accelerators-for-font-attributes"></a><span data-ttu-id="7bbbe-182">Создание ускорителей для атрибутов шрифта</span><span class="sxs-lookup"><span data-stu-id="7bbbe-182">Creating Accelerators for Font Attributes</span></span>

<span data-ttu-id="7bbbe-183">В примере в этом разделе показано, как выполнять следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="7bbbe-183">The example in this section shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="7bbbe-184">Создайте ресурс-таблицу ускорителя.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-184">Create an accelerator-table resource.</span></span>
-   <span data-ttu-id="7bbbe-185">Загрузка таблицы сочетаний клавиш во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-185">Load the accelerator table at run time.</span></span>
-   <span data-ttu-id="7bbbe-186">Преобразование ускорителей в цикле обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-186">Translate accelerators in a message loop.</span></span>
-   <span data-ttu-id="7bbbe-187">Обработка [**\_ командных сообщений WM**](wm-command.md) , созданных ускорителями.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-187">Process [**WM\_COMMAND**](wm-command.md) messages generated by the accelerators.</span></span>

<span data-ttu-id="7bbbe-188">Эти задачи демонстрируются в контексте приложения, которое содержит меню **символов** и соответствующие ускорители, позволяющие пользователю выбирать атрибуты текущего шрифта.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-188">These tasks are demonstrated in the context of an application that includes a **Character** menu and corresponding accelerators that allow the user to select attributes of the current font.</span></span>

<span data-ttu-id="7bbbe-189">В следующей части файла определения ресурсов определяется меню « **символ** » и связанная таблица сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-189">The following portion of a resource-definition file defines the **Character** menu and the associated accelerator table.</span></span> <span data-ttu-id="7bbbe-190">Обратите внимание, что пункты меню показывают клавиши быстрого вызова и что каждый ускоритель имеет тот же идентификатор, что и соответствующий пункт меню.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-190">Note that the menu items show the accelerator keystrokes and that each accelerator has the same identifier as its associated menu item.</span></span>


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



<span data-ttu-id="7bbbe-191">В следующих разделах из исходного файла приложения показано, как реализовать ускорители.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-191">The following sections from the application's source file show how to implement the accelerators.</span></span>


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a><span data-ttu-id="7bbbe-192">Использование таблицы сочетаний клавиш, созданной во время выполнения</span><span class="sxs-lookup"><span data-stu-id="7bbbe-192">Using an Accelerator Table Created at Run Time</span></span>

<span data-ttu-id="7bbbe-193">В этом разделе описывается использование таблиц сочетаний клавиш, созданных во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-193">This topic discusses how to use accelerator tables created at run time.</span></span>

-   [<span data-ttu-id="7bbbe-194">Создание Run-Time таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="7bbbe-194">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
-   [<span data-ttu-id="7bbbe-195">Ускорители обработки</span><span class="sxs-lookup"><span data-stu-id="7bbbe-195">Processing Accelerators</span></span>](#processing-accelerators)
-   [<span data-ttu-id="7bbbe-196">Уничтожение таблицы Run-Time Accelerator</span><span class="sxs-lookup"><span data-stu-id="7bbbe-196">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
-   [<span data-ttu-id="7bbbe-197">Создание пользовательских ускорителей редактирования</span><span class="sxs-lookup"><span data-stu-id="7bbbe-197">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a><span data-ttu-id="7bbbe-198">Создание Run-Time таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="7bbbe-198">Creating a Run-Time Accelerator Table</span></span>

<span data-ttu-id="7bbbe-199">Первым шагом при создании таблицы сочетаний клавиш во время выполнения является заполнение массива несамостоятельных [**структур.**](/windows/win32/api/winuser/ns-winuser-accel)</span><span class="sxs-lookup"><span data-stu-id="7bbbe-199">The first step in creating an accelerator table at run time is filling an array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures.</span></span> <span data-ttu-id="7bbbe-200">Каждая структура в массиве определяет ускоритель в таблице.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-200">Each structure in the array defines an accelerator in the table.</span></span> <span data-ttu-id="7bbbe-201">Определение ускорителя включает его флаги, ключ и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-201">An accelerator's definition includes its flags, its key, and its identifier.</span></span> <span data-ttu-id="7bbbe-202">Структура **для** рассогласования имеет следующий вид.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-202">The **ACCEL** structure has the following form.</span></span>

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

<span data-ttu-id="7bbbe-203">Вы определяете нажатие клавиши быстрого вызова, указывая код символа ASCII или код виртуальной клавиши в **ключевом** [**элементе структуры доступа**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-203">You define an accelerator's keystroke by specifying an ASCII character code or a virtual-key code in the **key** member of the [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structure.</span></span> <span data-ttu-id="7bbbe-204">Если указан код виртуального ключа, необходимо сначала включить флаг **фвирткэй** в член **фвирт** . в противном случае система интерпретирует код как код символа ASCII.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-204">If you specify a virtual-key code, you must first include the **FVIRTKEY** flag in the **fVirt** member; otherwise, the system interprets the code as an ASCII character code.</span></span> <span data-ttu-id="7bbbe-205">Можно включить флаг **фконтрол**, **ФАЛТ** или **фшифт** или все три, чтобы объединить клавиши CTRL, Alt или SHIFT с нажатием клавиши.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-205">You can include the **FCONTROL**, **FALT**, or **FSHIFT** flag, or all three, to combine the CTRL, ALT, or SHIFT key with the keystroke.</span></span>

<span data-ttu-id="7bbbe-206">Чтобы создать таблицу сочетаний клавиш, передайте указатель на массив несамостоятельных [**структур в**](/windows/win32/api/winuser/ns-winuser-accel) функцию [**креатеакцелератортабле**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-206">To create the accelerator table, pass a pointer to the array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures to the [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) function.</span></span> <span data-ttu-id="7bbbe-207">**Креатеакцелератортабле** создает таблицу сочетаний клавиш и возвращает маркер в таблицу.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-207">**CreateAcceleratorTable** creates the accelerator table and returns the handle to the table.</span></span>

### <a name="processing-accelerators"></a><span data-ttu-id="7bbbe-208">Ускорители обработки</span><span class="sxs-lookup"><span data-stu-id="7bbbe-208">Processing Accelerators</span></span>

<span data-ttu-id="7bbbe-209">Процесс загрузки и вызова ускорителей, предоставляемых таблицей ускорителя, созданной во время выполнения, аналогичен процессу обработки, предоставляемой ресурсом таблицы ускорителя.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-209">The process of loading and calling accelerators provided by an accelerator table created at run time is the same as processing those provided by an accelerator-table resource.</span></span> <span data-ttu-id="7bbbe-210">Дополнительные сведения см. [в разделе Загрузка ресурса таблицы ускорителя](#loading-the-accelerator-table-resource) с помощью [обработки \_ командных сообщений WM](/windows).</span><span class="sxs-lookup"><span data-stu-id="7bbbe-210">For more information, see [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through [Processing WM\_COMMAND Messages](/windows).</span></span>

### <a name="destroying-a-run-time-accelerator-table"></a><span data-ttu-id="7bbbe-211">Уничтожение таблицы Run-Time Accelerator</span><span class="sxs-lookup"><span data-stu-id="7bbbe-211">Destroying a Run-Time Accelerator Table</span></span>

<span data-ttu-id="7bbbe-212">Система автоматически уничтожает таблицы ускорителя, созданные во время выполнения, удаляя ресурсы из памяти после закрытия приложения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-212">The system automatically destroys accelerator tables created at run time, removing the resources from memory after the application closes.</span></span> <span data-ttu-id="7bbbe-213">Можно уничтожить таблицу сочетаний клавиш и удалить ее из памяти раньше, передав маркер таблицы в функцию [**дестройакцелератортабле**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-213">You can destroy an accelerator table and remove it from memory earlier by passing the table's handle to the [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) function.</span></span>

### <a name="creating-user-editable-accelerators"></a><span data-ttu-id="7bbbe-214">Создание пользовательских ускорителей редактирования</span><span class="sxs-lookup"><span data-stu-id="7bbbe-214">Creating User Editable Accelerators</span></span>

<span data-ttu-id="7bbbe-215">В этом примере показано, как создать диалоговое окно, позволяющее пользователю изменить сочетание клавиш, связанное с пунктом меню.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-215">This example shows how to construct a dialog box that allows the user to change the accelerator associated with a menu item.</span></span> <span data-ttu-id="7bbbe-216">Диалоговое окно состоит из поля со списком, содержащего пункты меню, поле со списком, содержащее имена ключей, и флажки для выбора клавиш CTRL, ALT и SHIFT.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-216">The dialog box consists of a combo box containing menu items, a combo box containing the names of keys, and check boxes for selecting the CTRL, ALT, and SHIFT keys.</span></span> <span data-ttu-id="7bbbe-217">На следующем рисунке показано диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-217">The following illustration shows the dialog box.</span></span>

![диалоговое окно с полями со списком и флажками](images/useredit.gif)

<span data-ttu-id="7bbbe-219">В следующем примере показано, как диалоговое окно определено в файле определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-219">The following example shows how the dialog box is defined in the resource-definition file.</span></span>

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

<span data-ttu-id="7bbbe-220">Строка меню приложения содержит подменю **символов** с элементами, с которыми связаны сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-220">The application's menu bar contains a **Character** submenu whose items have accelerators associated with them.</span></span>

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

<span data-ttu-id="7bbbe-221">Значения пунктов меню для шаблона меню являются константами, определенными в файле заголовка приложения.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-221">The menu item values for the menu template are constants defined as follows in the application's header file.</span></span>

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

<span data-ttu-id="7bbbe-222">В диалоговом окне используется массив определяемых приложением структур ключ, каждый из которых содержит текстовую строку с клавиатуры и текстовую строку сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-222">The dialog box uses an array of application-defined VKEY structures, each containing a keystroke-text string and an accelerator-text string.</span></span> <span data-ttu-id="7bbbe-223">При создании диалогового окна он анализирует массив и добавляет каждую строку текста нажатия клавиши в поле со списком **Выбор нажатия клавиши** .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-223">When the dialog box is created, it parses the array and adds each keystroke-text string to the **Select Keystroke** combo box.</span></span> <span data-ttu-id="7bbbe-224">Когда пользователь нажимает кнопку **ОК** , диалоговое окно ищет выбранную текстовую строку нажатия клавиши и получает соответствующую текстовую строку ускорителя.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-224">When the user clicks the **OK** button, the dialog box looks up the selected keystroke-text string and retrieves the corresponding accelerator-text string.</span></span> <span data-ttu-id="7bbbe-225">В диалоговом окне добавляется текстовая строка ускорителя к тексту выбранного пользователем пункта меню.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-225">The dialog box appends the accelerator-text string to the text of the menu item that the user selected.</span></span> <span data-ttu-id="7bbbe-226">В следующем примере показан массив структурных ключ:</span><span class="sxs-lookup"><span data-stu-id="7bbbe-226">The following example shows the array of VKEY structures:</span></span>


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



<span data-ttu-id="7bbbe-227">Процедура инициализации диалогового окна заполняет **элемент Выбор** и выбирает поля со списком **нажатия клавиш** .</span><span class="sxs-lookup"><span data-stu-id="7bbbe-227">The dialog box's initialization procedure fills the **Select Item** and **Select Keystroke** combo boxes.</span></span> <span data-ttu-id="7bbbe-228">После того как пользователь выберет пункт меню и связанный ускоритель, диалоговое окно проверит элементы управления в диалоговом окне, чтобы получить выбор пользователя, обновляет текст пункта меню, а затем создает новую таблицу сочетаний клавиш, содержащую определяемый пользователем новый ускоритель.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-228">After the user selects a menu item and associated accelerator, the dialog box examines the controls in the dialog box to get the user's selection, updates the text of the menu item, and then creates a new accelerator table that contains the user-defined new accelerator.</span></span> <span data-ttu-id="7bbbe-229">В следующем примере показана процедура диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-229">The following example shows the dialog-box procedure.</span></span> <span data-ttu-id="7bbbe-230">Обратите внимание, что в процедуре окна необходимо инициализировать.</span><span class="sxs-lookup"><span data-stu-id="7bbbe-230">Note that you must initialize in your window procedure.</span></span>


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 