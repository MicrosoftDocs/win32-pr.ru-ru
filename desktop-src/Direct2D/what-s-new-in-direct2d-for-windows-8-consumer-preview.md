---
title: Новые возможности в Direct2D
description: Ниже приведены некоторые из новых дополнений к Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 595a0833e88948585622d79907c81a1465e3fa7b11d1ebc8d6bbd697312509bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430474"
---
# <a name="whats-new-in-direct2d"></a>Новые возможности в Direct2D

Ниже приведены некоторые из новых дополнений к Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Новые возможности для Windows 10 Creators Update

Следующие функции и API были добавлены или обновлены для Windows 10 Creators Update.

### <a name="support-for-svg-image-rendering"></a>Поддержка отрисовки изображений SVG

начиная с Windows 10 Creators Update Direct2D обеспечивает поддержку синтаксического анализа и отрисовки изображений SVG, позволяя разработчикам визуализировать ресурсы, созданные в избранных инструментах векторной графики, не преобразуя их в растровые изображения. Используйте эту функцию, чтобы повысить эффективность работы с дисками и масштабирование в иконографи в приложении и использовать Direct2D's новые API-интерфейсы объектной модели SVG для внесения программных изменений в SVG приложения. Обратите внимание, что Direct2D поддерживает только ограниченный набор SVG, подходящий для изображений и не поддерживающий все функции рисования SVG. Если требуется совместимость с SVG в браузере или веб-ориентированный на элементы SVG, рассмотрите возможность использования [элемента управления WebView XAML](/uwp/api/Windows.UI.Xaml.Controls.WebView) . Дополнительные сведения см. в следующих разделах:

