---
title: Применение эффектов к примитивам
description: в этом разделе показано, как применить ряд эффектов к примитивам Direct2D и DirectWrite.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17cbf1efe17d1c23c90382f3b95fb41e33946a93935b0be02fc5b41f314a8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569599"
---
# <a name="how-to-apply-effects-to-primitives"></a>Применение эффектов к примитивам

в этом разделе показано, как применить ряд эффектов к примитивам [Direct2D](./direct2d-portal.md) и [DirectWrite](direct2d-and-directwrite.md) .

[API эффектов Direct2D](effects-overview.md) можно использовать для применения графов эффектов к примитивам, отображаемым [Direct2D](./direct2d-portal.md) в изображении. В примере ниже два скругленных прямоугольника и текст «Direct2D». используйте Direct2D для рисования прямоугольников и [DirectWrite](direct2d-and-directwrite.md) для рисования текста.

![прямоугольники с текстом «Direct2D» в.](images/direct2d-rounded.png)

Используя [эффекты Direct2D](effects-overview.md), можно сделать этот образ похожим на следующее изображение. Примените [Размытие по Гауссу](gaussian-blur.md), [поточечное освещение](specular-lighting.md), [арифметические составные](arithmetic-composite.md)и [Составные](composite.md) эффекты к 2D-примитивам, чтобы создать изображение здесь.

![прямоугольники с текстом «Direct2D» внутри после применения нескольких эффектов.](images/direct2d-svg.png)

После отрисовки прямоугольников и текста на промежуточной поверхности можно использовать его в качестве входных данных для объектов [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) в графе изображения.

В этом примере установите исходное изображение в качестве входных данных для [эффект размытия по Гауссу](gaussian-blur.md) , а затем установите выходные данные размытия в качестве входных данных для [эффектов отраженного освещения точки](specular-lighting.md). Затем результат этого действия совмещен с исходным изображением дважды для получения окончательного изображения, отображаемого в окне.

Ниже приведена схема графа изображения.

![Диаграмма графа эффектов.](images/effect-graph.png)

Эта диаграмма эффектов состоит из четырех объектов [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , каждый из которых представляет отдельный встроенный результат. Вы можете создавать и подключать пользовательские эффекты таким же образом после их регистрации с помощью [**ID1D1Factory1:: регистереффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring). Этот код создает эффекты, устанавливает свойства и подключается к показанной выше диаграмме эффектов.

1.  Создайте эффект [размытия по Гауссу](gaussian-blur.md) с помощью метода [**ID2D1DeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) и укажите правильный идентификатор CLSID. Идентификаторы CLSID для встроенных эффектов определяются в d2d1effects. h. Затем вы устанавливаете стандартное отклонение размытия с помощью метода [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    Эффект [размытия по Гауссу](gaussian-blur.md) выполняет размытие всех каналов изображения, включая альфа-канал.

2.  Создайте эффекты [отраженного освещения](point-specular.md) и задайте свойства. Положением освещения является вектор из 3 значений с плавающей запятой, поэтому его необходимо объявить как отдельную переменную и передать в метод [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) .

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    В результате [отраженного освещения](point-specular.md) используется альфа-канал входных данных, чтобы создать карту высоты для освещения.

3.  Существует два различных составных эффекта, с помощью которых можно использовать [составной](composite.md) эффект и [арифметическое составное](arithmetic-composite.md)действие. На этой диаграмме эффектов используются оба.

    Создайте [составной](composite.md) эффекты и задайте для режима режим D2D1 \_ составного \_ \_ источника \_ в, который выводит пересечение исходного и целевого образов.

    [Арифметический составной](arithmetic-composite.md) результат объединяет два входных изображения на основе формулы, определенной консорциум W3C (W3C) для стандарта масштабируемой векторной графики (SVG). Создайте арифметическое составное выражение и задайте коэффициенты для формулы.

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    Коэффициенты для [арифметических составных](arithmetic-composite.md) эффектов показаны здесь.

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    На этой диаграмме эффекта оба составных эффекта принимают выходные данные других эффектов и промежуточную поверхность в качестве входных и их составных.

4.  Наконец, вы подключаете эффекты для формирования графа, настроив входные значения для правильных изображений и точечных рисунков.

    Первый эффект [размытия по Гауссу](gaussian-blur.md)получает свои входные данные из промежуточной поверхности, в которую были отображены примитивы. Входные данные задаются с помощью метода [**ID2D1Effect:: сетинпут**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) и задают индекс объекта [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) . Эффекты размытия по Гауссу и [отраженного освещения](point-specular.md) имеют только один вход. Эффект отраженного освещения использует размытый альфа-канал размытия по Гауссу

    [Составные](composite.md) и [арифметические составные](arithmetic-composite.md) эффекты имеют несколько входов. Чтобы убедиться, что изображения помещаются вместе в правильном порядке, необходимо указать правильный индекс для каждого входного изображения.

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  Передайте объект [арифметического составного](arithmetic-composite.md) результата в метод [**ID2DDeviceContext::D равимаже**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) , который обрабатывает и рисует выходные данные графа.

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 