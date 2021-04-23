---
title: Элемент управления шрифтами
description: Для упрощения интеграции и настройки поддержки шрифтов в приложениях, требующих обработки текста и возможности редактирования текстов, платформа Windows Ribbon предоставляет специализированный элемент управления шрифтом, предоставляющий широкий спектр свойств шрифта, таких как имя гарнитуры, стиль, размер точки и эффекты.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413220"
---
# <a name="font-control"></a><span data-ttu-id="24778-103">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="24778-103">Font Control</span></span>

<span data-ttu-id="24778-104">Для упрощения интеграции и настройки поддержки шрифтов в приложениях, требующих обработки текста и возможности редактирования текстов, платформа Windows Ribbon предоставляет специализированный элемент управления шрифтом, предоставляющий широкий спектр свойств шрифта, таких как имя гарнитуры, стиль, размер точки и эффекты.</span><span class="sxs-lookup"><span data-stu-id="24778-104">To simplify the integration and configuration of font support in applications that require word processing and text editing capabilities, the Windows Ribbon framework provides a specialized Font Control that exposes a wide range of font properties such as typeface name, style, point size, and effects.</span></span>

-   [<span data-ttu-id="24778-105">Введение</span><span class="sxs-lookup"><span data-stu-id="24778-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="24778-106">Единообразный интерфейс</span><span class="sxs-lookup"><span data-stu-id="24778-106">A Consistent Experience</span></span>](#a-consistent-experience)
-   [<span data-ttu-id="24778-107">Простота интеграции и настройки</span><span class="sxs-lookup"><span data-stu-id="24778-107">Easy Integration and Configuration</span></span>](#easy-integration-and-configuration)
-   [<span data-ttu-id="24778-108">Выравнивание с помощью общих текстовых структур GDI</span><span class="sxs-lookup"><span data-stu-id="24778-108">Alignment with Common GDI Text Structures</span></span>](#alignment-with-common-gdi-text-structures)
-   [<span data-ttu-id="24778-109">Добавление Фонтконтрол</span><span class="sxs-lookup"><span data-stu-id="24778-109">Add a FontControl</span></span>](#add-a-fontcontrol)
    -   [<span data-ttu-id="24778-110">Объявление Фонтконтрол в разметке</span><span class="sxs-lookup"><span data-stu-id="24778-110">Declaring a FontControl in Markup</span></span>](#declaring-a-fontcontrol-in-markup)
    -   [<span data-ttu-id="24778-111">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="24778-111">Font Control Properties</span></span>](#font-control-properties)
-   [<span data-ttu-id="24778-112">Определение обработчика команд Фонтконтрол</span><span class="sxs-lookup"><span data-stu-id="24778-112">Define a FontControl Command Handler</span></span>](#define-a-fontcontrol-command-handler)
-   [<span data-ttu-id="24778-113">См. также</span><span class="sxs-lookup"><span data-stu-id="24778-113">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="24778-114">Введение</span><span class="sxs-lookup"><span data-stu-id="24778-114">Introduction</span></span>

<span data-ttu-id="24778-115">Элемент управления "Шрифт" — это составной элемент управления, состоящий из кнопок, выключателей, раскрывающихся списков и полей со списком, которые используются для указания конкретного свойства шрифта или параметра форматирования.</span><span class="sxs-lookup"><span data-stu-id="24778-115">The Font Control is a composite control that consists of buttons, toggle buttons, drop-down list boxes, and combo boxes, all of which are used to specify a particular font property or formatting option.</span></span>

<span data-ttu-id="24778-116">На следующем снимке экрана показан элемент управления шрифтом ленты в WordPad для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="24778-116">The following screen shot shows the Ribbon Font Control in WordPad for Windows 7.</span></span>

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a><span data-ttu-id="24778-118">Единообразный интерфейс</span><span class="sxs-lookup"><span data-stu-id="24778-118">A Consistent Experience</span></span>

<span data-ttu-id="24778-119">Как встроенный элемент управления "лента", элемент управления "Шрифт" улучшает общие функции управления шрифтами, выбора и форматирования, а также обеспечивает широкие возможности согласованного взаимодействия с пользователем во всех приложениях ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-119">As a built-in Ribbon control, the Font Control improves overall font management, selection and formatting functionality, and provides a rich, consistent user experience across all Ribbon applications.</span></span>

<span data-ttu-id="24778-120">Этот единый интерфейс включает</span><span class="sxs-lookup"><span data-stu-id="24778-120">This consistent experience includes</span></span>

-   <span data-ttu-id="24778-121">Стандартизированное форматирование и выбор шрифтов для различных приложений ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-121">Standardized formatting and selection of fonts across Ribbon applications.</span></span>
-   <span data-ttu-id="24778-122">Стандартизованное представление шрифтов для приложений ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-122">Standardized font representation across Ribbon applications.</span></span>
-   <span data-ttu-id="24778-123">Автоматический, в Windows 7 Активация шрифта, основанная на параметре **Показать** или **Скрыть** для каждого шрифта на панели управления **шрифты** .</span><span class="sxs-lookup"><span data-stu-id="24778-123">Automatic, in Windows 7, font activation that is based on the **Show** or **Hide** setting for each font in the **Fonts** control panel.</span></span> <span data-ttu-id="24778-124">Элемент управления "Шрифт" отображает только те шрифты, которые установлены для **отображения**.</span><span class="sxs-lookup"><span data-stu-id="24778-124">The Font Control only displays those fonts that are set to **Show**.</span></span>
    > [!Note]  
    > <span data-ttu-id="24778-125">В Windows Vista панель элементов управления " **шрифты** " не предлагает функции " **Показать** или **Скрыть** ", поэтому активируются все шрифты.</span><span class="sxs-lookup"><span data-stu-id="24778-125">In Windows Vista, the **Fonts** control panel does not offer the **Show** or **Hide** functionality, so all fonts are activated.</span></span>

     

-   <span data-ttu-id="24778-126">Управление шрифтами, доступ к которому осуществляется непосредственно из элемента управления.</span><span class="sxs-lookup"><span data-stu-id="24778-126">Font management that is available directly from the control.</span></span>

    <span data-ttu-id="24778-127">На следующем снимке экрана показано, что доступ к панели элементов управления " **шрифты** " можно получить непосредственно из элемента управления "Шрифт".</span><span class="sxs-lookup"><span data-stu-id="24778-127">The following screen shot shows that the **Fonts** control panel can be accessed directly from the Font Control.</span></span>

    ![снимок экрана со списком семейств шрифтов в WordPad для Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   <span data-ttu-id="24778-129">Поддержка автоматического предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="24778-129">Support for auto-preview.</span></span>
-   <span data-ttu-id="24778-130">Раскрытие шрифтов, которые наиболее важны для пользователя, например</span><span class="sxs-lookup"><span data-stu-id="24778-130">Exposure of fonts that are most relevant to a user, such as</span></span>
    -   <span data-ttu-id="24778-131">Локализованные списки шрифтов для международных пользователей.</span><span class="sxs-lookup"><span data-stu-id="24778-131">Localized font lists for international users.</span></span>
    -   <span data-ttu-id="24778-132">Списки шрифтов на основе устройства ввода.</span><span class="sxs-lookup"><span data-stu-id="24778-132">Font lists based on input device.</span></span>

    > [!Note]  
    > <span data-ttu-id="24778-133">Поддержка этой функции доступна не на всех платформах, предшествующих Windows 7.</span><span class="sxs-lookup"><span data-stu-id="24778-133">Support for this functionality is not available on any platform older than Windows 7.</span></span>

     

## <a name="easy-integration-and-configuration"></a><span data-ttu-id="24778-134">Простота интеграции и настройки</span><span class="sxs-lookup"><span data-stu-id="24778-134">Easy Integration and Configuration</span></span>

<span data-ttu-id="24778-135">Предоставляя стандартные, многократно используемые и легко используемые функции, элемент управления "шрифт ленты" упрощает интеграцию поддержки шрифтов в приложение.</span><span class="sxs-lookup"><span data-stu-id="24778-135">By providing standard, reusable, and easily consumed functionality, the Ribbon Font Control eases the burden of integrating font support into an application.</span></span>

<span data-ttu-id="24778-136">Сведения о выделении и форматировании шрифта упаковываются в один самодостаточный логический элемент, который</span><span class="sxs-lookup"><span data-stu-id="24778-136">The details of font selection and formatting are wrapped in one, self-contained logical element that</span></span>

-   <span data-ttu-id="24778-137">Устраняет сложное управление взаимозависимостями элементов управления, характерной для реализаций элементов управления шрифтами.</span><span class="sxs-lookup"><span data-stu-id="24778-137">Eliminates the complex management of control interdependencies typical of font control implementations.</span></span>
-   <span data-ttu-id="24778-138">Требуется один обработчик команд для всех функций, предоставляемых подэлементами управления шрифтами.</span><span class="sxs-lookup"><span data-stu-id="24778-138">Requires a single Command handler for all functionality exposed by the Font Control sub-controls.</span></span>

<span data-ttu-id="24778-139">Этот обработчик единственных команд позволяет элементу управления "Шрифт" управлять функциональностью различных подэлементов управления внутренним образом. вложенный элемент управления никогда не взаимодействует напрямую с приложением, независимо от его функции.</span><span class="sxs-lookup"><span data-stu-id="24778-139">This single Command handler allows the Font Control to manage the functionality of various sub-controls internally; a sub-control never interacts directly with the application, regardless of its function.</span></span>

<span data-ttu-id="24778-140">К другим функциям элемента управления "Шрифт" относятся</span><span class="sxs-lookup"><span data-stu-id="24778-140">Other features of the Font Control include</span></span>

-   <span data-ttu-id="24778-141">Автоматическое, поддерживающее DPI создание WYSIWYG (то есть что вы получаете) растровое представление для каждого шрифта в меню **семейства шрифтов** .</span><span class="sxs-lookup"><span data-stu-id="24778-141">Automatic, DPI-aware generation of a WYSIWYG (what you see is what you get) bitmap representation for each font in the **Font family** menu.</span></span>
-   <span data-ttu-id="24778-142">Интеграция [Windows интерфейс графических устройств (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="24778-142">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) integration.</span></span>
-   <span data-ttu-id="24778-143">Рисунки и подсказки для локализованных семейств шрифтов.</span><span class="sxs-lookup"><span data-stu-id="24778-143">Localized font family bitmaps and tooltips.</span></span>
-   <span data-ttu-id="24778-144">Перечисление шрифтов, группирование и метаданные для управления и представления шрифтов.</span><span class="sxs-lookup"><span data-stu-id="24778-144">Font enumeration, grouping, and metadata for managing and presenting fonts.</span></span>
    > [!Note]  
    > <span data-ttu-id="24778-145">Поддержка этой функции доступна не на всех платформах, предшествующих Windows 7.</span><span class="sxs-lookup"><span data-stu-id="24778-145">Support for this functionality is not available on any platform older than Windows 7 .</span></span>

     

-   <span data-ttu-id="24778-146">Раскрывающиеся цвета раскрывающегося списка Цвет **текста** и **выделения текста** , которые отражают поведение [средства выбора цвета](windowsribbon-controls-dropdowncolorpicker.md) раскрывающегося списка ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-146">The **Text color** and **Text highlight color** drop-down color pickers that mirror the Ribbon [Drop-Down Color Picker](windowsribbon-controls-dropdowncolorpicker.md) behavior.</span></span>
-   <span data-ttu-id="24778-147">Поддержка автоматического предварительного просмотра всеми подэлементами управления на основе коллекции шрифтов: **семейство шрифтов**, **Размер шрифта**, **Цвет текста** и **Цвет выделения текста**.</span><span class="sxs-lookup"><span data-stu-id="24778-147">Support of auto-previewing by all Font Control gallery-based sub-controls: **Font family**, **Font size**, **Text color**, and **Text highlight color**.</span></span>

## <a name="alignment-with-common-gdi-text-structures"></a><span data-ttu-id="24778-148">Выравнивание с помощью общих текстовых структур GDI</span><span class="sxs-lookup"><span data-stu-id="24778-148">Alignment with Common GDI Text Structures</span></span>

<span data-ttu-id="24778-149">Компоненты стека текста [Windows интерфейс графических устройств (GDI)](../gdi/windows-gdi.md) используются для предоставления функций выбора шрифта и форматирования с помощью элемента управления шрифта ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-149">[Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text stack components are used to expose font selection and formatting functionality through the Ribbon Font Control.</span></span> <span data-ttu-id="24778-150">Различные функции шрифтов, поддерживаемые [структурой LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [структурой CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)и [структурой CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) , предоставляются через вложенные элементы управления, которые включены в элемент управления Font.</span><span class="sxs-lookup"><span data-stu-id="24778-150">The various font features supported by the [LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a) are exposed through the sub-controls that are included in the Font Control.</span></span>

<span data-ttu-id="24778-151">Подэлементы управления, отображаемые в элементе управления Font, зависят от шаблона *фонттипе* , объявленного в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-151">The sub-controls that are displayed in the Font Control depend on the *FontType* template declared in the Ribbon markup.</span></span> <span data-ttu-id="24778-152">Шаблоны *фонттипе* (подробно рассматриваются в следующем разделе) предназначены для согласования с общими текстовыми структурами [Windows интерфейс графических устройств (GDI)](../gdi/windows-gdi.md) .</span><span class="sxs-lookup"><span data-stu-id="24778-152">The *FontType* templates (discussed in further detail in the following section) are designed to align with the common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) text structures.</span></span>

## <a name="add-a-fontcontrol"></a><span data-ttu-id="24778-153">Добавление Фонтконтрол</span><span class="sxs-lookup"><span data-stu-id="24778-153">Add a FontControl</span></span>

<span data-ttu-id="24778-154">В этом разделе описаны основные шаги по добавлению элемента управления шрифтом в приложение для ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-154">This section outlines the basic steps for adding a Font Control to a Ribbon application.</span></span>

### <a name="declaring-a-fontcontrol-in-markup"></a><span data-ttu-id="24778-155">Объявление Фонтконтрол в разметке</span><span class="sxs-lookup"><span data-stu-id="24778-155">Declaring a FontControl in Markup</span></span>

<span data-ttu-id="24778-156">Как и другие элементы управления Ribbon, элемент управления "Шрифт" объявляется в разметке с помощью элемента [**фонтконтрол**](windowsribbon-element-fontcontrol.md) и связывается с объявлением команды с помощью идентификатора команды.</span><span class="sxs-lookup"><span data-stu-id="24778-156">Like other Ribbon controls, the Font Control is declared in markup with a [**FontControl**](windowsribbon-element-fontcontrol.md) element and associated with a Command declaration through a Command ID.</span></span> <span data-ttu-id="24778-157">При компиляции приложения идентификатор команды используется для привязки команды к обработчику команд в ведущем приложении.</span><span class="sxs-lookup"><span data-stu-id="24778-157">When the application is compiled, the Command ID is used to bind the Command to a Command handler in the host application.</span></span>

> [!Note]  
> <span data-ttu-id="24778-158">Если идентификатор команды не объявлен с [**фонтконтрол**](windowsribbon-element-fontcontrol.md) в разметке, то он создается платформой.</span><span class="sxs-lookup"><span data-stu-id="24778-158">If no Command ID is declared with the [**FontControl**](windowsribbon-element-fontcontrol.md) in markup, then one is generated by the framework.</span></span>

 

<span data-ttu-id="24778-159">Поскольку подэлементы управления шрифтами не предоставляются напрямую, Настройка элемента управления шрифта ограничена тремя шаблонами макета *фонттипе* , определенными платформой.</span><span class="sxs-lookup"><span data-stu-id="24778-159">Because the sub-controls of the Font Control are not exposed directly, customization of the Font Control is limited to three *FontType* layout templates defined by the framework.</span></span>

<span data-ttu-id="24778-160">Дальнейшая настройка элемента управления шрифтом может быть выполнена путем объединения шаблона макета с атрибутами [**фонтконтрол**](windowsribbon-element-fontcontrol.md) , такими как *ишигхлигхтбуттонвисибле*, *исстрикесраугхбуттонвисибле* и *исундерлинебуттонвисибле*.</span><span class="sxs-lookup"><span data-stu-id="24778-160">Further customization of the Font Control can be accomplished by combining the layout template with [**FontControl**](windowsribbon-element-fontcontrol.md) attributes such as *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible*, and *IsUnderlineButtonVisible*.</span></span>

> [!Note]  
> <span data-ttu-id="24778-161">Функции шрифта, не предоставляемые стандартными шаблонами и атрибутами элементов управления шрифтом, требуют реализации пользовательского элемента управления шрифтом, который выходит за рамки этой статьи.</span><span class="sxs-lookup"><span data-stu-id="24778-161">Font functionality beyond that exposed by the standard Font Control templates and attributes requires a custom font control implementation that is outside the scope of this article.</span></span>

 

<span data-ttu-id="24778-162">В следующей таблице перечислены шаблоны элементов управления шрифтом и тип элемента управления Edit, с которым будет согласовываться каждый шаблон.</span><span class="sxs-lookup"><span data-stu-id="24778-162">The following table lists the Font Control templates and the edit control type that each template is aligned with.</span></span>



| <span data-ttu-id="24778-163">Шаблон</span><span class="sxs-lookup"><span data-stu-id="24778-163">Template</span></span>      | <span data-ttu-id="24778-164">Поддерживает</span><span class="sxs-lookup"><span data-stu-id="24778-164">Supports</span></span>                                                                 |
|---------------|--------------------------------------------------------------------------|
| <span data-ttu-id="24778-165">фонтонли</span><span class="sxs-lookup"><span data-stu-id="24778-165">FontOnly</span></span>      | [<span data-ttu-id="24778-166">Структура LOGFONT</span><span class="sxs-lookup"><span data-stu-id="24778-166">LOGFONT Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| <span data-ttu-id="24778-167">фонтвисколор</span><span class="sxs-lookup"><span data-stu-id="24778-167">FontWithColor</span></span> | [<span data-ttu-id="24778-168">Структура CHOOSEFONT</span><span class="sxs-lookup"><span data-stu-id="24778-168">CHOOSEFONT Structure</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| <span data-ttu-id="24778-169">ричфонт</span><span class="sxs-lookup"><span data-stu-id="24778-169">RichFont</span></span>      | [<span data-ttu-id="24778-170">Структура CHARFORMAT2</span><span class="sxs-lookup"><span data-stu-id="24778-170">CHARFORMAT2 Structure</span></span>](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

<span data-ttu-id="24778-171">В следующей таблице перечислены элементы управления, связанные с каждым шаблоном, и указаны элементы управления, которые являются необязательными для связанного шаблона.</span><span class="sxs-lookup"><span data-stu-id="24778-171">The following table lists the controls that are associated with each template and identifies the controls that are optional for an associated template.</span></span>



<span data-ttu-id="24778-172">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="24778-172">Controls</span></span>

<span data-ttu-id="24778-173">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="24778-173">Templates</span></span>

<span data-ttu-id="24778-174">**ричфонт**</span><span class="sxs-lookup"><span data-stu-id="24778-174">**RichFont**</span></span>

<span data-ttu-id="24778-175">**фонтвисколор**</span><span class="sxs-lookup"><span data-stu-id="24778-175">**FontWithColor**</span></span>

<span data-ttu-id="24778-176">**фонтонли**</span><span class="sxs-lookup"><span data-stu-id="24778-176">**FontOnly**</span></span>

<span data-ttu-id="24778-177">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="24778-177">Default</span></span>

<span data-ttu-id="24778-178">Необязательно</span><span class="sxs-lookup"><span data-stu-id="24778-178">Optional</span></span>

<span data-ttu-id="24778-179">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="24778-179">Default</span></span>

<span data-ttu-id="24778-180">Необязательно</span><span class="sxs-lookup"><span data-stu-id="24778-180">Optional</span></span>

<span data-ttu-id="24778-181">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="24778-181">Default</span></span>

<span data-ttu-id="24778-182">Необязательно</span><span class="sxs-lookup"><span data-stu-id="24778-182">Optional</span></span>

<span data-ttu-id="24778-183">Поле со списком " **Размер шрифта** "</span><span class="sxs-lookup"><span data-stu-id="24778-183">**Font size** combo box</span></span>

<span data-ttu-id="24778-184">Да</span><span class="sxs-lookup"><span data-stu-id="24778-184">Yes</span></span>

<span data-ttu-id="24778-185">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-185">No</span></span>

<span data-ttu-id="24778-186">Да</span><span class="sxs-lookup"><span data-stu-id="24778-186">Yes</span></span>

<span data-ttu-id="24778-187">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-187">No</span></span>

<span data-ttu-id="24778-188">Да</span><span class="sxs-lookup"><span data-stu-id="24778-188">Yes</span></span>

<span data-ttu-id="24778-189">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-189">No</span></span>

<span data-ttu-id="24778-190">Поле со списком для **семейства шрифтов**</span><span class="sxs-lookup"><span data-stu-id="24778-190">**Font family** combo box</span></span>

<span data-ttu-id="24778-191">Да</span><span class="sxs-lookup"><span data-stu-id="24778-191">Yes</span></span>

<span data-ttu-id="24778-192">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-192">No</span></span>

<span data-ttu-id="24778-193">Да</span><span class="sxs-lookup"><span data-stu-id="24778-193">Yes</span></span>

<span data-ttu-id="24778-194">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-194">No</span></span>

<span data-ttu-id="24778-195">Да</span><span class="sxs-lookup"><span data-stu-id="24778-195">Yes</span></span>

<span data-ttu-id="24778-196">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-196">No</span></span>

<span data-ttu-id="24778-197">Кнопка " **увеличить шрифт** "</span><span class="sxs-lookup"><span data-stu-id="24778-197">**Grow font** button</span></span>

<span data-ttu-id="24778-198">Да</span><span class="sxs-lookup"><span data-stu-id="24778-198">Yes</span></span>

<span data-ttu-id="24778-199">Да</span><span class="sxs-lookup"><span data-stu-id="24778-199">Yes</span></span>

<span data-ttu-id="24778-200">Да</span><span class="sxs-lookup"><span data-stu-id="24778-200">Yes</span></span>

<span data-ttu-id="24778-201">Да</span><span class="sxs-lookup"><span data-stu-id="24778-201">Yes</span></span>

\-

\-

<span data-ttu-id="24778-202">Кнопка " **Сжать шрифт** "</span><span class="sxs-lookup"><span data-stu-id="24778-202">**Shrink font** button</span></span>

<span data-ttu-id="24778-203">Да</span><span class="sxs-lookup"><span data-stu-id="24778-203">Yes</span></span>

<span data-ttu-id="24778-204">Да</span><span class="sxs-lookup"><span data-stu-id="24778-204">Yes</span></span>

<span data-ttu-id="24778-205">Да</span><span class="sxs-lookup"><span data-stu-id="24778-205">Yes</span></span>

<span data-ttu-id="24778-206">Да</span><span class="sxs-lookup"><span data-stu-id="24778-206">Yes</span></span>

\-

\-

<span data-ttu-id="24778-207">Кнопка **полужирного шрифта**</span><span class="sxs-lookup"><span data-stu-id="24778-207">**Bold** button</span></span>

<span data-ttu-id="24778-208">Да</span><span class="sxs-lookup"><span data-stu-id="24778-208">Yes</span></span>

<span data-ttu-id="24778-209">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-209">No</span></span>

<span data-ttu-id="24778-210">Да</span><span class="sxs-lookup"><span data-stu-id="24778-210">Yes</span></span>

<span data-ttu-id="24778-211">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-211">No</span></span>

<span data-ttu-id="24778-212">Да</span><span class="sxs-lookup"><span data-stu-id="24778-212">Yes</span></span>

<span data-ttu-id="24778-213">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-213">No</span></span>

<span data-ttu-id="24778-214">Кнопка с **курсивом**</span><span class="sxs-lookup"><span data-stu-id="24778-214">**Italic** button</span></span>

<span data-ttu-id="24778-215">Да</span><span class="sxs-lookup"><span data-stu-id="24778-215">Yes</span></span>

<span data-ttu-id="24778-216">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-216">No</span></span>

<span data-ttu-id="24778-217">Да</span><span class="sxs-lookup"><span data-stu-id="24778-217">Yes</span></span>

<span data-ttu-id="24778-218">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-218">No</span></span>

<span data-ttu-id="24778-219">Да</span><span class="sxs-lookup"><span data-stu-id="24778-219">Yes</span></span>

<span data-ttu-id="24778-220">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-220">No</span></span>

<span data-ttu-id="24778-221">Кнопка **подчеркивания**</span><span class="sxs-lookup"><span data-stu-id="24778-221">**Underline** button</span></span>

<span data-ttu-id="24778-222">Да</span><span class="sxs-lookup"><span data-stu-id="24778-222">Yes</span></span>

<span data-ttu-id="24778-223">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-223">No</span></span>

<span data-ttu-id="24778-224">Да</span><span class="sxs-lookup"><span data-stu-id="24778-224">Yes</span></span>

<span data-ttu-id="24778-225">Да</span><span class="sxs-lookup"><span data-stu-id="24778-225">Yes</span></span>

<span data-ttu-id="24778-226">Да</span><span class="sxs-lookup"><span data-stu-id="24778-226">Yes</span></span>

<span data-ttu-id="24778-227">Да</span><span class="sxs-lookup"><span data-stu-id="24778-227">Yes</span></span>

<span data-ttu-id="24778-228">Кнопка **перечеркивания**</span><span class="sxs-lookup"><span data-stu-id="24778-228">**Strikethrough** button</span></span>

<span data-ttu-id="24778-229">Да</span><span class="sxs-lookup"><span data-stu-id="24778-229">Yes</span></span>

<span data-ttu-id="24778-230">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-230">No</span></span>

<span data-ttu-id="24778-231">Да</span><span class="sxs-lookup"><span data-stu-id="24778-231">Yes</span></span>

<span data-ttu-id="24778-232">Да</span><span class="sxs-lookup"><span data-stu-id="24778-232">Yes</span></span>

<span data-ttu-id="24778-233">Да</span><span class="sxs-lookup"><span data-stu-id="24778-233">Yes</span></span>

<span data-ttu-id="24778-234">Да</span><span class="sxs-lookup"><span data-stu-id="24778-234">Yes</span></span>

<span data-ttu-id="24778-235">Кнопка **подстрочного сценария**</span><span class="sxs-lookup"><span data-stu-id="24778-235">**Subscript** button</span></span>

<span data-ttu-id="24778-236">Да</span><span class="sxs-lookup"><span data-stu-id="24778-236">Yes</span></span>

<span data-ttu-id="24778-237">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-237">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="24778-238">Кнопка **надстрочного скрипта**</span><span class="sxs-lookup"><span data-stu-id="24778-238">**Superscript** button</span></span>

<span data-ttu-id="24778-239">Да</span><span class="sxs-lookup"><span data-stu-id="24778-239">Yes</span></span>

<span data-ttu-id="24778-240">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-240">No</span></span>

\-

\-

\-

\-

<span data-ttu-id="24778-241">Кнопка **цвета выделения текста**</span><span class="sxs-lookup"><span data-stu-id="24778-241">**Text highlight color** button</span></span>

<span data-ttu-id="24778-242">Да</span><span class="sxs-lookup"><span data-stu-id="24778-242">Yes</span></span>

<span data-ttu-id="24778-243">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-243">No</span></span>

<span data-ttu-id="24778-244">Да</span><span class="sxs-lookup"><span data-stu-id="24778-244">Yes</span></span>

<span data-ttu-id="24778-245">Да</span><span class="sxs-lookup"><span data-stu-id="24778-245">Yes</span></span>

\-

\-

<span data-ttu-id="24778-246">Кнопка **цвета текста**</span><span class="sxs-lookup"><span data-stu-id="24778-246">**Text color** button</span></span>

<span data-ttu-id="24778-247">Да</span><span class="sxs-lookup"><span data-stu-id="24778-247">Yes</span></span>

<span data-ttu-id="24778-248">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-248">No</span></span>

<span data-ttu-id="24778-249">Да</span><span class="sxs-lookup"><span data-stu-id="24778-249">Yes</span></span>

<span data-ttu-id="24778-250">Нет</span><span class="sxs-lookup"><span data-stu-id="24778-250">No</span></span>

\-

\-



 

<span data-ttu-id="24778-251">При объявлении поведения макета элемента управления Font платформа Ribbon предоставляет необязательный шаблон макета *сизедефинитион* , `OneFontControl` который определяет две конфигурации подэлементов управления на основе размера ленты и места, доступного для элемента управления Font.</span><span class="sxs-lookup"><span data-stu-id="24778-251">When the layout behavior of a Font Control is declared, the Ribbon framework provides an optional *SizeDefinition* layout template, `OneFontControl`, that defines two sub-control configurations based on the size of the Ribbon and the space available for the Font Control.</span></span> <span data-ttu-id="24778-252">Дополнительные сведения см. в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="24778-252">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

### <a name="adding-a-fontcontrol-to-a-ribbon"></a><span data-ttu-id="24778-253">Добавление Фонтконтрол на ленту</span><span class="sxs-lookup"><span data-stu-id="24778-253">Adding a FontControl to a Ribbon</span></span>

<span data-ttu-id="24778-254">В следующих примерах кода демонстрируются основные требования к разметке для добавления элемента управления Font на ленту.</span><span class="sxs-lookup"><span data-stu-id="24778-254">The following code examples demonstrate the basic markup requirements for adding a Font Control to a Ribbon:</span></span>

<span data-ttu-id="24778-255">В этом разделе кода показана разметка объявления команды [**фонтконтрол**](windowsribbon-element-fontcontrol.md) , включая команды [**Tab**](windowsribbon-element-tab.md) и [**Group**](windowsribbon-element-group.md) , необходимые для отображения элемента управления на [**ленте**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="24778-255">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup, including the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) Commands that are required for displaying a control in the [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="24778-256">В этом разделе кода показана разметка, необходимая для объявления и связывания [**фонтконтрол**](windowsribbon-element-fontcontrol.md) с [**командой**](windowsribbon-element-command.md) с помощью идентификатора команды.</span><span class="sxs-lookup"><span data-stu-id="24778-256">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a [**Command**](windowsribbon-element-command.md) through a Command ID.</span></span> <span data-ttu-id="24778-257">В этом конкретном примере содержатся объявления [**вкладок**](windowsribbon-element-tab.md) и [**групп**](windowsribbon-element-group.md) с параметрами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="24778-257">This particular example includes the [**Tab**](windowsribbon-element-tab.md) and [**Group**](windowsribbon-element-group.md) declarations, with scaling preferences.</span></span>


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a><span data-ttu-id="24778-258">Добавление Фонтконтрол в Контекстпопуп</span><span class="sxs-lookup"><span data-stu-id="24778-258">Adding a FontControl to a ContextPopup</span></span>

<span data-ttu-id="24778-259">Для добавления элемента управления шрифтом в [всплывающее контекстное меню](windowsribbon-controls-contextpopup.md) требуется процедура, аналогичная процедуре добавления элемента управления шрифта на ленту.</span><span class="sxs-lookup"><span data-stu-id="24778-259">Adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md) requires a procedure similar to that of adding a Font Control to the Ribbon.</span></span> <span data-ttu-id="24778-260">Однако элемент управления шрифта в [**минитулбар**](windowsribbon-element-minitoolbar.md) ограничен набором элементов управления по умолчанию, которые являются общими для всех шаблонов элементов управления шрифтом: **семейство шрифтов**, **Размер шрифта**, **полужирный** и **курсив**.</span><span class="sxs-lookup"><span data-stu-id="24778-260">However, a Font Control in a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) is restricted to the set of default sub-controls that are common to all Font Control templates: **Font family**, **Font size**, **Bold**, and **Italic**.</span></span>

<span data-ttu-id="24778-261">В следующих примерах кода демонстрируются основные требования к разметке для добавления элемента управления шрифтом в [всплывающее контекстное меню](windowsribbon-controls-contextpopup.md):</span><span class="sxs-lookup"><span data-stu-id="24778-261">The following code examples demonstrate the basic markup requirements for adding a Font Control to a [Context Popup](windowsribbon-controls-contextpopup.md):</span></span>

<span data-ttu-id="24778-262">В этом разделе кода показана разметка объявления команды [**фонтконтрол**](windowsribbon-element-fontcontrol.md) , необходимая для отображения **фонтконтрол** в [**контекстпопуп**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="24778-262">This section of code shows the [**FontControl**](windowsribbon-element-fontcontrol.md) Command declaration markup that is required for displaying a **FontControl** in the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



<span data-ttu-id="24778-263">В этом разделе кода показана разметка, необходимая для объявления и связывания [**фонтконтрол**](windowsribbon-element-fontcontrol.md) с командой с помощью идентификатора команды.</span><span class="sxs-lookup"><span data-stu-id="24778-263">This section of code shows the markup required to declare and associate a [**FontControl**](windowsribbon-element-fontcontrol.md) with a Command through a Command ID.</span></span>


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a><span data-ttu-id="24778-264">Подсказки клавиш</span><span class="sxs-lookup"><span data-stu-id="24778-264">Keytips</span></span>

<span data-ttu-id="24778-265">Каждый подэлемент управления в элементе управления шрифтом ленты доступен через сочетание клавиш или keytip.</span><span class="sxs-lookup"><span data-stu-id="24778-265">Each sub-control in the Ribbon Font Control is accessible through a keyboard shortcut, or keytip.</span></span> <span data-ttu-id="24778-266">Этот KeyTip является стандартным и назначается для каждого подэлементного управления платформой.</span><span class="sxs-lookup"><span data-stu-id="24778-266">This keytip is predefined and assigned to each sub-control by the framework.</span></span>

<span data-ttu-id="24778-267">Если значение атрибута *KeyTip* присвоено элементу [**фонтконтрол**](windowsribbon-element-fontcontrol.md) в разметке, это значение добавляется в качестве префикса в определяемую платформой keytip.</span><span class="sxs-lookup"><span data-stu-id="24778-267">If a *Keytip* attribute value is assigned to the [**FontControl**](windowsribbon-element-fontcontrol.md) element in markup, this value is added as a prefix to the framework-defined keytip.</span></span>

> [!Note]  
> <span data-ttu-id="24778-268">Для этого префикса приложение должно применять правило с одним символом.</span><span class="sxs-lookup"><span data-stu-id="24778-268">The application should enforce a single-character rule for this prefix.</span></span>

 

<span data-ttu-id="24778-269">В следующей таблице перечислены ключевые подсказки, определенные платформой.</span><span class="sxs-lookup"><span data-stu-id="24778-269">The following table lists the keytips defined by the framework.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="24778-270">Дополнительный элемент управления</span><span class="sxs-lookup"><span data-stu-id="24778-270">Sub-control</span></span></th>
<th><span data-ttu-id="24778-271">Keytip</span><span class="sxs-lookup"><span data-stu-id="24778-271">Keytip</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="24778-272">Семейство шрифтов</span><span class="sxs-lookup"><span data-stu-id="24778-272">Font family</span></span></td>
<td><span data-ttu-id="24778-273">C</span><span class="sxs-lookup"><span data-stu-id="24778-273">F</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24778-274">Стиль шрифта</span><span class="sxs-lookup"><span data-stu-id="24778-274">Font style</span></span></td>
<td><span data-ttu-id="24778-275">T</span><span class="sxs-lookup"><span data-stu-id="24778-275">T</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24778-276">Размер шрифта</span><span class="sxs-lookup"><span data-stu-id="24778-276">Font size</span></span></td>
<td><span data-ttu-id="24778-277">S</span><span class="sxs-lookup"><span data-stu-id="24778-277">S</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24778-278">Увеличить шрифт</span><span class="sxs-lookup"><span data-stu-id="24778-278">Grow font</span></span></td>
<td><span data-ttu-id="24778-279">G</span><span class="sxs-lookup"><span data-stu-id="24778-279">G</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24778-280">Сжать шрифт</span><span class="sxs-lookup"><span data-stu-id="24778-280">Shrink font</span></span></td>
<td><span data-ttu-id="24778-281">K</span><span class="sxs-lookup"><span data-stu-id="24778-281">K</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24778-282">Жирный</span><span class="sxs-lookup"><span data-stu-id="24778-282">Bold</span></span></td>
<td><span data-ttu-id="24778-283">B</span><span class="sxs-lookup"><span data-stu-id="24778-283">B</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24778-284">Курсив</span><span class="sxs-lookup"><span data-stu-id="24778-284">Italic</span></span></td>
<td><span data-ttu-id="24778-285">I</span><span class="sxs-lookup"><span data-stu-id="24778-285">I</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24778-286">Underline</span><span class="sxs-lookup"><span data-stu-id="24778-286">Underline</span></span></td>
<td><span data-ttu-id="24778-287">U</span><span class="sxs-lookup"><span data-stu-id="24778-287">U</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24778-288">Зачеркнутый</span><span class="sxs-lookup"><span data-stu-id="24778-288">Strikethrough</span></span></td>
<td><span data-ttu-id="24778-289">X</span><span class="sxs-lookup"><span data-stu-id="24778-289">X</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24778-290">Надстрочный</span><span class="sxs-lookup"><span data-stu-id="24778-290">Superscript</span></span></td>
<td><span data-ttu-id="24778-291">Y или Z</span><span class="sxs-lookup"><span data-stu-id="24778-291">Y or Z</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="24778-292">Если атрибут <em>KeyTip</em> не объявлен в разметке, keytip по умолчанию имеет значение Y; в противном случае KeyTip по умолчанию — <em>KeyTip</em> + Z.</span><span class="sxs-lookup"><span data-stu-id="24778-292">If the <em>Keytip</em> attribute is not declared in markup, the default keytip is Y; otherwise, the default keytip is <em>Keytip</em> + Z.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24778-293">Подстрочный</span><span class="sxs-lookup"><span data-stu-id="24778-293">Subscript</span></span></td>
<td><span data-ttu-id="24778-294">Объект</span><span class="sxs-lookup"><span data-stu-id="24778-294">A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="24778-295">Цвет шрифта</span><span class="sxs-lookup"><span data-stu-id="24778-295">Font color</span></span></td>
<td><span data-ttu-id="24778-296">C</span><span class="sxs-lookup"><span data-stu-id="24778-296">C</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="24778-297">Выделение шрифта</span><span class="sxs-lookup"><span data-stu-id="24778-297">Font highlight</span></span></td>
<td><span data-ttu-id="24778-298">H</span><span class="sxs-lookup"><span data-stu-id="24778-298">H</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="24778-299">Рекомендуемый префикс для ленты EN-US многоязыкового интерфейса пользователя — "F", как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="24778-299">The recommended prefix for a Multilingual User Interface (MUI) EN-US Ribbon is 'F', as shown in the following example.</span></span>


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



<span data-ttu-id="24778-300">На следующем снимке экрана показаны ключевые подсказки элемента управления шрифтом, определенные в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="24778-300">The following screen shot illustrates the Font Control keytips as they are defined in the previous example.</span></span>

![снимок экрана: ключевые подсказки фонтконтрол в WordPad для Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a><span data-ttu-id="24778-302">Файл ресурсов ленты</span><span class="sxs-lookup"><span data-stu-id="24778-302">The Ribbon Resource File</span></span>

<span data-ttu-id="24778-303">При компиляции файла разметки создается файл ресурсов, содержащий все ссылки на ресурсы для приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="24778-303">When the markup file is compiled, a resource file that contains all resource references for the Ribbon application is generated.</span></span>

<span data-ttu-id="24778-304">Пример простого файла ресурсов:</span><span class="sxs-lookup"><span data-stu-id="24778-304">Example of a simple resource file:</span></span>


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a><span data-ttu-id="24778-305">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="24778-305">Font Control Properties</span></span>

<span data-ttu-id="24778-306">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления Font и его составляющих вложенных элементов управления.</span><span class="sxs-lookup"><span data-stu-id="24778-306">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Font Control and its constituent sub-controls.</span></span>

<span data-ttu-id="24778-307">Как правило, свойство элемента управления шрифтом обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="24778-307">Typically, a Font Control property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="24778-308">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="24778-308">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="24778-309">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="24778-309">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="24778-310">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="24778-310">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="24778-311">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="24778-311">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="24778-312">В следующей таблице перечислены ключи свойств, связанные с элементом управления "Шрифт".</span><span class="sxs-lookup"><span data-stu-id="24778-312">The following table lists the property keys that are associated with the Font Control.</span></span>



| <span data-ttu-id="24778-313">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="24778-313">Property Key</span></span>                                                                                                                  | <span data-ttu-id="24778-314">Примечания</span><span class="sxs-lookup"><span data-stu-id="24778-314">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24778-315">UI \_ PKEY \_ фонтпропертиес</span><span class="sxs-lookup"><span data-stu-id="24778-315">UI\_PKEY\_FontProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | <span data-ttu-id="24778-316">Представляется в статистическом выражении как объект [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) , все свойства подсвойства элемента управления Font.</span><span class="sxs-lookup"><span data-stu-id="24778-316">Exposes, in aggregate as an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) object, all Font Control sub-control properties.</span></span><br/> <span data-ttu-id="24778-317">Платформа запрашивает это свойство, когда `UI_INVALIDATIONS_VALUE` аргумент передается как значение *флагов* в вызове метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="24778-317">The framework queries this property when `UI_INVALIDATIONS_VALUE` is passed as the value of *flags* in the call to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span><br/> |
| [<span data-ttu-id="24778-318">UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес</span><span class="sxs-lookup"><span data-stu-id="24778-318">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | <span data-ttu-id="24778-319">Предоставляет в статистическом выражении в виде объекта [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) только те свойства элемента управления шрифта, которые были изменены.</span><span class="sxs-lookup"><span data-stu-id="24778-319">Exposes, in aggregate as an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object, only Font Control sub-control properties that have changed.</span></span><br/>                                                                                                                                                                                                        |
| [<span data-ttu-id="24778-320">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="24778-320">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | <span data-ttu-id="24778-321">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="24778-321">Can only be updated through invalidation.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="24778-322">Пользовательский интерфейс \_ PKEY \_ включен</span><span class="sxs-lookup"><span data-stu-id="24778-322">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | <span data-ttu-id="24778-323">Поддерживает [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="24778-323">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span>                                                                                                                                                                  |



 

<span data-ttu-id="24778-324">В дополнение к свойствам, поддерживаемым самим элементом управления шрифтом, платформа Ribbon также определяет [ключ свойства](windowsribbon-reference-properties.md) для каждого подэлементного элемента управления шрифта.</span><span class="sxs-lookup"><span data-stu-id="24778-324">In addition to the properties supported by the Font Control itself, the Ribbon framework also defines a [property key](windowsribbon-reference-properties.md) for each Font Control sub-control.</span></span> <span data-ttu-id="24778-325">Эти ключи свойств и их значения предоставляются платформой с помощью реализации интерфейса [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) , определяющей методы управления коллекцией, также называемые контейнером свойств, в парах имени и значения.</span><span class="sxs-lookup"><span data-stu-id="24778-325">These property keys and their values are exposed by the framework through an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface implementation that defines the methods for managing a collection, also called a property bag, of name and value pairs.</span></span>

<span data-ttu-id="24778-326">Приложение преобразует структуры шрифтов в свойства, доступные через методы интерфейса [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="24778-326">The application translates the font structures to properties that are accessible through the [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface methods.</span></span> <span data-ttu-id="24778-327">Эта модель подчеркивает различие между элементом управления шрифта и компонентами текстового стека Windows интерфейс графических устройств (GDI) ([Структура LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [Структура CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)и [Структура CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)), которые поддерживаются платформой.</span><span class="sxs-lookup"><span data-stu-id="24778-327">This model emphasizes the distinction between the Font Control and the Windows Graphics Device Interface (GDI) text stack components ([LOGFONT Structure](/windows/win32/api/wingdi/ns-wingdi-logfonta), [CHOOSEFONT Structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta), and [CHARFORMAT2 Structure](/windows/win32/api/richedit/ns-richedit-charformat2a)) that are supported by the framework.</span></span>

<span data-ttu-id="24778-328">В следующей таблице перечислены отдельные элементы управления и связанные с ними ключи свойств.</span><span class="sxs-lookup"><span data-stu-id="24778-328">The following table lists the individual controls and their associated property keys.</span></span>



| <span data-ttu-id="24778-329">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="24778-329">Controls</span></span>                 | <span data-ttu-id="24778-330">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="24778-330">Property Key</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="24778-331">Примечания</span><span class="sxs-lookup"><span data-stu-id="24778-331">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24778-332">**Размер шрифта**</span><span class="sxs-lookup"><span data-stu-id="24778-332">**Font size**</span></span>            | [<span data-ttu-id="24778-333">\_ \_ Размер фонтпропертиес пользовательского интерфейса PKEY \_</span><span class="sxs-lookup"><span data-stu-id="24778-333">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="24778-334">Если выделенный размер текста хетероженеаусли выделяется, платформа Ribbon устанавливает пустой элемент управления **размером шрифта** , а значение [UI \_ PKEY \_ фонтпропертиес \_ size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) — 0.</span><span class="sxs-lookup"><span data-stu-id="24778-334">When a run of heterogeneously sized text is highlighted, the Ribbon framework sets the **Font size** control to blank and the value of [UI\_PKEY\_FontProperties\_Size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) to 0.</span></span> <span data-ttu-id="24778-335">При нажатии кнопки **увеличить шрифт** или **Сжать шрифт** размер выделенного текста изменяется, но относительная разница в размерах текста сохраняется.</span><span class="sxs-lookup"><span data-stu-id="24778-335">When the **Grow font** or **Shrink font** button is clicked, all highlighted text is resized but the relative difference in text sizes is preserved.</span></span>                                                                                                                                                    |
| <span data-ttu-id="24778-336">**Семейство шрифтов**</span><span class="sxs-lookup"><span data-stu-id="24778-336">**Font family**</span></span>          | [<span data-ttu-id="24778-337">\_Семейство UI PKEY \_ фонтпропертиес \_</span><span class="sxs-lookup"><span data-stu-id="24778-337">UI\_PKEY\_FontProperties\_Family</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | <span data-ttu-id="24778-338">Имена семейств шрифтов GDI зависят от национальной настройки системы.</span><span class="sxs-lookup"><span data-stu-id="24778-338">GDI font family names vary with system locale.</span></span> <span data-ttu-id="24778-339">Таким образом, если значение [ \_ \_ \_ семейства UI PKEY фонтпропертиес](windowsribbon-reference-properties-uipkey-fontproperties-family.md) сохраняется в сеансах приложения, это значение должно быть получено в каждом новом сеансе.</span><span class="sxs-lookup"><span data-stu-id="24778-339">As such, if the value of [UI\_PKEY\_FontProperties\_Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) is preserved across application sessions, that value should be retrieved on each new session.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="24778-340">**Увеличить шрифт**</span><span class="sxs-lookup"><span data-stu-id="24778-340">**Grow font**</span></span>            | [<span data-ttu-id="24778-341">\_ \_ Размер фонтпропертиес пользовательского интерфейса PKEY \_</span><span class="sxs-lookup"><span data-stu-id="24778-341">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="24778-342">См. **Размер шрифта**.</span><span class="sxs-lookup"><span data-stu-id="24778-342">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="24778-343">**Сжать шрифт**</span><span class="sxs-lookup"><span data-stu-id="24778-343">**Shrink font**</span></span>          | [<span data-ttu-id="24778-344">\_ \_ Размер фонтпропертиес пользовательского интерфейса PKEY \_</span><span class="sxs-lookup"><span data-stu-id="24778-344">UI\_PKEY\_FontProperties\_Size</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | <span data-ttu-id="24778-345">См. **Размер шрифта**.</span><span class="sxs-lookup"><span data-stu-id="24778-345">See **Font size**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="24778-346">**Полужирный**</span><span class="sxs-lookup"><span data-stu-id="24778-346">**Bold**</span></span>                 | [<span data-ttu-id="24778-347">Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Bold</span><span class="sxs-lookup"><span data-stu-id="24778-347">UI\_PKEY\_FontProperties\_Bold</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="24778-348">**Наклонный**</span><span class="sxs-lookup"><span data-stu-id="24778-348">**Italic**</span></span>               | [<span data-ttu-id="24778-349">Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ курсивом</span><span class="sxs-lookup"><span data-stu-id="24778-349">UI\_PKEY\_FontProperties\_Italic</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="24778-350">**Начертан**</span><span class="sxs-lookup"><span data-stu-id="24778-350">**Underline**</span></span>            | [<span data-ttu-id="24778-351">Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_</span><span class="sxs-lookup"><span data-stu-id="24778-351">UI\_PKEY\_FontProperties\_Underline</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="24778-352">**Зачеркнутый**</span><span class="sxs-lookup"><span data-stu-id="24778-352">**Strikethrough**</span></span>        | [<span data-ttu-id="24778-353">Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Зачеркнутый</span><span class="sxs-lookup"><span data-stu-id="24778-353">UI\_PKEY\_FontProperties\_Strikethrough</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="24778-354">**Индекс**</span><span class="sxs-lookup"><span data-stu-id="24778-354">**Subscript**</span></span>            | [<span data-ttu-id="24778-355">UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг</span><span class="sxs-lookup"><span data-stu-id="24778-355">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="24778-356">Если задана кнопка « **индекс** », то **Надстрочный индекс** также не может быть установлен.</span><span class="sxs-lookup"><span data-stu-id="24778-356">If the **Subscript** button is set, then the **Superscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="24778-357">**Надстрочный**</span><span class="sxs-lookup"><span data-stu-id="24778-357">**Superscript**</span></span>          | [<span data-ttu-id="24778-358">UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг</span><span class="sxs-lookup"><span data-stu-id="24778-358">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | <span data-ttu-id="24778-359">Если задана кнопка **надстрочного скрипта** , то этот **индекс** также не может быть установлен.</span><span class="sxs-lookup"><span data-stu-id="24778-359">If the **Superscript** button is set, then the **Subscript** cannot also be set.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="24778-360">**Цвет выделения текста**</span><span class="sxs-lookup"><span data-stu-id="24778-360">**Text highlight color**</span></span> | <span data-ttu-id="24778-361">[Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="24778-361">[UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI\_PKEY\_FontProperties\_BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md)</span></span> | <span data-ttu-id="24778-362">Предоставляет те же функциональные возможности, что и `HighlightColors` шаблон элемента [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="24778-362">Provides the same functionality as the `HighlightColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="24778-363">Мы настоятельно рекомендуем, чтобы приложение было установлено только первоначальное значение **цвета выделения текста** .</span><span class="sxs-lookup"><span data-stu-id="24778-363">We highly recommend that only an initial **Text highlight color** value be set by the application.</span></span> <span data-ttu-id="24778-364">Последнее выбранное значение должно быть сохранено и не задаваться при перемещении курсора в пределах документа.</span><span class="sxs-lookup"><span data-stu-id="24778-364">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="24778-365">Это обеспечивает быстрый доступ к последнему выделенному пользователю, и средство выбора цвета не нужно открывать повторно.</span><span class="sxs-lookup"><span data-stu-id="24778-365">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="24778-366">Образцы цветов не могут быть настроены.</span><span class="sxs-lookup"><span data-stu-id="24778-366">Color swatches cannot be customized.</span></span><br/> |
| <span data-ttu-id="24778-367">**Цвет текста**</span><span class="sxs-lookup"><span data-stu-id="24778-367">**Text color**</span></span>           | <span data-ttu-id="24778-368">[Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span><span class="sxs-lookup"><span data-stu-id="24778-368">[UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI\_PKEY\_FontProperties\_ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)</span></span>           | <span data-ttu-id="24778-369">Предоставляет те же функциональные возможности, что и `StandardColors` шаблон элемента [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) .</span><span class="sxs-lookup"><span data-stu-id="24778-369">Provides the same functionality as the `StandardColors` template of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) element.</span></span><br/> <span data-ttu-id="24778-370">Мы настоятельно рекомендуем установить только исходное значение **цвета текста** , установленное приложением.</span><span class="sxs-lookup"><span data-stu-id="24778-370">We highly recommend that only an initial **Text color** value be set by the application.</span></span> <span data-ttu-id="24778-371">Последнее выбранное значение должно быть сохранено и не задаваться при перемещении курсора в пределах документа.</span><span class="sxs-lookup"><span data-stu-id="24778-371">The last selected value should be preserved and not set when the cursor is repositioned within a document.</span></span> <span data-ttu-id="24778-372">Это обеспечивает быстрый доступ к последнему выделенному пользователю, и средство выбора цвета не нужно открывать повторно.</span><span class="sxs-lookup"><span data-stu-id="24778-372">This allows quick access to the user's last selection, and the color picker does not have to be reopened.</span></span><br/> <span data-ttu-id="24778-373">Образцы цветов не могут быть настроены.</span><span class="sxs-lookup"><span data-stu-id="24778-373">Color swatches cannot be customized.</span></span><br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a><span data-ttu-id="24778-374">Определение обработчика команд Фонтконтрол</span><span class="sxs-lookup"><span data-stu-id="24778-374">Define a FontControl Command Handler</span></span>

<span data-ttu-id="24778-375">В этом разделе описаны шаги, необходимые для привязки элемента управления "Шрифт" к обработчику команд.</span><span class="sxs-lookup"><span data-stu-id="24778-375">This section describes the steps required to bind a Font Control to a Command handler.</span></span>

> [!WARNING]
> <span data-ttu-id="24778-376">Любая попытка выбрать цветовую палитру из палитры элементов управления шрифта может привести к нарушению прав доступа, если с элементом управления не связан ни один обработчик команд.</span><span class="sxs-lookup"><span data-stu-id="24778-376">Any attempt to select a color swatch from the color picker of a Font Control may result in an access violation if no Command handler is associated with the control.</span></span>

 

<span data-ttu-id="24778-377">В следующем примере кода показано, как привязать команды, объявленные в разметке к обработчику команд.</span><span class="sxs-lookup"><span data-stu-id="24778-377">The following code example demonstrates how to bind Commands that are declared in markup to a Command handler.</span></span>


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



<span data-ttu-id="24778-378">В следующем примере кода показано, как реализовать метод [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) для элемента управления Font.</span><span class="sxs-lookup"><span data-stu-id="24778-378">The following code example illustrates how to implement the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



<span data-ttu-id="24778-379">В следующем примере кода показано, как реализовать метод [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) для элемента управления Font.</span><span class="sxs-lookup"><span data-stu-id="24778-379">The following code example illustrates how to implement the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method for a Font Control.</span></span>


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="24778-380">См. также</span><span class="sxs-lookup"><span data-stu-id="24778-380">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24778-381">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="24778-381">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="24778-382">**Фонтконтрол, элемент**</span><span class="sxs-lookup"><span data-stu-id="24778-382">**FontControl element**</span></span>](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="24778-383">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="24778-383">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="24778-384">Пример Фонтконтрол</span><span class="sxs-lookup"><span data-stu-id="24778-384">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

