---
title: Таблицы сочетаний клавиш
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104070014"
---
# <a name="accelerator-tables"></a><span data-ttu-id="3b408-103">Таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="3b408-103">Accelerator Tables</span></span>

<span data-ttu-id="3b408-104">Приложения часто определяют сочетания клавиш, например CTRL + O для команды File Open.</span><span class="sxs-lookup"><span data-stu-id="3b408-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="3b408-105">Можно реализовать сочетания клавиш, обрабатывая отдельные сообщения [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) , но таблицы ускорителей обеспечивают лучшее решение, которое:</span><span class="sxs-lookup"><span data-stu-id="3b408-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="3b408-106">Требует меньше кода.</span><span class="sxs-lookup"><span data-stu-id="3b408-106">Requires less coding.</span></span>
-   <span data-ttu-id="3b408-107">Объединяет все сочетания клавиш в один файл данных.</span><span class="sxs-lookup"><span data-stu-id="3b408-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="3b408-108">Поддерживает локализацию на другие языки.</span><span class="sxs-lookup"><span data-stu-id="3b408-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="3b408-109">Позволяет сочетаниям клавиш и команд меню использовать одну и ту же логику приложения.</span><span class="sxs-lookup"><span data-stu-id="3b408-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="3b408-110">*Таблица сочетаний клавиш* — это ресурс данных, который сопоставляет сочетания клавиш, такие как CTRL + O, с командами приложения.</span><span class="sxs-lookup"><span data-stu-id="3b408-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="3b408-111">Прежде чем мы увидим, как использовать таблицу сочетаний клавиш, нам потребуются краткие сведения о ресурсах.</span><span class="sxs-lookup"><span data-stu-id="3b408-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="3b408-112">*Ресурс* — это большой двоичный объект данных, встроенный в двоичный файл приложения (exe или DLL).</span><span class="sxs-lookup"><span data-stu-id="3b408-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="3b408-113">Ресурсы хранят данные, необходимые для приложения, такие как меню, курсоры, значки, изображения, текстовые строки или любые пользовательские данные приложения.</span><span class="sxs-lookup"><span data-stu-id="3b408-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="3b408-114">Приложение загружает данные ресурсов из двоичного файла во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3b408-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="3b408-115">Чтобы включить ресурсы в двоичный файл, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3b408-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="3b408-116">Создайте файл определения ресурса (RC).</span><span class="sxs-lookup"><span data-stu-id="3b408-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="3b408-117">Этот файл определяет типы ресурсов и их идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="3b408-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="3b408-118">Файл определения ресурсов может содержать ссылки на другие файлы.</span><span class="sxs-lookup"><span data-stu-id="3b408-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="3b408-119">Например, ресурс значка объявляется в RC-файле, но изображение значка хранится в отдельном файле.</span><span class="sxs-lookup"><span data-stu-id="3b408-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="3b408-120">Используйте компилятор ресурсов Microsoft Windows (RC) для компиляции файла определения ресурса в скомпилированный файл ресурсов (с расширением RES).</span><span class="sxs-lookup"><span data-stu-id="3b408-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="3b408-121">Компилятор RC поставляется с Visual Studio, а также с Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3b408-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="3b408-122">Свяжите скомпилированный файл ресурсов с двоичным файлом.</span><span class="sxs-lookup"><span data-stu-id="3b408-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="3b408-123">Эти шаги примерно эквивалентны процессу компиляции и компоновки файлов кода.</span><span class="sxs-lookup"><span data-stu-id="3b408-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="3b408-124">Visual Studio предоставляет набор редакторов ресурсов, которые упрощают создание и изменение ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b408-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="3b408-125">(Эти средства недоступны в выпусках Visual Studio Express.) Но RC-файл — это просто текстовый файл, а синтаксис описан на сайте MSDN, поэтому можно создать RC-файл в любом текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="3b408-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="3b408-126">Дополнительные сведения см. в разделе [о файлах ресурсов](/windows/desktop/menurc/about-resource-files).</span><span class="sxs-lookup"><span data-stu-id="3b408-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="3b408-127">Определение таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="3b408-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="3b408-128">Таблица сочетаний клавиш — это таблица сочетаний клавиш.</span><span class="sxs-lookup"><span data-stu-id="3b408-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="3b408-129">Каждое сочетание клавиш определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3b408-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="3b408-130">Числовой идентификатор.</span><span class="sxs-lookup"><span data-stu-id="3b408-130">A numeric identifier.</span></span> <span data-ttu-id="3b408-131">Этот номер идентифицирует команду приложения, которая будет вызываться ярлыком.</span><span class="sxs-lookup"><span data-stu-id="3b408-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="3b408-132">Символ ASCII или код виртуального ключа ярлыка.</span><span class="sxs-lookup"><span data-stu-id="3b408-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="3b408-133">Необязательные клавиши модификатора: ALT, SHIFT или CTRL.</span><span class="sxs-lookup"><span data-stu-id="3b408-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="3b408-134">Сама таблица сочетаний клавиш имеет числовой идентификатор, который определяет таблицу в списке ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="3b408-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="3b408-135">Давайте создадим таблицу сочетаний клавиш для простой программы рисования.</span><span class="sxs-lookup"><span data-stu-id="3b408-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="3b408-136">Эта программа будет иметь два режима, режим рисования и режим выбора.</span><span class="sxs-lookup"><span data-stu-id="3b408-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="3b408-137">В режиме рисования пользователь может рисовать фигуры.</span><span class="sxs-lookup"><span data-stu-id="3b408-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="3b408-138">В режиме выбора пользователь может выбрать фигуры.</span><span class="sxs-lookup"><span data-stu-id="3b408-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="3b408-139">Для этой программы мы хотим определить следующие сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="3b408-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="3b408-140">Сочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="3b408-140">Shortcut</span></span> | <span data-ttu-id="3b408-141">Get-Help</span><span class="sxs-lookup"><span data-stu-id="3b408-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="3b408-142">CTRL+M</span><span class="sxs-lookup"><span data-stu-id="3b408-142">CTRL+M</span></span>   | <span data-ttu-id="3b408-143">Переключение между режимами.</span><span class="sxs-lookup"><span data-stu-id="3b408-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="3b408-144">F1</span><span class="sxs-lookup"><span data-stu-id="3b408-144">F1</span></span>       | <span data-ttu-id="3b408-145">Переключиться в режим рисования.</span><span class="sxs-lookup"><span data-stu-id="3b408-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="3b408-146">F2</span><span class="sxs-lookup"><span data-stu-id="3b408-146">F2</span></span>       | <span data-ttu-id="3b408-147">Переключиться в режим выбора.</span><span class="sxs-lookup"><span data-stu-id="3b408-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="3b408-148">Сначала определите числовые идентификаторы для таблицы и для команд приложения.</span><span class="sxs-lookup"><span data-stu-id="3b408-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="3b408-149">Эти значения являются произвольными.</span><span class="sxs-lookup"><span data-stu-id="3b408-149">These values are arbitrary.</span></span> <span data-ttu-id="3b408-150">Для идентификаторов можно назначить символьные константы, определив их в файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="3b408-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="3b408-151">Пример:</span><span class="sxs-lookup"><span data-stu-id="3b408-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="3b408-152">В этом примере значение `IDR_ACCEL1` идентифицирует таблицу сочетаний клавиш, а следующие три константы определяют команды приложения.</span><span class="sxs-lookup"><span data-stu-id="3b408-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="3b408-153">По соглашению файл заголовка, определяющий константы ресурсов, часто называется Resource. h.</span><span class="sxs-lookup"><span data-stu-id="3b408-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="3b408-154">В следующем листинге показан файл определения ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b408-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="3b408-155">Сочетания клавиш определяются в фигурных скобках.</span><span class="sxs-lookup"><span data-stu-id="3b408-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="3b408-156">Каждый ярлык содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="3b408-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="3b408-157">Код виртуального ключа или символ ASCII, который вызывает ярлык.</span><span class="sxs-lookup"><span data-stu-id="3b408-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="3b408-158">Команда приложения.</span><span class="sxs-lookup"><span data-stu-id="3b408-158">The application command.</span></span> <span data-ttu-id="3b408-159">Обратите внимание, что в примере используются символьные константы.</span><span class="sxs-lookup"><span data-stu-id="3b408-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="3b408-160">Файл определения ресурса включает Resource. h, где определены эти константы.</span><span class="sxs-lookup"><span data-stu-id="3b408-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="3b408-161">Ключевое слово **VIRTKEY** означает, что первая запись является кодом виртуального ключа.</span><span class="sxs-lookup"><span data-stu-id="3b408-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="3b408-162">Другой вариант — использовать символы ASCII.</span><span class="sxs-lookup"><span data-stu-id="3b408-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="3b408-163">Необязательные модификаторы: ALT, CONTROL или SHIFT.</span><span class="sxs-lookup"><span data-stu-id="3b408-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="3b408-164">Если для ярлыков используются символы ASCII, то символ нижнего регистра будет отличаться от сочетания символов в верхнем регистре.</span><span class="sxs-lookup"><span data-stu-id="3b408-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="3b408-165">(Например, ввод "a" может вызвать другую команду, чем ввод "A".) Это может запутать пользователей, поэтому для сочетаний клавиш лучше использовать коды виртуальных клавиш, а не символы ASCII.</span><span class="sxs-lookup"><span data-stu-id="3b408-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="3b408-166">Загрузка таблицы сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="3b408-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="3b408-167">Ресурс для таблицы сочетаний клавиш должен быть загружен, прежде чем программа сможет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="3b408-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="3b408-168">Чтобы загрузить таблицу сочетаний клавиш, вызовите функцию [**лоадакцелераторс**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .</span><span class="sxs-lookup"><span data-stu-id="3b408-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="3b408-169">Вызовите эту функцию перед входом в цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b408-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="3b408-170">Первый параметр — это обработчик для модуля.</span><span class="sxs-lookup"><span data-stu-id="3b408-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="3b408-171">(Этот параметр передается функции [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="3b408-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="3b408-172">Дополнительные сведения см. [в разделе WinMain: точка входа приложения](winmain--the-application-entry-point.md). Вторым параметром является идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b408-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="3b408-173">Функция возвращает маркер ресурса.</span><span class="sxs-lookup"><span data-stu-id="3b408-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="3b408-174">Помните, что handle является непрозрачным типом, который ссылается на объект, управляемый системой.</span><span class="sxs-lookup"><span data-stu-id="3b408-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="3b408-175">Если функция завершается ошибкой, возвращается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3b408-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="3b408-176">Вы можете освободить таблицу сочетаний клавиш, вызвав [**дестройакцелератортабле**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span><span class="sxs-lookup"><span data-stu-id="3b408-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="3b408-177">Однако система автоматически освобождает таблицу при выходе из программы, поэтому эту функцию нужно вызывать только при замене одной таблицы другой.</span><span class="sxs-lookup"><span data-stu-id="3b408-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="3b408-178">В разделе, посвященном [созданию редактируемых пользователем ускорителей](/windows/desktop/menurc/using-keyboard-accelerators), есть интересный пример.</span><span class="sxs-lookup"><span data-stu-id="3b408-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="3b408-179">Преобразование ключевых штрихов в команды</span><span class="sxs-lookup"><span data-stu-id="3b408-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="3b408-180">Таблица сочетаний клавиш работает путем преобразования ключевых штрихов в сообщения [**\_ командной строки WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="3b408-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="3b408-181">Параметр *wParam* **\_ команды WM** содержит числовой идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="3b408-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="3b408-182">Например, при использовании приведенной выше таблицы сочетание клавиш CTRL + M преобразуется в сообщение **\_ команды WM** со значением `ID_TOGGLE_MODE` .</span><span class="sxs-lookup"><span data-stu-id="3b408-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="3b408-183">Чтобы это произошло, измените цикл обработки сообщений следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3b408-183">To make this happen, change your message loop to the following:</span></span>


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



<span data-ttu-id="3b408-184">Этот код добавляет вызов функции [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) в цикле обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b408-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="3b408-185">Функция **TranslateAccelerator** проверяет каждое сообщение окна, выполняя поиск сообщений о ключах.</span><span class="sxs-lookup"><span data-stu-id="3b408-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="3b408-186">Если пользователь нажимает одну из сочетаний клавиш, перечисленных в таблице сочетаний клавиш, **TranslateAccelerator** отправляет [**\_ командное сообщение WM**](/windows/desktop/menurc/wm-command) в окно.</span><span class="sxs-lookup"><span data-stu-id="3b408-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="3b408-187">Функция отправляет **\_ команду WM** , напрямую вызывая процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="3b408-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="3b408-188">Когда **TranslateAccelerator** успешно переводит нажатие клавиши, функция возвращает ненулевое значение, что означает, что следует пропустить нормальную обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b408-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="3b408-189">В противном случае **TranslateAccelerator** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="3b408-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="3b408-190">В этом случае передайте сообщение окна в [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) и [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)в нормальном режиме.</span><span class="sxs-lookup"><span data-stu-id="3b408-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="3b408-191">Вот как программа рисования может работать с [**\_ командным**](/windows/desktop/menurc/wm-command) сообщением WM:</span><span class="sxs-lookup"><span data-stu-id="3b408-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



<span data-ttu-id="3b408-192">В этом коде предполагается, что `SetMode` — это функция, определенная приложением для переключения между двумя режимами.</span><span class="sxs-lookup"><span data-stu-id="3b408-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="3b408-193">Сведения о том, как можно было бы справиться с выполнением команды, зависят от программы.</span><span class="sxs-lookup"><span data-stu-id="3b408-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="3b408-194">Следующая</span><span class="sxs-lookup"><span data-stu-id="3b408-194">Next</span></span>

[<span data-ttu-id="3b408-195">Установка изображения курсора</span><span class="sxs-lookup"><span data-stu-id="3b408-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 