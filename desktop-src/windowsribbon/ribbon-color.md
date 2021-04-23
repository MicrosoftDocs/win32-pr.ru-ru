---
title: Настройка цветов ленты
description: Платформа Windows Ribbon предоставляет набор свойств цвета, позволяющих приложению настраивать внешний вид различных элементов пользовательского интерфейса ленты во время выполнения.
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Лента Windows, Настройка цветов
- Лента, Настройка цветов
- Настройка цветов ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ff6527dc67ee18df4723fc33e4b764e20127e8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103789006"
---
# <a name="customizing-ribbon-colors"></a><span data-ttu-id="9ba67-106">Настройка цветов ленты</span><span class="sxs-lookup"><span data-stu-id="9ba67-106">Customizing Ribbon Colors</span></span>

<span data-ttu-id="9ba67-107">Платформа Windows Ribbon предоставляет набор свойств цвета, позволяющих приложению настраивать внешний вид различных элементов пользовательского интерфейса ленты во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9ba67-107">The Windows Ribbon framework exposes a set of color properties that allow an application to customize the appearance of various Ribbon UI elements at run time.</span></span>

-   [<span data-ttu-id="9ba67-108">Введение</span><span class="sxs-lookup"><span data-stu-id="9ba67-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="9ba67-109">Указание цветов ленты</span><span class="sxs-lookup"><span data-stu-id="9ba67-109">Specify Ribbon Colors</span></span>](#specify-ribbon-colors)
-   [<span data-ttu-id="9ba67-110">Преобразование RGB в HSB</span><span class="sxs-lookup"><span data-stu-id="9ba67-110">Convert RGB to HSB</span></span>](#convert-rgb-to-hsb)
-   [<span data-ttu-id="9ba67-111">См. также</span><span class="sxs-lookup"><span data-stu-id="9ba67-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="9ba67-112">Введение</span><span class="sxs-lookup"><span data-stu-id="9ba67-112">Introduction</span></span>

<span data-ttu-id="9ba67-113">[Ключи свойств платформы](windowsribbon-reference-properties-framework.md) , перечисленные в следующей таблице, используются для задания цвета различных элементов пользовательского интерфейса в приложении на ленте.</span><span class="sxs-lookup"><span data-stu-id="9ba67-113">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to set the color of various UI elements in a Ribbon application.</span></span> <span data-ttu-id="9ba67-114">Эти свойства позволяют платформе Ribbon поддерживать персонализацию, требования к удостоверениям и спецификации фирменной символики в разных приложениях.</span><span class="sxs-lookup"><span data-stu-id="9ba67-114">These properties allow the Ribbon framework to support personalization, identity requirements, and branding specifications across applications.</span></span>

| <span data-ttu-id="9ba67-115">Цвет ленты</span><span class="sxs-lookup"><span data-stu-id="9ba67-115">Ribbon Color</span></span>                     | <span data-ttu-id="9ba67-116">Ключ свойства платформы</span><span class="sxs-lookup"><span data-stu-id="9ba67-116">Framework Property Key</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba67-117">Цвет фона</span><span class="sxs-lookup"><span data-stu-id="9ba67-117">Background color</span></span>                 | [<span data-ttu-id="9ba67-118">UI \_ PKEY \_ глобалбаккграундколор</span><span class="sxs-lookup"><span data-stu-id="9ba67-118">UI\_PKEY\_GlobalBackgroundColor</span></span>](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9ba67-119">Цвет выделения (только Windows 7)</span><span class="sxs-lookup"><span data-stu-id="9ba67-119">Highlight color (Windows 7 only)</span></span> | <span data-ttu-id="9ba67-120">[Пользовательский интерфейс \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\* \* \* \*, введенный в Windows 8 \* \*: \* \* [UI \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) , нельзя задать независимо от [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9ba67-120">[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)\*\*\*\*Introduced in Windows 8\*\*:  \*\* [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) cannot be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span><br/> <br/>                                                              |
| <span data-ttu-id="9ba67-121">Цвет текста</span><span class="sxs-lookup"><span data-stu-id="9ba67-121">Text color</span></span>                       | <span data-ttu-id="9ba67-122">[Пользовательский интерфейс \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\* \* \* \* впервые появился в Windows 8 **:** изменения значения по умолчанию [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) в Windows 8 может потребовать корректировки [пользовательского интерфейса \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md) в лентах, предназначенных для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9ba67-122">[UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)\*\*\*\*Introduced in Windows 8 **:** Changes to the default value of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in Windows 8 might require an adjustment to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) in Ribbon apps designed for Windows 7.</span></span><br/> <br/> |



 

## <a name="specify-ribbon-colors"></a><span data-ttu-id="9ba67-123">Указание цветов ленты</span><span class="sxs-lookup"><span data-stu-id="9ba67-123">Specify Ribbon Colors</span></span>

<span data-ttu-id="9ba67-124">Платформа Ribbon использует цветовую модель оттенков, насыщенности, яркости (HSB), которая отличается от наиболее распространенных цветовых пространств оттенка, насыщенности, яркости (HSL) или оттенков, насыщенности, значения (HSV).</span><span class="sxs-lookup"><span data-stu-id="9ba67-124">The Ribbon framework uses a Hue, Saturation, Brightness (HSB) color model, which differs from the more common hue, saturation, luminosity (HSL) or hue, saturation, value (HSV) color spaces.</span></span> <span data-ttu-id="9ba67-125">В частности, B представляет общий уровень яркости или яркости, а не яркость определенного цвета.</span><span class="sxs-lookup"><span data-stu-id="9ba67-125">In particular, B represents an overall brightness or luminosity level rather than the lightness of a particular color.</span></span>

<span data-ttu-id="9ba67-126">Чтобы указать цвет элементов пользовательского интерфейса в платформе Ribbon, приложение назначает значения HSB каждому из свойств глобального цвета.</span><span class="sxs-lookup"><span data-stu-id="9ba67-126">To specify the color of UI elements in the Ribbon framework, an application assigns HSB values to each of the global color properties.</span></span> <span data-ttu-id="9ba67-127">Затем эти значения применяются для всех элементов ленты, как это требуется для приложения ленты (платформа не поддерживает присваивание значений HSB отдельным элементам и элементам управления).</span><span class="sxs-lookup"><span data-stu-id="9ba67-127">These values are then applied universally across all Ribbon elements as required by the Ribbon application (the framework does not support assigning HSB values to individual elements and controls).</span></span>

<span data-ttu-id="9ba67-128">В Windows 8 \* \*: \* \*[UI \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) присваивается то же значение, что и [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9ba67-128">\*\*\*\*Introduced in Windows 8\*\*:  \*\*[UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) is assigned the same value as [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

<span data-ttu-id="9ba67-129">В следующей таблице описаны параметры HSB платформы ленты.</span><span class="sxs-lookup"><span data-stu-id="9ba67-129">The following table describes the Ribbon framework HSB parameters.</span></span>



<span data-ttu-id="9ba67-130">Компонент</span><span class="sxs-lookup"><span data-stu-id="9ba67-130">Component</span></span>

<span data-ttu-id="9ba67-131">Описание</span><span class="sxs-lookup"><span data-stu-id="9ba67-131">Description</span></span>

<span data-ttu-id="9ba67-132">Скорректированные значения\*</span><span class="sxs-lookup"><span data-stu-id="9ba67-132">Adjusted Values\*</span></span>

<span data-ttu-id="9ba67-133">Оттенок (H)</span><span class="sxs-lookup"><span data-stu-id="9ba67-133">Hue (H)</span></span>

<span data-ttu-id="9ba67-134">Пигмент (или фактический цвет) обычно определяется как значение из диапазона Цирклулар от 0 до 359 градусов.</span><span class="sxs-lookup"><span data-stu-id="9ba67-134">The pigment, or actual, color is typically identified as a value from a circlular range of 0 to 359 degrees.</span></span>

<span data-ttu-id="9ba67-135">0 (красный) до 255 (красный)</span><span class="sxs-lookup"><span data-stu-id="9ba67-135">0 (red) to 255 (red)</span></span>

<span data-ttu-id="9ba67-136">Насыщенность (с)</span><span class="sxs-lookup"><span data-stu-id="9ba67-136">Saturation (S)</span></span>

<span data-ttu-id="9ba67-137">Чистота (или насыщенность) цвета измеряется в процентах от 0 до 100%.</span><span class="sxs-lookup"><span data-stu-id="9ba67-137">The purity, or saturation, of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="9ba67-138">от 0 (серый) до 255 (полностью насыщенный)</span><span class="sxs-lookup"><span data-stu-id="9ba67-138">0 (grey) to 255 (fully saturated)</span></span>

<span data-ttu-id="9ba67-139">Яркость (B)</span><span class="sxs-lookup"><span data-stu-id="9ba67-139">Brightness (B)</span></span>

<span data-ttu-id="9ba67-140">Общая яркость или интенсивность оттенков цвета, измеряемая в процентах от 0 до 100%.</span><span class="sxs-lookup"><span data-stu-id="9ba67-140">The overall brightness or darkness of the color measured as a percentage from 0 to 100%.</span></span>

<span data-ttu-id="9ba67-141">от 0 (темного) до 255 (светло)</span><span class="sxs-lookup"><span data-stu-id="9ba67-141">0 (dark) to 255 (light)</span></span>

<span data-ttu-id="9ba67-142">\* Исходный диапазон для каждого значения параметра преобразуется в диапазон от 0 до 255 для платформы.</span><span class="sxs-lookup"><span data-stu-id="9ba67-142">\* The original range for each parameter value is translated into a range of 0 to 255 for the framework.</span></span>



 

<span data-ttu-id="9ba67-143">Значения HSB не обозначают определенные цвета.</span><span class="sxs-lookup"><span data-stu-id="9ba67-143">HSB values do not identify specific colors.</span></span> <span data-ttu-id="9ba67-144">Вместо этого сочетание значений свойств HSB влияет на то, как цветовые градиенты в пользовательском интерфейсе корректируются относительно друг друга.</span><span class="sxs-lookup"><span data-stu-id="9ba67-144">Instead, the combination of HSB property values influences how color gradients throughout the UI are adjusted relative to each other.</span></span>

<span data-ttu-id="9ba67-145">При назначении настраиваемых значений HSB для [UI \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md) и [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)рекомендуется, чтобы эти значения были достаточно высокой контрастностью, чтобы обеспечить удобочитаемость.</span><span class="sxs-lookup"><span data-stu-id="9ba67-145">When assigning custom HSB values to [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) and [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), it is recommended that these values be of high enough contrast to ensure readability.</span></span> <span data-ttu-id="9ba67-146">В частности, цвет текста должен быть темнее, чем самый светлый оттенок пользовательского интерфейса ленты.</span><span class="sxs-lookup"><span data-stu-id="9ba67-146">Specifically, the text color should be darker than the lightest shade of the ribbon UI.</span></span> <span data-ttu-id="9ba67-147">При необходимости платформа автоматически настраивает \_ \_ значение HSB UI PKEY глобалтекстколор, чтобы обеспечить достаточную контрастность с любым фоновым затенением или градиентом, производным от UI \_ PKEY \_ глобалбаккграундколор.</span><span class="sxs-lookup"><span data-stu-id="9ba67-147">Where necessary, the framework automatically adjusts the UI\_PKEY\_GlobalTextColor HSB value to provide sufficient contrast against any background shade or gradient derived from UI\_PKEY\_GlobalBackgroundColor.</span></span>

> [!Note]  
> <span data-ttu-id="9ba67-148">В Windows 7 [Пользовательский интерфейс \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) можно задать независимо от [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span><span class="sxs-lookup"><span data-stu-id="9ba67-148">In Windows 7, [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) can be set independently of [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).</span></span>

 

<span data-ttu-id="9ba67-149">В следующем примере показано, как задать пользовательский цвет для свойств [UI \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)и [UI \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="9ba67-149">The following example demonstrates how to specify a custom color for the [UI\_PKEY\_GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md), and [UI\_PKEY\_GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) properties.</span></span>


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a><span data-ttu-id="9ba67-150">Преобразование RGB в HSB</span><span class="sxs-lookup"><span data-stu-id="9ba67-150">Convert RGB to HSB</span></span>

<span data-ttu-id="9ba67-151">В этом разделе описывается формула, необходимая для динамического сопоставления значения HSB платформы ленты, [пользовательского интерфейса \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) в этом примере с конкретным цветом RGB во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="9ba67-151">This section describes the formula that is required for dynamically matching a Ribbon framework HSB value, the [UI\_PKEY\_GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) in this example, to a specific RGB color at run time.</span></span>

<span data-ttu-id="9ba67-152">Фон строки табуляции используется в качестве опорной точки, так как он отображается как поверхность плоского цвета по сравнению с градиентом яркости фона ленты.</span><span class="sxs-lookup"><span data-stu-id="9ba67-152">The tab row background is used as a reference point because it is rendered as a flat color surface compared to the brightness gradient of the ribbon background.</span></span>

<span data-ttu-id="9ba67-153">Для получения промежуточного значения HSL необходимо предварительное преобразование.</span><span class="sxs-lookup"><span data-stu-id="9ba67-153">A preliminary conversion is necessary to obtain an intermediate HSL value.</span></span> <span data-ttu-id="9ba67-154">Это значение HSL может быть преобразовано в значение HSB.</span><span class="sxs-lookup"><span data-stu-id="9ba67-154">This HSL value can then be converted to an HSB value.</span></span>

> [!Note]  
> <span data-ttu-id="9ba67-155">Преобразование из RGB в HSL легко осуществляется с помощью большинства средств редактирования фотографий.</span><span class="sxs-lookup"><span data-stu-id="9ba67-155">The conversion from RGB to HSL is easily accomplished with most photo editing software.</span></span>

 

<span data-ttu-id="9ba67-156">Преобразование HSL (с каждым компонентом в диапазоне от 0,0 до 1,0) к параметру HSB ленты осуществляется с помощью следующих формул:</span><span class="sxs-lookup"><span data-stu-id="9ba67-156">Conversion of HSL (with each component in the range of 0.0 to 1.0) to a Ribbon HSB setting is accomplished through the following formulas:</span></span>

-   <span data-ttu-id="9ba67-157">H<sub>Background</sub> = Round (255.0 h)</span><span class="sxs-lookup"><span data-stu-id="9ba67-157">H<sub>background</sub> = Round(255.0 H)</span></span>
-   <span data-ttu-id="9ba67-158">S<sub>Background</sub> = Round (255.0 S)</span><span class="sxs-lookup"><span data-stu-id="9ba67-158">S<sub>background</sub> = Round(255.0 S)</span></span>
-   <span data-ttu-id="9ba67-159">B<sub>Background</sub> = Round (257.7 + 149,9 LN (L)), если 0,1793 <= L <= 0,9821</span><span class="sxs-lookup"><span data-stu-id="9ba67-159">B<sub>background</sub> = Round(257.7 + 149.9 ln(L)) if 0.1793 <= L <= 0.9821</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ba67-160">См. также</span><span class="sxs-lookup"><span data-stu-id="9ba67-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ba67-161">Цветовые рекомендации</span><span class="sxs-lookup"><span data-stu-id="9ba67-161">Color Guidelines</span></span>](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[<span data-ttu-id="9ba67-162">Свойства платформы</span><span class="sxs-lookup"><span data-stu-id="9ba67-162">Framework Properties</span></span>](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





