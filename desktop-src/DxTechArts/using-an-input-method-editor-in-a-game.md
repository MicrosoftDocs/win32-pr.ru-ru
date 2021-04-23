---
title: Использование редактора метода ввода в игре
description: В этой статье объясняется, как можно реализовать базовый элемент управления редактора IME в полноэкранном приложении Microsoft DirectX.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104000290"
---
# <a name="using-an-input-method-editor-in-a-game"></a><span data-ttu-id="3fcee-103">Использование редактора метода ввода в игре</span><span class="sxs-lookup"><span data-stu-id="3fcee-103">Using an Input Method Editor in a Game</span></span>

> [!Note]  
> <span data-ttu-id="3fcee-104">В этой статье подробно описывается работа с редактором методов ввода Windows XP (IME).</span><span class="sxs-lookup"><span data-stu-id="3fcee-104">This article details working with the Windows XP Input Method Editor (IME).</span></span> <span data-ttu-id="3fcee-105">В IME для Windows Vista были внесены изменения, которые не полностью описаны в этой статье.</span><span class="sxs-lookup"><span data-stu-id="3fcee-105">Changes were made to the IME for Windows Vista that are not fully detailed in this article.</span></span> <span data-ttu-id="3fcee-106">Дополнительные сведения об изменениях IME для Windows Vista см. в разделе [редакторы методов ввода (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) в [windows Vista — Ever-Expanding представление интернационализации](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) на портале Microsoft Global Development and Computing.</span><span class="sxs-lookup"><span data-stu-id="3fcee-106">For more info about changes to the IME for Windows Vista, see [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal.</span></span>

 

<span data-ttu-id="3fcee-107">Редактор методов ввода (IME) — это программа, которая позволяет легко вводить текст с помощью стандартной клавиатуры для восточно-азиатских языков, таких как китайский, японский, корейский и другие языки со сложными символами.</span><span class="sxs-lookup"><span data-stu-id="3fcee-107">An input method editor (IME) is a program that allows easy text entry using a standard keyboard for East Asian languages such as Chinese, Japanese, Korean, and other languages with complex characters.</span></span> <span data-ttu-id="3fcee-108">Например, с помощью редакторов IME пользователь может вводить сложные символы в текстовом процессоре, или проигрыватель многомногопользовательской Интернет-игры может общаться с друзьями в сложных символах.</span><span class="sxs-lookup"><span data-stu-id="3fcee-108">For example, with IMEs a user can type complex characters in a word processor, or a player of a massive multiplayer online game can chat with friends in complex characters.</span></span>

<span data-ttu-id="3fcee-109">В этой статье объясняется, как можно реализовать базовый элемент управления редактора IME в полноэкранном приложении Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="3fcee-109">This article explains how you can implement a basic IME edit control in a full-screen Microsoft DirectX application.</span></span> <span data-ttu-id="3fcee-110">Приложения, использующие преимущества ДКСУТ, автоматически получают функции IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-110">Applications that take advantage of DXUT automatically get IME functionality.</span></span> <span data-ttu-id="3fcee-111">Для приложений, которые не используют платформу, в этой статье описывается добавление поддержки IME в элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="3fcee-111">For applications that do not make use of the framework, this article describes how to add IME support to an edit control.</span></span>

<span data-ttu-id="3fcee-112">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="3fcee-112">Contents:</span></span>

-   [<span data-ttu-id="3fcee-113">Поведение IME по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3fcee-113">Default IME Behavior</span></span>](#default-ime-behavior)
-   [<span data-ttu-id="3fcee-114">Использование IME с ДКСУТ</span><span class="sxs-lookup"><span data-stu-id="3fcee-114">Using IMEs with DXUT</span></span>](#using-imes-with-dxut)
-   [<span data-ttu-id="3fcee-115">Переопределение поведения IME по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3fcee-115">Overriding the Default IME Behavior</span></span>](#overriding-the-default-ime-behavior)
-   [<span data-ttu-id="3fcee-116">Функции</span><span class="sxs-lookup"><span data-stu-id="3fcee-116">Functions</span></span>](#functions)
-   [<span data-ttu-id="3fcee-117">Сообщения</span><span class="sxs-lookup"><span data-stu-id="3fcee-117">Messages</span></span>](#ime-messages)
-   [<span data-ttu-id="3fcee-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="3fcee-118">Examples</span></span>](#examples)
    -   [<span data-ttu-id="3fcee-119">Редактор метода CHT версии 4,2, 4,3 и 4,4</span><span class="sxs-lookup"><span data-stu-id="3fcee-119">CHT IME version 4.2, 4.3 and 4.4</span></span>](#cht-ime-version-42-43-and-44)
    -   [<span data-ttu-id="3fcee-120">Метод IME для CHT версии 5,0</span><span class="sxs-lookup"><span data-stu-id="3fcee-120">CHT IME version 5.0</span></span>](#cht-ime-version-50)
    -   [<span data-ttu-id="3fcee-121">Метод IME версии 5,1, 5,2 и CHS IME версии 5,3</span><span class="sxs-lookup"><span data-stu-id="3fcee-121">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [<span data-ttu-id="3fcee-122">CHS IME версии 4,1</span><span class="sxs-lookup"><span data-stu-id="3fcee-122">CHS IME version 4.1</span></span>](#chs-ime-version-41)
    -   [<span data-ttu-id="3fcee-123">CHS IME версии 4,2</span><span class="sxs-lookup"><span data-stu-id="3fcee-123">CHS IME version 4.2</span></span>](#chs-ime-version-42)
-   [<span data-ttu-id="3fcee-124">Сообщения IME</span><span class="sxs-lookup"><span data-stu-id="3fcee-124">IME Messages</span></span>](#ime-messages)
    -   [<span data-ttu-id="3fcee-125">WM \_ инпутлангчанже</span><span class="sxs-lookup"><span data-stu-id="3fcee-125">WM\_INPUTLANGCHANGE</span></span>](#wm_inputlangchange)
    -   [<span data-ttu-id="3fcee-126">\_старткомпоситион IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="3fcee-126">WM\_IME\_STARTCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="3fcee-127">\_композиция IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="3fcee-127">WM\_IME\_COMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="3fcee-128">\_ендкомпоситион IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="3fcee-128">WM\_IME\_ENDCOMPOSITION</span></span>](/windows)
    -   [<span data-ttu-id="3fcee-129">\_уведомление редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="3fcee-129">WM\_IME\_NOTIFY</span></span>](/windows)
-   [<span data-ttu-id="3fcee-130">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="3fcee-130">Rendering</span></span>](#rendering)
    -   [<span data-ttu-id="3fcee-131">Индикатор локали ввода</span><span class="sxs-lookup"><span data-stu-id="3fcee-131">Input Locale Indicator</span></span>](#input-locale-indicator)
    -   [<span data-ttu-id="3fcee-132">Окно композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-132">Composition Window</span></span>](#composition-window)
    -   [<span data-ttu-id="3fcee-133">Чтение и потенциальные окна</span><span class="sxs-lookup"><span data-stu-id="3fcee-133">Reading and Candidate Windows</span></span>](#reading-and-candidate-windows)
-   [<span data-ttu-id="3fcee-134">Ограничения</span><span class="sxs-lookup"><span data-stu-id="3fcee-134">Limitations</span></span>](#limitations)
-   [<span data-ttu-id="3fcee-135">Сведения о реестре</span><span class="sxs-lookup"><span data-stu-id="3fcee-135">Registry Information</span></span>](#registry-information)
-   [<span data-ttu-id="3fcee-136">Приложение а. версии CHT для каждой операционной системы</span><span class="sxs-lookup"><span data-stu-id="3fcee-136">Appendix A: CHT Versions per Operating System</span></span>](#appendix-a-cht-versions-per-operating-system)
-   [<span data-ttu-id="3fcee-137">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3fcee-137">Further Information</span></span>](#further-information)
-   [<span data-ttu-id="3fcee-138">жетреадингстринг</span><span class="sxs-lookup"><span data-stu-id="3fcee-138">GetReadingString</span></span>](#getreadingstring)
-   [<span data-ttu-id="3fcee-139">шовреадингвиндов</span><span class="sxs-lookup"><span data-stu-id="3fcee-139">ShowReadingWindow</span></span>](#showreadingwindow)

## <a name="default-ime-behavior"></a><span data-ttu-id="3fcee-140">Поведение IME по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3fcee-140">Default IME Behavior</span></span>

<span data-ttu-id="3fcee-141">Редакторы IME сопоставляют ввод с клавиатуры с фонетическими компонентами или другими элементами языка, характерными для выбранного языка.</span><span class="sxs-lookup"><span data-stu-id="3fcee-141">IMEs map keyboard input to phonetic components or other language elements specific to a selected language.</span></span> <span data-ttu-id="3fcee-142">В типичном сценарии пользователь вводит ключи, представляющие произношение сложного символа.</span><span class="sxs-lookup"><span data-stu-id="3fcee-142">In a typical scenario, the user types keys that represent pronunciation of a complex character.</span></span> <span data-ttu-id="3fcee-143">Если редактор IME распознает произношение как допустимый, он предоставляет пользователю список кандидатов слов или фраз, из которых пользователь может выбрать последний вариант.</span><span class="sxs-lookup"><span data-stu-id="3fcee-143">If the IME recognizes the pronunciation as valid, it presents the user with a list of word or phrase candidates from which the user can select a final choice.</span></span> <span data-ttu-id="3fcee-144">Затем выбранное слово отправляется в приложение через ряд сообщений Microsoft Windows [**WM \_ char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="3fcee-144">The chosen word is then sent to the application through a series of Microsoft Windows [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages.</span></span> <span data-ttu-id="3fcee-145">Поскольку редактор IME работает на уровне ниже приложения путем перехвата ввода с клавиатуры, наличие редактора IME прозрачно для приложения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-145">Because the IME works at a level below the application by intercepting keyboard input, the presence of an IME is transparent to the application.</span></span> <span data-ttu-id="3fcee-146">Почти все приложения Windows могут воспользоваться преимуществами IME, не обращаясь к их существованию и не требуя специального программирования.</span><span class="sxs-lookup"><span data-stu-id="3fcee-146">Almost all Windows applications can readily take advantage of IMEs without being aware of their existence and without requiring special coding.</span></span>

<span data-ttu-id="3fcee-147">Типичный редактор IME отображает несколько окон для указания пользователя в символьной записи, как показано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="3fcee-147">A typical IME displays several windows to guide the user through character entry, as shown in the following examples.</span></span>

![в IME отображается несколько окон](images/ime-elements.png)

| <span data-ttu-id="3fcee-149">Тип окна</span><span class="sxs-lookup"><span data-stu-id="3fcee-149">Window Type</span></span>                                       | <span data-ttu-id="3fcee-150">Описание</span><span class="sxs-lookup"><span data-stu-id="3fcee-150">Description</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="3fcee-151">Выходные данные IME</span><span class="sxs-lookup"><span data-stu-id="3fcee-151">IME Output</span></span>                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="3fcee-152">A.</span><span class="sxs-lookup"><span data-stu-id="3fcee-152">A.</span></span> <span data-ttu-id="3fcee-153">Окно чтения</span><span class="sxs-lookup"><span data-stu-id="3fcee-153">Reading Window</span></span>                                 | <span data-ttu-id="3fcee-154">Содержит нажатия клавиш с клавиатуры; как правило, изменения после каждого нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="3fcee-154">Contains keystrokes from the keyboard; typically changes after each keystroke.</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="3fcee-155">считывание строки</span><span class="sxs-lookup"><span data-stu-id="3fcee-155">reading string</span></span>                               |
| <span data-ttu-id="3fcee-156">Б.</span><span class="sxs-lookup"><span data-stu-id="3fcee-156">B.</span></span> <span data-ttu-id="3fcee-157">Окно композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-157">Composition Window</span></span>                             | <span data-ttu-id="3fcee-158">Содержит коллекцию символов, которые пользователь состоял с редактором IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-158">Contains the collection of characters that the user has composed with the IME.</span></span> <span data-ttu-id="3fcee-159">Эти символы рисуются редактором IME поверх приложения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-159">These characters are drawn by the IME on top of the application.</span></span> <span data-ttu-id="3fcee-160">Когда пользователь уведомляет IME о приемлемой строке композиции, редактор IME отправляет строку композиции приложению через ряд \_ сообщений WM char.</span><span class="sxs-lookup"><span data-stu-id="3fcee-160">When the user notifies the IME that the composition string is satisfactory, the IME then sends the composition string to the application via a series of WM\_CHAR messages.</span></span> | <span data-ttu-id="3fcee-161">Строка композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-161">composition string</span></span>                           |
| <span data-ttu-id="3fcee-162">В.</span><span class="sxs-lookup"><span data-stu-id="3fcee-162">C.</span></span> <span data-ttu-id="3fcee-163">Окно кандидатов</span><span class="sxs-lookup"><span data-stu-id="3fcee-163">Candidate Window</span></span>                               | <span data-ttu-id="3fcee-164">Когда пользователь вводит допустимое произношение, редактор IME отображает список символов-кандидатов, которые соответствуют заданному произношению.</span><span class="sxs-lookup"><span data-stu-id="3fcee-164">When the user has entered a valid pronunciation, the IME displays a list of candidate characters that all match the given pronunciation.</span></span> <span data-ttu-id="3fcee-165">Затем пользователь выбирает из этого списка предполагаемый символ, а редактор IME добавляет этот символ в окно композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-165">The user then selects the intended character from this list, and the IME adds this character to the Composition Window display.</span></span>                                                    | <span data-ttu-id="3fcee-166">Следующий символ в строке композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-166">the next character in the composition string</span></span> |
| <span data-ttu-id="3fcee-167">Г.</span><span class="sxs-lookup"><span data-stu-id="3fcee-167">D.</span></span> <span data-ttu-id="3fcee-168">Индикатор [локали ввода](/windows/desktop/Intl/nls-terminology)</span><span class="sxs-lookup"><span data-stu-id="3fcee-168">[Input Locale](/windows/desktop/Intl/nls-terminology) indicator</span></span> | <span data-ttu-id="3fcee-169">Показывает язык, выбранный пользователем для ввода с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="3fcee-169">Shows the language the user has selected for keyboard input.</span></span> <span data-ttu-id="3fcee-170">Этот индикатор внедрен на панель задач Windows.</span><span class="sxs-lookup"><span data-stu-id="3fcee-170">This indicator is embedded in the Windows taskbar.</span></span> <span data-ttu-id="3fcee-171">Чтобы выбрать язык ввода, откройте панель управления язык и региональные стандарты, а затем щелкните сведения на вкладке языки.</span><span class="sxs-lookup"><span data-stu-id="3fcee-171">The input language can be selected by opening the Regional and Language Options Control Panel and then clicking Details on the Languages tab.</span></span>                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a><span data-ttu-id="3fcee-172">Использование IME с ДКСУТ</span><span class="sxs-lookup"><span data-stu-id="3fcee-172">Using IMEs with DXUT</span></span>

<span data-ttu-id="3fcee-173">В ДКСУТ класс Кдксутимидитбокс реализует функциональность IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-173">In DXUT, the CDXUTIMEEditBox class implements IME functionality.</span></span> <span data-ttu-id="3fcee-174">Этот класс является производным от класса Кдксутедитбокс, базового элемента управления Edit, предоставляемого платформой.</span><span class="sxs-lookup"><span data-stu-id="3fcee-174">This class is derived from the CDXUTEditBox class, the basic edit control provided by the framework.</span></span> <span data-ttu-id="3fcee-175">Кдксутимидитбокс расширяет этот элемент управления "поле ввода" для поддержки IME путем переопределения методов Кдксутимидитбокс.</span><span class="sxs-lookup"><span data-stu-id="3fcee-175">CDXUTIMEEditBox extends that edit control to support IMEs by overriding the CDXUTIMEEditBox methods.</span></span> <span data-ttu-id="3fcee-176">Эти классы разработаны таким образом, чтобы помочь разработчикам узнать, что нужно сделать из платформы, чтобы реализовать поддержку IME в своих собственных элементах управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="3fcee-176">The classes are designed this way to help developers learn what they need to take from the framework to implement IME support in their own edit controls.</span></span> <span data-ttu-id="3fcee-177">В оставшейся части этого раздела объясняется, как платформа и Кдксутимидитбокс в частности, переопределяет базовый элемент управления "поле ввода" для реализации функций IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-177">The rest of this topic explains how the framework, and CDXUTIMEEditBox in particular, overrides a basic edit control to implement IME functionality.</span></span>

<span data-ttu-id="3fcee-178">Большинство переменных IME в Кдксутимидитбокс объявляются как статические, поскольку многие буферы и состояния IME относятся к конкретному процессу.</span><span class="sxs-lookup"><span data-stu-id="3fcee-178">Most of the IME-specific variables in CDXUTIMEEditBox are declared as static, because many IME buffers and states are specific to the process.</span></span> <span data-ttu-id="3fcee-179">Например, процесс содержит только один буфер для строки композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-179">For instance, a process has only one buffer for the composition string.</span></span> <span data-ttu-id="3fcee-180">Даже если процесс имеет десять элементов управления "поле ввода", все они будут совместно использовать один и тот же буфер строк композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-180">Even if the process has ten edit controls, they will all be sharing the same composition string buffer.</span></span> <span data-ttu-id="3fcee-181">Таким образом, буфер строк композиции для Кдксутимидитбокс является статическим и не позволяет приложению занимать ненужное пространство памяти.</span><span class="sxs-lookup"><span data-stu-id="3fcee-181">The composition string buffer for CDXUTIMEEditBox is therefore static, preventing the application from taking up unnecessary memory space.</span></span>

<span data-ttu-id="3fcee-182">Кдксутимидитбокс реализуется в следующем коде ДКСУТ:</span><span class="sxs-lookup"><span data-stu-id="3fcee-182">CDXUTIMEEditBox is implemented in the following DXUT code:</span></span>

<span data-ttu-id="3fcee-183">(Корень пакета SDK) \\ Примеры \\ C++ \\ Common \\ дксутгуи. cpp</span><span class="sxs-lookup"><span data-stu-id="3fcee-183">(SDK root)\\Samples\\C++\\Common\\DXUTgui.cpp</span></span>

## <a name="overriding-the-default-ime-behavior"></a><span data-ttu-id="3fcee-184">Переопределение поведения IME по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3fcee-184">Overriding the Default IME Behavior</span></span>

<span data-ttu-id="3fcee-185">Обычно редактор IME использует стандартные процедуры Windows для создания окна (см. раздел [Использование Windows](/windows/desktop/winmsg/using-windows)).</span><span class="sxs-lookup"><span data-stu-id="3fcee-185">Normally an IME uses standard Windows procedures to create a window (see [Using Windows](/windows/desktop/winmsg/using-windows)).</span></span> <span data-ttu-id="3fcee-186">В обычных обстоятельствах это дает удовлетворительные результаты.</span><span class="sxs-lookup"><span data-stu-id="3fcee-186">Under normal circumstances, this produces satisfactory results.</span></span> <span data-ttu-id="3fcee-187">Однако если приложение представлено в полноэкранном режиме, как обычно используется для игр, стандартные окна больше не работают и могут не отображаться поверх приложения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-187">However, when the application presents in full-screen mode, as is common for games, standard windows no longer work and may not display on top of the application.</span></span> <span data-ttu-id="3fcee-188">Чтобы преодолеть эту ошибку, приложение должно изобразить сами окна IME, а не полагаться на Windows для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="3fcee-188">To overcome this issue, the application must draw the IME windows itself instead of relying on Windows to perform this task.</span></span>

<span data-ttu-id="3fcee-189">Если поведение при создании окна IME по умолчанию не позволяет определить, что требуется приложению, приложение может переопределить обработку окна IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-189">When the default IME window creation behavior does not provide what an application requires, the application can override the IME window handling.</span></span> <span data-ttu-id="3fcee-190">Приложение может достичь этого, обрабатывая сообщения, связанные с IME, и вызывая API [диспетчера методов ввода](/windows/desktop/Intl/input-method-manager) (IMM).</span><span class="sxs-lookup"><span data-stu-id="3fcee-190">An application can achieve this by processing IME-related messages and calling the [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM) API.</span></span>

<span data-ttu-id="3fcee-191">Когда пользователь взаимодействует с IME для ввода сложных символов, IMM отправляет сообщения в приложение, чтобы уведомить его о важных событиях, таких как запуск композиции или отображение окна кандидатов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-191">When a user interacts with an IME to input complex characters, the IMM sends messages to the application to notify it of important events, such as starting a composition or showing the candidate window.</span></span> <span data-ttu-id="3fcee-192">Приложение обычно игнорирует эти сообщения и передает их в обработчик сообщений по умолчанию, что приводит к их обработке редактором IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-192">An application typically ignores these messages and passes them to the default message handler, which causes the IME to handle them.</span></span> <span data-ttu-id="3fcee-193">Когда приложение, а не обработчик по умолчанию, обрабатывает сообщения, оно точно определяет, что происходит в каждом из событий IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-193">When the application, instead of the default handler, handles the messages, it controls exactly what happens at each of the IME events.</span></span> <span data-ttu-id="3fcee-194">Часто обработчик сообщений получает содержимое различных окон IME путем вызова API IMM.</span><span class="sxs-lookup"><span data-stu-id="3fcee-194">Often the message handler retrieves the content of the various IME windows by calling the IMM API.</span></span> <span data-ttu-id="3fcee-195">После того, как приложение покажет эти сведения, оно может правильно отображать окна IME, когда оно должно отображаться на экране.</span><span class="sxs-lookup"><span data-stu-id="3fcee-195">Once the application has this information, it can properly draw the IME windows itself when it needs to render to the display.</span></span>

## <a name="functions"></a><span data-ttu-id="3fcee-196">Функции</span><span class="sxs-lookup"><span data-stu-id="3fcee-196">Functions</span></span>

<span data-ttu-id="3fcee-197">Редактору IME необходимо получить строку чтения, скрыть окно чтения и получить ориентацию окна чтения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-197">An IME needs to get the reading string, hide the reading window, and get the orientation of reading window.</span></span> <span data-ttu-id="3fcee-198">В этой таблице показаны функции для каждой версии IME:</span><span class="sxs-lookup"><span data-stu-id="3fcee-198">This table shows the functionalities per IME version:</span></span>



|                    | <span data-ttu-id="3fcee-199">Идет чтение строки</span><span class="sxs-lookup"><span data-stu-id="3fcee-199">Getting reading string</span></span>                                                | <span data-ttu-id="3fcee-200">Скрытие окна чтения</span><span class="sxs-lookup"><span data-stu-id="3fcee-200">Hiding reading window</span></span>                       | <span data-ttu-id="3fcee-201">Ориентация окна чтения</span><span class="sxs-lookup"><span data-stu-id="3fcee-201">Orientation of reading window</span></span>                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3fcee-202">До версии 6,0</span><span class="sxs-lookup"><span data-stu-id="3fcee-202">Before version 6.0</span></span> | <span data-ttu-id="3fcee-203">A.</span><span class="sxs-lookup"><span data-stu-id="3fcee-203">A.</span></span> <span data-ttu-id="3fcee-204">Чтение закрытых данных IME в окне прямого доступа.</span><span class="sxs-lookup"><span data-stu-id="3fcee-204">Reading Window Access IME private data directly.</span></span> <span data-ttu-id="3fcee-205">См. раздел "4 структуры".</span><span class="sxs-lookup"><span data-stu-id="3fcee-205">See "4 Structure"</span></span> | <span data-ttu-id="3fcee-206">Ловушки частных сообщений IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-206">Trap IME private messages.</span></span> <span data-ttu-id="3fcee-207">См. "3 сообщения"</span><span class="sxs-lookup"><span data-stu-id="3fcee-207">See "3 Messages"</span></span> | <span data-ttu-id="3fcee-208">Изучите сведения реестра.</span><span class="sxs-lookup"><span data-stu-id="3fcee-208">Examine registry information.</span></span> <span data-ttu-id="3fcee-209">См. раздел «5 данных реестра».</span><span class="sxs-lookup"><span data-stu-id="3fcee-209">See "5 Registry Information"</span></span> |
| <span data-ttu-id="3fcee-210">После версии 6,0</span><span class="sxs-lookup"><span data-stu-id="3fcee-210">After version 6.0</span></span>  | [<span data-ttu-id="3fcee-211">жетреадингстринг</span><span class="sxs-lookup"><span data-stu-id="3fcee-211">GetReadingString</span></span>](#getreadingstring)                                 | [<span data-ttu-id="3fcee-212">шовреадингвиндов</span><span class="sxs-lookup"><span data-stu-id="3fcee-212">ShowReadingWindow</span></span>](#showreadingwindow)     | [<span data-ttu-id="3fcee-213">жетреадингстринг</span><span class="sxs-lookup"><span data-stu-id="3fcee-213">GetReadingString</span></span>](#getreadingstring)                      |



 

## <a name="messages"></a><span data-ttu-id="3fcee-214">Сообщения</span><span class="sxs-lookup"><span data-stu-id="3fcee-214">Messages</span></span>

<span data-ttu-id="3fcee-215">Следующие сообщения не должны обрабатываться для нового редактора IME, реализующего [шовреадингвиндов](#showreadingwindow)().</span><span class="sxs-lookup"><span data-stu-id="3fcee-215">The following messages don't have to be processed for newer IME that implements [ShowReadingWindow](#showreadingwindow)().</span></span>

<span data-ttu-id="3fcee-216">Следующие сообщения перехватываются обработчиком сообщений приложения (т. е. они не передаются в Дефвиндовпрок), чтобы предотвратить отображение окна чтения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-216">The following messages are trapped by application message handler (i.e. they are not passed to DefWindowProc) to prevent the reading window from showing up.</span></span>

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a><span data-ttu-id="3fcee-217">Примеры</span><span class="sxs-lookup"><span data-stu-id="3fcee-217">Examples</span></span>

<span data-ttu-id="3fcee-218">В следующих примерах показано, как получить сведения о строках из старого редактора IME, не имеющего Жетреадингстринг ().</span><span class="sxs-lookup"><span data-stu-id="3fcee-218">The following examples illustrate how to get reading string information from older IME that doesn't have GetReadingString().</span></span> <span data-ttu-id="3fcee-219">Код создает следующие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="3fcee-219">The code generates the following outputs:</span></span>



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fcee-220">DWORD двлен</span><span class="sxs-lookup"><span data-stu-id="3fcee-220">DWORD dwlen</span></span>  | <span data-ttu-id="3fcee-221">Длина строки чтения</span><span class="sxs-lookup"><span data-stu-id="3fcee-221">Length of the reading string</span></span>                                                          |
| <span data-ttu-id="3fcee-222">DWORD дверр</span><span class="sxs-lookup"><span data-stu-id="3fcee-222">DWORD dwerr</span></span>  | <span data-ttu-id="3fcee-223">Индекс знака ошибки</span><span class="sxs-lookup"><span data-stu-id="3fcee-223">Index of error char</span></span>                                                                   |
| <span data-ttu-id="3fcee-224">LPWSTR встр</span><span class="sxs-lookup"><span data-stu-id="3fcee-224">LPWSTR wstr</span></span>  | <span data-ttu-id="3fcee-225">Указатель на строку чтения</span><span class="sxs-lookup"><span data-stu-id="3fcee-225">Pointer to the reading string</span></span>                                                         |
| <span data-ttu-id="3fcee-226">BOOL (Юникод)</span><span class="sxs-lookup"><span data-stu-id="3fcee-226">BOOL unicode</span></span> | <span data-ttu-id="3fcee-227">Если значение равно true, строка чтения имеет формат Юникода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-227">If true, the reading string is in Unicode format.</span></span> <span data-ttu-id="3fcee-228">В противном случае он имеет формат многобайтового формата.</span><span class="sxs-lookup"><span data-stu-id="3fcee-228">Otherwise it's in multibyte format.</span></span> |



 

### <a name="cht-ime-version-42-43-and-44"></a><span data-ttu-id="3fcee-229">Редактор метода CHT версии 4,2, 4,3 и 4,4</span><span class="sxs-lookup"><span data-stu-id="3fcee-229">CHT IME version 4.2, 4.3 and 4.4</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a><span data-ttu-id="3fcee-230">Метод IME для CHT версии 5,0</span><span class="sxs-lookup"><span data-stu-id="3fcee-230">CHT IME version 5.0</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a><span data-ttu-id="3fcee-231">Метод IME версии 5,1, 5,2 и CHS IME версии 5,3</span><span class="sxs-lookup"><span data-stu-id="3fcee-231">CHT IME version 5.1, 5.2 and CHS IME version 5.3</span></span>

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a><span data-ttu-id="3fcee-232">CHS IME версии 4,1</span><span class="sxs-lookup"><span data-stu-id="3fcee-232">CHS IME version 4.1</span></span>

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a><span data-ttu-id="3fcee-233">CHS IME версии 4,2</span><span class="sxs-lookup"><span data-stu-id="3fcee-233">CHS IME version 4.2</span></span>

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a><span data-ttu-id="3fcee-234">Сообщения IME</span><span class="sxs-lookup"><span data-stu-id="3fcee-234">IME Messages</span></span>

<span data-ttu-id="3fcee-235">Полноэкранное приложение должно правильно работать со следующими сообщениями, связанными с IME:</span><span class="sxs-lookup"><span data-stu-id="3fcee-235">A full-screen application must properly handle the following IME-related messages:</span></span>

### <a name="wm_inputlangchange"></a><span data-ttu-id="3fcee-236">WM \_ инпутлангчанже</span><span class="sxs-lookup"><span data-stu-id="3fcee-236">WM\_INPUTLANGCHANGE</span></span>

<span data-ttu-id="3fcee-237">Модуль IMM отправляет сообщение WM \_ инпутлангчанже в активное окно приложения после того, как пользовательский язык ввода был изменен пользователем с помощью сочетания клавиш (обычно Alt + Shift) или с индикатором локали ввода на панели задач или в языковой панели.</span><span class="sxs-lookup"><span data-stu-id="3fcee-237">The IMM sends a WM\_INPUTLANGCHANGE message to the active window of an application after the input locale has been changed by the user with a key combination (usually ALT+SHIFT), or with the input locale indicator on the taskbar or language bar.</span></span> <span data-ttu-id="3fcee-238">Языковая панель — это элемент управления на экране, с помощью которого пользователь может настроить службу текстового ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-238">The language bar is an on-screen control with which the user can configure a text service.</span></span> <span data-ttu-id="3fcee-239">(См. раздел [как показать языковую панель](/windows/desktop/TSF/how-to-set-up-tsf).) На следующем снимке экрана показан список выбора языка, который отображается, когда пользователь щелкает индикатор локали.</span><span class="sxs-lookup"><span data-stu-id="3fcee-239">(See [How to show the language bar](/windows/desktop/TSF/how-to-set-up-tsf).) The following screen shot shows a language selection list that is displayed when the user clicks on the locale indicator.</span></span>

![Список выбора языка, который отображается, когда пользователь щелкает индикатор локали](images/ime-langselection.png)

<span data-ttu-id="3fcee-241">Когда модуль IMM отправляет сообщение WM \_ инпутлангчанже, кдксутимидитбокс должен выполнить несколько важных задач:</span><span class="sxs-lookup"><span data-stu-id="3fcee-241">When the IMM sends a WM\_INPUTLANGCHANGE message, CDXUTIMEEditBox must perform several important tasks:</span></span>

1.  <span data-ttu-id="3fcee-242">Метод Жеткэйбоардлайаут вызывается для возврата идентификатора локали ввода (ID) для потока приложения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-242">The GetKeyboardLayout method is called to return the input locale identifier (ID) for the application thread.</span></span> <span data-ttu-id="3fcee-243">Класс Кдксутимидитбокс сохраняет этот идентификатор в статической переменной члена s \_ хклкуррент для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="3fcee-243">The CDXUTIMEEditBox class saves this ID in its static member variable s\_hklCurrent for later use.</span></span> <span data-ttu-id="3fcee-244">Важно, чтобы приложение знало текущий язык ввода, поскольку редактор IME для каждого языка имеет собственное поведение.</span><span class="sxs-lookup"><span data-stu-id="3fcee-244">It is important for the application to know the current input locale, because the IME for each language has its own distinct behavior.</span></span> <span data-ttu-id="3fcee-245">Разработчику может потребоваться предоставить другой код для разных языков ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-245">The developer may need to provide different code for different input locales.</span></span>
2.  <span data-ttu-id="3fcee-246">Кдксутимидитбокс инициализирует строку для отображения в индикаторе языка поля редактирования.</span><span class="sxs-lookup"><span data-stu-id="3fcee-246">CDXUTIMEEditBox initializes a string to display in the edit box language indicator.</span></span> <span data-ttu-id="3fcee-247">Этот индикатор может отображать активный язык ввода, когда приложение работает в полноэкранном режиме, и ни панель задач, ни языковая панель не видны.</span><span class="sxs-lookup"><span data-stu-id="3fcee-247">This indicator can display the active input language when the application is running in full-screen mode and neither the taskbar nor language bar is visible.</span></span>
3.  <span data-ttu-id="3fcee-248">Метод Иммжетконверсионстатус вызывается для указания того, находится ли язык ввода в собственном или несобственном режиме преобразования.</span><span class="sxs-lookup"><span data-stu-id="3fcee-248">The ImmGetConversionStatus method is called to indicate whether the input locale is in native or non-native conversion mode.</span></span> <span data-ttu-id="3fcee-249">Собственный режим преобразования позволяет пользователю вводить текст на выбранном языке.</span><span class="sxs-lookup"><span data-stu-id="3fcee-249">Native conversion mode lets the user enter text in the chosen language.</span></span> <span data-ttu-id="3fcee-250">Неуправляемый режим преобразования делает клавиатуру стандартной английской клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="3fcee-250">Non-native conversion mode makes the keyboard act as a standard English keyboard.</span></span> <span data-ttu-id="3fcee-251">Важно дать пользователю визуальную подсказку о том, в каком типе преобразования находится редактор IME, чтобы пользователь мог легко узнать, какие символы должны быть доступны при попадании в ключ.</span><span class="sxs-lookup"><span data-stu-id="3fcee-251">It is important to give the user a visual cue as to what type of conversion mode the IME is in, so that the user can easily know what characters to expect when hitting a key.</span></span> <span data-ttu-id="3fcee-252">Кдксутимидитбокс предоставляет эту визуальную подсказку с цветом индикатора языка.</span><span class="sxs-lookup"><span data-stu-id="3fcee-252">CDXUTIMEEditBox provides this visual cue with a language indicator color.</span></span> <span data-ttu-id="3fcee-253">Когда язык ввода использует IME с собственным режимом преобразования, класс Кдксутимидитбокс рисует текст индикатора цветом, определенным \_ параметром m индикаторимеколор.</span><span class="sxs-lookup"><span data-stu-id="3fcee-253">When the input locale uses an IME with native conversion mode, the CDXUTIMEEditBox class draws the indicator text with the color defined by the m\_IndicatorImeColor parameter.</span></span> <span data-ttu-id="3fcee-254">Если редактор IME находится в режиме преобразования, отличном от Native, или вообще не используется IME, класс рисует текст индикатора с цветом, определенным \_ параметром m индикаторенгколор.</span><span class="sxs-lookup"><span data-stu-id="3fcee-254">When the IME is in non-native conversion mode, or no IME is used at all, the class draws the indicator text with the color defined by the m\_IndicatorEngColor parameter.</span></span>
4.  <span data-ttu-id="3fcee-255">Кдксутимидитбокс проверяет язык ввода и устанавливает для статической переменной члена s \_ бинсертонтипе значение true для корейского языка и false для всех остальных языков.</span><span class="sxs-lookup"><span data-stu-id="3fcee-255">CDXUTIMEEditBox checks the input locale and sets the static member variable s\_bInsertOnType to TRUE for Korean and FALSE for all other languages.</span></span> <span data-ttu-id="3fcee-256">Этот флаг необходим из-за различных вариантов поведения корейского IME и других редакторов IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-256">This flag is required because of the different behaviors of Korean IMEs and all other IMEs.</span></span> <span data-ttu-id="3fcee-257">При вводе символов на языках, отличных от корейского, вводимый пользователем текст отображается в окне композиции, и пользователь может свободно изменять содержимое строки композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-257">When entering characters in languages other than Korean, the user-entered text is displayed in the composition window, and the user can freely change the content of the composition string.</span></span> <span data-ttu-id="3fcee-258">Пользователь нажимает клавишу ВВОД при удовлетворении строки композиции, а строка композиции отправляется в приложение как ряд \_ сообщений WM char.</span><span class="sxs-lookup"><span data-stu-id="3fcee-258">The user presses the ENTER key when satisfied with the composition string, and the composition string is sent to the application as a series of WM\_CHAR messages.</span></span> <span data-ttu-id="3fcee-259">Однако в редакторах IME для корейского языка, когда пользователь нажимает клавишу для ввода текста, символ немедленно отправляется в приложение.</span><span class="sxs-lookup"><span data-stu-id="3fcee-259">In Korean IMEs, however, when a user presses a key to enter text, a character is immediately sent to the application.</span></span> <span data-ttu-id="3fcee-260">Когда пользователь в дальнейшем нажимает больше ключей для изменения начального символа, символ в поле ввода изменяется в соответствии с дополнительными входными данными пользователя.</span><span class="sxs-lookup"><span data-stu-id="3fcee-260">When the user subsequently presses more keys to modify that initial character, the character in the edit box changes to reflect additional input from the user.</span></span> <span data-ttu-id="3fcee-261">По сути, пользователь состоит из составляющих символов в поле ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-261">Essentially, the user is composing characters in the edit box.</span></span> <span data-ttu-id="3fcee-262">Эти два поведения по-разному могут быть Кдксутимидитбокс для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="3fcee-262">These two behaviors are different enough that CDXUTIMEEditBox must code for each of them specifically.</span></span>
5.  <span data-ttu-id="3fcee-263">Статический метод-член Сетупимеапи вызывается для получения адресов двух функций из модуля IME: Жетреадингстринг и Шовреадингвиндов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-263">The static member method SetupImeApi is called to retrieve addresses of two functions from the IME module: GetReadingString and ShowReadingWindow.</span></span> <span data-ttu-id="3fcee-264">Если эти функции существуют, вызывается Шовреадингвиндов, чтобы скрыть окно чтения по умолчанию для этого редактора IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-264">If these functions exist, ShowReadingWindow is called to hide the default reading window for this IME.</span></span> <span data-ttu-id="3fcee-265">Так как приложение визуализирует само окно чтения, оно уведомляет редактор IME о необходимости отключить прорисовку окна чтения по умолчанию, чтобы оно не мешало отрисовке в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="3fcee-265">Because the application renders the reading window itself, it notifies the IME to disable drawing the default reading window so that it will not interfere with full-screen rendering.</span></span>

<span data-ttu-id="3fcee-266">Модуль IMM отправляет \_ сообщение SETCONTEXT редактора WM IME \_ при активации окна приложения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-266">The IMM sends a WM\_IME\_SETCONTEXT message when a window of the application is activated.</span></span> <span data-ttu-id="3fcee-267">Параметр lParam этого сообщения содержит флаг, указывающий редактору IME, что должны быть выведены окна, а какие — нет.</span><span class="sxs-lookup"><span data-stu-id="3fcee-267">The lParam parameter of this message contains a flag that indicates to the IME which windows should get drawn and which should not.</span></span> <span data-ttu-id="3fcee-268">Поскольку приложение обрабатывает всю прорисовку, редактор IME не требует прорисовки каких-либо окон IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-268">Because the application is handling all of the drawing, it does not need the IME to draw any of the IME windows.</span></span> <span data-ttu-id="3fcee-269">Таким образом, обработчик сообщений приложения просто устанавливает параметр lParam в значение 0 и возвращает.</span><span class="sxs-lookup"><span data-stu-id="3fcee-269">Therefore, the application's message handler simply sets lParam to 0 and returns.</span></span>

<span data-ttu-id="3fcee-270">Чтобы обеспечить поддержку редактора IME для приложений, требуется специальная обработка, связанная с IME, \_ \_ SETCONTEXT IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-270">In order for applications to support IME, special processing is needed for the IME-related message WM\_IME\_SETCONTEXT.</span></span> <span data-ttu-id="3fcee-271">Так как Windows обычно отправляет это сообщение приложению до вызова метода Панорамаинитиализе (), панораму не удается обработать пользовательский интерфейс для отображения окон списка кандидатов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-271">Since Windows typically sends this message to the application prior to calling the PanoramaInitialize() method, Panorama doesn't have a chance to process the UI for showing candidate list windows.</span></span>

<span data-ttu-id="3fcee-272">В приведенном ниже фрагменте кода указано, что приложения Windows не отображают пользовательский интерфейс, связанный с окном списка кандидатов, что позволяет использовать панораму для специально обрабатывающего этот пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3fcee-272">The following code snippet specifies to Windows applications not to display any UI associated with the candidate list window, allowing Panorama to specifically handle this UI.</span></span>

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a><span data-ttu-id="3fcee-273">\_старткомпоситион IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="3fcee-273">WM\_IME\_STARTCOMPOSITION</span></span>

<span data-ttu-id="3fcee-274">Модуль IMM отправляет \_ сообщение старткомпоситион редактора IME WM в \_ приложение, когда композиция IME собирается начать работу в результате нажатия клавиш пользователем.</span><span class="sxs-lookup"><span data-stu-id="3fcee-274">The IMM sends a WM\_IME\_STARTCOMPOSITION message to the application when an IME composition is about to begin as a result of keystrokes by the user.</span></span> <span data-ttu-id="3fcee-275">Если редактор IME использует окно композиции, то он отображает текущую строку композиции в окне композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-275">If the IME uses the composition window, it displays the current composition string in a composition window.</span></span> <span data-ttu-id="3fcee-276">Кдксутимидитбокс обрабатывает это сообщение, выполняя две задачи:</span><span class="sxs-lookup"><span data-stu-id="3fcee-276">CDXUTIMEEditBox handles this message by performing two tasks:</span></span>

1.  <span data-ttu-id="3fcee-277">Кдксутимидитбокс очищает буфер строк композиции и буфер атрибутов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-277">CDXUTIMEEditBox clears the composition string buffer and attribute buffer.</span></span> <span data-ttu-id="3fcee-278">Эти буферы являются статическими членами Кдксутимидитбокс.</span><span class="sxs-lookup"><span data-stu-id="3fcee-278">These buffers are static members of CDXUTIMEEditBox.</span></span>
2.  <span data-ttu-id="3fcee-279">Кдксутимидитбокс задает \_ значение true для статической переменной члена бхидекарет.</span><span class="sxs-lookup"><span data-stu-id="3fcee-279">CDXUTIMEEditBox sets the s\_bHideCaret static member variable to TRUE.</span></span> <span data-ttu-id="3fcee-280">Этот член, определенный в базовом классе Кдксутедитбокс, определяет, следует ли рисовать курсор в поле ввода при отрисовке поля редактирования.</span><span class="sxs-lookup"><span data-stu-id="3fcee-280">This member, defined in the base CDXUTEditBox class, controls whether the cursor in the edit box should be drawn when the edit box is rendered.</span></span> <span data-ttu-id="3fcee-281">Окно композиции работает аналогично полю редактирования с текстом и курсором.</span><span class="sxs-lookup"><span data-stu-id="3fcee-281">The composition window functions similarly to an edit box with text and cursor.</span></span> <span data-ttu-id="3fcee-282">Чтобы избежать путаницы при отображении окна композиции, поле редактирования скрывает курсор таким образом, чтобы в каждый момент времени был виден только один курсор.</span><span class="sxs-lookup"><span data-stu-id="3fcee-282">To avoid confusion when the composition window is visible, the edit box hides its cursor so that only one cursor is visible at a time.</span></span>

### <a name="wm_ime_composition"></a><span data-ttu-id="3fcee-283">\_композиция IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="3fcee-283">WM\_IME\_COMPOSITION</span></span>

<span data-ttu-id="3fcee-284">Модуль IMM отправляет в \_ приложение сообщение композиции редактора IME WM, \_ когда пользователь вводит нажатие клавиши для изменения строки композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-284">The IMM sends a WM\_IME\_COMPOSITION message to the application when the user enters a keystroke to change the composition string.</span></span> <span data-ttu-id="3fcee-285">Значение lParam указывает тип информации, которую приложение может извлечь из диспетчера метода ввода (IMM).</span><span class="sxs-lookup"><span data-stu-id="3fcee-285">The value of lParam indicates what type of information the application can retrieve from the Input Method Manager (IMM).</span></span> <span data-ttu-id="3fcee-286">Приложение должно извлечь доступную информацию, вызвав [**иммжеткомпоситионстринг**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) , а затем сохранить данные в своем частном буфере, чтобы он мог ВИЗУАЛИЗИРОВАТЬ элементы IME позже.</span><span class="sxs-lookup"><span data-stu-id="3fcee-286">The application should retrieve the available information by calling [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) and then should save the information in its private buffer so that it can render the IME elements later.</span></span>

<span data-ttu-id="3fcee-287">Кдксутимидитбокс проверяет наличие и получает следующие данные строки композиции:</span><span class="sxs-lookup"><span data-stu-id="3fcee-287">CDXUTIMEEditBox checks for and retrieves the following composition string data:</span></span>



| <span data-ttu-id="3fcee-288">[**WM \_ Значение \_**](/windows/desktop/Intl/wm-ime-composition) флага lParam для композиции IME</span><span class="sxs-lookup"><span data-stu-id="3fcee-288">[**WM\_IME\_COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam Flag Value</span></span> | <span data-ttu-id="3fcee-289">Данные</span><span class="sxs-lookup"><span data-stu-id="3fcee-289">Data</span></span>                           | <span data-ttu-id="3fcee-290">Описание</span><span class="sxs-lookup"><span data-stu-id="3fcee-290">Description</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fcee-291">\_КОМПАТТР GC</span><span class="sxs-lookup"><span data-stu-id="3fcee-291">GCS\_COMPATTR</span></span>                                                         | <span data-ttu-id="3fcee-292">Атрибут компоновки</span><span class="sxs-lookup"><span data-stu-id="3fcee-292">Composition Attribute</span></span>          | <span data-ttu-id="3fcee-293">Этот атрибут содержит такие сведения, как состояние каждого символа в строке композиции (например, преобразованный или не преобразованный).</span><span class="sxs-lookup"><span data-stu-id="3fcee-293">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="3fcee-294">Эти сведения необходимы, так как Кдксутимидитбокс цвета символы строки композиции по-разному основаны на их атрибутах.</span><span class="sxs-lookup"><span data-stu-id="3fcee-294">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span>                                                                                   |
| <span data-ttu-id="3fcee-295">\_КОМПКЛАУСЕ GC</span><span class="sxs-lookup"><span data-stu-id="3fcee-295">GCS\_COMPCLAUSE</span></span>                                                       | <span data-ttu-id="3fcee-296">Сведения о предложении композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-296">Composition Clause Information</span></span> | <span data-ttu-id="3fcee-297">Сведения об этом предложении используются, когда активен редактор IME для японского языка.</span><span class="sxs-lookup"><span data-stu-id="3fcee-297">This clause information is used when the Japanese IME is active.</span></span> <span data-ttu-id="3fcee-298">При преобразовании строки компоновки на японском языке символы могут быть сгруппированы вместе как предложение, которое преобразуется в одну сущность.</span><span class="sxs-lookup"><span data-stu-id="3fcee-298">When a Japanese composition string is converted, characters may be grouped together as a clause that gets converted to a single entity.</span></span> <span data-ttu-id="3fcee-299">Когда пользователь перемещает курсор, Кдксутимидитбокс использует эти сведения для выделения всего предложения целиком, а не всего одного символа в предложении.</span><span class="sxs-lookup"><span data-stu-id="3fcee-299">When the user moves the cursor, CDXUTIMEEditBox uses this information to highlight the entire clause, instead of just a single character within the clause.</span></span> |
| <span data-ttu-id="3fcee-300">\_КОМПСТР GC</span><span class="sxs-lookup"><span data-stu-id="3fcee-300">GCS\_COMPSTR</span></span>                                                          | <span data-ttu-id="3fcee-301">Строка композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-301">Composition String</span></span>             | <span data-ttu-id="3fcee-302">Эта строка является актуальной строкой, которая формируется пользователем.</span><span class="sxs-lookup"><span data-stu-id="3fcee-302">This string is the up-to-date string being composed by the user.</span></span> <span data-ttu-id="3fcee-303">Это также строка, отображаемая в окне композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-303">This is also the string displayed in the composition window.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="3fcee-304">\_КУРСОРПОС GC</span><span class="sxs-lookup"><span data-stu-id="3fcee-304">GCS\_CURSORPOS</span></span>                                                        | <span data-ttu-id="3fcee-305">Расположение курсора композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-305">Composition Cursor Position</span></span>    | <span data-ttu-id="3fcee-306">В окне композиции реализуется курсор, аналогичный курсору в поле ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-306">The composition window implements a cursor, similar to the cursor in an edit box.</span></span> <span data-ttu-id="3fcee-307">Приложение может извлекать позицию курсора при обработке \_ \_ сообщения композиции редактора мыши WM, чтобы правильно нарисовать курсор.</span><span class="sxs-lookup"><span data-stu-id="3fcee-307">The application can retrieve the cursor position when processing the WM\_IME\_COMPOSITION message in order to draw the cursor properly.</span></span>                                                                                                                                            |
| <span data-ttu-id="3fcee-308">\_РЕСУЛТСТР GC</span><span class="sxs-lookup"><span data-stu-id="3fcee-308">GCS\_RESULTSTR</span></span>                                                        | <span data-ttu-id="3fcee-309">Результирующая строка</span><span class="sxs-lookup"><span data-stu-id="3fcee-309">Result String</span></span>                  | <span data-ttu-id="3fcee-310">Результирующая строка доступна, когда пользователь собирается завершить процесс композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-310">The result string is available when the user is about to complete the composition process.</span></span> <span data-ttu-id="3fcee-311">Эта строка должна быть получена, а символы должны быть отправлены в поле ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-311">This string should be retrieved and the characters should be sent to the edit box.</span></span>                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a><span data-ttu-id="3fcee-312">\_ендкомпоситион IME \_ WM</span><span class="sxs-lookup"><span data-stu-id="3fcee-312">WM\_IME\_ENDCOMPOSITION</span></span>

<span data-ttu-id="3fcee-313">Модуль IMM отправляет \_ сообщение ендкомпоситион редактора IME WM в \_ приложение при завершении операции композиции IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-313">The IMM sends a WM\_IME\_ENDCOMPOSITION message to the application when the IME composition operation is ending.</span></span> <span data-ttu-id="3fcee-314">Это может произойти, когда пользователь нажимает клавишу ВВОД для утверждения строки композиции или клавишу ESC для отмены композиции.</span><span class="sxs-lookup"><span data-stu-id="3fcee-314">This can occur when the user presses the ENTER key to approve the composition string, or the ESC key to cancel the composition.</span></span> <span data-ttu-id="3fcee-315">Кдксутимидитбокс обрабатывает это сообщение, настроив буфер строк композиции как пустой.</span><span class="sxs-lookup"><span data-stu-id="3fcee-315">CDXUTIMEEditBox handles this message by setting the composition string buffer to be empty.</span></span> <span data-ttu-id="3fcee-316">Затем \_ параметру бхидекарет присваивается значение false, так как окно композиции закрывается, а курсор в поле ввода снова становится видимым.</span><span class="sxs-lookup"><span data-stu-id="3fcee-316">It then sets s\_bHideCaret to FALSE because the composition window is closed and the cursor in the edit box should again be visible.</span></span>

<span data-ttu-id="3fcee-317">Обработчик сообщений Кдксутимидитбокс также устанавливает \_ для бшовреадингвиндов значение false.</span><span class="sxs-lookup"><span data-stu-id="3fcee-317">The CDXUTIMEEditBox message handler also sets s\_bShowReadingWindow to FALSE.</span></span> <span data-ttu-id="3fcee-318">Этот флаг определяет, будет ли класс рисовать окно чтения, когда поле ввода отображается, поэтому при завершении компоновки должно быть задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="3fcee-318">This flag controls whether the class draws the reading window when the edit box renders itself, so it must be set to FALSE when a composition ends.</span></span>

### <a name="wm_ime_notify"></a><span data-ttu-id="3fcee-319">\_уведомление редактора IME WM \_</span><span class="sxs-lookup"><span data-stu-id="3fcee-319">WM\_IME\_NOTIFY</span></span>

<span data-ttu-id="3fcee-320">Модуль IMM отправляет сообщение с \_ уведомлением редактора IME WM \_ в приложение при каждом изменении окна редактора IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-320">The IMM sends a WM\_IME\_NOTIFY message to the application whenever an IME window changes.</span></span> <span data-ttu-id="3fcee-321">Приложение, обрабатывающее Рисование окон IME, должно обработать это сообщение, чтобы оно знало о любом обновлении содержимого окна.</span><span class="sxs-lookup"><span data-stu-id="3fcee-321">An application that handles the drawing of the IME windows should process this message so that it is aware of any update to the content of the window.</span></span> <span data-ttu-id="3fcee-322">Параметр wParam обозначает выполняемую команду или изменение.</span><span class="sxs-lookup"><span data-stu-id="3fcee-322">The wParam indicates the command or the change that is taking place.</span></span> <span data-ttu-id="3fcee-323">Кдксутимидитбокс обрабатывает следующие команды:</span><span class="sxs-lookup"><span data-stu-id="3fcee-323">CDXUTIMEEditBox handles the following commands:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fcee-324">Команда IME</span><span class="sxs-lookup"><span data-stu-id="3fcee-324">IME Command</span></span></th>
<th><span data-ttu-id="3fcee-325">Описание</span><span class="sxs-lookup"><span data-stu-id="3fcee-325">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3fcee-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span><span class="sxs-lookup"><span data-stu-id="3fcee-326"><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></span></span></td>
<td><span data-ttu-id="3fcee-327">Этот атрибут содержит такие сведения, как состояние каждого символа в строке композиции (например, преобразованный или не преобразованный).</span><span class="sxs-lookup"><span data-stu-id="3fcee-327">This attribute contains information such as the status of each character in the composition string (for example, converted or non-converted).</span></span> <span data-ttu-id="3fcee-328">Эти сведения необходимы, так как Кдксутимидитбокс цвета символы строки композиции по-разному основаны на их атрибутах.</span><span class="sxs-lookup"><span data-stu-id="3fcee-328">This information is needed because CDXUTIMEEditBox colors the composition string characters differently based upon their attributes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fcee-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="3fcee-329"><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a> / <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></span></span></td>
<td><span data-ttu-id="3fcee-330">Отправляется в приложение, когда окно кандидатов будет открыто или Обновлено соответственно.</span><span class="sxs-lookup"><span data-stu-id="3fcee-330">Sent to the application when the candidate window is about to be opened or updated, respectively.</span></span> <span data-ttu-id="3fcee-331">Если пользователь хочет изменить преобразованный текст, откроется окно кандидатов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-331">The candidate window opens when a user wishes to change the converted text choice.</span></span> <span data-ttu-id="3fcee-332">Окно обновляется, когда пользователь перемещает индикатор выделения или изменяет страницу.</span><span class="sxs-lookup"><span data-stu-id="3fcee-332">The window is updated when a user moves the selection indicator or changes the page.</span></span> <span data-ttu-id="3fcee-333">Кдксутимидитбокс использует один обработчик сообщений для обеих этих команд, так как необходимые задачи точно одинаковы:</span><span class="sxs-lookup"><span data-stu-id="3fcee-333">CDXUTIMEEditBox uses one message handler for both of these commands because the tasks required are exactly the same:</span></span><br/>
<ol>
<li><span data-ttu-id="3fcee-334">Кдксутимидитбокс задает элемент Бшоввиндов структуры списка кандидатов s_CandList значение TRUE, чтобы указать, что окно кандидатов должно рисоваться во время отрисовки кадров.</span><span class="sxs-lookup"><span data-stu-id="3fcee-334">CDXUTIMEEditBox sets the bShowWindow member of the candidate list structure s_CandList to TRUE to indicate that the candidate window needs to be drawn during frame rendering.</span></span></li>
<li><span data-ttu-id="3fcee-335">Кдксутимидитбокс извлекает список кандидатов, вызывая <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>иммжеткандидателист</strong></a>, сначала для получения требуемого размера буфера, а затем снова для получения фактических данных.</span><span class="sxs-lookup"><span data-stu-id="3fcee-335">CDXUTIMEEditBox retrieves the candidate list by calling <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, first to get the required buffer size, and then again to get the actual data.</span></span></li>
<li><span data-ttu-id="3fcee-336">Структура списка частных кандидатов s_CandList инициализируется извлеченными данными-кандидатами.</span><span class="sxs-lookup"><span data-stu-id="3fcee-336">The private candidate list structure s_CandList is initialized with the retrieved candidate data.</span></span></li>
<li><span data-ttu-id="3fcee-337">Строки-кандидаты хранятся в виде массива строк.</span><span class="sxs-lookup"><span data-stu-id="3fcee-337">The candidate strings are stored as an array of strings.</span></span></li>
<li><span data-ttu-id="3fcee-338">Будет сохранен индекс выбранной записи, а также индекс страницы.</span><span class="sxs-lookup"><span data-stu-id="3fcee-338">The index of the selected entry, as well as the page index, is saved.</span></span></li>
<li><span data-ttu-id="3fcee-339">Кдксутимидитбокс проверяет, является ли стиль окна кандидатов вертикальным или горизонтальным.</span><span class="sxs-lookup"><span data-stu-id="3fcee-339">CDXUTIMEEditBox checks whether the candidate window style is vertical or horizontal.</span></span> <span data-ttu-id="3fcee-340">Если стиль окна является горизонтальным, то дополнительный буфер строки, член Хориканд s_CandList, должен инициализироваться со всеми строками-кандидатами, в которых вставлены символы пробела между соседними строками.</span><span class="sxs-lookup"><span data-stu-id="3fcee-340">If the window style is horizontal, an additional string buffer, the HoriCand member of s_CandList, must be initialized with all of the candidate strings, with space characters inserted between all adjacent strings.</span></span> <span data-ttu-id="3fcee-341">При отрисовке вертикального окна-кандидата отдельные строки-кандидаты рисуются по одному за раз, а координаты y увеличиваются для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="3fcee-341">When rendering a vertical candidate window, the individual candidate strings are drawn one at a time, with the y coordinates incremented for each string.</span></span> <span data-ttu-id="3fcee-342">Однако эту строку Хориканд следует использовать при отрисовке горизонтального окна-кандидата, поскольку символ пробела является лучшим способом разделения двух смежных строк в одной строке.</span><span class="sxs-lookup"><span data-stu-id="3fcee-342">However, this HoriCand string should be used when rendering a horizontal candidate window, because the space character is the best way to separate two adjacent strings on the same line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3fcee-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span><span class="sxs-lookup"><span data-stu-id="3fcee-343"><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></span></span></td>
<td><span data-ttu-id="3fcee-344">Отправляется в приложение, когда будет закрыто окно кандидатов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-344">Sent to the application when a candidate window is about to close.</span></span> <span data-ttu-id="3fcee-345">Это происходит, когда пользователь сделал выбор из списка кандидатов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-345">This happens when a user has made a selection from the candidate list.</span></span> <span data-ttu-id="3fcee-346">Кдксутимидитбокс обрабатывает эту команду, устанавливая для флага Visible окна кандидатов значение FALSE, а затем очищает буфер строки-кандидата.</span><span class="sxs-lookup"><span data-stu-id="3fcee-346">CDXUTIMEEditBox handles this command by setting the visible flag of the candidate window to FALSE and then clearing the candidate string buffer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3fcee-347">IMN_PRIVATE</span><span class="sxs-lookup"><span data-stu-id="3fcee-347">IMN_PRIVATE</span></span></td>
<td><span data-ttu-id="3fcee-348">Отправляется в приложение, когда редактор IME обновляет строку чтения в результате ввода или удаления символов пользователем.</span><span class="sxs-lookup"><span data-stu-id="3fcee-348">Sent to the application when the IME has updated its reading string as a result of the user typing or removing characters.</span></span> <span data-ttu-id="3fcee-349">Приложение должно получить строку чтения и сохранить ее для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="3fcee-349">The application should retrieve the reading string and save it for rendering.</span></span> <span data-ttu-id="3fcee-350">Кдксутимидитбокс имеет два метода для получения строки чтения, основываясь на том, как считывание строк поддерживается в IME:</span><span class="sxs-lookup"><span data-stu-id="3fcee-350">CDXUTIMEEditBox has two methods to retrieve the reading string, based upon how reading strings are supported in the IME:</span></span> <br/>
<ul>
<li><span data-ttu-id="3fcee-351">Если редактор IME поддерживает функцию Жетреадингстринг, вызывается Жетреадингстринг для получения строки чтения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-351">If the IME supports the GetReadingString function, GetReadingString is called to retrieve the reading string.</span></span></li>
<li><span data-ttu-id="3fcee-352">Если редактор IME не реализует Жетреадингстринг, Кдксутимидитбокс извлекает строку чтения из содержимого входного контекста.</span><span class="sxs-lookup"><span data-stu-id="3fcee-352">If the IME does not implement GetReadingString, CDXUTIMEEditBox retrieves the reading string from the input context content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a><span data-ttu-id="3fcee-353">Отрисовка</span><span class="sxs-lookup"><span data-stu-id="3fcee-353">Rendering</span></span>

<span data-ttu-id="3fcee-354">Отрисовка элементов IME и окон осуществляется просто.</span><span class="sxs-lookup"><span data-stu-id="3fcee-354">Rendering of the IME elements and windows is straightforward.</span></span> <span data-ttu-id="3fcee-355">Кдксутимидитбокс позволяет сначала подготовить базовый класс, так как окна IME должны отображаться в верхней части элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="3fcee-355">CDXUTIMEEditBox lets the base class render first because IME windows should appear on top of the edit control.</span></span> <span data-ttu-id="3fcee-356">После отображения базового поля редактирования Кдксутимидитбокс проверяет флаг видимости для каждого окна IME (индикатор, композиция, кандидат и окно чтения) и отображает окно, если оно должно быть видимым.</span><span class="sxs-lookup"><span data-stu-id="3fcee-356">After the base edit box is rendered, CDXUTIMEEditBox checks the visibility flag of each IME window (indicator, composition, candidate, and reading window) and draws the window if it should be visible.</span></span> <span data-ttu-id="3fcee-357">Описание различных типов окон IME см. в разделе поведение IME по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3fcee-357">See Default IME Behavior for descriptions of the different IME window types.</span></span>

### <a name="input-locale-indicator"></a><span data-ttu-id="3fcee-358">Индикатор локали ввода</span><span class="sxs-lookup"><span data-stu-id="3fcee-358">Input Locale Indicator</span></span>

<span data-ttu-id="3fcee-359">Индикатор локали ввода подготавливается к просмотру перед любыми другими окнами IME, так как это элемент, который всегда отображается.</span><span class="sxs-lookup"><span data-stu-id="3fcee-359">The input locale indicator is rendered before any other IME windows because it is an element that is always displayed.</span></span> <span data-ttu-id="3fcee-360">Поэтому он должен отображаться под другими окнами IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-360">It should therefore appear below other IME windows.</span></span> <span data-ttu-id="3fcee-361">Кдксутимидитбокс визуализирует индикатор, вызывая метод Рендериндикатор, в котором цвет шрифта индикатора определяется с помощью проверки \_ статической переменной s, которая отражает текущий режим преобразования IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-361">CDXUTIMEEditBox renders the indicator by calling the RenderIndicator method, in which the indicator font color is determined by examining the s\_ImeState static variable, which reflects the current IME conversion mode.</span></span> <span data-ttu-id="3fcee-362">Если редактор IME включен и встроенное преобразование активно, метод использует m индикаторимеколор в \_ качестве цвета индикатора.</span><span class="sxs-lookup"><span data-stu-id="3fcee-362">When the IME is enabled and native conversion is active, the method uses m\_IndicatorImeColor as the indicator color.</span></span> <span data-ttu-id="3fcee-363">Если редактор IME отключен или находится в несобственном режиме преобразования, \_ для рисования текста индикатора используется m индикаторимеколор.</span><span class="sxs-lookup"><span data-stu-id="3fcee-363">If the IME is disabled or is in non-native conversion mode, m\_IndicatorImeColor is used to draw the indicator text.</span></span> <span data-ttu-id="3fcee-364">По умолчанию окно индикатора отображается справа от поля ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-364">By default, the indicator window itself is drawn to the right of the edit box.</span></span> <span data-ttu-id="3fcee-365">Приложения могут изменить это поведение, переопределив метод Рендериндикатор.</span><span class="sxs-lookup"><span data-stu-id="3fcee-365">Applications can change this behavior by overriding the RenderIndicator method.</span></span>

<span data-ttu-id="3fcee-366">На следующем рисунке показаны различные варианты обозначения языка ввода для английского языка, японского языка в алфавитно-цифровых режимах преобразования и японского языка в режиме встроенного преобразования:</span><span class="sxs-lookup"><span data-stu-id="3fcee-366">The following figure shows the different appearances of an input locale indicator for English, Japanese in alphanumeric conversion mode, and Japanese in native conversion mode:</span></span>

![различные варианты обозначения языка ввода для английского и японского языков](images/ime-indicator.png)

### <a name="composition-window"></a><span data-ttu-id="3fcee-368">Окно композиции</span><span class="sxs-lookup"><span data-stu-id="3fcee-368">Composition Window</span></span>

<span data-ttu-id="3fcee-369">Рисование окна композиции обрабатывается в методе Рендеркомпоситион объекта Кдксутимидитбокс.</span><span class="sxs-lookup"><span data-stu-id="3fcee-369">The drawing of the composition window is handled in the RenderComposition method of CDXUTIMEEditBox.</span></span> <span data-ttu-id="3fcee-370">Окно композиции перемещается над полем ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-370">The composition window floats above the edit box.</span></span> <span data-ttu-id="3fcee-371">Он должен отображаться в позиции курсора базового элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="3fcee-371">It should be drawn at the cursor position of the underlying edit control.</span></span> <span data-ttu-id="3fcee-372">Кдксутимидитбокс обрабатывает отрисовку следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3fcee-372">CDXUTIMEEditBox handles the rendering as follows:</span></span>

1.  <span data-ttu-id="3fcee-373">Вся строка композиции рисуется с использованием цветов строк композиции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3fcee-373">The entire composition string is drawn using the default composition string colors.</span></span>
2.  <span data-ttu-id="3fcee-374">Символы с определенными специальными атрибутами должны отображаться на разных цветах, поэтому Кдксутимидитбокс проверяет символы строки композиции и проверяет атрибут String.</span><span class="sxs-lookup"><span data-stu-id="3fcee-374">Characters with certain special attributes should be drawn in different colors, so CDXUTIMEEditBox reviews the characters of the composition string and inspects the string attribute.</span></span> <span data-ttu-id="3fcee-375">Если атрибут вызывает разные цвета, символ снова рисуется с соответствующими цветами.</span><span class="sxs-lookup"><span data-stu-id="3fcee-375">If the attribute calls for different colors, the character is drawn again with the appropriate colors.</span></span>
3.  <span data-ttu-id="3fcee-376">Курсор окна композиции рисуется для завершения отрисовки.</span><span class="sxs-lookup"><span data-stu-id="3fcee-376">The cursor of the composition window is drawn to complete the rendering.</span></span>

<span data-ttu-id="3fcee-377">Курсор должен мигать для корейского IME, но не для других редакторов IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-377">The cursor should blink for Korean IMEs, but it should not for other IMEs.</span></span> <span data-ttu-id="3fcee-378">Рендеркомпоситион определяет, должен ли курсор быть видимым на основе значений таймера при использовании корейского редактора IME.</span><span class="sxs-lookup"><span data-stu-id="3fcee-378">RenderComposition determines whether the cursor should be visible based upon timer values when the Korean IME is used.</span></span>

### <a name="reading-and-candidate-windows"></a><span data-ttu-id="3fcee-379">Чтение и потенциальные окна</span><span class="sxs-lookup"><span data-stu-id="3fcee-379">Reading and Candidate Windows</span></span>

<span data-ttu-id="3fcee-380">Окна чтения и кандидатов отображаются одним и тем же методом Кдксутимидитбокс, Рендеркандидатереадингвиндов.</span><span class="sxs-lookup"><span data-stu-id="3fcee-380">The reading and candidate windows are rendered by the same CDXUTIMEEditBox method, RenderCandidateReadingWindow.</span></span> <span data-ttu-id="3fcee-381">Оба окна содержат массив строк для вертикального макета или одну строку в случае горизонтального макета.</span><span class="sxs-lookup"><span data-stu-id="3fcee-381">Both windows contain an array of strings for vertical layout, or a single string in the case of horizontal layout.</span></span> <span data-ttu-id="3fcee-382">Основная часть кода в Рендеркандидатереадингвиндов используется для размещения окна таким образом, чтобы ни одна часть окна не находилась вне окна приложения и не была обрезана.</span><span class="sxs-lookup"><span data-stu-id="3fcee-382">The bulk of the code in RenderCandidateReadingWindow is used to position the window so that no part of the window falls outside the application window and gets clipped.</span></span>

## <a name="limitations"></a><span data-ttu-id="3fcee-383">Ограничения</span><span class="sxs-lookup"><span data-stu-id="3fcee-383">Limitations</span></span>

<span data-ttu-id="3fcee-384">Редакторы IME иногда содержат дополнительные функции, позволяющие упростить ввод текста.</span><span class="sxs-lookup"><span data-stu-id="3fcee-384">IMEs sometimes contain advanced features to improve the ease of inputting text.</span></span> <span data-ttu-id="3fcee-385">Некоторые функции, доступные в более новых редакторах IME, показаны на следующих рисунках.</span><span class="sxs-lookup"><span data-stu-id="3fcee-385">Some of the features found in newer IMEs are shown in the following figures.</span></span> <span data-ttu-id="3fcee-386">Эти дополнительные функции отсутствуют в ДКСУТ.</span><span class="sxs-lookup"><span data-stu-id="3fcee-386">These advanced features are not present in DXUT.</span></span> <span data-ttu-id="3fcee-387">Реализация поддержки этих дополнительных функций может быть сложной, поскольку для получения необходимой информации из редакторов IME не определен интерфейс.</span><span class="sxs-lookup"><span data-stu-id="3fcee-387">Implementing support for these advanced features can be challenging because there is no interface defined to obtain the necessary information from the IMEs.</span></span>

<span data-ttu-id="3fcee-388">Расширенный китайский язык IME с расширенным списком кандидатов:</span><span class="sxs-lookup"><span data-stu-id="3fcee-388">Advanced Traditional Chinese IME with expanded candidate list:</span></span>

![Расширенный китайский язык IME с расширенным списком кандидатов](images/ime-advanced1.png)

<span data-ttu-id="3fcee-390">Расширенный IME для японского языка с некоторыми потенциальными записями, содержащими дополнительный текст для описания их значений:</span><span class="sxs-lookup"><span data-stu-id="3fcee-390">Advanced Japanese IME with some candidate entries that contain additional text to describe their meanings:</span></span>

![Расширенный японский редактор IME с некоторыми потенциальными записями, содержащими дополнительный текст для описания их значений](images/ime-advanced2.png)

<span data-ttu-id="3fcee-392">Расширенный редактор IME для корейского языка, включающий систему распознавания рукописного текста:</span><span class="sxs-lookup"><span data-stu-id="3fcee-392">Advanced Korean IME that includes a handwriting recognition system:</span></span>

![Расширенный корейский язык IME, включающий систему распознавания рукописного текста](images/ime-advanced3.png)

## <a name="registry-information"></a><span data-ttu-id="3fcee-394">Сведения о реестре</span><span class="sxs-lookup"><span data-stu-id="3fcee-394">Registry Information</span></span>

<span data-ttu-id="3fcee-395">Следующие данные реестра проверяются, чтобы определить ориентацию окна чтения, если текущий редактор IME имеет старую версию CHT New фонетическая, не реализующая Жетреадингстринг ().</span><span class="sxs-lookup"><span data-stu-id="3fcee-395">The following registry information is checked to determine the orientation of the reading window, when the current IME is older CHT New Phonetic that doesn't implement GetReadingString().</span></span>



| <span data-ttu-id="3fcee-396">Ключ</span><span class="sxs-lookup"><span data-stu-id="3fcee-396">Key</span></span>                                                           | <span data-ttu-id="3fcee-397">Значение</span><span class="sxs-lookup"><span data-stu-id="3fcee-397">Value</span></span>            |
|---------------------------------------------------------------|------------------|
| <span data-ttu-id="3fcee-398">HKCU \\ программное обеспечение \\ Microsoft \\ Windows \\ CurrentVersion \\ IME \_ Name</span><span class="sxs-lookup"><span data-stu-id="3fcee-398">HKCU\\software\\microsoft\\windows\\currentversion\\IME\_Name</span></span> | <span data-ttu-id="3fcee-399">Сопоставление клавиш</span><span class="sxs-lookup"><span data-stu-id="3fcee-399">keyboard mapping</span></span> |



 

<span data-ttu-id="3fcee-400">Где: \_ имя IME — мстЦиф, если версия файла IME — 5,1 или более поздняя; в противном случае \_ имя IME — тинтлгнт.</span><span class="sxs-lookup"><span data-stu-id="3fcee-400">Where: IME\_Name is MSTCIPH if the IME file version is 5.1 or later; otherwise IME\_Name is TINTLGNT.</span></span>

<span data-ttu-id="3fcee-401">Ориентация окна чтения горизонтальна, если:</span><span class="sxs-lookup"><span data-stu-id="3fcee-401">The orientation of reading window is horizontal if either:</span></span>

-   <span data-ttu-id="3fcee-402">Редактор IME имеет версию 5,0, а значение сопоставления клавиатуры — 0x22 или 0x23.</span><span class="sxs-lookup"><span data-stu-id="3fcee-402">The IME is version 5.0 and keyboard mapping value is 0x22 or 0x23</span></span>
-   <span data-ttu-id="3fcee-403">Редактор IME имеет версию 5,1 или 5,2, а параметр сопоставления клавиатуры имеет значение 0x22, 0x23 или 0x24.</span><span class="sxs-lookup"><span data-stu-id="3fcee-403">The IME is version 5.1 or version 5.2 and keyboard mapping value is 0x22, 0x23 or 0x24.</span></span>

<span data-ttu-id="3fcee-404">Если ни одно из условий не выполнено, окно чтения является вертикальным.</span><span class="sxs-lookup"><span data-stu-id="3fcee-404">If neither condition is met, the reading window is vertical.</span></span>

## <a name="appendix-a-cht-versions-per-operating-system"></a><span data-ttu-id="3fcee-405">Приложение а. версии CHT для каждой операционной системы</span><span class="sxs-lookup"><span data-stu-id="3fcee-405">Appendix A: CHT Versions per Operating System</span></span>



| <span data-ttu-id="3fcee-406">Операционная система</span><span class="sxs-lookup"><span data-stu-id="3fcee-406">Operating System</span></span>           | <span data-ttu-id="3fcee-407">Версия IME для CHT</span><span class="sxs-lookup"><span data-stu-id="3fcee-407">CHT IME Version</span></span> |
|----------------------------|-----------------|
| <span data-ttu-id="3fcee-408">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3fcee-408">Windows 98</span></span>                 | <span data-ttu-id="3fcee-409">4.2</span><span class="sxs-lookup"><span data-stu-id="3fcee-409">4.2</span></span>             |
| <span data-ttu-id="3fcee-410">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3fcee-410">Windows 2000</span></span>               | <span data-ttu-id="3fcee-411">4.3</span><span class="sxs-lookup"><span data-stu-id="3fcee-411">4.3</span></span>             |
| <span data-ttu-id="3fcee-412">неизвестно</span><span class="sxs-lookup"><span data-stu-id="3fcee-412">unknown</span></span>                    | <span data-ttu-id="3fcee-413">4.4.</span><span class="sxs-lookup"><span data-stu-id="3fcee-413">4.4</span></span>             |
| <span data-ttu-id="3fcee-414">Windows ME</span><span class="sxs-lookup"><span data-stu-id="3fcee-414">Windows ME</span></span>                 | <span data-ttu-id="3fcee-415">5.0</span><span class="sxs-lookup"><span data-stu-id="3fcee-415">5.0</span></span>             |
| <span data-ttu-id="3fcee-416">Office XP</span><span class="sxs-lookup"><span data-stu-id="3fcee-416">Office XP</span></span>                  | <span data-ttu-id="3fcee-417">5.1</span><span class="sxs-lookup"><span data-stu-id="3fcee-417">5.1</span></span>             |
| <span data-ttu-id="3fcee-418">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3fcee-418">Windows XP</span></span>                 | <span data-ttu-id="3fcee-419">5,2</span><span class="sxs-lookup"><span data-stu-id="3fcee-419">5.2</span></span>             |
| <span data-ttu-id="3fcee-420">Автономный веб-довнлоадбле</span><span class="sxs-lookup"><span data-stu-id="3fcee-420">Standalone web downloadble</span></span> | <span data-ttu-id="3fcee-421">6.0</span><span class="sxs-lookup"><span data-stu-id="3fcee-421">6.0</span></span>             |



 

## <a name="further-information"></a><span data-ttu-id="3fcee-422">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3fcee-422">Further Information</span></span>

<span data-ttu-id="3fcee-423">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="3fcee-423">For additional information, see the following:</span></span>

-   [<span data-ttu-id="3fcee-424">Установка и использование редакторов метода ввода</span><span class="sxs-lookup"><span data-stu-id="3fcee-424">Installing and Using Input Method Editors</span></span>](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [<span data-ttu-id="3fcee-425">Международный вывод текста</span><span class="sxs-lookup"><span data-stu-id="3fcee-425">International Text Display</span></span>](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [<span data-ttu-id="3fcee-426">Консорциум Unicode</span><span class="sxs-lookup"><span data-stu-id="3fcee-426">The Unicode Consortium</span></span>](https://www.unicode.org/)
-   <span data-ttu-id="3fcee-427">Разработка международного программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-427">Developing International Software.</span></span> <span data-ttu-id="3fcee-428">Dr. International.</span><span class="sxs-lookup"><span data-stu-id="3fcee-428">Dr. International.</span></span> <span data-ttu-id="3fcee-429">второй Ed.</span><span class="sxs-lookup"><span data-stu-id="3fcee-429">2nd ed.</span></span> <span data-ttu-id="3fcee-430">Redmond, штат Вашингтон: Microsoft Press, 2003.</span><span class="sxs-lookup"><span data-stu-id="3fcee-430">Redmond, WA: Microsoft Press, 2003.</span></span>

## <a name="getreadingstring"></a><span data-ttu-id="3fcee-431">жетреадингстринг</span><span class="sxs-lookup"><span data-stu-id="3fcee-431">GetReadingString</span></span>

<span data-ttu-id="3fcee-432">Получает сведения о строках.</span><span class="sxs-lookup"><span data-stu-id="3fcee-432">Gets reading string information.</span></span>

<span data-ttu-id="3fcee-433">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="3fcee-433">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="3fcee-434"><span id="himc_"></span><span id="HIMC_"></span>*химк*</span><span class="sxs-lookup"><span data-stu-id="3fcee-434"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcee-435">\[в \] контексте ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-435">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*уреадингбуфлен*</span><span class="sxs-lookup"><span data-stu-id="3fcee-436"><span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*</span></span>
</dt> <dd>

<span data-ttu-id="3fcee-437">\[\]Длина лпвреадингбуф в WCHAR.</span><span class="sxs-lookup"><span data-stu-id="3fcee-437">\[in\] Length of lpwReadingBuf, in WCHAR.</span></span> <span data-ttu-id="3fcee-438">Если он равен нулю, это означает, что длина буфера чтения запросов превышает.</span><span class="sxs-lookup"><span data-stu-id="3fcee-438">If it is zero, it means query reading buffer length.</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*лпвреадингбуф*</span><span class="sxs-lookup"><span data-stu-id="3fcee-439"><span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcee-440">\[исходящий \] Возврат строки (не ноль в конце).</span><span class="sxs-lookup"><span data-stu-id="3fcee-440">\[out\] Return reading string (not zero end).</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*пнеррориндекс*</span><span class="sxs-lookup"><span data-stu-id="3fcee-441"><span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcee-442">\[out \] возвращает индекс символа ошибки в строке чтения, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="3fcee-442">\[out\] Return index of error character in the reading string if there is.</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*пфисвертикал*</span><span class="sxs-lookup"><span data-stu-id="3fcee-443"><span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcee-444">\[Если это так \] , то пользовательский интерфейс считывается вертикально.</span><span class="sxs-lookup"><span data-stu-id="3fcee-444">\[out\] If it is TRUE, reading UI is vertical.</span></span> <span data-ttu-id="3fcee-445">В противном случае — горизонтальное Пумаксреадинглен.</span><span class="sxs-lookup"><span data-stu-id="3fcee-445">Otherwise, horizontal puMaxReadingLen.</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*пумаксреадинглен*</span><span class="sxs-lookup"><span data-stu-id="3fcee-446"><span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcee-447">\[\]Длина пользовательского интерфейса чтения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-447">\[out\] The reading UI length.</span></span> <span data-ttu-id="3fcee-448">Максимальная длина чтения не фиксирована; Он зависит не только от раскладки клавиатуры, но и от режима ввода (например, внутреннего кода, суррогатного ввода).</span><span class="sxs-lookup"><span data-stu-id="3fcee-448">The max reading length is not fixed; it depends not only on keyboard layout, but also on input mode (for example, internal code, surrogate input).</span></span>

</dd> </dl>

<span data-ttu-id="3fcee-449">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="3fcee-449">**Return Values**</span></span>

<span data-ttu-id="3fcee-450">Длина строки чтения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-450">The reading string length.</span></span>

<span data-ttu-id="3fcee-451">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3fcee-451">**Remarks**</span></span>

<span data-ttu-id="3fcee-452">Если возвращаемое значение больше значения параметра Уреадингбуфлен, то все выходные параметры не определены.</span><span class="sxs-lookup"><span data-stu-id="3fcee-452">If the return value is greater than the value of uReadingBufLen, then all output parameters are undefined.</span></span>

<span data-ttu-id="3fcee-453">Эта функция реализована в CHT IME 6,0 или более поздней версии и может быть получена с помощью GetProcAddress в обработчике модуля IME. обработчик модуля IME может быть получен с помощью Иммжетимефиленаме и LoadLibrary.</span><span class="sxs-lookup"><span data-stu-id="3fcee-453">This function is implemented in CHT IME 6.0 or later, and can be acquired by GetProcAddress on an IME module handle; the IME module handle can be acquired by ImmGetIMEFileName and LoadLibrary.</span></span>

<span data-ttu-id="3fcee-454">**Требования**</span><span class="sxs-lookup"><span data-stu-id="3fcee-454">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="3fcee-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3fcee-455"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="3fcee-456">Объявлено в IMM. h.</span><span class="sxs-lookup"><span data-stu-id="3fcee-456">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Импорт библиотеки**</span><span class="sxs-lookup"><span data-stu-id="3fcee-457"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="3fcee-458">Используйте IMM. lib.</span><span class="sxs-lookup"><span data-stu-id="3fcee-458">Use Imm.lib.</span></span>

</dd> </dl>

## <a name="showreadingwindow"></a><span data-ttu-id="3fcee-459">шовреадингвиндов</span><span class="sxs-lookup"><span data-stu-id="3fcee-459">ShowReadingWindow</span></span>

<span data-ttu-id="3fcee-460">Показать (или скрыть) окно чтения.</span><span class="sxs-lookup"><span data-stu-id="3fcee-460">Show (or hide) the reading window.</span></span>

<span data-ttu-id="3fcee-461">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="3fcee-461">**Parameters**</span></span>

<dl> <dt>

<span data-ttu-id="3fcee-462"><span id="himc_"></span><span id="HIMC_"></span>*химк*</span><span class="sxs-lookup"><span data-stu-id="3fcee-462"><span id="himc_"></span><span id="HIMC_"></span>*himc*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcee-463">\[в \] контексте ввода.</span><span class="sxs-lookup"><span data-stu-id="3fcee-463">\[in\] Input context.</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*бшов*</span><span class="sxs-lookup"><span data-stu-id="3fcee-464"><span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow*</span></span> 
</dt> <dd>

<span data-ttu-id="3fcee-465">\[в поле имеет \] значение true, чтобы показать окно чтения (или false, чтобы скрыть его).</span><span class="sxs-lookup"><span data-stu-id="3fcee-465">\[in\] Set to TRUE to show the reading window (or FALSE to hide it).</span></span>

</dd> </dl>

<span data-ttu-id="3fcee-466">**Возвращаемые значения**</span><span class="sxs-lookup"><span data-stu-id="3fcee-466">**Return Values**</span></span>

<span data-ttu-id="3fcee-467">**Замечания**</span><span class="sxs-lookup"><span data-stu-id="3fcee-467">**Remarks**</span></span>

<span data-ttu-id="3fcee-468">Возвращает значение TRUE в случае успеха или FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3fcee-468">Return TRUE if successful or FALSE if otherwise.</span></span>

<span data-ttu-id="3fcee-469">**Требования**</span><span class="sxs-lookup"><span data-stu-id="3fcee-469">**Requirements**</span></span>

<dl> <dt>

<span data-ttu-id="3fcee-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3fcee-470"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**</span></span>
</dt> <dd>

<span data-ttu-id="3fcee-471">Объявлено в IMM. h.</span><span class="sxs-lookup"><span data-stu-id="3fcee-471">Declared in Imm.h.</span></span>

</dd> <dt>

<span data-ttu-id="3fcee-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Импорт библиотеки**</span><span class="sxs-lookup"><span data-stu-id="3fcee-472"><span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Import Library**</span></span>
</dt> <dd>

<span data-ttu-id="3fcee-473">Используйте IMM. lib.</span><span class="sxs-lookup"><span data-stu-id="3fcee-473">Use Imm.lib.</span></span>

</dd> </dl>