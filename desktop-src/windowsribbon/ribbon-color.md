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
# <a name="customizing-ribbon-colors"></a>Настройка цветов ленты

Платформа Windows Ribbon предоставляет набор свойств цвета, позволяющих приложению настраивать внешний вид различных элементов пользовательского интерфейса ленты во время выполнения.

-   [Введение](#introduction)
-   [Указание цветов ленты](#specify-ribbon-colors)
-   [Преобразование RGB в HSB](#convert-rgb-to-hsb)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

[Ключи свойств платформы](windowsribbon-reference-properties-framework.md) , перечисленные в следующей таблице, используются для задания цвета различных элементов пользовательского интерфейса в приложении на ленте. Эти свойства позволяют платформе Ribbon поддерживать персонализацию, требования к удостоверениям и спецификации фирменной символики в разных приложениях.

| Цвет ленты                     | Ключ свойства платформы                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Цвет фона                 | [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| Цвет выделения (только Windows 7) | [Пользовательский интерфейс \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)* * * *, введенный в Windows 8 * *: * * [UI \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) , нельзя задать независимо от [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).<br/> <br/>                                                              |
| Цвет текста                       | [Пользовательский интерфейс \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md)* * * * впервые появился в Windows 8 **:** изменения значения по умолчанию [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) в Windows 8 может потребовать корректировки [пользовательского интерфейса \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md) в лентах, предназначенных для Windows 7.<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>Указание цветов ленты

Платформа Ribbon использует цветовую модель оттенков, насыщенности, яркости (HSB), которая отличается от наиболее распространенных цветовых пространств оттенка, насыщенности, яркости (HSL) или оттенков, насыщенности, значения (HSV). В частности, B представляет общий уровень яркости или яркости, а не яркость определенного цвета.

Чтобы указать цвет элементов пользовательского интерфейса в платформе Ribbon, приложение назначает значения HSB каждому из свойств глобального цвета. Затем эти значения применяются для всех элементов ленты, как это требуется для приложения ленты (платформа не поддерживает присваивание значений HSB отдельным элементам и элементам управления).

В Windows 8 * *: * *[UI \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) присваивается то же значение, что и [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

В следующей таблице описаны параметры HSB платформы ленты.



Компонент

Описание

Скорректированные значения\*

Оттенок (H)

Пигмент (или фактический цвет) обычно определяется как значение из диапазона Цирклулар от 0 до 359 градусов.

0 (красный) до 255 (красный)

Насыщенность (с)

Чистота (или насыщенность) цвета измеряется в процентах от 0 до 100%.

от 0 (серый) до 255 (полностью насыщенный)

Яркость (B)

Общая яркость или интенсивность оттенков цвета, измеряемая в процентах от 0 до 100%.

от 0 (темного) до 255 (светло)

\* Исходный диапазон для каждого значения параметра преобразуется в диапазон от 0 до 255 для платформы.



 

Значения HSB не обозначают определенные цвета. Вместо этого сочетание значений свойств HSB влияет на то, как цветовые градиенты в пользовательском интерфейсе корректируются относительно друг друга.

При назначении настраиваемых значений HSB для [UI \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md) и [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)рекомендуется, чтобы эти значения были достаточно высокой контрастностью, чтобы обеспечить удобочитаемость. В частности, цвет текста должен быть темнее, чем самый светлый оттенок пользовательского интерфейса ленты. При необходимости платформа автоматически настраивает \_ \_ значение HSB UI PKEY глобалтекстколор, чтобы обеспечить достаточную контрастность с любым фоновым затенением или градиентом, производным от UI \_ PKEY \_ глобалбаккграундколор.

> [!Note]  
> В Windows 7 [Пользовательский интерфейс \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) можно задать независимо от [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md).

 

В следующем примере показано, как задать пользовательский цвет для свойств [UI \_ PKEY \_ глобалтекстколор](windowsribbon-reference-properties-uipkey-globaltextcolor.md), [UI \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)и [UI \_ PKEY \_ глобалхигхлигхтколор](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) .


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



## <a name="convert-rgb-to-hsb"></a>Преобразование RGB в HSB

В этом разделе описывается формула, необходимая для динамического сопоставления значения HSB платформы ленты, [пользовательского интерфейса \_ PKEY \_ глобалбаккграундколор](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) в этом примере с конкретным цветом RGB во время выполнения.

Фон строки табуляции используется в качестве опорной точки, так как он отображается как поверхность плоского цвета по сравнению с градиентом яркости фона ленты.

Для получения промежуточного значения HSL необходимо предварительное преобразование. Это значение HSL может быть преобразовано в значение HSB.

> [!Note]  
> Преобразование из RGB в HSL легко осуществляется с помощью большинства средств редактирования фотографий.

 

Преобразование HSL (с каждым компонентом в диапазоне от 0,0 до 1,0) к параметру HSB ленты осуществляется с помощью следующих формул:

-   H<sub>Background</sub> = Round (255.0 h)
-   S<sub>Background</sub> = Round (255.0 S)
-   B<sub>Background</sub> = Round (257.7 + 149,9 LN (L)), если 0,1793 <= L <= 0,9821

## <a name="related-topics"></a>См. также

<dl> <dt>

[Цветовые рекомендации](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[Свойства платформы](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





