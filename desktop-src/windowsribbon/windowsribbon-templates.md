---
title: Настройка ленты с помощью определений размеров и политик масштабирования
description: Элементы управления, размещенные на панели команд ленты, подчиняются правилам макета, которые применяются платформой Windows Ribbon и основаны на сочетании поведения по умолчанию и шаблонов макета (определяемых платформой и настраиваемых), как объявлено в разметке ленты. Эти правила определяют поведение адаптивного макета для платформы Ribbon, влияющее на то, как элементы управления на панели команд адаптируются к различным размерам ленты во время выполнения.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Лента Windows, Настройка
- Лента, Настройка
- Лента Windows, шаблоны Сизедефинитион
- Лента, шаблоны Сизедефинитион
- Лента Windows, пользовательские шаблоны
- Лента, пользовательские шаблоны
- Настройка ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6576a672aa8c3d328a341370a7568595e988908
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444145"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a><span data-ttu-id="2fc14-111">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="2fc14-111">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>

<span data-ttu-id="2fc14-112">Элементы управления, размещенные на панели команд ленты, подчиняются правилам макета, которые применяются платформой Windows Ribbon и основаны на сочетании поведения по умолчанию и шаблонов макета (определяемых платформой и настраиваемых), как объявлено в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="2fc14-112">Controls hosted in the ribbon Command bar are subject to layout rules that are enforced by the Windows Ribbon framework and based on a combination of default behaviors and layout templates (both framework-defined and custom) as declared in the Ribbon markup.</span></span> <span data-ttu-id="2fc14-113">Эти правила определяют поведение адаптивного макета для платформы Ribbon, влияющее на то, как элементы управления на панели команд адаптируются к различным размерам ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2fc14-113">These rules define the adaptive layout behaviors of the Ribbon framework that influence how controls in the Command bar adapt to various ribbon sizes at run time.</span></span>

