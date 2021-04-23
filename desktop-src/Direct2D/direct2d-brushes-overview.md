---
title: 'Обзор кистей '
description: Описывает различные типы кистей, предоставляемых Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104414077"
---
# <a name="brushes-overview"></a><span data-ttu-id="a39f0-103">Обзор кистей </span><span class="sxs-lookup"><span data-stu-id="a39f0-103">Brushes overview</span></span>

<span data-ttu-id="a39f0-104">В этом обзоре описывается создание и использование объектов [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)и [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для заливки областей сплошными цветами, градиентами и точечными рисунками.</span><span class="sxs-lookup"><span data-stu-id="a39f0-104">This overview describes how to create and use [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) objects to paint areas with solid colors, gradients, and bitmaps.</span></span> <span data-ttu-id="a39f0-105">В него входят следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="a39f0-105">It contains the following sections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a39f0-106">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a39f0-106">Prerequisites</span></span>

<span data-ttu-id="a39f0-107">В этом обзоре предполагается, что вы знакомы с структурой базового приложения Direct2D, как описано в разделе [Создание простого приложения Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="a39f0-107">This overview assumes that you are familiar with the structure of a basic Direct2D application, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="brush-types"></a><span data-ttu-id="a39f0-108">Типы кистей</span><span class="sxs-lookup"><span data-stu-id="a39f0-108">Brush types</span></span>

<span data-ttu-id="a39f0-109">Кисть закрашивает область с выходными данными.</span><span class="sxs-lookup"><span data-stu-id="a39f0-109">A brush "paints" an area with its output.</span></span> <span data-ttu-id="a39f0-110">Разные кисти имеют различные типы выводимых данных.</span><span class="sxs-lookup"><span data-stu-id="a39f0-110">Different brushes have different types of output.</span></span> <span data-ttu-id="a39f0-111">Direct2D предоставляет четыре типа кистей: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) закрашивает область сплошным цветом, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) с линейным градиентом, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) с радиальным градиентом и [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с растровым изображением.</span><span class="sxs-lookup"><span data-stu-id="a39f0-111">Direct2D provides four brush types: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints an area with a solid color, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) with a linear gradient, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) with a radial gradient, and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with a bitmap.</span></span>

> [!NOTE]  
> <span data-ttu-id="a39f0-112">Начиная с Windows 8, можно также использовать [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), который похож на растровую кисть, но также можно использовать примитивы.</span><span class="sxs-lookup"><span data-stu-id="a39f0-112">Starting with Windows 8, you can also use [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), which is similar to a bitmap brush, but you can use primitives, too.</span></span>