-   [Пример подготовки изображения SVG Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [Поддержка SVG](svg-support.md)
-   Метод [**ID2D1DeviceContext5:: креатесвгдокумент**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument)
-   [**ID2D1DeviceContext5: метод:D равсвгдокумент**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   Интерфейс [**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Улучшенная поддержка управления цветом

начиная с Windows 10 Creators Update Direct2D предоставляет улучшенные возможности управления цветом. Разработчикам больше не нужен профиль ICC для использования Direct2D's управления цветом. Теперь они могут использовать цветовые пространства DXGI или создавать собственное определение параметризованного цветового пространства. Дополнительные сведения см. в следующих разделах:

-   [Эффекты управления цветом](color-management.md)
-   [**ID2D1DeviceContext5:: Креатеколорконтекстфромдксгиколорспаце**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5:: Креатеколорконтекстфромсимплеколорпрофиле**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>новые возможности обновления для Windows 10 годовщины

следующие функции и api были добавлены или обновлены для Windows 10ного обновления годовщины.

### <a name="improved-support-for-color-fonts"></a>Улучшенная поддержка цветных шрифтов

начиная с Windows 10ного обновления годовщины, Direct2D теперь поддерживает визуализацию более широкого спектра форматов цветовых шрифтов, позволяя разработчикам использовать в своих приложениях больше типов шрифтов, чем когда-либо ранее. Среди прочего, поддерживаются следующие шрифты:

-   Таблица OpenType "КОЛР", которая включает компактный Векторный контент в шрифтах. (Поддерживается с Windows 8.1.)
-   Таблица OpenType «SVG», которая включает содержимое SVG в шрифтах.
-   Таблица OpenType "КБДТ", которая включает содержимое цветовой битовой карты в шрифтах.
-   Таблица OpenType "сбикс", которая включает содержимое цветовой битовой карты в шрифтах.

Direct2D поддерживает эти форматы цветовых шрифтов автоматически, если включен параметр [**D2D1 \_ нарисовать \_ текст \_ включить флажок \_ \_ цветового \_ шрифта**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) . Дополнительные сведения см. в следующих разделах:

-   [Шрифты цвета](/windows/desktop/DirectWrite/color-fonts)
-   [пример цветового глифа DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Новые эффекты для изображений

начиная с Windows 10ного обновления годовщины, Direct2D включает эффекты алфамаск, плавного перехода, непрозрачности и оттенков. Эта функция ранее была доступна из конкретных конфигураций составных, Арисметиккомпосите и КолорМатрикс эффектов, но новые встроенные эффекты упрощают выполнение этих стандартных операций.

## <a name="whats-new-for-windows-10"></a>Новые возможности для Windows 10

Следующие функции и API были добавлены или обновлены для Windows 10.

### <a name="sprite-batches"></a>Пакеты спрайтов

начиная с Windows 10 Direct2D обеспечивает поддержку создания и подготовки пакетов спрайтов. По сравнению с методом [**DrawImage**](id2d1devicecontext-drawimage-overload.md) общего назначения, пакеты спрайтов значительно снижают НАГРУЗКУ на ЦП для каждого образа. Это делает их идеальным решением для сценариев, включающих сотни или тысячи одновременных образов, таких как игровые спрайты или системы частиц. Дополнительные сведения см. в следующих разделах:

-   Метод [**ID2D1DeviceContext3:: креатеспритебатч**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch)
-   [**ID2D1DeviceContext3: методы:D равспритебатч**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options))
-   Интерфейс [**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Сетки градиента

начиная с Windows 10 Direct2D предоставляет новый примитив для сеток градиентов. Сетки градиента часто используются профессиональными иллюстрациями в программном обеспечении для работы с графикой и позволяют исполнителям визуализировать сложные (даже фотографии) многоцветные фигуры со всеми преимуществами памяти и масштабируемости векторов. Дополнительные сведения см. в следующих разделах:

-   [Пример сетки градиента Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2D1 \_ Структура \_ \_ исправления сетки градиента**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**ID2D1DeviceContext2: метод:D равградиентмеш**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>Улучшенные интерфейсы API загрузки изображений

начиная с Windows 10, Direct2D предлагает новый API для загрузки изображений, ID2D1ImageSource. Источник изображения улучшает существующие API загрузки изображений, включая Креатебитмапфромвикбитмап, эффекты источника растрового изображения и эффекты Икбкр. Источник изображения Direct2D сочетает возможности этих API с поддержкой произвольно больших изображений, простотой интеграции с печатью и эффектами, а также многочисленных оптимизаций, включая Икбкр JPEG и индексированный JPEG. Дополнительные сведения см. в следующих статьях:

-   [Пример пакета SDK для настройки Direct2D Photo](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [Ивикжпегфрамедекоде:: Сетиндексинг](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Улучшенная поддержка отрисовки рукописных данных

начиная с Windows 10 Direct2D предоставляет новый примитив для представления рукописных штрихов. Direct2D рукописные штрихи определяются кривыми Безье, поддерживают различные фигуры NIB и преобразования и могут иметь фиксированную или переменную толщину. Встроенная поддержка рукописного ввода Direct2D's позволяет приложениям легко визуализироваться быстрее, более привлекательной краской, чем предыдущие подходы, которые обычно требуются приложениям для управления рукописными данными, как ряд эллипсов и куадрилатералс. Дополнительные сведения см. в следующих разделах:

-   [**Интерфейс ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceContext2: метод:D Равинк**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**Интерфейс ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Связывание шейдера эффектов

Эффекты Direct2D реализуются с помощью HLSL пикселей, вершин или шейдеров вычислений. начиная с Windows 10, Direct2D теперь автоматически анализирует графы эффектов для возможностей объединения и выполнения отдельных шейдеров. Это может значительно повысить пропускную способность. Потребителям встроенных эффектов не нужно ничего делать, чтобы воспользоваться преимуществами связывания шейдера, но разработчики, создающие собственные пользовательские эффекты, должны следовать обновленным рекомендациям по использованию связывания с шейдером эффектов. Дополнительные сведения см. в следующих разделах:

-   [Связывание шейдеров эффектов](effect-shader-linking.md)
-   [Вспомогательные Direct2D HLSL](hlsl-helpers.md)
-   [Пример пакета SDK для пользовательских эффектов Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

Связывание шейдера эффектов не влияет на визуальный вывод эффектов. Однако это не всегда возможно из-за конкретного поведения в отношении точности и числовой обрезки. Дополнительные сведения об управлении этими поведениями см. в следующих статьях:

-   [Управление точностью и числовыми обрезками на диаграммах эффектов](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Новые встроенные эффекты

начиная с Windows 10, Direct2D включает обширный набор новых встроенных эффектов, которые предназначены для лучших запросов разработчиков и обеспечивают новые виды визуальных сценариев. Новые эффекты:

### <a name="color"></a>Цвет:

-   [Эффекты оттенка RGB](rgb-to-hue-effect.md)
-   [Оттенок для влияния RGB](hue-to-rgb-effect.md)
-   [эффект трехмерной таблицы подстановки](3d-lookup-table-effect.md)

### <a name="photo"></a>Галерея

-   [Контрастный результат](contrast-effect.md)
-   [Воздействие на выдержки](exposure-effect.md)
-   [Эффекты оттенков серого](grayscale-effect.md)
-   [Эффект выделения и теней](highlights-and-shadows-effect.md)
-   [Обратить воздействие](invert-effect.md)
-   [Выцветшей, результат](sepia-effect.md)
-   [Эффекты резкости](sharpen-effect.md)
-   [Результат выпрямления](straighten-effect.md)
-   [Воздействие на температуру и оттенок](temperature-and-tint-effect.md)
-   [Вигнетте, результат](vignette-effect.md)

### <a name="filter"></a>Фильтр:

-   [Воздействие на обнаружение границ](edge-detection-effect.md)

### <a name="stylize"></a>Стилизовать

-   [Эффект приподнятости](emboss-effect.md)
-   [Постеризе, результат](posterize-effect.md)

### <a name="transparency"></a>Прозрачность:

-   [Чрома-клавиша](chromakey-effect.md)

В [образце пакета SDK Direct2D Photo корректировок](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)показаны эффекты выравнивания, насыщенности, контрастности, выделения и тени, а также эффект температуры и оттенков.

## <a name="whats-new-for-windows-81"></a>Новые возможности для Windows 8.1

Следующие функции и API были добавлены или обновлены для Windows 8.1.

начиная с Windows 8.1, Direct2D построен на основе Direct3D 11,2.

### <a name="geometry-realizations"></a>Реализации геометрических объектов

начиная с Windows 8.1 Direct2D предлагает реализации геометрических объектов. Реализации геометрии позволяют приложениям улучшать производительность отрисовки геометрии в определенных ситуациях без некоторых недостатков растеризации геометрии до точечного рисунка. Дополнительные сведения см. в следующих разделах:

-   Интерфейс [**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**ID2D1DeviceContext1: метод:D равжеометриреализатион**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Поддержка изображений JPEG Икбкр

начиная с Windows 8.1 Direct2D обеспечивает поддержку отрисовки данных изображения в формате JPEG и'кбкр. Приложения могут визуализировать содержимое JPEG в собственном И'кбкр представлении вместо распаковки в BGRA. Это может значительно снизить потребление памяти и время создания ресурсов. Дополнительные сведения см. в следующих разделах:

-   Direct2D [икбкр](ycbcr-effect.md)
-   Интерфейс [**ивикпланарбитмапсаурцетрансформ**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Поддержка блочных сжатых форматов (файлы DDS)

начиная с Windows 8.1 Direct2D обеспечивает поддержку точечных рисунков, которые содержат \_ формат dxgi \_ BC1 \_ UNORM, в \_ формате dxgi \_ BC2 \_ UNORM и в \_ формате dxgi \_ BC3 \_ UNORM данных пикселей. Приложения могут заменять свои активы с изображениями блоками сжатых образов DDS. Это может значительно снизить потребление памяти и время создания ресурсов. Дополнительные сведения см. в следующих разделах:

-   Метод [**ID2D1DeviceContext:: креатебитмапфромвикбитмап**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md)
-   Интерфейс [**ивикддсфрамедекоде**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Приоритет отрисовки

начиная с Windows 8.1 Direct2D обеспечивает поддержку приоритета отрисовки каждого устройства. Эта новая функция позволяет приложениям переключать устройство между обычным приоритетом отрисовки (по умолчанию) и низким приоритетом отрисовки (в котором устройство не блокирует другие задачи подготовки к просмотру в системе). Рекомендуется, чтобы приложения использовали низкий приоритет визуализации для задач, которые не являются критически важными для реагирования на запросы пользователей, например предварительно подготовленное содержимое, отрисовка, а также другие операции, которые обычно выполняются в фоновом режиме. Дополнительные сведения см. в следующих разделах:

-   Метод [**ID2D1Device1:: сетрендерингприорити**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority)
-   [**D2D1 \_ Перечисление \_ приоритетов отрисовки**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority)

## <a name="whats-new-for-windows-8"></a>Новые возможности для Windows 8

Следующие функции и API были добавлены или обновлены для Windows 8.

новые интерфейсы Direct2D поддерживаются в Windows 7 с установленным [обновлением платформы для Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) .

семантика Direct2D's для устройств и контекстов устройств была обновлена с учетом семантики, используемой Direct3D, и для обеспечения краткой работы с приложениями Windows Store. Дополнительные сведения см. в разделе [устройства и контексты устройств](devices-and-device-contexts.md) .

Выбранные связанные API:

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

API списка команд позволяет совместно использовать путь отрисовки для отображения и печати на экране. Он также позволяет использовать примитивы для создания кисти изображения для заполнения примитивов.

Выбранные связанные API:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Direct2D effects](effects-overview.md) — это набор api-интерфейсов, новый в Windows 8 для применения высококачественных эффектов к изображениям. Он также включает API, позволяющие создавать собственные пользовательские эффекты.

Выбранные связанные API:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

начиная с Windows 8, Direct2D включает дополнительные api для создания многопоточных приложений. Дополнительные сведения см. в разделе [многопоточные приложения Direct2D](multi-threaded-direct2d-apps.md) .

Выбранные связанные API:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**\_Тип фабрики D2D1 с \_ \_ несколькими \_ потоками**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 