---
description: Начиная с Windows 8.1 кодек Windows Imaging Component (WIC) JPEG поддерживает чтение и запись данных изображений в собственной форме Икбкр.
ms.assetid: 50B89A96-72E8-4771-9109-207F4CDD06CB
title: Поддержка Икбкр JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a8f05fe55e724a12513f24fc7401d277ebf097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998576"
---
# <a name="jpeg-ycbcr-support"></a>Поддержка Икбкр JPEG

Начиная с Windows 8.1 кодек [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG поддерживает чтение и запись данных изображений в собственной форме Yc<sub>b</sub>C<sub>r</sub> . Поддержка WIC YC<sub>b</sub>c<sub>r</sub> может использоваться вместе с [DIRECT2D](../direct2d/direct2d-portal.md) для отрисовки данных Yc<sub>b</sub>C<sub>r</sub> пикселей с помощью эффектов изображения. Кроме того, кодек WIC JPEG может использовать данные YC<sub>b</sub>C<sub>r</sub> Pixel, созданные определенными драйверами камеры с помощью Media Foundation.

YC<sub>b</sub>C<sub>r</sub> пиксель Data потребляет значительно меньше памяти, чем стандартные форматы пикселей BGRA. Кроме того, доступ к данным YC<sub>b</sub>C<sub>r</sub> позволяет разгрузить некоторые этапы конвейера декодирования и кодирования JPEG в DIRECT2D, который поддерживает процессор с ускорителем. С помощью YC<sub>b</sub>C<sub>r</sub>приложение может сократить потребление памяти JPEG и время загрузки для тех же образов размеров и качества. Или приложение может использовать более высокое разрешение изображений JPEG, не низкий от потерь производительности.

В этом разделе описывается, как работают данные YC<sub>b</sub>C<sub>r</sub> и как использовать их в WIC и Direct2D.

-   [О формате JPEG YC<sub>b</sub>C<sub>r</sub> Data](#about-jpeg-ycbcr-data)
    -   [Цветовая модель YC<sub>b</sub>C<sub>r</sub>](#ycbcr-color-model)
    -   [Плоские и чередующиеся макеты памяти](#planar-versus-interleaved-memory-layouts)
    -   [Подвыборка чрома](#chroma-subsampling)
    -   [Использование JPEG для YC<sub>b</sub>C<sub>r</sub>](#jpeg-usage-of-ycbcr)
-   [Использование JPEG YC<sub>b</sub>C<sub>r</sub> Data](#using-jpeg-ycbcr-data)
    -   [Использование изображений в формате JPEG YC<sub>b</sub>C<sub>r</sub>](#using-ycbcr-jpeg-images)
    -   [API компонентов работы с образами Windows](#windows-imaging-component-apis)
    -   [API-интерфейсы Direct2D](#direct2d-apis)
    -   [Определение, поддерживается ли конфигурация YC<sub>b</sub>C<sub>r</sub>](#determining-if-the-ycbcr-configuration-is-supported)
    -   [Декодирование данных YC<sub>b</sub>C<sub>r</sub> Pixel](#decoding-ycbcr-pixel-data)
    -   [Преобразование данных YC<sub>b</sub>C<sub>r</sub> Pixel](#transforming-ycbcr-pixel-data)
    -   [Кодирование YC<sub>b</sub>C<sub>r</sub> пиксель Data](#encoding-ycbcr-pixel-data)
    -   [Декодирование данных YC<sub>b</sub>C<sub>r</sub> Pixel в Windows 10](#decoding-ycbcr-pixel-data-in-windows-10)
-   [См. также](#related-topics)

## <a name="about-jpeg-ycsubbsubcsubrsub-data"></a>О формате JPEG YC<sub>b</sub>C<sub>r</sub> Data

В этом разделе объясняются некоторые основные понятия, необходимые для понимания того, как работает YC<sub>b</sub>C<sub>r</sub> в WIC и его основные преимущества.

### <a name="ycsubbsubcsubrsub-color-model"></a>Цветовая модель YC<sub>b</sub>C<sub>r</sub>

Компонент WIC в Windows 8 и более ранних версий поддерживает четыре различные [цветовые модели](-wic-codec-native-pixel-formats.md), наиболее распространенный из которых — RGB/BGR. Эта цветовая модель определяет цвет данных с помощью красного, зеленого и синего компонентов; также можно использовать Четвертый альфа-компонент.

Ниже приведено изображение, разстоящее в красном, зеленом и синем компонентах.

![изображение, разстоящее в красно, зеленом и синем компонентах.](graphics/ycbcr1.png)

YC<sub>b</sub>C<sub>r</sub> — это альтернативная цветовая модель, определяющая цветовые данные с помощью компонента освещенности (Y) и двух компонентов чроминанце (c<sub>b</sub> и c<sub>r</sub>). Она обычно используется в сценариях работы с цифровыми изображениями и видео. Термин YC<sub>b</sub>C<sub>r</sub> часто используется с YUV, хотя эти два являются неизменными.

Существует несколько разновидностей YC<sub>b</sub>C<sub>r</sub> , которые отличаются цветовым пространством и динамическими определениями диапазонов — WIC специально поддерживает JPEG JFIF Yc<sub>b</sub>C<sub>r</sub> Data. Дополнительные сведения см. в [спецификации JPEG ITU-T81](https://www.w3.org/Graphics/JPEG/itu-t81.pdf).

Ниже приведен образ, состоящий из компонентов Y, C<sub>b</sub>и c<sub>r</sub> .

![изображение, разстоящее в компонентах y, CB и CR.](graphics/ycbcr2.png)

### <a name="planar-versus-interleaved-memory-layouts"></a>Плоские и чередующиеся макеты памяти

В этом разделе описываются некоторые различия между доступом и хранением данных пикселей RGB в памяти и YC<sub>b</sub>C<sub>r</sub> Data.

Данные пикселей RGB обычно хранятся с использованием чередования макета памяти. Это означает, что данные для одного компонента цвета чередуются между пикселями, и каждый пиксель хранится непрерывно в памяти.

Ниже приведен рисунок, показывающий пиксельные данные типа RGBA, хранящиеся в макете памяти с чередованием.

![Рисунок, показывающий пиксельные данные типа RGBA, хранящиеся в макете памяти с чередованием.](graphics/ycbcr3.png)

Данные YC<sub>b</sub>C<sub>r</sub> обычно хранятся с помощью плоского макета памяти. Это означает, что каждый компонент цвета хранится отдельно в отдельной непрерывной плоскости для всего трех плоскостей. В другой распространенной конфигурации компоненты C<sub>b</sub> и c<sub>r</sub> чередуются и хранятся вместе, а компонент Y остается в собственной плоскости, что составляет всего две плоскости.

Ниже приведена фигура с плоской Y и чередованием данных<sub>в пикселах на c</sub> <sub>b</sub>c в виде общей структуры памяти Yc<sub>b</sub>c<sub>r</sub> .

![Рисунок, показывающий плоские и чередующиеся кбкр данные пикселей, общий макет памяти икбкр.](graphics/ycbcr4.png)

В WIC и Direct2D Каждая цветовая палитра рассматривается как отдельный отдельный объект ( [IWICBitmapSource](-wic-imp-iwicbitmapsource.md) или [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)), и вместе эти плоскости формируют резервные данные для изображения Yc <sub>b</sub>C <sub>r</sub> .

Хотя компонент WIC поддерживает доступ к данным YC<sub>b</sub>C<sub>r</sub> в конфигурациях плоскости 2 и 3, Direct2D поддерживает только бывшие первые (Y и c<sub>b</sub>c<sub>r</sub>). Поэтому при совместном использовании WIC и Direct2D следует всегда использовать конфигурацию 2 плоскости YC<sub>b</sub>C<sub>r</sub> .

### <a name="chroma-subsampling"></a>Подвыборка чрома

Цветовая модель YC<sub>b</sub>C<sub>r</sub> хорошо подходит для сценариев работы с цифровыми образами, поскольку она может использовать преимущества некоторых аспектов системы человеческого визуального элемента. В частности, люди более чувствительны к изменениям светимости (яркости) изображения и менее чувствительны к чроминанце (цвету). Разделив данные цвета на отдельные компоненты светимости и чроминанце, можно выборочно сжимать только компоненты чроминанце, чтобы добиться экономии места с минимальной потерей качества.

Один из способов сделать это называется подвыборкой чрома. Плоскости C<sub>b</sub> и c<sub>r</sub> являются подвыборкой (довнскалед) в одном или обоих горизонтальных и вертикальных измерениях. По историческим причинам каждый чрома режим подвыборки часто именуется с использованием трех частей Ж:а: b.



| Режим подвыборки | Горизонтальное довнскале | Вертикальный довнскале | Бит на пиксель\* |
|------------------|----------------------|--------------------|------------------|
| 4:4:4            | 1x                   | 1x                 | 24               |
| 4:2:2            | 2x                   | 1x                 | 16               |
| 4:4:0            | 1x                   | 2x                 | 16               |
| 4:2:0            | 2x                   | 2x                 | 12               |



 

\* Включает данные Y.

В приведенной выше таблице при использовании YC<sub>b</sub>C<sub>r</sub> для хранения несжатых данных изображения можно добиться экономии памяти от 25% до 62,5% относительно 32 бит на пиксельные данные RGBA в зависимости от того, какой режим подвыборки чрома используется.

### <a name="jpeg-usage-of-ycsubbsubcsubrsub"></a>Использование JPEG для YC<sub>b</sub>C<sub>r</sub>

На высоком уровне конвейер распаковки JPEG состоит из следующих этапов:

1.  Выполнить распаковку (например, Хаффмана)
2.  Выполнение декуантизатион
3.  Выполнить обратное дискретное преобразование косинуса
4.  Выполнить чроманую выборку данных на C<sub>b</sub>c<sub>r</sub>
5.  Преобразование данных YC<sub>b</sub>C<sub>r</sub> в RGBA (при необходимости)

Если кодек JPEG создает данные YC<sub>b</sub>C<sub>r</sub> , мы можем избежать заключительных двух этапов процесса декодирования или отложить их на GPU. Помимо экономии памяти, приведенной в предыдущем разделе, это значительно сокращает общее время, необходимое для декодирования изображения. Такая же экономия применяется при кодировании данных YC<sub>b</sub>C<sub>r</sub> .

## <a name="using-jpeg-ycsubbsubcsubrsub-data"></a>Использование JPEG YC<sub>b</sub>C<sub>r</sub> Data

В этом разделе объясняется, как использовать WIC и Direct2D для работы с данными YC<sub>b</sub>C<sub>r</sub> .

Рекомендации из этого документа, используемые на практике, см. в разделе [Оптимизация Икбкр JPEG в Direct2D и WIC пример](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample) , демонстрирующий все шаги, необходимые для декодирования и визуализации содержимого Yc<sub>b</sub>C<sub>r</sub> в приложении Direct2D.

### <a name="using-ycsubbsubcsubrsub-jpeg-images"></a>Использование изображений в формате JPEG YC<sub>b</sub>C<sub>r</sub>

Подавляющее большинство изображений JPEG хранится в виде YC<sub>b</sub>C<sub>r</sub>. Некоторые файлы JPEG содержат данные CMYK или градации серого и не используют YC<sub>b</sub>C<sub>r</sub>. Это означает, что обычно, но не всегда, может напрямую использовать уже существующее содержимое JPEG без каких-либо изменений.

WIC и Direct2D не поддерживают все возможные конфигурации YC<sub>b</sub>c<sub>r</sub> , а поддержка Yc<sub>b</sub>c<sub>r</sub> в Direct2D зависит от базового графического оборудования и драйвера. По этой причине конвейер создания образов общего назначения должен быть устойчивым к изображениям, которые не используют YC<sub>b</sub>C<sub>r</sub> (включая другие распространенные форматы изображений, например PNG или BMP), а также в случаях, когда поддержка Yc<sub>b</sub>c<sub>r</sub> недоступна. Мы рекомендуем использовать существующий конвейер создания образов на основе BGRA и включить YC<sub>b</sub>C<sub>r</sub> в качестве оптимизации производительности, если это возможно.

### <a name="windows-imaging-component-apis"></a>API компонентов работы с образами Windows

WIC в Windows 8.1 добавляет три новых интерфейса для предоставления доступа к данным JPEG YC<sub>b</sub>C<sub>r</sub> .

### <a name="iwicplanarbitmapsourcetransform"></a>ивикпланарбитмапсаурцетрансформ

[**Ивикпланарбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) является аналогом [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), за исключением того, что он создает Пиксели в плоской конфигурации, включая Yc <sub>b</sub>C <sub>r</sub> Data. Этот интерфейс можно получить путем вызова QueryInterface в реализации [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , которая поддерживает плоский доступ. Сюда входит реализация [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) КОДЕка JPEG, а также [**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)и [**ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform).

### <a name="iwicplanarbitmapframeencode"></a>ивикпланарбитмапфраминкоде

[**Ивикпланарбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) предоставляет возможность кодирования плоских данных пикселей, в том числе Yc <sub>b</sub>C <sub>r</sub> Data. Этот интерфейс можно получить, вызвав QueryInterface в реализации [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)кодека JPEG.

### <a name="iwicplanarformatconverter"></a>ивикпланарформатконвертер

[**Ивикпланарформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) позволяет [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) использовать данные плоской точки, включая Yc <sub>b</sub>C <sub>r</sub>, и преобразовывать их в формат пикселей с чередованием. Он не предоставляет возможность преобразования чередующихся данных пикселей в плоский формат. Этот интерфейс можно получить, вызвав QueryInterface в реализации **ивикформатконвертер**, предоставляемой Windows.

### <a name="direct2d-apis"></a>API-интерфейсы Direct2D

Direct2D в Windows 8.1 поддерживает данные о YC<sub>b</sub>c<sub>в плоском</sub> пикселе с новым результатом создания изображения Yc<sub>b</sub>c<sub>r</sub> . Этот результат дает возможность визуализировать данные YC<sub>b</sub>C<sub>r</sub> . Этот результат принимает в качестве входных двух интерфейсов [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) : один, содержащий плоские данные Y в формате DXGI \_ \_ R8 \_ UNORM, и один, содержащий чередующиеся кбкр данные в формате DXGI \_ \_ R8G8 \_ UNORM. Обычно этот результат используется вместо **ID2D1Bitmap** , который СОДЕРЖАЛ данные BGRA пикселей.

Изображение YC<sub>b</sub>c на языке<sub>r</sub> предназначено для использования в сочетании<sub>с API-</sub> интерфейсами WIC Yc<sub>b</sub>c, которые предоставляют данные Yc<sub>b</sub>c<sub>r</sub> . Это эффективно отвечает за отправку некоторых операций декодирования от ЦП к GPU, где он может обрабатываться намного быстрее и параллельно.

### <a name="determining-if-the-ycsubbsubcsubrsub-configuration-is-supported"></a>Определение, поддерживается ли конфигурация YC<sub>b</sub>C<sub>r</sub>

Как отмечалось ранее, приложение должно быть устойчивым к случаям, когда поддержка YC<sub>b</sub>C<sub>r</sub> недоступна. В этом разделе обсуждаются условия, которые должно проверить приложение. При сбое любой из следующих проверок приложение должно вернуться к стандартному конвейеру на основе BGRA.

### <a name="does-the-wic-component-support-ycsubbsubcsubrsub-data-access"></a>Поддерживает ли компонент WIC доступ к данным YC<sub>b</sub>C<sub>r</sub> ?

Только предоставляемый Windows кодек JPEG и определенные преобразования WIC поддерживают доступ к данным YC<sub>b</sub>C<sub>r</sub> . Полный список см. в разделе [API компонента Windows Imaging Component](#windows-imaging-component-apis) .

Чтобы получить один из интерфейсов YC<sub>b</sub>C<sub>r</sub> , вызовите QueryInterface в исходном интерфейсе. Это приведет к сбою, если компонент не поддерживает доступ к данным YC<sub>b</sub>C<sub>r</sub> .

### <a name="is-the-requested-wic-transform-supported-for-ycsubbsubcsubrsub"></a>Поддерживается ли запрошенное преобразование WIC для YC<sub>b</sub>C<sub>r</sub>?

После получения [**ивикпланарбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)необходимо сначала вызвать [**доессуппорттрансформ**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-doessupporttransform). Этот метод принимает в качестве входных параметров полный набор преобразований, которые необходимо применить к YC<sub>b</sub>C<sub>r</sub> -данным, и возвращает логическое значение, обозначающее поддержку, а также ближайшие измерения с запрошенным размером, который может быть возвращен. Прежде чем обращаться к данным пикселей с помощью [**ивикпланарбитмапсаурцетрансформ:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels), необходимо проверить все три значения.

Этот шаблон аналогичен использованию [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="does-the-graphics-driver-support-the-features-necessary-to-use-ycsubbsubcsubrsub-with-direct2d"></a>Поддерживает ли графический драйвер функции, необходимые для использования YC<sub>b</sub>C<sub>r</sub> с Direct2D?

Эта проверка необходима только в том случае, если вы используете Direct2D YC<sub>b</sub>c<sub>r</sub> для визуализации содержимого Yc<sub>b</sub>c<sub>r</sub> . Direct2D сохраняет данные<sub>Yc в</sub>C<sub>r</sub> с помощью \_ формата DXGI \_ R8 \_ UNORM и \_ формата DXGI \_ R8G8 \_ UNORM пикселей, которые недоступны во всех графических драйверах.

Перед использованием изображения YC <sub>b</sub>C в формате <sub>r</sub> необходимо вызвать [**ID2D1DeviceContext:: исдксгиформатсуппортед**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isdxgiformatsupported) , чтобы убедиться, что оба формата поддерживаются драйвером.

### <a name="sample-code"></a>Пример кода

Ниже приведен пример кода, демонстрирующий Рекомендуемые проверки. Этот пример взят из [оптимизации Икбкр JPEG в примере Direct2D и WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
bool DirectXSampleRenderer::DoesWicSupportRequestedYCbCr()
{
    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    HRESULT hr = m_wicScaler.As(&wicPlanarSource);
    if (SUCCEEDED(hr))
    {
        BOOL isTransformSupported;
        uint32 supportedWidth = m_cachedBitmapPixelWidth;
        uint32 supportedHeight = m_cachedBitmapPixelHeight;
        DX::ThrowIfFailed(
            wicPlanarSource->DoesSupportTransform(
                &supportedWidth,
                &supportedHeight,
                WICBitmapTransformRotate0,
                WICPlanarOptionsDefault,
                SampleConstants::WicYCbCrFormats,
                m_planeDescriptions,
                SampleConstants::NumPlanes,
                &isTransformSupported
                )
            );

        // The returned width and height may be larger if IWICPlanarBitmapSourceTransform does not
        // exactly support what is requested.
        if ((isTransformSupported == TRUE) &&
            (supportedWidth == m_cachedBitmapPixelWidth) &&
            (supportedHeight == m_cachedBitmapPixelHeight))
        {
            return true;
        }
    }

    return false;
}

bool DirectXSampleRenderer::DoesDriverSupportYCbCr()
{
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    return (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8_UNORM)) &&
        (d2dContext->IsDxgiFormatSupported(DXGI_FORMAT_R8G8_UNORM));
}
```



### <a name="decoding-ycsubbsubcsubrsub-pixel-data"></a>Декодирование данных YC<sub>b</sub>C<sub>r</sub> Pixel

Если вы хотите получить данные о точках YC <sub>b</sub>C <sub>r</sub> , необходимо вызвать [**ивикпланарбитмапсаурцетрансформ:: CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapsourcetransform-copypixels). Этот метод копирует пиксельные данные в массив [**викбитмаппланеных**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) структур, по одному для каждой плоскости данных (например, Y и c <sub>b</sub>c <sub>r</sub>). **Викбитмапплане** содержит сведения о точках данных и указывает на буфер памяти, который будет принимать данные.

Если вы хотите использовать данные YC <sub>b</sub>C <sub>r</sub> x в других API-интерфейсах WIC, следует создать соответствующим образом настроенный [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), вызвать [**блокировку**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) , чтобы получить базовый буфер памяти, и связать буфер с [**викбитмапплане**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) , который использовался для получения данных Yc <sub>b</sub>на <sub>r</sub> пиксель. Затем можно использовать [ивикбитмап](-wic-imp-iwicbitmapdecoder.md) в обычном режиме.

Наконец, если вы хотите визуализировать данные YC <sub>b</sub>c <sub>r</sub> в Direct2D, необходимо создать [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) из каждого [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) и использовать их в качестве источника для изображения Yc <sub>b</sub>C <sub>r</sub> . Компонент WIC позволяет запрашивать несколько плоских конфигураций. При взаимодействии с Direct2D необходимо запросить две плоскости, одну с идентификаторами GUID \_ WICPixelFormat8bppY, а другую — с помощью идентификатора GUID \_ WICPixelFormat16bppCbCr, так как это ожидаемая конфигурация Direct2D.

### <a name="code-sample"></a>Образец кода

Ниже приведен пример кода, демонстрирующий действия по декодированию и визуализации данных YC<sub>b</sub>C<sub>r</sub> в Direct2D. Этот пример взят из [оптимизации Икбкр JPEG в примере Direct2D и WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample).


```C++
void DirectXSampleRenderer::CreateYCbCrDeviceResources()
{
    auto wicFactory = m_deviceResources->GetWicImagingFactory();
    auto d2dContext = m_deviceResources->GetD2DDeviceContext();

    ComPtr<IWICPlanarBitmapSourceTransform> wicPlanarSource;
    DX::ThrowIfFailed(
        m_wicScaler.As(&wicPlanarSource)
        );

    ComPtr<IWICBitmap> bitmaps[SampleConstants::NumPlanes];
    ComPtr<IWICBitmapLock> locks[SampleConstants::NumPlanes];
    WICBitmapPlane planes[SampleConstants::NumPlanes];

    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        DX::ThrowIfFailed(
            wicFactory->CreateBitmap(
                m_planeDescriptions[i].Width,
                m_planeDescriptions[i].Height,
                m_planeDescriptions[i].Format,
                WICBitmapCacheOnLoad,
                &bitmaps[i]
                )
            );

        LockBitmap(bitmaps[i].Get(), WICBitmapLockWrite, nullptr, &locks[i], &planes[i]);
    }

    DX::ThrowIfFailed(
        wicPlanarSource->CopyPixels(
            nullptr, // Copy the entire source region.
            m_cachedBitmapPixelWidth,
            m_cachedBitmapPixelHeight,
            WICBitmapTransformRotate0,
            WICPlanarOptionsDefault,
            planes,
            SampleConstants::NumPlanes
            )
        );

    DX::ThrowIfFailed(d2dContext->CreateEffect(CLSID_D2D1YCbCr, &m_d2dYCbCrEffect));

    ComPtr<ID2D1Bitmap1> d2dBitmaps[SampleConstants::NumPlanes];
    for (uint32 i = 0; i < SampleConstants::NumPlanes; i++)
    {
        // IWICBitmapLock must be released before using the IWICBitmap.
        locks[i] = nullptr;

        // First ID2D1Bitmap1 is DXGI_FORMAT_R8 (Y), second is DXGI_FORMAT_R8G8 (CbCr).
        DX::ThrowIfFailed(d2dContext->CreateBitmapFromWicBitmap(bitmaps[i].Get(), &d2dBitmaps[i]));
        m_d2dYCbCrEffect->SetInput(i, d2dBitmaps[i].Get());
    }
}

void DirectXSampleRenderer::LockBitmap(
    _In_ IWICBitmap *pBitmap,
    DWORD bitmapLockFlags,
    _In_opt_ const WICRect *prcSource,
    _Outptr_ IWICBitmapLock **ppBitmapLock,
    _Out_ WICBitmapPlane *pPlane
    )
{
    // ComPtr guarantees the IWICBitmapLock is released if an exception is thrown.
    ComPtr<IWICBitmapLock> lock;
    DX::ThrowIfFailed(pBitmap->Lock(prcSource, bitmapLockFlags, &lock));
    DX::ThrowIfFailed(lock->GetStride(&pPlane->cbStride));
    DX::ThrowIfFailed(lock->GetDataPointer(&pPlane->cbBufferSize, &pPlane->pbBuffer));
    DX::ThrowIfFailed(lock->GetPixelFormat(&pPlane->Format));
    *ppBitmapLock = lock.Detach();
}
```



### <a name="transforming-ycsubbsubcsubrsub-pixel-data"></a>Преобразование данных YC<sub>b</sub>C<sub>r</sub> Pixel

Преобразование данных YC <sub>b</sub>C <sub>r</sub> практически идентично декодированию, как и в случае с [**ивикпланарбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). Единственное отличие заключается в том, какой объект WIC получил интерфейс. Подсистема Windows, перевернутая по мере вращения и преобразования цветов, поддерживает доступ к YC<sub>b</sub>C<sub>r</sub> .

### <a name="chaining-transforms-together"></a>Объединение преобразований

WIC поддерживает понятие объединения нескольких преобразований. Например, можно создать следующий конвейер WIC:

![Схема конвейера WIC, начиная с декодера JPEG.](graphics/ycbcr5.png)

Затем можно вызвать QueryInterface в [**ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) , чтобы получить [**ивикпланарбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform). Преобразование цветов может взаимодействовать с предыдущими преобразованиями и может предоставлять агрегатные возможности каждого этапа в конвейере. Компонент WIC гарантирует, что данные YC<sub>b</sub>C<sub>r</sub> сохраняются во всем процессе. Эта цепочка работает только при использовании компонентов, поддерживающих доступ к YC<sub>b</sub>C<sub>r</sub> .

### <a name="jpeg-codec-optimizations"></a>Оптимизация кодека JPEG

Как и при декодировании в формате JPEG, реализация [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), декодирование кадров JPEG, реализованная в [**ивикпланарбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) , поддерживает собственное масштабирование и поворот домена в формате JPEG ДКТ. Вы можете запросить мощь двух довнскале или вращения непосредственно из декодера JPEG. Это обычно приводит к более высокому качеству и производительности, чем использование дискретных преобразований.

Кроме того, при сцеплении одного или нескольких преобразований WIC после декодера JPEG он может использовать собственное масштабирование и вращение JPEG для удовлетворения запрошенной операции агрегирования.

### <a name="format-conversions"></a>Преобразования формата

Используйте [**ивикпланарформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarformatconverter) для преобразования плоских данных Yc <sub>b</sub><sub>в C пикселей</sub> в формат ПИКСЕЛЕЙ с чередованием, например GUID \_ WICPixelFormat32bppPBGRA. WIC в Windows 8.1 не обеспечивает возможность преобразования в плоский YC<sub>b</sub><sub>C в</sub> формате пикселей.

### <a name="encoding-ycsubbsubcsubrsub-pixel-data"></a>Кодирование YC<sub>b</sub>C<sub>r</sub> пиксель Data

Используйте [**ивикпланарбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode) для кодирования данных Yc <sub>b</sub>C <sub>r</sub> x в кодировщик JPEG. Кодировка YC <sub>b</sub>Data **ивикпланарбитмапфраминкоде** похожа, но не идентична кодированию <sub>данных с</sub> чередованием с помощью [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Плоский интерфейс предоставляет возможность записи данных изображения с плоскими кадрами, поэтому следует продолжать использовать интерфейс кодирования фрейма для установки метаданных или эскиза и фиксации в конце операции.

В типичном случае необходимо выполнить следующие действия.

1.  Получите [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) как обычную. Если вы хотите настроить подвыборку чрома, задайте параметр кодировщика [**жпегикркбсубсамплинг**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) при создании рамки.
2.  Если необходимо задать метаданные или эскиз, сделайте это с помощью [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) в качестве обычного.
3.  QueryInterface для [**ивикпланарбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode).
4.  Задайте YC <sub>b</sub>C <sub>r</sub> пиксель Data с помощью [**Ивикпланарбитмапфраминкоде:: Вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writesource) или [**ивикпланарбитмапфраминкоде:: WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicplanarbitmapframeencode-writepixels). В отличие от своих [**ивикбитмапфраминкоденых**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) аналогов, вы предоставляете эти методы с массивом [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) или [**ВИКБИТМАППЛАНЕ**](/windows/desktop/api/Wincodec/ns-wincodec-wicbitmapplane) , которые содержат плоскости Yc <sub>b</sub>C <sub>r</sub> Pixel.
5.  По завершении вызовите метод [**ивикбитмапфраминкоде:: Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit).

### <a name="decoding-ycsubbsubcsubrsub-pixel-data-in-windows-10"></a>Декодирование данных YC<sub>b</sub>C<sub>r</sub> Pixel в Windows 10

Начиная с Windows 10 Build 1507, Direct2D предоставляет [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic), более простой способ декодирования JPEG-файлов в Direct2D при использовании оптимизации Yc <sub>b</sub>C <sub>r</sub> . **ID2D1ImageSourceFromWic** автоматически выполняет все необходимые проверки возможностей <sub>r</sub> в Yc <sub>b</sub>. по возможности он использует оптимизированную коду, и в противном случае использует резервный. Он также позволяет выполнять новые оптимизации, такие как кэширование только подобластей изображения, которые необходимы за раз.

Дополнительные сведения об использовании [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)см. в [образце](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)пакета SDK Direct2D Photo корректировок.

## <a name="related-topics"></a>См. также

* [Оптимизация Икбкр JPEG в примерах Direct2D и WIC](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/JPEG%20YCbCr%20optimizations%20in%20Direct2D%20and%20WIC%20sample)
