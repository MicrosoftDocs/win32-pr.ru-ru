---
title: Эффекты (Direct2D)
description: Обзор Direct2Dных эффектов.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070371"
---
# <a name="effects"></a>Произведенный эффект

## <a name="what-are-direct2d-effects"></a>Что такое Direct2Dные эффекты?

Direct2D можно использовать для применения одного или более высококачественных эффектов к изображению или набору изображений. Интерфейсы API эффектов основаны на [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) и используют возможности GPU для обработки изображений. Можно создать цепочку эффектов на диаграмме эффектов, а также составить или смешать выходные данные эффектов.

Эффект Direct2D выполняет задачу создания образов, например изменение яркости, снятие насыщенности изображения или создание тени. Эффекты могут принимать ноль или более входных изображений, предоставлять несколько свойств, управляющих их работой, и создавать одно выходное изображение.

Каждый результат создает внутренний граф преобразования, состоящие из отдельных преобразований. Каждое преобразование представляет одну операцию с изображением. Основное назначение преобразования заключается в размещении шейдеров, которые выполняются для каждого выходного пикселя. Эти шейдеры могут включать шейдеры пикселей, шейдеры вершин, стадию смешения GPU и шейдеры вычислений.

Как [встроенные эффекты](built-in-effects.md) [Direct2D](./direct2d-portal.md) , так и пользовательские эффекты, которые можно использовать для работы с [API пользовательских эффектов](custom-effects.md) .

Существует ряд [встроенных эффектов](built-in-effects.md) из категорий, таких как здесь. Полный список см. в разделе [встроенные эффекты](built-in-effects.md) .

-   [Записей](built-in-effects.md)
-   [Композиция и смешивание](built-in-effects.md)
-   [Прозрачность](built-in-effects.md)
-   [Цвет](built-in-effects.md)
-   [Освещение и стилизация](built-in-effects.md)
-   [Преобразование и масштабирование](built-in-effects.md)
-   [Источники](built-in-effects.md)

Эффекты можно применять к любым растровым изображениям, включая изображения, загруженные [компонентом Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), примитивы, нарисованные [Direct2D](./direct2d-portal.md), Text FROM [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)или сцены, отображаемые [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).

С помощью эффектов Direct2D можно создавать собственные эффекты, которые можно использовать для приложений. Платформа настраиваемых эффектов позволяет использовать такие возможности GPU, как шейдеры пикселей, шейдер вершин и блок смешения. В пользовательский эффект также можно включить другие встроенные или пользовательские эффекты. Платформой для создания пользовательских эффектов является то же, что использовалось для создания встроенных эффектов [Direct2D](./direct2d-portal.md). [API Direct2D Effect Author](custom-effects.md) предоставляет набор интерфейсов для создания и регистрации эффектов.

### <a name="more-effects-topics"></a>Дополнительные эффекты

Оставшаяся часть этого раздела посвящена основам эффектов Direct2D, таких как применение эффекта к изображению. В таблице ниже приведены ссылки на дополнительные разделы, посвященные влиянию.

| Раздел                                                                                                                    | Описание                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Связывание шейдеров эффектов](effect-shader-linking.md)<br/>                                                            | Direct2D использует оптимизацию, называемую связыванием шейдера эффектов, которая сочетает визуализацию диаграммы с несколькими эффектыми, передавая один проход.<br/>                                               |
| [Пользовательские эффекты](custom-effects.md)<br/>                                                                          | Описание процесса написания собственных пользовательских эффектов с помощью стандартных HLSL.<br/>                                                                                                                |
| [Как загрузить изображение в эффекты Direct2D с помощью операция filepicker](load-a-id2d1image-using-the-filepicker.md)<br/> | Показывает, как использовать [**Windows:: Storage::P иккерс:: филеопенпиккер**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) для загрузки изображения в эффекты Direct2D.<br/>                                      |
| [Сохранение содержимого Direct2D в файл изображения](save-direct2d-content-to-an-image-file.md)<br/>                   | В этом разделе показано, как использовать [**ивиЦимажеенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) для сохранения содержимого в виде [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) в закодированный файл изображения, например JPEG.<br/> |
| [Применение эффектов к примитивам](how-to-apply-effects-to-primitives.md)<br/>                                  | В этом разделе показано, как применить ряд эффектов к примитивам [Direct2D](./direct2d-portal.md) и [DirectWrite](direct2d-and-directwrite.md) .<br/>                           |
| [Управление точностью и числовыми обрезками на диаграммах эффектов](precision-and-clipping-in-effect-graphs.md)<br/>  | Приложения, которые визуализируют эффекты с помощью Direct2D, должны обеспечивать требуемый уровень качества и предсказуемости относительно числовой точности. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Применение эффектов к изображению