<span data-ttu-id="a39f0-113">Все кисти наследуют от [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) и совместно используют набор общих функций (Установка и получение непрозрачности и преобразование кистей); они создаются [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) и являются ресурсами, зависящими от устройства. приложение должно создавать кисти после инициализации целевого объекта рендеринга, с которым будут использоваться кисти, и повторно создавать кисти при необходимости повторного создания целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="a39f0-113">All brushes inherit from [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) and share a set of common features (setting and getting opacity, and transforming brushes); they are created by [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) and are device-dependent resources: your application should create brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated.</span></span> <span data-ttu-id="a39f0-114">(Дополнительные сведения о ресурсах см. в разделе [Общие сведения о ресурсах](resources-and-resource-domains.md).)</span><span class="sxs-lookup"><span data-stu-id="a39f0-114">(For more information about resources, see [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="a39f0-115">На следующем рисунке показаны примеры различных типов кистей.</span><span class="sxs-lookup"><span data-stu-id="a39f0-115">The following illustration shows examples of each of the different brush types.</span></span>

![Иллюстрация визуальных эффектов от сплошных цветных кистей, кистей линейного градиента, кистей радиального градиента и растровых кистей](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a><span data-ttu-id="a39f0-117">Основы цвета</span><span class="sxs-lookup"><span data-stu-id="a39f0-117">Color basics</span></span>

<span data-ttu-id="a39f0-118">Перед началом рисования с помощью [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) или градиентной кисти необходимо выбрать цвета.</span><span class="sxs-lookup"><span data-stu-id="a39f0-118">Before you paint with an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or a gradient brush, you need to choose colors.</span></span> <span data-ttu-id="a39f0-119">В Direct2D цвета представлены структурой [**D2D1 \_ Color \_ F**](d2d1-color-f.md) (на самом деле это только новое имя для структуры, используемой Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span><span class="sxs-lookup"><span data-stu-id="a39f0-119">In Direct2D, colors are represented by the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure (which is actually just a new name for the structure that is used by Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span></span>

<span data-ttu-id="a39f0-120">До Windows 8 [**D2D1 \_ Color \_ F**](d2d1-color-f.md) использует кодировку sRGB.</span><span class="sxs-lookup"><span data-stu-id="a39f0-120">Prior to Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) uses sRGB encoding.</span></span> <span data-ttu-id="a39f0-121">в кодировке sRGB цвета делятся на четыре компонента: красный, зеленый, синий и альфа.</span><span class="sxs-lookup"><span data-stu-id="a39f0-121">sRGB encoding divides colors into four components: red, green, blue, and alpha.</span></span> <span data-ttu-id="a39f0-122">Каждый компонент представлен значением с плавающей запятой, которое имеет нормальный диапазон от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-122">Each component is represented by a floating point value with a normal range of 0.0 to 1.0.</span></span> <span data-ttu-id="a39f0-123">Значение 0,0 указывает на полное отсутствие данного цвета, а значение 1,0 указывает на его максимальное присутствие.</span><span class="sxs-lookup"><span data-stu-id="a39f0-123">A value of 0.0 indicates the complete absence of that color, while a value of 1.0 indicates that the color is fully present.</span></span> <span data-ttu-id="a39f0-124">Для альфа-компонента значение 0,0 означает полностью прозрачный цвет, а 1,0 — полностью непрозрачный цвет.</span><span class="sxs-lookup"><span data-stu-id="a39f0-124">For the alpha component, 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span>

<span data-ttu-id="a39f0-125">Начиная с Windows 8, [**D2D1 \_ Color \_ F**](d2d1-color-f.md) также принимает кодирование ScRGB.</span><span class="sxs-lookup"><span data-stu-id="a39f0-125">Starting in Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) also accepts scRGB encoding.</span></span> <span data-ttu-id="a39f0-126">scRGB — это надмножество, позволяющее значения цветов выше 1,0 и ниже 0,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-126">scRGB is a superset of that allows color values above 1.0 and below 0.0.</span></span>

<span data-ttu-id="a39f0-127">Чтобы определить цвет, можно использовать структуру [**\_ цвета \_ F D2D1**](d2d1-color-f.md) и самостоятельно инициализировать свои поля. также можно использовать класс [**D2D1:: колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) , чтобы облегчить создание цвета.</span><span class="sxs-lookup"><span data-stu-id="a39f0-127">To define a color, you can use the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure and initialize its fields yourself, or you can use the [**D2D1::ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to help you create the color.</span></span> <span data-ttu-id="a39f0-128">Класс **колорф** предоставляет несколько конструкторов для определения цветов.</span><span class="sxs-lookup"><span data-stu-id="a39f0-128">The **ColorF** class provides several constructors for defining colors.</span></span> <span data-ttu-id="a39f0-129">Если значение Alpha не указано в конструкторах, по умолчанию оно равно 1,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-129">If the alpha value is not specified in the constructors, it defaults to 1.0.</span></span>

-   <span data-ttu-id="a39f0-130">Используйте конструктор [**колорф (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) , чтобы указать Стандартный цвет и значение альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="a39f0-130">Use the [**ColorF(Enum, FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) constructor to specify a predefined color and an alpha channel value.</span></span> <span data-ttu-id="a39f0-131">Значение альфа-канала лежит в диапазоне от 0,0 до 1,0, где 0,0 представляет полностью прозрачный цвет, а 1,0 — полностью непрозрачный цвет.</span><span class="sxs-lookup"><span data-stu-id="a39f0-131">An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span> <span data-ttu-id="a39f0-132">На следующем рисунке показаны несколько предопределенных цветов и их шестнадцатеричных эквивалентов.</span><span class="sxs-lookup"><span data-stu-id="a39f0-132">The following illustration shows several predefined colors and their hexadecimal equivalents.</span></span> <span data-ttu-id="a39f0-133">Полный список стандартных цветов см. в разделе Константы цвета класса [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-133">For a complete list of predefined colors, see the Color constants section of the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span>

    ![Иллюстрация предопределенных цветов](images/brushes-ovw-colors.png)

    <span data-ttu-id="a39f0-135">В следующем примере создается стандартный цвет, который используется для указания цвета [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="a39f0-135">The following example creates a predefined color and uses it to specify the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   <span data-ttu-id="a39f0-136">Используйте конструктор [**колорф (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) , чтобы указать цвет в последовательности красного, зеленого, синего и альфа-канала, где каждый элемент имеет значение от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-136">Use the [**ColorF(FLOAT, FLOAT, FLOAT, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) constructor to specify a color in the sequence of a red, green, blue, and alpha, where each element has a value between 0.0 and 1.0.</span></span>

    <span data-ttu-id="a39f0-137">В следующем примере задаются значения красного, зеленого, синего и альфа-канала для цвета.</span><span class="sxs-lookup"><span data-stu-id="a39f0-137">The following example specifies the red, green, blue, and alpha values for a color.</span></span>

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   <span data-ttu-id="a39f0-138">Используйте конструктор [**колорф (UINT32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) , чтобы указать шестнадцатеричное значение цвета и альфа-значение, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="a39f0-138">Use the [**ColorF(UINT32, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) constructor to specify the hexadecimal value of a color and an alpha value, as shown in the following example.</span></span>
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a><span data-ttu-id="a39f0-139">Режимы альфа</span><span class="sxs-lookup"><span data-stu-id="a39f0-139">Alpha modes</span></span>

<span data-ttu-id="a39f0-140">Независимо от режима альфа целевого объекта отрисовки, с помощью которого используется кисть, значения [**D2D1 \_ Color \_ F**](d2d1-color-f.md) всегда обрабатываются как прямые альфа-каналы.</span><span class="sxs-lookup"><span data-stu-id="a39f0-140">Regardless of the alpha mode of the render target with which you use a brush, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span>

## <a name="using-solid-color-brushes"></a><span data-ttu-id="a39f0-141">Использование сплошных цветных кистей</span><span class="sxs-lookup"><span data-stu-id="a39f0-141">Using solid color brushes</span></span>

<span data-ttu-id="a39f0-142">Чтобы создать сплошную цветовую кисть, вызовите метод [**ID2D1RenderTarget:: креатесолидколорбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , который возвращает значение HRESULT и объект [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-142">To create a solid color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method, which returns an HRESULT and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) object.</span></span> <span data-ttu-id="a39f0-143">На следующем рисунке показан квадрат, обводка которого является цветовая кисть с черной заливкой и окрашена сплошной цветовой кистью, имеющей значение цвета 0x9ACD32.</span><span class="sxs-lookup"><span data-stu-id="a39f0-143">The following illustration shows a square that is stroked with a black color brush and painted with a solid color brush that has the color value of 0x9ACD32.</span></span>

![Иллюстрация квадрата, окрашенного сплошной цветовой кистью](images/brushes-ovw-solidcolor.png)

<span data-ttu-id="a39f0-145">В следующем коде показано, как создать и использовать цветовую кисть и кисть с цветовым значением 0x9ACD32 для заполнения и рисования этого квадрата.</span><span class="sxs-lookup"><span data-stu-id="a39f0-145">The following code shows how to create and use a black color brush and a brush with a color value of 0x9ACD32 to fill and draw this square.</span></span>


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



<span data-ttu-id="a39f0-146">В отличие от других кистей создание [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) является относительно недорогой операцией.</span><span class="sxs-lookup"><span data-stu-id="a39f0-146">Unlike other brushes, creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is a relatively inexpensive operation.</span></span> <span data-ttu-id="a39f0-147">Вы можете создавать объекты **ID2D1SolidColorBrush** каждый раз, когда вы выполняете немалое влияние на производительность.</span><span class="sxs-lookup"><span data-stu-id="a39f0-147">You may create **ID2D1SolidColorBrush** objects each time you render with little to no performance impact.</span></span> <span data-ttu-id="a39f0-148">Этот подход не рекомендуется для градиентных или растровых кистей.</span><span class="sxs-lookup"><span data-stu-id="a39f0-148">This approach is not recommended for gradient or bitmap brushes.</span></span>

## <a name="using-linear-gradient-brushes"></a><span data-ttu-id="a39f0-149">Использование кистей линейного градиента</span><span class="sxs-lookup"><span data-stu-id="a39f0-149">Using linear gradient brushes</span></span>

<span data-ttu-id="a39f0-150">[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) закрашивает область с линейным градиентом, определенным вдоль линии, оси градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-150">An [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) paints an area with a linear gradient defined along a line, the gradient axis.</span></span> <span data-ttu-id="a39f0-151">Цвета градиента и их расположение указываются вдоль оси градиента с помощью объектов [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-151">You specify the gradient's colors and their location along the gradient axis using [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) objects.</span></span> <span data-ttu-id="a39f0-152">Можно также изменить ось градиента, которая позволяет создавать горизонтальные и вертикальные градиенты и менять направление градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-152">You may also modify the gradient axis, which enables you to create horizontal and vertical gradient and to reverse the gradient direction.</span></span> <span data-ttu-id="a39f0-153">Чтобы создать кисть линейного градиента, вызовите метод [**ID2D1RenderTarget:: креателинеарградиентбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-153">To create a linear gradient brush, call the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method.</span></span>

<span data-ttu-id="a39f0-154">На следующем рисунке показан квадрат, нарисованный с помощью [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) с двумя предопределенными цветами: "желтый" и "форестгрин".</span><span class="sxs-lookup"><span data-stu-id="a39f0-154">The following illustration shows a square that is painted with an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that has two predefined colors, "Yellow" and "ForestGreen".</span></span>

![Иллюстрация квадратной заливки с помощью кисти линейного градиента желтого цвета и зеленого леса](images/brushes-ovw-lineargradient.png)

<span data-ttu-id="a39f0-156">Чтобы создать градиент, показанный на предыдущем рисунке, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a39f0-156">To create the gradient shown in the preceding illustration, complete these steps:</span></span>

1.  <span data-ttu-id="a39f0-157">Объявите два объекта [**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-157">Declare two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="a39f0-158">Каждая позиция градиента задает цвет и расположение.</span><span class="sxs-lookup"><span data-stu-id="a39f0-158">Each gradient stop specifies a color and a position.</span></span> <span data-ttu-id="a39f0-159">Позиция 0,0 обозначает начало градиента, а позиция 1,0 — конец градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-159">A position of 0.0 indicates the beginning of the gradient, while a position of 1.0 indicates the end of the gradient.</span></span>

    <span data-ttu-id="a39f0-160">Следующий код создает массив из двух объектов [**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-160">The following code creates an array of two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="a39f0-161">Первая позиция указывает цвет "желтый" в позиции 0, а вторая — цвет "Форестгрин" в позиции 1.</span><span class="sxs-lookup"><span data-stu-id="a39f0-161">The first stop specifies the color "Yellow" at a position 0, and the second stop specifies the color "ForestGreen" at position 1.</span></span>

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  <span data-ttu-id="a39f0-162">Создайте [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="a39f0-162">Create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span> <span data-ttu-id="a39f0-163">В следующем примере вызывается [**креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), передающий массив объектов-остановок [**\_ градиента D2D1 \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , число ограничителей градиента (2), [**D2D1 \_ гамма \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) для интерполяции и [**D2D1 в \_ \_ режиме расширения \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) для режима расширения.</span><span class="sxs-lookup"><span data-stu-id="a39f0-163">The following example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passing in the array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects, the number of gradient stops (2), [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) for interpolation, and [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) for the extend mode.</span></span>

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  <span data-ttu-id="a39f0-164">Создайте [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="a39f0-164">Create the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="a39f0-165">В следующем примере вызывается метод [**креателинеарградиентбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) и ему передаются свойства кисти линейного градиента, содержащие начальную точку в (0, 0) и конечную точку в (150, 150), и градиентные остановки, созданные на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="a39f0-165">The next example calls the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and passes it the linear gradient brush properties that contain the start point at (0, 0) and the end point at (150, 150), and the gradient stops created in the previous step.</span></span>
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  <span data-ttu-id="a39f0-166">Используйте [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="a39f0-166">Use the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="a39f0-167">В следующем примере кода кисть используется для заполнения прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a39f0-167">The next code example uses the brush to fille a rectangle.</span></span>
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a><span data-ttu-id="a39f0-168">Дополнительные сведения об ограничениях градиента</span><span class="sxs-lookup"><span data-stu-id="a39f0-168">More about gradient stops</span></span>

<span data-ttu-id="a39f0-169">[**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) — это базовый строительный блок кисти градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-169">The [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) is the basic building block of a gradient brush.</span></span> <span data-ttu-id="a39f0-170">Ограничитель градиента определяет цвет и расположение вдоль оси градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-170">A gradient stop specifies the color and the position along the gradient axis.</span></span> <span data-ttu-id="a39f0-171">Значение позиции градиента в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-171">The value of the gradient position ranges between 0.0 and 1.0.</span></span> <span data-ttu-id="a39f0-172">Чем ближе это к 0,0, тем ближе цвет к началу градиента; чем ближе это к 1,0, тем ближе цвет к концу градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-172">The closer it is to 0.0, the closer the color is to the start of the gradient; the closer it is to 1.0, the closer the color is to the end of the gradient.</span></span>

<span data-ttu-id="a39f0-173">На следующем рисунке показаны ограничения градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-173">The following illustration highlights the gradient stops.</span></span> <span data-ttu-id="a39f0-174">Кружок отмечает позиции ограничителей градиента, а пунктирная линия отображает ось градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-174">The circle marks the position of gradient stops and a dashed line shows the gradient axis.</span></span>

![Иллюстрация кисти линейного градиента с четырьмя остановками вдоль оси](images/4stoplineargradient.png)

<span data-ttu-id="a39f0-176">Первая позиция градиента определяет желтый цвет в позиции 0,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-176">The first gradient stop specifies the color yellow at a position of 0.0.</span></span> <span data-ttu-id="a39f0-177">Вторая позиция градиента задает красный цвет в позиции 0,25.</span><span class="sxs-lookup"><span data-stu-id="a39f0-177">The second gradient stop specifies red color at a position of 0.25.</span></span> <span data-ttu-id="a39f0-178">Слева направо вдоль оси градиента цвета между ними постепенно меняются от желтого к красному.</span><span class="sxs-lookup"><span data-stu-id="a39f0-178">From left to right along the gradient axis, the colors between these two stops gradually change from yellow to red.</span></span> <span data-ttu-id="a39f0-179">Третья позиция градиента задает синий цвет в позиции 0,75.</span><span class="sxs-lookup"><span data-stu-id="a39f0-179">The third gradient stop specifies blue color at a position of 0.75.</span></span> <span data-ttu-id="a39f0-180">Цвета между второй и третьей позициями градиента постепенно меняются с красного на синий.</span><span class="sxs-lookup"><span data-stu-id="a39f0-180">The colors between the second and third gradient stops gradually change from red to blue.</span></span> <span data-ttu-id="a39f0-181">Четвертая позиция градиента задает травяной зеленый цвет в позиции 1,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-181">The fourth gradient stop specifies lime green at a position of 1.0.</span></span> <span data-ttu-id="a39f0-182">Цвета между третьей и четвертой позициями градиента постепенно меняются с голубого на светлое зеленым.</span><span class="sxs-lookup"><span data-stu-id="a39f0-182">The colors between the third and fourth gradient stops gradually change from blue to lime green.</span></span>

## <a name="the-gradient-axis"></a><span data-ttu-id="a39f0-183">Ось градиента</span><span class="sxs-lookup"><span data-stu-id="a39f0-183">The gradient axis</span></span>

<span data-ttu-id="a39f0-184">Как упоминалось ранее, позиции градиента кисти линейного градиента размещаются вдоль линии, оси градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-184">As mentioned previously, gradient stops of a linear gradient brush are positioned along a line, the gradient axis.</span></span> <span data-ttu-id="a39f0-185">Можно указать ориентацию и размер линии, используя поля **StartPoint** и **Endpoint** в структуре [**\_ \_ \_ \_ свойств кисти линейного градиента D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) при создании кисти линейного градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-185">You can specify the orientation and size of the line using the **startPoint** and **endPoint** fields of the [**D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) structure when you create a linear gradient brush.</span></span> <span data-ttu-id="a39f0-186">После создания кисти можно настроить ось градиента, вызвав методы [**сетстартпоинт**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) и [**сетендпоинт**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) кисти.</span><span class="sxs-lookup"><span data-stu-id="a39f0-186">After you've created a brush, you can adjust the gradient axis by calling the brush's [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) and [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) methods.</span></span> <span data-ttu-id="a39f0-187">Управляя начальной и конечной точками кисти, можно создавать горизонтальные и вертикальные градиенты, менять направление градиента и многое другое.</span><span class="sxs-lookup"><span data-stu-id="a39f0-187">By manipulating the brush's start point and end point, you can create horizontal and vertical gradients, reverse the gradient direction, and more.</span></span>

<span data-ttu-id="a39f0-188">Например, на следующем рисунке начальная точка имеет значение (0, 0) и конечную точку (150, 50); При этом создается диагональный градиент, который начинается в левом верхнем углу и расширяется в правый нижний угол закрашиваемой области.</span><span class="sxs-lookup"><span data-stu-id="a39f0-188">For example, in the following illustration, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted.</span></span> <span data-ttu-id="a39f0-189">Если задать начальную точку (0, 25) и конечную точку (150, 25), то будет создан горизонтальный градиент.</span><span class="sxs-lookup"><span data-stu-id="a39f0-189">When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created.</span></span> <span data-ttu-id="a39f0-190">Аналогично, если задать для начальной точки (75, 0), а конечной точки — (75, 50), то будет создан вертикальный градиент.</span><span class="sxs-lookup"><span data-stu-id="a39f0-190">Similarly, setting the start point to (75, 0) and the end point to (75, 50) creates a vertical gradient.</span></span> <span data-ttu-id="a39f0-191">Установка начальной точки (0, 50) и конечной точки (150, 0) создает диагональный градиент, который начинается в левом нижнем углу и расширяется в правый верхний угол закрашиваемой области.</span><span class="sxs-lookup"><span data-stu-id="a39f0-191">Setting the start point to (0, 50) and the end point to (150, 0) creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.</span></span>

![Иллюстрация четырех различных осей градиента в пределах одного прямоугольника](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a><span data-ttu-id="a39f0-193">Использование кистей радиального градиента</span><span class="sxs-lookup"><span data-stu-id="a39f0-193">Using radial gradient brushes</span></span>

<span data-ttu-id="a39f0-194">В отличие от [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), который смешивает два или более цвета вдоль оси градиента, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) закрашивает область с радиальным градиентом, который смешивает два или более цветов в эллипсе.</span><span class="sxs-lookup"><span data-stu-id="a39f0-194">Unlike an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), which blends two or more colors along a gradient axis, an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) paints an area with a radial gradient that blends two or more colors across an ellipse.</span></span> <span data-ttu-id="a39f0-195">Хотя **ID2D1LinearGradientBrush** определяет свою ось градиента с начальной и конечной точкой, **ID2D1RadialGradientBrush** определяет градиентный эллипс, указывая Центральный, горизонтальный и вертикальный радиусы и смещение источника градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-195">While a **ID2D1LinearGradientBrush** defines its gradient axis with a start point and an end point, a **ID2D1RadialGradientBrush** defines its gradient ellipse by specifying a center, horizontal and vertical radii, and a gradient origin offset.</span></span>

<span data-ttu-id="a39f0-196">Как и [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) использует [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) для указания цветов и позиций в градиенте.</span><span class="sxs-lookup"><span data-stu-id="a39f0-196">Like an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) uses an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to specify the colors and positions in the gradient.</span></span>

<span data-ttu-id="a39f0-197">На следующем рисунке показан круг, нарисованный с помощью [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="a39f0-197">The following illustration shows a circle painted with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span> <span data-ttu-id="a39f0-198">Окружность имеет две остановки градиента: первый указывает Стандартный цвет "желтый" в позиции 0,0, а второй указывает предопределенный цвет "Форестгрин" в позиции 1,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-198">The circle has two gradient stops: the first specifies a predefined color "Yellow" at a position of 0.0, and the second specifies a predefined color "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="a39f0-199">Градиент имеет центр (75, 75), смещение источника градиента (0, 0) и x-and y-радиус 75.</span><span class="sxs-lookup"><span data-stu-id="a39f0-199">The gradient has a center of (75, 75), a gradient origin offset of (0, 0), and an x- and y-radius of 75.</span></span>

![Иллюстрация круга, окрашенного в кисть радиального градиента](images/brushes-ovw-radials.png)

<span data-ttu-id="a39f0-201">В следующих примерах кода показано, как закрасить этот круг с помощью [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) с двумя пределами цвета: "желтый" в позиции 0,0 и "форестгрин" в позиции 1,0.</span><span class="sxs-lookup"><span data-stu-id="a39f0-201">The following code examples shows how to paint this circle with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that has two color stops: "Yellow" at a position of 0.0, and "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="a39f0-202">Как и при создании [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), в примере вызывается [**Креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) для создания [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) из массива точек градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-202">Similar to creating an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), the example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from an array of gradient stops.</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="a39f0-203">Чтобы создать [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), используйте метод [**ID2D1RenderTarget:: креатерадиалградиентбруш**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-203">To create an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use the [**ID2D1RenderTarget::CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) method.</span></span> <span data-ttu-id="a39f0-204">**Креатерадиалградиентбруш** принимает три параметра.</span><span class="sxs-lookup"><span data-stu-id="a39f0-204">The **CreateRadialGradientBrush** takes three parameters.</span></span> <span data-ttu-id="a39f0-205">Первый параметр, [**\_ \_ \_ \_ Свойства кисти радиального градиента D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) , задает центр, смещение источника градиента и горизонтальный и вертикальный радиусы градиента.</span><span class="sxs-lookup"><span data-stu-id="a39f0-205">The first parameter, a [**D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) specifies the center, gradient origin offset, and the horizontal and vertical radii of the gradient.</span></span> <span data-ttu-id="a39f0-206">Второй параметр — это [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) , описывающий цвета и их позиции в градиенте, а третий параметр — адрес указателя, получающего новую ссылку **ID2D1RadialGradientBrush** .</span><span class="sxs-lookup"><span data-stu-id="a39f0-206">The second parameter is an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) that describes the colors and their positions in the gradient, and the third parameter is the address of the pointer that receive the new **ID2D1RadialGradientBrush** reference.</span></span> <span data-ttu-id="a39f0-207">Некоторые перегрузки принимают дополнительный параметр — структуру [**свойств D2D1 \_ Brush \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) , которая задает значение непрозрачности и преобразование, применяемое к новой кисти.</span><span class="sxs-lookup"><span data-stu-id="a39f0-207">Some overloads take an additional parameter, a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) structure that specifies an opacity value and a transform to apply to the new brush.</span></span>

<span data-ttu-id="a39f0-208">В следующем примере вызывается [**креатерадиалградиентбруш**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), передается массив ограничителей градиента и свойства кисти радиального градиента, для которых в качестве *центра* задано значение (75, 75), *градиенторигиноффсет* задаются равными (0, 0), а *RadiusX* и *радиусу* — 75.</span><span class="sxs-lookup"><span data-stu-id="a39f0-208">The next example calls [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passing in the array of gradient stops, and the radial gradient brush properties that have the *center* value set to (75, 75), the *gradientOriginOffset* set to (0, 0), and *radiusX* and *radiusY* both set to 75.</span></span>


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



<span data-ttu-id="a39f0-209">В последнем примере кисть используется для заполнения эллипса.</span><span class="sxs-lookup"><span data-stu-id="a39f0-209">The final example uses the brush to fill an ellipse.</span></span>


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a><span data-ttu-id="a39f0-210">Настройка радиального градиента</span><span class="sxs-lookup"><span data-stu-id="a39f0-210">Configuring a radial gradient</span></span>

<span data-ttu-id="a39f0-211">Различные значения для *Center*, *градиенторигиноффсет*, *RadiusX* и (или) *RADIUS* создают различные градиенты.</span><span class="sxs-lookup"><span data-stu-id="a39f0-211">Different values for *center*, *gradientOriginOffset*, *radiusX* and/or *radiusY* produce different gradients.</span></span> <span data-ttu-id="a39f0-212">На следующем рисунке показано несколько радиальных градиентов с разными смещениями источника градиента, создавая внешний вид освещения, который освещает круги из разных углов.</span><span class="sxs-lookup"><span data-stu-id="a39f0-212">The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.</span></span>

![Иллюстрация того же круга, окрашенного в кисти радиального градиента с разными смещениями источника](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a><span data-ttu-id="a39f0-214">Использование растровых кистей</span><span class="sxs-lookup"><span data-stu-id="a39f0-214">Using bitmap brushes</span></span>

<span data-ttu-id="a39f0-215">[**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) заполняет область растровым изображением (представленным объектом [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).</span><span class="sxs-lookup"><span data-stu-id="a39f0-215">An [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) paints an area with a bitmap (represented by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object).</span></span>

<span data-ttu-id="a39f0-216">На следующем рисунке показана квадратная закрашенная с растровым изображением растения.</span><span class="sxs-lookup"><span data-stu-id="a39f0-216">The following illustration shows a square painted with a bitmap of a plant.</span></span>

![Иллюстрация квадратного рисунка с изображением завода](images/brushes-ovw-bitmap.png)

<span data-ttu-id="a39f0-218">В приведенных ниже примерах показано, как закрасить этот квадрат с помощью [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="a39f0-218">The examples that follow shows how to paint this square with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>

<span data-ttu-id="a39f0-219">В первом примере инициализируется [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) для использования с кистью.</span><span class="sxs-lookup"><span data-stu-id="a39f0-219">The first example initializes an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) for use with the brush.</span></span> <span data-ttu-id="a39f0-220">**ID2D1Bitmap** предоставляется вспомогательным методом лоадресаурцебитмап, который определен в любом расположении в образце.</span><span class="sxs-lookup"><span data-stu-id="a39f0-220">The **ID2D1Bitmap** is provided by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



<span data-ttu-id="a39f0-221">Чтобы создать растровую кисть, вызовите метод [**ID2D1RenderTarget:: креатебитмапбруш**](id2d1rendertarget-createbitmapbrush.md) и укажите [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) для рисования.</span><span class="sxs-lookup"><span data-stu-id="a39f0-221">To create the bitmap brush, call the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with which to paint.</span></span> <span data-ttu-id="a39f0-222">Метод возвращает **значение HRESULT** и объект [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-222">The method returns an **HRESULT** and an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) object.</span></span> <span data-ttu-id="a39f0-223">Некоторые перегрузки **креатебитмапбруш** позволяют указать дополнительные параметры, приняв [**D2D1 \_ \_ Свойства кисти**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) и структуру [**\_ \_ \_ свойств Bitmap**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .</span><span class="sxs-lookup"><span data-stu-id="a39f0-223">Some **CreateBitmapBrush** overloads enable you to specify additional options by accepting a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) and a [**D2D1\_BITMAP\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) structure.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



<span data-ttu-id="a39f0-224">В следующем примере кисть используется для заливки прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="a39f0-224">The next example uses the brush to fill a rectangle.</span></span>


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a><span data-ttu-id="a39f0-225">Настройка режимов расширения</span><span class="sxs-lookup"><span data-stu-id="a39f0-225">Configuring extend modes</span></span>

<span data-ttu-id="a39f0-226">Иногда градиент кисти градиента или точечный рисунок для растровой кисти не полностью заполняет закрашиваемую область.</span><span class="sxs-lookup"><span data-stu-id="a39f0-226">Sometimes, the gradient of a gradient brush or the bitmap for a bitmap brush doesn't completely fill the area being painted.</span></span>

-   <span data-ttu-id="a39f0-227">Когда это происходит для [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D использует параметры горизонтального ([**сетекстендмодекс**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) и вертикального ([**сетекстендмодэй**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) расширения кисти для определения способа заполнения оставшейся области.</span><span class="sxs-lookup"><span data-stu-id="a39f0-227">When this happens for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D uses the brush's horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) and vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) extend mode settings to determine how to fill the remaining area.</span></span>

-   <span data-ttu-id="a39f0-228">Если это происходит для градиентной кисти, Direct2D определяет, как заполнять оставшуюся область с помощью значения параметра [**\_ \_ режима расширения D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) , указанного при вызове [**креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) для создания [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)градиентной кисти.</span><span class="sxs-lookup"><span data-stu-id="a39f0-228">When this happens for a gradient brush, Direct2D determines how to fill the remaining area by using the value of the [**D2D1\_EXTEND\_MODE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) parameter that you specified when you called the [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create the gradient brush's [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>

<span data-ttu-id="a39f0-229">На следующем рисунке показаны результаты каждого возможного сочетания режимов расширения для [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): D2D1 (зажим) в [**\_ \_ режиме \_ расширения**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) , **D2D1 \_ \_ \_ переносить по словам** (wrap) и **D2D1 \_ расширять \_ зеркало** (зеркало).</span><span class="sxs-lookup"><span data-stu-id="a39f0-229">The following illustration shows the results from every possible combination of the extend modes for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (CLAMP), **D2D1\_EXTEND\_MODE\_WRAP** (WRAP), and **D2D1\_EXTEND\_MIRROR** (MIRROR).</span></span>

![Иллюстрация исходного изображения и полученных изображений из различных режимов расширения](images/bitmapwrap-clamp-mirror.png)

<span data-ttu-id="a39f0-231">В следующем примере показано, как установить режимы расширения x и y растровой кисти для [**D2D1 \_ расширения \_ Mirror**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="a39f0-231">The following example shows how to set the bitmap brush's x- and y-extend modes to [**D2D1\_EXTEND\_MIRROR**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span> <span data-ttu-id="a39f0-232">Затем он рисует прямоугольник с помощью [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="a39f0-232">It then paints the rectangle with the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



<span data-ttu-id="a39f0-233">Выводится результат, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="a39f0-233">It produces output as shown in the following illustration.</span></span>

![Иллюстрация исходного изображения и полученного изображения после отражения оси x и направления по оси y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a><span data-ttu-id="a39f0-235">Преобразование кистей</span><span class="sxs-lookup"><span data-stu-id="a39f0-235">Transforming brushes</span></span>

<span data-ttu-id="a39f0-236">При рисовании с помощью кисти она рисуется в пространстве координат целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="a39f0-236">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="a39f0-237">Кисти не размещаются автоматически, чтобы они совпадали с закрашиваемым объектом; по умолчанию они начинают рисовать в источнике (0, 0) целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="a39f0-237">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="a39f0-238">Можно «переместить» градиент, определенный [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , в целевую область, задав его начальную и конечную точки.</span><span class="sxs-lookup"><span data-stu-id="a39f0-238">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="a39f0-239">Аналогичным образом можно переместить градиент, определенный [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , изменив его центр и радиусы.</span><span class="sxs-lookup"><span data-stu-id="a39f0-239">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="a39f0-240">Чтобы согласовать содержимое [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с закрашиваемой областью, можно использовать метод [**сеттрансформ**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) для преобразования растрового изображения в нужное место.</span><span class="sxs-lookup"><span data-stu-id="a39f0-240">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="a39f0-241">Это преобразование влияет только на кисть. Он не влияет на содержимое, рисуемое целевым объектом рендеринга.</span><span class="sxs-lookup"><span data-stu-id="a39f0-241">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="a39f0-242">На следующих иллюстрациях показан результат использования [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для заполнения прямоугольника, расположенного в (100, 100).</span><span class="sxs-lookup"><span data-stu-id="a39f0-242">The following illustrations shows the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="a39f0-243">На рисунке слева показан результат заполнения прямоугольника без преобразования кисти: точечный рисунок отображается в источнике целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="a39f0-243">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="a39f0-244">В результате в прямоугольнике появляется только часть точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="a39f0-244">As a result, only a portion of the bitmap appears in the rectangle.</span></span> <span data-ttu-id="a39f0-245">На рисунке справа показан результат преобразования **ID2D1BitmapBrush** , чтобы его содержимое было смещено на 50 пикселей вправо и 50 пикселей вниз.</span><span class="sxs-lookup"><span data-stu-id="a39f0-245">The illustration on the right shows the result of transforming the **ID2D1BitmapBrush** so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="a39f0-246">Теперь точечный рисунок заполняет прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="a39f0-246">The bitmap now fills the rectangle.</span></span>

![Иллюстрация квадрата, нарисованного с помощью растровой кисти, без преобразования кисти и преобразования кисти](images/brushes-ovw-transform.png)

<span data-ttu-id="a39f0-248">В следующем коде показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="a39f0-248">The following code shows how to accomplish this.</span></span> <span data-ttu-id="a39f0-249">Сначала примените перевод к [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), переместив кисть 50 пикселей вправо вдоль оси x и 50 пикселей вниз по оси y.</span><span class="sxs-lookup"><span data-stu-id="a39f0-249">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="a39f0-250">Затем используйте **ID2D1BitmapBrush** для заполнения прямоугольника с верхним левым углом в (100, 100) и правом нижнем углу в (200, 200).</span><span class="sxs-lookup"><span data-stu-id="a39f0-250">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a><span data-ttu-id="a39f0-251">См. также</span><span class="sxs-lookup"><span data-stu-id="a39f0-251">Related topics</span></span>

* [<span data-ttu-id="a39f0-252">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="a39f0-252">Direct2D reference</span></span>](reference.md)
* [<span data-ttu-id="a39f0-253">Создание сплошной кисти цвета</span><span class="sxs-lookup"><span data-stu-id="a39f0-253">How to create a solid color brush</span></span>](how-to-create-a-solid-color-brush.md)
* [<span data-ttu-id="a39f0-254">Создание кисти линейного градиента</span><span class="sxs-lookup"><span data-stu-id="a39f0-254">How to create a linear gradient brush</span></span>](how-to-create-a-linear-gradient-brush.md)
* [<span data-ttu-id="a39f0-255">Создание кисти радиального градиента</span><span class="sxs-lookup"><span data-stu-id="a39f0-255">How to create a radial gradient brush</span></span>](how-to-create-a-radial-gradient-brush.md)
* [<span data-ttu-id="a39f0-256">Создание растровой кисти</span><span class="sxs-lookup"><span data-stu-id="a39f0-256">How to create a bitmap brush</span></span>](how-to-create-a-bitmap-brush.md)
