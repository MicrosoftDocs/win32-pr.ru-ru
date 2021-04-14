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
# <a name="brushes-overview"></a>Обзор кистей 

В этом обзоре описывается создание и использование объектов [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)и [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для заливки областей сплошными цветами, градиентами и точечными рисунками. В него входят следующие разделы.

## <a name="prerequisites"></a>Предварительные условия

В этом обзоре предполагается, что вы знакомы с структурой базового приложения Direct2D, как описано в разделе [Создание простого приложения Direct2D](direct2d-quickstart.md).

## <a name="brush-types"></a>Типы кистей

Кисть закрашивает область с выходными данными. Разные кисти имеют различные типы выводимых данных. Direct2D предоставляет четыре типа кистей: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) закрашивает область сплошным цветом, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) с линейным градиентом, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) с радиальным градиентом и [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с растровым изображением.

> [!NOTE]  
> Начиная с Windows 8, можно также использовать [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), который похож на растровую кисть, но также можно использовать примитивы.

Все кисти наследуют от [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) и совместно используют набор общих функций (Установка и получение непрозрачности и преобразование кистей); они создаются [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) и являются ресурсами, зависящими от устройства. приложение должно создавать кисти после инициализации целевого объекта рендеринга, с которым будут использоваться кисти, и повторно создавать кисти при необходимости повторного создания целевого объекта отрисовки. (Дополнительные сведения о ресурсах см. в разделе [Общие сведения о ресурсах](resources-and-resource-domains.md).)

На следующем рисунке показаны примеры различных типов кистей.

![Иллюстрация визуальных эффектов от сплошных цветных кистей, кистей линейного градиента, кистей радиального градиента и растровых кистей](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a>Основы цвета

Перед началом рисования с помощью [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) или градиентной кисти необходимо выбрать цвета. В Direct2D цвета представлены структурой [**D2D1 \_ Color \_ F**](d2d1-color-f.md) (на самом деле это только новое имя для структуры, используемой Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).

До Windows 8 [**D2D1 \_ Color \_ F**](d2d1-color-f.md) использует кодировку sRGB. в кодировке sRGB цвета делятся на четыре компонента: красный, зеленый, синий и альфа. Каждый компонент представлен значением с плавающей запятой, которое имеет нормальный диапазон от 0,0 до 1,0. Значение 0,0 указывает на полное отсутствие данного цвета, а значение 1,0 указывает на его максимальное присутствие. Для альфа-компонента значение 0,0 означает полностью прозрачный цвет, а 1,0 — полностью непрозрачный цвет.

Начиная с Windows 8, [**D2D1 \_ Color \_ F**](d2d1-color-f.md) также принимает кодирование ScRGB. scRGB — это надмножество, позволяющее значения цветов выше 1,0 и ниже 0,0.

Чтобы определить цвет, можно использовать структуру [**\_ цвета \_ F D2D1**](d2d1-color-f.md) и самостоятельно инициализировать свои поля. также можно использовать класс [**D2D1:: колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) , чтобы облегчить создание цвета. Класс **колорф** предоставляет несколько конструкторов для определения цветов. Если значение Alpha не указано в конструкторах, по умолчанию оно равно 1,0.

-   Используйте конструктор [**колорф (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) , чтобы указать Стандартный цвет и значение альфа-канала. Значение альфа-канала лежит в диапазоне от 0,0 до 1,0, где 0,0 представляет полностью прозрачный цвет, а 1,0 — полностью непрозрачный цвет. На следующем рисунке показаны несколько предопределенных цветов и их шестнадцатеричных эквивалентов. Полный список стандартных цветов см. в разделе Константы цвета класса [**колорф**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .

    ![Иллюстрация предопределенных цветов](images/brushes-ovw-colors.png)

    В следующем примере создается стандартный цвет, который используется для указания цвета [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   Используйте конструктор [**колорф (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) , чтобы указать цвет в последовательности красного, зеленого, синего и альфа-канала, где каждый элемент имеет значение от 0,0 до 1,0.

    В следующем примере задаются значения красного, зеленого, синего и альфа-канала для цвета.

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   Используйте конструктор [**колорф (UINT32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) , чтобы указать шестнадцатеричное значение цвета и альфа-значение, как показано в следующем примере.
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a>Режимы альфа

Независимо от режима альфа целевого объекта отрисовки, с помощью которого используется кисть, значения [**D2D1 \_ Color \_ F**](d2d1-color-f.md) всегда обрабатываются как прямые альфа-каналы.

## <a name="using-solid-color-brushes"></a>Использование сплошных цветных кистей

Чтобы создать сплошную цветовую кисть, вызовите метод [**ID2D1RenderTarget:: креатесолидколорбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , который возвращает значение HRESULT и объект [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) . На следующем рисунке показан квадрат, обводка которого является цветовая кисть с черной заливкой и окрашена сплошной цветовой кистью, имеющей значение цвета 0x9ACD32.

![Иллюстрация квадрата, окрашенного сплошной цветовой кистью](images/brushes-ovw-solidcolor.png)

В следующем коде показано, как создать и использовать цветовую кисть и кисть с цветовым значением 0x9ACD32 для заполнения и рисования этого квадрата.


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



В отличие от других кистей создание [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) является относительно недорогой операцией. Вы можете создавать объекты **ID2D1SolidColorBrush** каждый раз, когда вы выполняете немалое влияние на производительность. Этот подход не рекомендуется для градиентных или растровых кистей.

## <a name="using-linear-gradient-brushes"></a>Использование кистей линейного градиента

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) закрашивает область с линейным градиентом, определенным вдоль линии, оси градиента. Цвета градиента и их расположение указываются вдоль оси градиента с помощью объектов [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) . Можно также изменить ось градиента, которая позволяет создавать горизонтальные и вертикальные градиенты и менять направление градиента. Чтобы создать кисть линейного градиента, вызовите метод [**ID2D1RenderTarget:: креателинеарградиентбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .

На следующем рисунке показан квадрат, нарисованный с помощью [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) с двумя предопределенными цветами: "желтый" и "форестгрин".

![Иллюстрация квадратной заливки с помощью кисти линейного градиента желтого цвета и зеленого леса](images/brushes-ovw-lineargradient.png)

Чтобы создать градиент, показанный на предыдущем рисунке, выполните следующие действия.

1.  Объявите два объекта [**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Каждая позиция градиента задает цвет и расположение. Позиция 0,0 обозначает начало градиента, а позиция 1,0 — конец градиента.

    Следующий код создает массив из двух объектов [**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) . Первая позиция указывает цвет "желтый" в позиции 0, а вторая — цвет "Форестгрин" в позиции 1.

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

    

2.  Создайте [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection). В следующем примере вызывается [**креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), передающий массив объектов-остановок [**\_ градиента D2D1 \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , число ограничителей градиента (2), [**D2D1 \_ гамма \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) для интерполяции и [**D2D1 в \_ \_ режиме расширения \_**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) для режима расширения.

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

    

3.  Создайте [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). В следующем примере вызывается метод [**креателинеарградиентбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) и ему передаются свойства кисти линейного градиента, содержащие начальную точку в (0, 0) и конечную точку в (150, 150), и градиентные остановки, созданные на предыдущем шаге.
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

    

4.  Используйте [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). В следующем примере кода кисть используется для заполнения прямоугольника.
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a>Дополнительные сведения об ограничениях градиента

[**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) — это базовый строительный блок кисти градиента. Ограничитель градиента определяет цвет и расположение вдоль оси градиента. Значение позиции градиента в диапазоне от 0,0 до 1,0. Чем ближе это к 0,0, тем ближе цвет к началу градиента; чем ближе это к 1,0, тем ближе цвет к концу градиента.

На следующем рисунке показаны ограничения градиента. Кружок отмечает позиции ограничителей градиента, а пунктирная линия отображает ось градиента.

![Иллюстрация кисти линейного градиента с четырьмя остановками вдоль оси](images/4stoplineargradient.png)

Первая позиция градиента определяет желтый цвет в позиции 0,0. Вторая позиция градиента задает красный цвет в позиции 0,25. Слева направо вдоль оси градиента цвета между ними постепенно меняются от желтого к красному. Третья позиция градиента задает синий цвет в позиции 0,75. Цвета между второй и третьей позициями градиента постепенно меняются с красного на синий. Четвертая позиция градиента задает травяной зеленый цвет в позиции 1,0. Цвета между третьей и четвертой позициями градиента постепенно меняются с голубого на светлое зеленым.

## <a name="the-gradient-axis"></a>Ось градиента

Как упоминалось ранее, позиции градиента кисти линейного градиента размещаются вдоль линии, оси градиента. Можно указать ориентацию и размер линии, используя поля **StartPoint** и **Endpoint** в структуре [**\_ \_ \_ \_ свойств кисти линейного градиента D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) при создании кисти линейного градиента. После создания кисти можно настроить ось градиента, вызвав методы [**сетстартпоинт**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) и [**сетендпоинт**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) кисти. Управляя начальной и конечной точками кисти, можно создавать горизонтальные и вертикальные градиенты, менять направление градиента и многое другое.

Например, на следующем рисунке начальная точка имеет значение (0, 0) и конечную точку (150, 50); При этом создается диагональный градиент, который начинается в левом верхнем углу и расширяется в правый нижний угол закрашиваемой области. Если задать начальную точку (0, 25) и конечную точку (150, 25), то будет создан горизонтальный градиент. Аналогично, если задать для начальной точки (75, 0), а конечной точки — (75, 50), то будет создан вертикальный градиент. Установка начальной точки (0, 50) и конечной точки (150, 0) создает диагональный градиент, который начинается в левом нижнем углу и расширяется в правый верхний угол закрашиваемой области.

![Иллюстрация четырех различных осей градиента в пределах одного прямоугольника](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a>Использование кистей радиального градиента

В отличие от [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), который смешивает два или более цвета вдоль оси градиента, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) закрашивает область с радиальным градиентом, который смешивает два или более цветов в эллипсе. Хотя **ID2D1LinearGradientBrush** определяет свою ось градиента с начальной и конечной точкой, **ID2D1RadialGradientBrush** определяет градиентный эллипс, указывая Центральный, горизонтальный и вертикальный радиусы и смещение источника градиента.

Как и [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) использует [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) для указания цветов и позиций в градиенте.

На следующем рисунке показан круг, нарисованный с помощью [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush). Окружность имеет две остановки градиента: первый указывает Стандартный цвет "желтый" в позиции 0,0, а второй указывает предопределенный цвет "Форестгрин" в позиции 1,0. Градиент имеет центр (75, 75), смещение источника градиента (0, 0) и x-and y-радиус 75.

![Иллюстрация круга, окрашенного в кисть радиального градиента](images/brushes-ovw-radials.png)

В следующих примерах кода показано, как закрасить этот круг с помощью [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) с двумя пределами цвета: "желтый" в позиции 0,0 и "форестгрин" в позиции 1,0. Как и при создании [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), в примере вызывается [**Креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) для создания [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) из массива точек градиента.


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



Чтобы создать [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), используйте метод [**ID2D1RenderTarget:: креатерадиалградиентбруш**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) . **Креатерадиалградиентбруш** принимает три параметра. Первый параметр, [**\_ \_ \_ \_ Свойства кисти радиального градиента D2D1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) , задает центр, смещение источника градиента и горизонтальный и вертикальный радиусы градиента. Второй параметр — это [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) , описывающий цвета и их позиции в градиенте, а третий параметр — адрес указателя, получающего новую ссылку **ID2D1RadialGradientBrush** . Некоторые перегрузки принимают дополнительный параметр — структуру [**свойств D2D1 \_ Brush \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) , которая задает значение непрозрачности и преобразование, применяемое к новой кисти.

В следующем примере вызывается [**креатерадиалградиентбруш**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), передается массив ограничителей градиента и свойства кисти радиального градиента, для которых в качестве *центра* задано значение (75, 75), *градиенторигиноффсет* задаются равными (0, 0), а *RadiusX* и *радиусу* — 75.


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



В последнем примере кисть используется для заполнения эллипса.


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a>Настройка радиального градиента

Различные значения для *Center*, *градиенторигиноффсет*, *RadiusX* и (или) *RADIUS* создают различные градиенты. На следующем рисунке показано несколько радиальных градиентов с разными смещениями источника градиента, создавая внешний вид освещения, который освещает круги из разных углов.

![Иллюстрация того же круга, окрашенного в кисти радиального градиента с разными смещениями источника](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a>Использование растровых кистей

[**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) заполняет область растровым изображением (представленным объектом [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).

На следующем рисунке показана квадратная закрашенная с растровым изображением растения.

![Иллюстрация квадратного рисунка с изображением завода](images/brushes-ovw-bitmap.png)

В приведенных ниже примерах показано, как закрасить этот квадрат с помощью [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).

В первом примере инициализируется [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) для использования с кистью. **ID2D1Bitmap** предоставляется вспомогательным методом лоадресаурцебитмап, который определен в любом расположении в образце.


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



Чтобы создать растровую кисть, вызовите метод [**ID2D1RenderTarget:: креатебитмапбруш**](id2d1rendertarget-createbitmapbrush.md) и укажите [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) для рисования. Метод возвращает **значение HRESULT** и объект [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) . Некоторые перегрузки **креатебитмапбруш** позволяют указать дополнительные параметры, приняв [**D2D1 \_ \_ Свойства кисти**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) и структуру [**\_ \_ \_ свойств Bitmap**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



В следующем примере кисть используется для заливки прямоугольника.


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a>Настройка режимов расширения

Иногда градиент кисти градиента или точечный рисунок для растровой кисти не полностью заполняет закрашиваемую область.

-   Когда это происходит для [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D использует параметры горизонтального ([**сетекстендмодекс**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) и вертикального ([**сетекстендмодэй**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) расширения кисти для определения способа заполнения оставшейся области.

-   Если это происходит для градиентной кисти, Direct2D определяет, как заполнять оставшуюся область с помощью значения параметра [**\_ \_ режима расширения D2D1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) , указанного при вызове [**креатеградиентстопколлектион**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) для создания [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)градиентной кисти.

На следующем рисунке показаны результаты каждого возможного сочетания режимов расширения для [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): D2D1 (зажим) в [**\_ \_ режиме \_ расширения**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) , **D2D1 \_ \_ \_ переносить по словам** (wrap) и **D2D1 \_ расширять \_ зеркало** (зеркало).

![Иллюстрация исходного изображения и полученных изображений из различных режимов расширения](images/bitmapwrap-clamp-mirror.png)

В следующем примере показано, как установить режимы расширения x и y растровой кисти для [**D2D1 \_ расширения \_ Mirror**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode). Затем он рисует прямоугольник с помощью [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



Выводится результат, как показано на следующем рисунке.

![Иллюстрация исходного изображения и полученного изображения после отражения оси x и направления по оси y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a>Преобразование кистей

При рисовании с помощью кисти она рисуется в пространстве координат целевого объекта отрисовки. Кисти не размещаются автоматически, чтобы они совпадали с закрашиваемым объектом; по умолчанию они начинают рисовать в источнике (0, 0) целевого объекта отрисовки.

Можно «переместить» градиент, определенный [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) , в целевую область, задав его начальную и конечную точки. Аналогичным образом можно переместить градиент, определенный [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) , изменив его центр и радиусы.

Чтобы согласовать содержимое [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) с закрашиваемой областью, можно использовать метод [**сеттрансформ**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) для преобразования растрового изображения в нужное место. Это преобразование влияет только на кисть. Он не влияет на содержимое, рисуемое целевым объектом рендеринга.

На следующих иллюстрациях показан результат использования [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) для заполнения прямоугольника, расположенного в (100, 100). На рисунке слева показан результат заполнения прямоугольника без преобразования кисти: точечный рисунок отображается в источнике целевого объекта рендеринга. В результате в прямоугольнике появляется только часть точечного рисунка. На рисунке справа показан результат преобразования **ID2D1BitmapBrush** , чтобы его содержимое было смещено на 50 пикселей вправо и 50 пикселей вниз. Теперь точечный рисунок заполняет прямоугольник.

![Иллюстрация квадрата, нарисованного с помощью растровой кисти, без преобразования кисти и преобразования кисти](images/brushes-ovw-transform.png)

В следующем коде показано, как это сделать. Сначала примените перевод к [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), переместив кисть 50 пикселей вправо вдоль оси x и 50 пикселей вниз по оси y. Затем используйте **ID2D1BitmapBrush** для заполнения прямоугольника с верхним левым углом в (100, 100) и правом нижнем углу в (200, 200).


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

## <a name="related-topics"></a>См. также

* [Справочник по Direct2D](reference.md)
* [Создание сплошной кисти цвета](how-to-create-a-solid-color-brush.md)
* [Создание кисти линейного градиента](how-to-create-a-linear-gradient-brush.md)
* [Создание кисти радиального градиента](how-to-create-a-radial-gradient-brush.md)
* [Создание растровой кисти](how-to-create-a-bitmap-brush.md)