Для применения преобразований к изображениям можно использовать API Direct2D Effects.

> [!Note]  
> В этом примере предполагается, что объекты [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) и [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) уже созданы. Дополнительные сведения о создании этих объектов см. в статье [Загрузка изображения в эффекты Direct2D с помощью операция filepicker](load-a-id2d1image-using-the-filepicker.md) и [устройств и контекстов устройств](devices-and-device-contexts.md).

 

1.  Объявите переменную [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , а затем создайте [Исходный растровый](bitmap-source.md) результат с помощью метода [**ID2DDeviceContext:: креатиффект**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Задайте свойство «Источник битовой карты WIC» с помощью [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Объявите переменную [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) , а затем создайте эффект [размытия по Гауссу](gaussian-blur.md) .

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Задайте входные данные, чтобы получить изображение из исходного результата растрового изображения. Задайте степень размытия для метода [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) и стандартного свойства отклонения.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Используйте контекст устройства для отрисовки результирующего вывода изображения.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    Метод [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) должен вызываться между вызовами [**ID2DDeviceContext:: бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) и [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , как и другие операции отрисовки Direct2D. **DrawImage** может принимать изображение или выходные данные действия и подготавливать его к целевой поверхности.

## <a name="spatial-transforms"></a>Пространственные преобразования

Direct2D предоставляет встроенные эффекты, которые могут преобразовывать изображения в 2D-и трехмерном пространстве, а также масштабировать. Эффекты масштабирования и преобразования предлагают различные уровни качества, например: ближайший соседний, линейный, кубический, многопримерный линейный, анизотропный и высококачественный кубический уровень.

> [!Note]  
> В режиме анизотропного масштабирования создается MIP-карты при масштабировании, однако если для свойства **кэширования** задано значение true на эффектах, вводимых для преобразования, MIP-карты не будет создаваться каждый раз для достаточно мелких изображений.

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



При использовании этого действия 2D-преобразование поворачивает растровое изображение немного против часовой стрелки.



| До                                                            |
|-------------------------------------------------------------------|
| ![2D-аффинное действие перед изображением.](images/default-before.jpg)      |
| После                                                             |
| ![двумерные аффинное эффекты после изображения.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Совмещение изображений

Некоторые эффекты принимают несколько входных данных и объединяют их в один полученный образ.

Встроенные составные и арифметические составные эффекты предоставляют различные режимы. Дополнительные сведения см. в [составном](composite.md) разделе. В результате [смешения](blend.md) доступны разнообразные режимы ускорения GPU.


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Составной результат объединяет изображения разными способами в соответствии с заданным режимом.

## <a name="pixel-adjustments"></a>Корректировки пикселей

Существует несколько встроенных эффектов Direct2D, позволяющих изменять данные пикселей. Например, для изменения цвета изображения можно использовать эффекты матрицы цветов.


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



Этот код принимает изображение и изменяет цвет, как показано в примерах изображений здесь.



| До                                                          |
|-----------------------------------------------------------------|
| ![Матрица цветов перед изображением.](images/default-before.jpg) |
| После                                                           |
| ![Цветовая матрица после изображения.](images/15-colormatrix.png)  |



 

Дополнительные сведения см. в разделе [встроенные эффекты цвета](how-to-create-a-solid-color-brush.md) .

## <a name="building-effect-graphs"></a>Создание графов эффектов

Вы можете объединить эффекты в цепочки для преобразования изображений. Например, код здесь применяет тень и 2D-преобразование, а затем объединяет результаты вместе.


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Ниже приводится результат.

![выходные данные эффект тени.](images/effect-overview-shadow.png)

Эффекты принимают в качестве входных данных объекты [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) . Можно использовать [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , поскольку интерфейс является производным от **ID2D1Image**. Можно также использовать [**ID2D1Effect::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) GetObject для получения выходных данных объекта [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) в качестве **ID2D1Image** или использовать метод **сетинпутеффект** , который преобразует выходные данные для вас. В большинстве случаев граф эффектов состоит из объектов **ID2D1Effect** , напрямую связанных друг с другом, что позволяет легко применить к изображению несколько эффектов для создания привлекательных визуальных элементов.

Дополнительные сведения см. [в разделе Применение эффектов к примитивам](how-to-apply-effects-to-primitives.md) .

## <a name="related-topics"></a>См. также

[Пример Direct2D Basic Image Effects](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Встроенные эффекты](built-in-effects.md)