-   [<span data-ttu-id="2fc14-114">Введение</span><span class="sxs-lookup"><span data-stu-id="2fc14-114">Introduction</span></span>](#introduction)
    -   [<span data-ttu-id="2fc14-115">Шаблоны Сизедефинитион ленты</span><span class="sxs-lookup"><span data-stu-id="2fc14-115">Ribbon SizeDefinition Templates</span></span>](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [<span data-ttu-id="2fc14-116">Пользовательские шаблоны</span><span class="sxs-lookup"><span data-stu-id="2fc14-116">Custom Templates</span></span>](#custom-templates)
-   [<span data-ttu-id="2fc14-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2fc14-117">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="2fc14-118">Введение</span><span class="sxs-lookup"><span data-stu-id="2fc14-118">Introduction</span></span>

<span data-ttu-id="2fc14-119">Адаптивный макет, как определено платформой Ribbon, — это способность всех элементов управления в пользовательском интерфейсе ленты динамически настраивать организацию, размер, формат и относительный масштаб на основе изменений размера ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="2fc14-119">Adaptive layout, as defined by the Ribbon framework, is the ability of all controls within the ribbon UI to dynamically adjust their organization, size, format, and relative scale based on changes to the size of the ribbon at run time.</span></span>

<span data-ttu-id="2fc14-120">Платформа предоставляет функции адаптивного макета через набор элементов разметки, предназначенных для указания и настройки различных поведений макета.</span><span class="sxs-lookup"><span data-stu-id="2fc14-120">The framework exposes adaptive layout functionality through a set of markup elements that are dedicated to specifying and customizing various layout behaviors.</span></span> <span data-ttu-id="2fc14-121">Коллекция шаблонов, именуемая [**сизедефинитионс**](windowsribbon-element-sizedefinition.md), определяется платформой, каждая из которых поддерживает различные сценарии управления и макета.</span><span class="sxs-lookup"><span data-stu-id="2fc14-121">A collection of templates, called [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), is defined by the framework, each of which support various control and layout scenarios.</span></span> <span data-ttu-id="2fc14-122">Однако платформа также поддерживает пользовательские шаблоны, если предопределенные шаблоны не предоставляют интерфейс пользователя или макеты, необходимые для приложения.</span><span class="sxs-lookup"><span data-stu-id="2fc14-122">However, the framework also supports custom templates should the predefined templates not provide the UI experience or layouts required by an application.</span></span>

<span data-ttu-id="2fc14-123">Чтобы элементы управления отображались в предпочтительном макете на определенном уровне ленты, стандартные шаблоны и пользовательские шаблоны работают совместно с элементом [**скалингполици**](windowsribbon-element-scalingpolicy.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc14-123">To display controls in a preferred layout at a particular ribbon size, both predefined templates and custom templates work in conjunction with the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element.</span></span> <span data-ttu-id="2fc14-124">Этот элемент содержит манифест настроек размера, которые платформа использует в качестве инструкции при отрисовке ленты.</span><span class="sxs-lookup"><span data-stu-id="2fc14-124">This element contains a manifest of size preferences that the framework uses as a guide when rendering the ribbon.</span></span>

> [!Note]  
> <span data-ttu-id="2fc14-125">Платформа Ribbon обеспечивает поведение макета по умолчанию на основе набора встроенных эвристических методов для Организации и представления элементов управления во время выполнения без необходимости использования предопределенных шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc14-125">The Ribbon framework provides default layout behaviors based on a set of built-in heuristics for the organization and presentation of controls at run time without the need for the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates.</span></span> <span data-ttu-id="2fc14-126">Однако эта возможность предназначена только для создания прототипов.</span><span class="sxs-lookup"><span data-stu-id="2fc14-126">However, this capability is intended for prototyping purposes only.</span></span>

 

### <a name="ribbon-sizedefinition-templates"></a><span data-ttu-id="2fc14-127">Шаблоны Сизедефинитион ленты</span><span class="sxs-lookup"><span data-stu-id="2fc14-127">Ribbon SizeDefinition Templates</span></span>

<span data-ttu-id="2fc14-128">Платформа Ribbon предоставляет исчерпывающий набор шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) , которые определяют поведение размера и макета для [группы](windowsribbon-controls-group.md) элементов управления ленты.</span><span class="sxs-lookup"><span data-stu-id="2fc14-128">The Ribbon framework provides a comprehensive set of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates that specify size and layout behavior for a [Group](windowsribbon-controls-group.md) of Ribbon controls.</span></span> <span data-ttu-id="2fc14-129">Эти шаблоны охватывают наиболее распространенные сценарии организации элементов управления в приложении на ленте.</span><span class="sxs-lookup"><span data-stu-id="2fc14-129">These templates cover most common scenarios for organizing controls in a Ribbon application.</span></span>

<span data-ttu-id="2fc14-130">Чтобы обеспечить единообразное взаимодействие с пользователем в приложениях ленты, каждый шаблон [**сизедефинитион**](windowsribbon-element-sizedefinition.md) накладывает ограничения на элементы управления или семейство элементов управления, которые он поддерживает.</span><span class="sxs-lookup"><span data-stu-id="2fc14-130">To enforce a consistent user experience across Ribbon applications, each [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template imposes restrictions on the controls or the family of controls it supports.</span></span>

<span data-ttu-id="2fc14-131">Например, семейство элементов управления Button содержит:</span><span class="sxs-lookup"><span data-stu-id="2fc14-131">For example, the button family of controls includes:</span></span>

-   [<span data-ttu-id="2fc14-132">Button</span><span class="sxs-lookup"><span data-stu-id="2fc14-132">Button</span></span>](windowsribbon-controls-button.md)
-   [<span data-ttu-id="2fc14-133">Выключатель</span><span class="sxs-lookup"><span data-stu-id="2fc14-133">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)
-   [<span data-ttu-id="2fc14-134">Кнопка раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="2fc14-134">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)
-   [<span data-ttu-id="2fc14-135">Разворачивающаяся кнопка</span><span class="sxs-lookup"><span data-stu-id="2fc14-135">Split Button</span></span>](windowsribbon-controls-splitbutton.md)
-   [<span data-ttu-id="2fc14-136">Раскрывающийся список</span><span class="sxs-lookup"><span data-stu-id="2fc14-136">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)
-   [<span data-ttu-id="2fc14-137">Коллекция разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="2fc14-137">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)
-   [<span data-ttu-id="2fc14-138">Выбор цвета для раскрывающегося списка</span><span class="sxs-lookup"><span data-stu-id="2fc14-138">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md)

<span data-ttu-id="2fc14-139">Хотя входное семейство элементов управления включает:</span><span class="sxs-lookup"><span data-stu-id="2fc14-139">While the input family of controls includes:</span></span>

-   [<span data-ttu-id="2fc14-140">Поле со списком</span><span class="sxs-lookup"><span data-stu-id="2fc14-140">Combo Box</span></span>](windowsribbon-controls-combobox.md)
-   [<span data-ttu-id="2fc14-141">Spinner</span><span class="sxs-lookup"><span data-stu-id="2fc14-141">Spinner</span></span>](windowsribbon-controls-spinner.md)

<span data-ttu-id="2fc14-142">[Флажок](windowsribbon-controls-checkbox.md) и [коллекция в ленте](windowsribbon-controls-inribbongallery.md) не принадлежат семейству кнопок или семейству входных данных.</span><span class="sxs-lookup"><span data-stu-id="2fc14-142">[Check Box](windowsribbon-controls-checkbox.md) and [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) do not belong to either the button family or the input family.</span></span> <span data-ttu-id="2fc14-143">Эти два элемента управления можно использовать только в том случае, если явно указано в шаблоне [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc14-143">These two controls can be used only where explicitly indicated in a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template.</span></span>

<span data-ttu-id="2fc14-144">Ниже приведен список шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с описанием макета и элементов управления, которые допускаются каждым шаблоном.</span><span class="sxs-lookup"><span data-stu-id="2fc14-144">The following is a list of the [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates with a description of the layout and controls allowed by each template.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fc14-145">Если элементы управления, объявленные в разметке, не соответствуют типу, упорядочению и количеству, определенным в связанном шаблоне, то [Ошибка проверки](windowsribbon-compilationerrors.md) заносится в журнал [компилятором разметки](windowsribbon-intentcl.md) , а компиляция завершается.</span><span class="sxs-lookup"><span data-stu-id="2fc14-145">If the controls declared in markup do not map exactly to control type, order, and quantity defined in the associated template, a [validation error](windowsribbon-compilationerrors.md) is logged by the [markup compiler](windowsribbon-intentcl.md) and compilation is terminated.</span></span>

 



<span data-ttu-id="2fc14-146">онебуттон</span><span class="sxs-lookup"><span data-stu-id="2fc14-146">OneButton</span></span>

<span data-ttu-id="2fc14-147">Одна кнопка — Управление семейством.</span><span class="sxs-lookup"><span data-stu-id="2fc14-147">One button-family control.</span></span><br/> <span data-ttu-id="2fc14-148">Поддерживается только большой размер группы.</span><span class="sxs-lookup"><span data-stu-id="2fc14-148">Only Large group size is supported.</span></span><br/>

![Рисунок шаблона онебуттон сизедефинитион.](images/overviews/sizedefinition-onebutton.png)

<span data-ttu-id="2fc14-150">твобуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-150">TwoButtons</span></span>

<span data-ttu-id="2fc14-151">Две кнопки — элементы управления семейства.</span><span class="sxs-lookup"><span data-stu-id="2fc14-151">Two button-family controls.</span></span><br/> <span data-ttu-id="2fc14-152">Поддерживаются только размеры больших и средних групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-152">Only Large and Medium group sizes are supported.</span></span><br/>

![Рисунок шаблона твобуттонс Large сизедефинитион.](images/overviews/sizedefinition-twobuttons-large.png)

![Рисунок шаблона твобуттонс Medium сизедефинитион.](images/overviews/sizedefinition-twobuttons-medium.png)

<span data-ttu-id="2fc14-155">срибуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-155">ThreeButtons</span></span>

<span data-ttu-id="2fc14-156">Три кнопки — элементы управления семейства.</span><span class="sxs-lookup"><span data-stu-id="2fc14-156">Three button-family controls.</span></span><br/> <span data-ttu-id="2fc14-157">Поддерживаются только размеры больших и средних групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-157">Only Large and Medium group sizes are supported.</span></span><br/>

![Рисунок шаблона срибуттонс Large сизедефинитион.](images/overviews/sizedefinition-threebuttons-large.png)

![Рисунок шаблона срибуттонс Medium сизедефинитион.](images/overviews/sizedefinition-threebuttons-medium.png)

<span data-ttu-id="2fc14-160">ThreeButtons-OneBigAndTwoSmall</span><span class="sxs-lookup"><span data-stu-id="2fc14-160">ThreeButtons-OneBigAndTwoSmall</span></span>

<span data-ttu-id="2fc14-161">Три кнопки — элементы управления семейства.</span><span class="sxs-lookup"><span data-stu-id="2fc14-161">Three button-family controls.</span></span><br/> <span data-ttu-id="2fc14-162">Первая кнопка представлена на самом деле во всех трех размерах.</span><span class="sxs-lookup"><span data-stu-id="2fc14-162">The first button is presented prominently in all three sizes.</span></span><br/>

![Рисунок шаблона срибуттонс-онебигандтвосмалл Large сизедефинитион.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![Рисунок шаблона срибуттонс-онебигандтвосмалл Medium сизедефинитион.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![Рисунок шаблона срибуттонс-онебигандтвосмалл Small сизедефинитион.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

<span data-ttu-id="2fc14-166">срибуттонсандонечеккбокс</span><span class="sxs-lookup"><span data-stu-id="2fc14-166">ThreeButtonsAndOneCheckBox</span></span>

<span data-ttu-id="2fc14-167">Три кнопки — элементы управления семейством, сопровождаемые одним элементом управления CheckBox.</span><span class="sxs-lookup"><span data-stu-id="2fc14-167">Three button-family controls accompanied by a single CheckBox control.</span></span><br/> <span data-ttu-id="2fc14-168">Поддерживаются только размеры больших и средних групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-168">Only Large and Medium group sizes are supported.</span></span><br/>

![Рисунок шаблона срибуттонсандонечеккбокс Large сизедефинитион.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![Рисунок шаблона срибуттонсандонечеккбокс Medium сизедефинитион.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

<span data-ttu-id="2fc14-171">фаурбуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-171">FourButtons</span></span>

<span data-ttu-id="2fc14-172">Четыре кнопки — элементы управления семейства.</span><span class="sxs-lookup"><span data-stu-id="2fc14-172">Four button-family controls.</span></span><br/>

![Рисунок шаблона фаурбуттонс Large сизедефинитион.](images/overviews/sizedefinition-fourbuttons-large.png)

![Рисунок шаблона фаурбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-fourbuttons-medium.png)

![Рисунок шаблона фаурбуттонс Small сизедефинитион.](images/overviews/sizedefinition-fourbuttons-small.png)

<span data-ttu-id="2fc14-176">фивебуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-176">FiveButtons</span></span>

<span data-ttu-id="2fc14-177">Пять элементов управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="2fc14-177">Five button-family controls.</span></span><br/>

![Рисунок шаблона фивебуттонс Large сизедефинитион.](images/overviews/sizedefinition-fivebuttons-large.png)

![Рисунок шаблона фивебуттонс Medium сизедефинитион.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Рисунок шаблона фивебуттонс Small сизедефинитион.](images/overviews/sizedefinition-fivebuttons-small.png)

<span data-ttu-id="2fc14-181">фивеорсиксбуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-181">FiveOrSixButtons</span></span>

<span data-ttu-id="2fc14-182">Пять элементов управления "Кнопка" и необязательная кнопка "шестая".</span><span class="sxs-lookup"><span data-stu-id="2fc14-182">Five button-family controls and an optional sixth button.</span></span><br/>

![Рисунок шаблона фивеорсиксбуттонс Large сизедефинитион.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![Рисунок шаблона фивеорсиксбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![Рисунок шаблона фивеорсиксбуттонс Small сизедефинитион.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

<span data-ttu-id="2fc14-186">сиксбуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-186">SixButtons</span></span>

<span data-ttu-id="2fc14-187">Шесть элементов управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="2fc14-187">Six button-family controls.</span></span><br/>

![Рисунок шаблона сиксбуттонс Large сизедефинитион.](images/overviews/sizedefinition-sixbuttons-large.png)

![Рисунок шаблона сиксбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-sixbuttons-medium.png)

![Рисунок шаблона сиксбуттонс Small сизедефинитион.](images/overviews/sizedefinition-sixbuttons-small.png)

<span data-ttu-id="2fc14-191">SixButtons-TwoColumns</span><span class="sxs-lookup"><span data-stu-id="2fc14-191">SixButtons-TwoColumns</span></span>

<span data-ttu-id="2fc14-192">Шесть кнопок — элементы управления семейства (альтернативная презентация).</span><span class="sxs-lookup"><span data-stu-id="2fc14-192">Six button-family controls (alternate presentation).</span></span><br/>

![Рисунок шаблона сиксбуттонс-твоколумнс Large сизедефинитион.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![шаблон сиксбуттонс-твоколумнс Medium сизедефинитион.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![Рисунок шаблона сиксбуттонс-твоколумнс Small сизедефинитион.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

<span data-ttu-id="2fc14-196">севенбуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-196">SevenButtons</span></span>

<span data-ttu-id="2fc14-197">Семь элементов управления "Кнопка" — "семейство".</span><span class="sxs-lookup"><span data-stu-id="2fc14-197">Seven button-family controls.</span></span><br/>

![Рисунок шаблона севенбуттонс Large сизедефинитион.](images/overviews/sizedefinition-sevenbuttons-large.png)

![Рисунок шаблона севенбуттонс медиумсизедефинитион.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![Рисунок шаблона севенбуттонс Small сизедефинитион.](images/overviews/sizedefinition-sevenbuttons-small.png)

<span data-ttu-id="2fc14-201">еигхтбуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-201">EightButtons</span></span>

<span data-ttu-id="2fc14-202">Восемь элементов управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="2fc14-202">Eight button-family controls.</span></span><br/>

![Рисунок шаблона еигхтбуттонс-ластсрисмалл Large сизедефинитион.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Рисунок шаблона еигхтбуттонс-ластсрисмалл Medium сизедефинитион.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![Рисунок шаблона еигхтбуттонс-ластсрисмалл Small сизедефинитион.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

<span data-ttu-id="2fc14-206">EightButtons-LastThreeSmall</span><span class="sxs-lookup"><span data-stu-id="2fc14-206">EightButtons-LastThreeSmall</span></span>

<span data-ttu-id="2fc14-207">Восемь кнопок — элементы управления семейства (альтернативная презентация).</span><span class="sxs-lookup"><span data-stu-id="2fc14-207">Eight button-family controls (alternate presentation).</span></span><br/>

> [!Note]  
> <span data-ttu-id="2fc14-208">Все элементы управления, объявленные с помощью этого шаблона, должны содержаться в двух элементах [**контролграуп**](windowsribbon-element-controlgroup.md) : один для первых пяти элементов и один для последних трех элементов.</span><span class="sxs-lookup"><span data-stu-id="2fc14-208">All control elements declared with this template must be contained in two [**ControlGroup**](windowsribbon-element-controlgroup.md) elements: one for the first five elements and one for the last three elements.</span></span>

<br/> <span data-ttu-id="2fc14-209">В следующем примере показана разметка, необходимая для этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fc14-209">The following example demonstrates the markup required for this template.</span></span><br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![Рисунок шаблона еигхтбуттонс Large сизедефинитион.](images/overviews/sizedefinition-eightbuttons-large.png)

![Рисунок шаблона еигхтбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-eightbuttons-medium.png)

![Рисунок шаблона еигхтбуттонс Small сизедефинитион.](images/overviews/sizedefinition-eightbuttons-small.png)

<span data-ttu-id="2fc14-213">нинебуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-213">NineButtons</span></span>

<span data-ttu-id="2fc14-214">Девять элементов управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="2fc14-214">Nine button-family controls.</span></span>

![Рисунок шаблона нинебуттонс Large сизедефинитион.](images/overviews/sizedefinition-ninebuttons-large.png)

![Рисунок шаблона нинебуттонс Medium сизедефинитион.](images/overviews/sizedefinition-ninebuttons-medium.png)

![Рисунок шаблона нинебуттонс Small сизедефинитион.](images/overviews/sizedefinition-ninebuttons-small.png)

<span data-ttu-id="2fc14-218">тенбуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-218">TenButtons</span></span>

<span data-ttu-id="2fc14-219">Десять элементов управления для семейства кнопок.</span><span class="sxs-lookup"><span data-stu-id="2fc14-219">Ten button-family controls.</span></span>

![Рисунок шаблона тенбуттонс Large сизедефинитион.](images/overviews/sizedefinition-tenbuttons-large.png)

![Рисунок шаблона тенбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-tenbuttons-medium.png)

![Рисунок шаблона тенбуттонс Small сизедефинитион.](images/overviews/sizedefinition-tenbuttons-small.png)

<span data-ttu-id="2fc14-223">елевенбуттонс</span><span class="sxs-lookup"><span data-stu-id="2fc14-223">ElevenButtons</span></span>

<span data-ttu-id="2fc14-224">Одиннадцать кнопок — элементы управления семейства.</span><span class="sxs-lookup"><span data-stu-id="2fc14-224">Eleven button-family controls.</span></span>

![Рисунок шаблона елевенбуттонс Large сизедефинитион.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Рисунок шаблона елевенбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![Рисунок шаблона елевенбуттонс Small сизедефинитион.](images/overviews/sizedefinition-elevenbuttons-small.png)

<span data-ttu-id="2fc14-228">онефонтконтрол</span><span class="sxs-lookup"><span data-stu-id="2fc14-228">OneFontControl</span></span>

<span data-ttu-id="2fc14-229">Один [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="2fc14-229">One [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

<span data-ttu-id="2fc14-230">Поддерживаются только размеры больших и средних групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-230">Only Large and Medium group sizes are supported.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fc14-231">Включение [**фонтконтрол**](windowsribbon-element-fontcontrol.md) в определение пользовательского шаблона не поддерживается платформой.</span><span class="sxs-lookup"><span data-stu-id="2fc14-231">Including a [**FontControl**](windowsribbon-element-fontcontrol.md) within a custom template definition is not supported by the framework.</span></span>

 

![Рисунок шаблона онефонтконтрол Large сизедефинитион.](images/overviews/sizedefinition-onefontcontrol-large.png)

![Рисунок шаблона онефонтконтрол Medium сизедефинитион.](images/overviews/sizedefinition-onefontcontrol-medium.png)

<span data-ttu-id="2fc14-234">онеинриббонгаллери</span><span class="sxs-lookup"><span data-stu-id="2fc14-234">OneInRibbonGallery</span></span>

<span data-ttu-id="2fc14-235">Один элемент управления [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc14-235">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control.</span></span>

<span data-ttu-id="2fc14-236">Поддерживаются только крупные и небольшие размеры групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-236">Only Large and Small group sizes are supported.</span></span>

![Рисунок шаблона онеинриббонгаллери Large сизедефинитион.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![Рисунок шаблона онеинриббонгаллери Small сизедефинитион.](images/overviews/sizedefinition-oneinribbongallery-small.png)

<span data-ttu-id="2fc14-239">инриббонгаллеряндбигбуттон</span><span class="sxs-lookup"><span data-stu-id="2fc14-239">InRibbonGalleryAndBigButton</span></span>

<span data-ttu-id="2fc14-240">Один элемент управления [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) и элемент управления семейства Button.</span><span class="sxs-lookup"><span data-stu-id="2fc14-240">One [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) control and a button-family control.</span></span>

<span data-ttu-id="2fc14-241">Поддерживаются только крупные и небольшие размеры групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-241">Only Large and Small group sizes are supported.</span></span>

![Рисунок шаблона инриббонгаллеряндбигбуттон Large сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![Рисунок шаблона инриббонгаллеряндбигбуттон Small сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

<span data-ttu-id="2fc14-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span><span class="sxs-lookup"><span data-stu-id="2fc14-244">InRibbonGalleryAndButtons-GalleryScalesFirst</span></span>

<span data-ttu-id="2fc14-245">Один элемент управления [коллекции в ленте](windowsribbon-controls-inribbongallery.md) и два или три элемента управления семейства кнопок.</span><span class="sxs-lookup"><span data-stu-id="2fc14-245">One [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control and two or three button-family controls.</span></span>

<span data-ttu-id="2fc14-246">Коллекция сворачивается в всплывающее представление в средних и мелких группах.</span><span class="sxs-lookup"><span data-stu-id="2fc14-246">The gallery collapses to Popup representation in Medium and Small group sizes.</span></span>

![Рисунок шаблона инриббонгаллеряндбуттонс-галлерискалесфирст Large сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Рисунок шаблона инриббонгаллеряндбуттонс-галлерискалесфирст Medium сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![Рисунок шаблона инриббонгаллеряндбуттонс-галлерискалесфирст Small сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

<span data-ttu-id="2fc14-250">буттонграупс</span><span class="sxs-lookup"><span data-stu-id="2fc14-250">ButtonGroups</span></span>

<span data-ttu-id="2fc14-251">Комплексное размещение элементов управления "Кнопка" 32 (большинство из них необязательны).</span><span class="sxs-lookup"><span data-stu-id="2fc14-251">A complex arrangement of 32 button-family controls (most of which are optional).</span></span>

> [!Note]  
> <span data-ttu-id="2fc14-252">Помимо необязательной полной кнопки крупного шаблона Буттонграупс, все элементы управления, объявленные с помощью этого шаблона, должны содержаться в элементах [**контролграуп**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc14-252">Aside from the optional full-sized button of the large ButtonGroups template, all control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="2fc14-253">В следующем примере показана разметка, необходимая для вывода всех элементов управления 32 (обязательных и необязательных) с помощью этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fc14-253">The following example demonstrates the markup required to display all 32 control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![Рисунок шаблона буттонграупс Large сизедефинитион.](images/overviews/sizedefinition-buttongroups-large.png)

![Рисунок шаблона буттонграупс Medium сизедефинитион.](images/overviews/sizedefinition-buttongroups-medium.png)

![Рисунок шаблона буттонграупс Small сизедефинитион.](images/overviews/sizedefinition-buttongroups-small.png)

<span data-ttu-id="2fc14-257">буттонграупсандинпутс</span><span class="sxs-lookup"><span data-stu-id="2fc14-257">ButtonGroupsAndInputs</span></span>

<span data-ttu-id="2fc14-258">Два элемента управления для семейства входных данных (второй — необязательный), за которыми следует комплексное упорядочение 29 элементов управления "Кнопка" (большинство из которых являются необязательными).</span><span class="sxs-lookup"><span data-stu-id="2fc14-258">Two input-family controls (the second is optional) followed by a complex arrangement of 29 button-family controls (most of which are optional).</span></span>

<span data-ttu-id="2fc14-259">Поддерживаются только размеры больших и средних групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-259">Only Large and Medium group sizes are supported.</span></span>

> [!Note]  
> <span data-ttu-id="2fc14-260">Все элементы управления, объявленные с помощью этого шаблона, должны содержаться в элементах [**контролграуп**](windowsribbon-element-controlgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc14-260">All control elements declared with this template must be contained in [**ControlGroup**](windowsribbon-element-controlgroup.md) elements.</span></span>

 

<span data-ttu-id="2fc14-261">В следующем примере показана разметка, необходимая для вывода всех элементов управления (обязательных и необязательных) с помощью этого шаблона.</span><span class="sxs-lookup"><span data-stu-id="2fc14-261">The following example demonstrates the markup required to display all control elements (required and optional) with this template.</span></span>


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![Рисунок шаблона буттонграупсандинпутс Large сизедефинитион.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Рисунок шаблона буттонграупсандинпутс Medium сизедефинитион.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

<span data-ttu-id="2fc14-264">бигбуттонсандсмаллбуттонсоринпутс</span><span class="sxs-lookup"><span data-stu-id="2fc14-264">BigButtonsAndSmallButtonsOrInputs</span></span>

<span data-ttu-id="2fc14-265">Две кнопки — элементы управления семействами (необязательные), за которыми следует две или три кнопки или элементы управления для семейства входных данных.</span><span class="sxs-lookup"><span data-stu-id="2fc14-265">Two button-family controls (both optional) followed by two or three button or input-family controls.</span></span>

<span data-ttu-id="2fc14-266">Поддерживаются только размеры больших и средних групп.</span><span class="sxs-lookup"><span data-stu-id="2fc14-266">Only Large and Medium group sizes are supported.</span></span>

![Рисунок шаблона бигбуттонсандсмаллбуттонсоринпутс Large сизедефинитион.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Рисунок шаблона бигбуттонсандсмаллбуттонсоринпутс Medium сизедефинитион.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a><span data-ttu-id="2fc14-269">Пример Basic Сизедефинитион</span><span class="sxs-lookup"><span data-stu-id="2fc14-269">Basic SizeDefinition Example</span></span>

<span data-ttu-id="2fc14-270">В следующем примере кода показана базовая Демонстрация объявления шаблона [**сизедефинитион**](windowsribbon-element-sizedefinition.md) в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="2fc14-270">The following code example provides a basic demonstration of how to declare a [**SizeDefinition**](windowsribbon-element-sizedefinition.md) template in Ribbon markup.</span></span>

<span data-ttu-id="2fc14-271">*Онеинриббонгаллери* [**сизедефинитион**](windowsribbon-element-sizedefinition.md) используется в этом конкретном примере, но все шаблоны инфраструктуры указаны аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="2fc14-271">The *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) is used for this particular example, but all framework templates are specified in a similar fashion.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a><span data-ttu-id="2fc14-272">Сложный пример Сизедефинитион с политиками масштабирования</span><span class="sxs-lookup"><span data-stu-id="2fc14-272">Complex SizeDefinition Example with Scaling Policies</span></span>

<span data-ttu-id="2fc14-273">Поведением сворачивания шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) можно управлять с помощью политик масштабирования в разметке ленты.</span><span class="sxs-lookup"><span data-stu-id="2fc14-273">The collapsing behavior of [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates can be controlled through the use of scaling policies in the Ribbon markup.</span></span>

<span data-ttu-id="2fc14-274">Элемент [**скалингполици**](windowsribbon-element-scalingpolicy.md) содержит манифест для объявлений [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) и [**Scale**](windowsribbon-element-scale.md) , задающих параметры адаптивного макета для одного или нескольких элементов [**группы**](windowsribbon-element-group.md) при изменении размера ленты.</span><span class="sxs-lookup"><span data-stu-id="2fc14-274">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) element contains a manifest of [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) and [**Scale**](windowsribbon-element-scale.md) declarations that specify adaptive layout preferences for one or more [**Group**](windowsribbon-element-group.md) elements when the Ribbon is resized.</span></span>

> [!Note]  
> <span data-ttu-id="2fc14-275">Настоятельно рекомендуется указывать соответствующие сведения о политике масштабирования таким образом, чтобы большинство, если не все, элементы [**группы**](windowsribbon-element-group.md) были связаны с элементом [**Scale**](windowsribbon-element-scale.md) , где атрибут *size* равен `Popup` .</span><span class="sxs-lookup"><span data-stu-id="2fc14-275">It is highly recommended that adequate scaling policy detail be specified such that most, if not all, [**Group**](windowsribbon-element-group.md) elements are associated with a [**Scale**](windowsribbon-element-scale.md) element where the *Size* attribute is equal to `Popup`.</span></span> <span data-ttu-id="2fc14-276">Это позволяет платформе визуализировать ленту с минимально возможным размером и поддерживать самые разнообразные устройства отображения, прежде чем автоматически представить механизм прокрутки.</span><span class="sxs-lookup"><span data-stu-id="2fc14-276">Doing so allows the framework to render the ribbon at the smallest size possible, and support the broadest range of display devices, before automatically introducing a scrolling mechanism.</span></span>

 

<span data-ttu-id="2fc14-277">В следующем примере кода показан манифест [**скалингполици**](windowsribbon-element-scalingpolicy.md) , указывающий предпочтение [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы [**масштаба**](windowsribbon-element-scale.md) задаются для влияния на режим свертывания в порядке убывания размера каждой группы.</span><span class="sxs-lookup"><span data-stu-id="2fc14-277">The following code example demonstrates a [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) manifest that specifies a [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) preference for each of four groups of controls on a **Home** tab. In addition, [**Scale**](windowsribbon-element-scale.md) elements are specified to influence the collapsing behavior, in descending size order, of each group.</span></span>


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a><span data-ttu-id="2fc14-278">Пользовательские шаблоны</span><span class="sxs-lookup"><span data-stu-id="2fc14-278">Custom Templates</span></span>

<span data-ttu-id="2fc14-279">Если поведение макета по умолчанию и стандартные шаблоны [**сизедефинитион**](windowsribbon-element-sizedefinition.md) не предлагают гибкости или поддержки для конкретного сценария макета, платформа Ribbon поддерживает пользовательские шаблоны с помощью элемента [**Ribbon. сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md) .</span><span class="sxs-lookup"><span data-stu-id="2fc14-279">If the default layout behaviors and the predefined [**SizeDefinition**](windowsribbon-element-sizedefinition.md) templates do not offer the flexibility or support for a particular layout scenario, custom templates are supported by the Ribbon framework through the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element.</span></span>

<span data-ttu-id="2fc14-280">Пользовательские шаблоны можно объявить двумя способами: автономный метод, использующий элемент [**Ribbon. сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md) для объявления многократно используемых именованных шаблонов или встроенный метод, зависящий от [**группы**](windowsribbon-element-group.md).</span><span class="sxs-lookup"><span data-stu-id="2fc14-280">Custom templates can be declared in two ways: a standalone method using the [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) element for declaring reusable, named templates or an inline method that is [**Group**](windowsribbon-element-group.md)-specific.</span></span>

### <a name="standalone-template"></a><span data-ttu-id="2fc14-281">Автономный шаблон</span><span class="sxs-lookup"><span data-stu-id="2fc14-281">Standalone Template</span></span>

<span data-ttu-id="2fc14-282">В следующем примере кода показан базовый, многократно используемый настраиваемый шаблон.</span><span class="sxs-lookup"><span data-stu-id="2fc14-282">The following code example illustrates a basic, reusable custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a><span data-ttu-id="2fc14-283">Встроенный шаблон</span><span class="sxs-lookup"><span data-stu-id="2fc14-283">Inline Template</span></span>

<span data-ttu-id="2fc14-284">В следующих примерах кода показан базовый встроенный пользовательский шаблон для группы из четырех кнопок.</span><span class="sxs-lookup"><span data-stu-id="2fc14-284">The following code examples illustrate a basic inline custom template for a group of four buttons.</span></span>

<span data-ttu-id="2fc14-285">В этом разделе кода показаны объявления команд для группы кнопок.</span><span class="sxs-lookup"><span data-stu-id="2fc14-285">This section of code shows the Command declarations for a group of buttons.</span></span> <span data-ttu-id="2fc14-286">Здесь также указаны крупные и небольшие ресурсы изображений.</span><span class="sxs-lookup"><span data-stu-id="2fc14-286">Large and small image resources are also specified here.</span></span>


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



<span data-ttu-id="2fc14-287">В этом разделе кода показано, как определить крупные, средние и малые шаблоны [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) для отображения четырех кнопок в различных размерах и макетах.</span><span class="sxs-lookup"><span data-stu-id="2fc14-287">This section of code demonstrates how to define large, medium, and small [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) templates to display the four buttons at various sizes and layouts.</span></span> <span data-ttu-id="2fc14-288">Объявление [**скалингполици**](windowsribbon-element-scalingpolicy.md) для вкладки определяет, какой шаблон используется для группы элементов управления на основе размера ленты и пространства, необходимого активной вкладке.</span><span class="sxs-lookup"><span data-stu-id="2fc14-288">The [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) declaration for the tab defines which template is used for a group of controls based on the ribbon size and space required by the active tab.</span></span>


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



<span data-ttu-id="2fc14-289">На следующих изображениях показано, как шаблоны из предыдущего примера применяются к пользовательскому интерфейсу Ribbon для уменьшения размера ленты.</span><span class="sxs-lookup"><span data-stu-id="2fc14-289">The following images show how the templates from the previous example are applied to the ribbon UI to accommodate a decrease in ribbon size.</span></span>



|  <span data-ttu-id="2fc14-290">Type</span><span class="sxs-lookup"><span data-stu-id="2fc14-290">Type</span></span>  |      <span data-ttu-id="2fc14-291">Образ</span><span class="sxs-lookup"><span data-stu-id="2fc14-291">Image</span></span>                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc14-292">Большой</span><span class="sxs-lookup"><span data-stu-id="2fc14-292">Large</span></span>  | ![Рисунок встроенного большого пользовательского шаблона.](images/overviews/sizedefinition-custom-large.png)   |
| <span data-ttu-id="2fc14-294">Средний</span><span class="sxs-lookup"><span data-stu-id="2fc14-294">Medium</span></span> | ![Рисунок встроенного пользовательского шаблона среднего уровня.](images/overviews/sizedefinition-custom-medium.png) |
| <span data-ttu-id="2fc14-296">Малый</span><span class="sxs-lookup"><span data-stu-id="2fc14-296">Small</span></span>  | ![Рисунок встроенного небольшого настраиваемого шаблона.](images/overviews/sizedefinition-custom-small.png)   |
| <span data-ttu-id="2fc14-298">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="2fc14-298">Popup</span></span>  | ![Рисунок встроенного всплывающего пользовательского шаблона.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a><span data-ttu-id="2fc14-300">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2fc14-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fc14-301">**сизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="2fc14-301">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[<span data-ttu-id="2fc14-302">**Масштабирование**</span><span class="sxs-lookup"><span data-stu-id="2fc14-302">**Scale**</span></span>](windowsribbon-element-scale.md)
</dt> <dt>

[<span data-ttu-id="2fc14-303">**Группа**</span><span class="sxs-lookup"><span data-stu-id="2fc14-303">**Group**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

 

 





