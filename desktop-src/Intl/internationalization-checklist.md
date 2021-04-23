---
description: В этом разделе приводятся действия для создания кода, поддерживающего несколько рынков. Эти инструкции можно рассматривать как руководство во время разработки кода и как метрики при оценке сборок.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Контрольный список интернационализации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b18ef8cf88efa8d496d19c0b66208cd44abaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896681"
---
# <a name="internationalization-checklist"></a><span data-ttu-id="c0492-104">Контрольный список интернационализации</span><span class="sxs-lookup"><span data-stu-id="c0492-104">Internationalization Checklist</span></span>

<span data-ttu-id="c0492-105">В этом разделе приводятся действия для создания кода, поддерживающего несколько рынков.</span><span class="sxs-lookup"><span data-stu-id="c0492-105">This topic provides actions to take to create code that supports multiple markets.</span></span> <span data-ttu-id="c0492-106">Эти инструкции можно рассматривать как руководство во время разработки кода и как метрики при оценке сборок.</span><span class="sxs-lookup"><span data-stu-id="c0492-106">Consider these statements as a guide during code design, and as metrics when you evaluate the builds.</span></span>

-   <span data-ttu-id="c0492-107">Создайте спецификацию программы, которая учитывает международные вопросы с самого начала.</span><span class="sxs-lookup"><span data-stu-id="c0492-107">Create program specifications that account for international considerations from the outset.</span></span>
    -   <span data-ttu-id="c0492-108">Значки и точечные рисунки должны быть осмысленными и неоскорбительными на целевых рынках и не содержат текста.</span><span class="sxs-lookup"><span data-stu-id="c0492-108">Design icons and bitmaps to be meaningful and not offensive in your target markets, and to not contain text.</span></span>
    -   <span data-ttu-id="c0492-109">Меню и диалоговые окна проектирования, чтобы оставить место для расширения текста.</span><span class="sxs-lookup"><span data-stu-id="c0492-109">Design menus and dialog boxes to leave room for text expansion.</span></span> <span data-ttu-id="c0492-110">Например, строки на английском языке часто расширяются на 40% при переводе на немецкий или голландский.</span><span class="sxs-lookup"><span data-stu-id="c0492-110">For example, English strings often expand by 40% when translated into German or Dutch.</span></span>
    -   <span data-ttu-id="c0492-111">Не используйте сленговых выражений или зависящие от культуры ссылки в элементах пользовательского интерфейса или сообщениях.</span><span class="sxs-lookup"><span data-stu-id="c0492-111">Do not use slang or culturally-specific references in UI elements or messages.</span></span>
    -   <span data-ttu-id="c0492-112">Создание сочетаний клавиш, доступных на международных клавиатурах.</span><span class="sxs-lookup"><span data-stu-id="c0492-112">Create shortcut key combinations that are accessible on international keyboards.</span></span> <span data-ttu-id="c0492-113">Например, старайтесь не использовать знаки пунктуации в качестве сочетаний клавиш, так как они не всегда находятся на международных клавиатурах или просто созданы пользователем.</span><span class="sxs-lookup"><span data-stu-id="c0492-113">For example, avoid using punctuation character keys as shortcut keys because they are not always found on international keyboards or easily produced by the user.</span></span> <span data-ttu-id="c0492-114">Примеры раскладок клавиатуры см. в разделе [раскладки клавиатуры Windows](https://msdn.microsoft.com/goglobal/bb964651.aspx).</span><span class="sxs-lookup"><span data-stu-id="c0492-114">For examples of keyboard layouts, see [Windows Keyboard Layouts](https://msdn.microsoft.com/goglobal/bb964651.aspx).</span></span>
    -   <span data-ttu-id="c0492-115">Примите во внимание местные законы, влияющие на модели компонентов, например требования, приобретаемые правительственными организациями по, которые поддерживают несколько официальных языков.</span><span class="sxs-lookup"><span data-stu-id="c0492-115">Consider local laws affecting feature designs, such as requirements that government entities purchase software that supports multiple official languages.</span></span>
    -   <span data-ttu-id="c0492-116">Разрабатывайте сторонние соглашения, поддерживающие международные стандарты пользовательского интерфейса и архитектурные решения вашей организации.</span><span class="sxs-lookup"><span data-stu-id="c0492-116">Develop third-party agreements that support your organization's international UI standards and design decisions.</span></span>
    -   <span data-ttu-id="c0492-117">Используйте постоянную терминологию в строках пользовательского интерфейса, которые необходимо перевести.</span><span class="sxs-lookup"><span data-stu-id="c0492-117">Use consistent terminology in user interface strings that must be translated.</span></span>

<!-- -->

-   <span data-ttu-id="c0492-118">Создайте код, который не зависит от языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="c0492-118">Create code that is independent of locale.</span></span>
    -   <span data-ttu-id="c0492-119">Не объединяйте строки в предложения с формами.</span><span class="sxs-lookup"><span data-stu-id="c0492-119">Don't concatenate strings to form sentences.</span></span>
    -   <span data-ttu-id="c0492-120">Не используйте указанную строковую переменную более чем в одном контексте, например при повторном использовании фрагмента предложения в различных сообщениях и запросах, так как такие строки не могут быть легко преобразованы.</span><span class="sxs-lookup"><span data-stu-id="c0492-120">Don't use a given string variable in more than one context, such as reusing a sentence fragment in different messages and prompts, because such strings may not be easy to translate.</span></span>
    -   <span data-ttu-id="c0492-121">Строки документа с использованием комментариев для предоставления контекста для переводчиков и четкого обозначения строк или символов, которые не должны быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="c0492-121">Document strings using comments to provide context for translators, and clearly mark strings or characters that should not be localized.</span></span>
    -   <span data-ttu-id="c0492-122">Не используйте жестко запрограммированные символьные константы, числовые константы, положения экрана, имена файлов или пути, которые предполагают определенный язык.</span><span class="sxs-lookup"><span data-stu-id="c0492-122">Don't use hard-coded character constants, numeric constants, screen positions, filenames, or pathnames that presume a particular language.</span></span>
    -   <span data-ttu-id="c0492-123">Сделайте буферы достаточно большими, чтобы вместить переведенные строки.</span><span class="sxs-lookup"><span data-stu-id="c0492-123">Make buffers large enough to hold translated strings.</span></span>
    -   <span data-ttu-id="c0492-124">Разрешение ввода данных с использованием форматов, зависящих от языкового стандарта, например даты, времени и денежных единиц.</span><span class="sxs-lookup"><span data-stu-id="c0492-124">Allow the input of data with formats that vary by locale, such as dates, times, and currencies.</span></span>
    -   <span data-ttu-id="c0492-125">Используйте размер бумаги, размер конверта и другие значения по умолчанию, соответствующие заданному языку.</span><span class="sxs-lookup"><span data-stu-id="c0492-125">Use paper size, envelope size, and other defaults that are appropriate to a given locale.</span></span>
    -   <span data-ttu-id="c0492-126">Убедитесь, что каждый языковой выпуск может читать документы, созданные в других выпусках.</span><span class="sxs-lookup"><span data-stu-id="c0492-126">Ensure that each language edition can read documents created by the other editions.</span></span>
    -   <span data-ttu-id="c0492-127">При необходимости предоставьте поддержку оборудования для конкретного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="c0492-127">Provide support for locale-specific hardware, if necessary.</span></span>
    -   <span data-ttu-id="c0492-128">Настройка функций, которые не применяются к международным рынкам, в качестве вариантов реализации, которые можно легко отключить.</span><span class="sxs-lookup"><span data-stu-id="c0492-128">Configure features that don't apply to international markets as implementation options that can be disabled easily.</span></span>

<!-- -->

-   <span data-ttu-id="c0492-129">Создайте код, который использует преимущества международных функций, предлагаемых Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c0492-129">Create code that takes advantage of international functionality offered by Microsoft Windows.</span></span>
    -   <span data-ttu-id="c0492-130">Использование международных сведений, переданных системой (поддержка национальных языков).</span><span class="sxs-lookup"><span data-stu-id="c0492-130">Use international information carried by the system (National Language Support).</span></span>
    -   <span data-ttu-id="c0492-131">Используйте системные функции для сортировки, преобразования регистра и сопоставления строк.</span><span class="sxs-lookup"><span data-stu-id="c0492-131">Use system functions for sorting, case conversion, and string mapping.</span></span>
    -   <span data-ttu-id="c0492-132">Используйте общие функции макета текста.</span><span class="sxs-lookup"><span data-stu-id="c0492-132">Use generic text layout functions.</span></span>
    -   <span data-ttu-id="c0492-133">Реагирование на изменения региональных параметров в панели управления.</span><span class="sxs-lookup"><span data-stu-id="c0492-133">Respond to changes to international settings in Control Panel.</span></span>
    -   <span data-ttu-id="c0492-134">Обработайте \_ сообщение WM инпутлангчанжерекуест.</span><span class="sxs-lookup"><span data-stu-id="c0492-134">Handle the WM\_INPUTLANGCHANGEREQUEST message.</span></span>
    -   <span data-ttu-id="c0492-135">Поддержка редакторов методов ввода, вертикального текста и правил переноса строк в восточно-азиатских выпусках.</span><span class="sxs-lookup"><span data-stu-id="c0492-135">Support input method editors, vertical text, and line-breaking rules in East Asian editions.</span></span>

<!-- -->

-   <span data-ttu-id="c0492-136">Скомпилируйте все международные версии программы из одного набора исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="c0492-136">Compile all international editions of the program from one set of source files.</span></span>
    -   <span data-ttu-id="c0492-137">Свести или исключить механизмы, требующие повторной компиляции кода для разных языковых выпусков.</span><span class="sxs-lookup"><span data-stu-id="c0492-137">Minimize or eliminate mechanisms that require code to be recompiled for different language editions.</span></span>
    -   <span data-ttu-id="c0492-138">Сохраняйте локализуемые элементы, такие как строки и значки, в файлах ресурсов Windows.</span><span class="sxs-lookup"><span data-stu-id="c0492-138">Store localizable items, such as strings and icons, in Windows resource files.</span></span>
    -   <span data-ttu-id="c0492-139">Храните документы во всех выпусках на всех языках, используя тот же формат файла.</span><span class="sxs-lookup"><span data-stu-id="c0492-139">Store documents in all language editions using the same file format.</span></span>

<!-- -->

-   <span data-ttu-id="c0492-140">Поддержка различных наборов символов, а не только кодовой страницы Latin 1, номер 1252.</span><span class="sxs-lookup"><span data-stu-id="c0492-140">Support different character sets, not just the Latin 1 code page, number 1252.</span></span>
    -   <span data-ttu-id="c0492-141">Программа поддерживает сетевые среды, в которых компьютеры работают под управлением операционных систем с разными кодовыми страницами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c0492-141">Program supports network environments in which computers run operating systems with different default code pages.</span></span>
    -   <span data-ttu-id="c0492-142">Используйте Жеткпинфоекс для получения диапазонов старших байтов для кодовых страниц Восточной Азии.</span><span class="sxs-lookup"><span data-stu-id="c0492-142">Use GetCPInfoEx to retrieve lead-byte ranges for East Asian code pages.</span></span>
    -   <span data-ttu-id="c0492-143">Разбирать двухбайтовые символы в приложениях на восточноазиатских языках, если код не основан на Юникоде.</span><span class="sxs-lookup"><span data-stu-id="c0492-143">Parse double-byte characters in East Asian–language applications unless the code is based on Unicode.</span></span>
    -   <span data-ttu-id="c0492-144">Поддержка Юникода или преобразование между Юникодом и локальной кодовой страницей.</span><span class="sxs-lookup"><span data-stu-id="c0492-144">Support Unicode or conversion between Unicode and the local code page.</span></span>
    -   <span data-ttu-id="c0492-145">Не следует рассчитывать, что все символы являются 8-разрядными или 16-разрядными.</span><span class="sxs-lookup"><span data-stu-id="c0492-145">Don't assume that all characters are 8-bit or 16-bit.</span></span>
    -   <span data-ttu-id="c0492-146">Используйте универсальные типы данных и универсальные прототипы функций.</span><span class="sxs-lookup"><span data-stu-id="c0492-146">Use generic data types and generic function prototypes.</span></span>
    -   <span data-ttu-id="c0492-147">Используйте свойство charset Font, которое вызывает EnumFontFamiliesEx и общую функцию диалога ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="c0492-147">Use the font charset property, which calls EnumFontFamiliesEx and the ChooseFont common dialog function.</span></span>
    -   <span data-ttu-id="c0492-148">Отображение и печать текста с использованием шрифтов, подходящих для языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="c0492-148">Display and print text using the fonts that are appropriate for the locale.</span></span>

<!-- -->

-   <span data-ttu-id="c0492-149">Протестируйте международные функции программы.</span><span class="sxs-lookup"><span data-stu-id="c0492-149">Test the international features of the program.</span></span>
    -   <span data-ttu-id="c0492-150">Переведенный текст должен соответствовать стандартам собственных докладчиков.</span><span class="sxs-lookup"><span data-stu-id="c0492-150">Translated text should meet the standards of native speakers.</span></span>
    -   <span data-ttu-id="c0492-151">Размер диалоговых окон должен изменяться должным образом, а текст должен быть соответствующим образом переноситься при отображении различных языков.</span><span class="sxs-lookup"><span data-stu-id="c0492-151">Dialog boxes should resize properly, and text should be hyphenated appropriately, when different languages are displayed.</span></span>
    -   <span data-ttu-id="c0492-152">Диалоговые окна, строки состояния, панели инструментов и меню должны помещаться на экране и читать разборчиво, когда для отображения заданы разные разрешения, для всех переведенных языков.</span><span class="sxs-lookup"><span data-stu-id="c0492-152">Dialog boxes, status bars, toolbars, and menus should fit on the screen and read legibly when the display is set at different resolutions, for all translated languages.</span></span>
    -   <span data-ttu-id="c0492-153">Сочетания клавиш для меню и диалоговых окон должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="c0492-153">Menu and dialog-box accelerators should be unique.</span></span>
    -   <span data-ttu-id="c0492-154">Пользователи должны иметь возможность вводить символы из неевропейских скриптов в документы, диалоговые окна и имена файлов.</span><span class="sxs-lookup"><span data-stu-id="c0492-154">Users should be able to type characters from non-European scripts into documents, dialog boxes, and filenames.</span></span>
    -   <span data-ttu-id="c0492-155">Пользователи должны иметь возможность вырезания, вставки, сохранения и печати символов из неевропейских скриптов.</span><span class="sxs-lookup"><span data-stu-id="c0492-155">Users should be able to cut, paste, save, and print characters from non-European scripts successfully.</span></span>
    -   <span data-ttu-id="c0492-156">Сортировка и преобразование регистра должны быть точными для разных языков.</span><span class="sxs-lookup"><span data-stu-id="c0492-156">Sorting and case conversion should be accurate for different locales.</span></span>
    -   <span data-ttu-id="c0492-157">Приложение должно правильно работать в локализованных выпусках Windows.</span><span class="sxs-lookup"><span data-stu-id="c0492-157">The application should work correctly on localized editions of Windows.</span></span>

 

 



