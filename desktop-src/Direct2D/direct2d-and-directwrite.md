---
title: Отрисовка текста с помощью Direct2D и DirectWrite
description: в отличие от других интерфейсов api, таких как GDI, GDI+ или WPF, Direct2D взаимодействует с другим API, DirectWrite, для обработки и отрисовки текста. В этом разделе описываются преимущества и взаимодействие этих отдельных компонентов.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd95e7644b5f429d4dd91d2276213d5b7ffb92b058d8e530bfcf47fee77fea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698242"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Отрисовка текста с помощью Direct2D и DirectWrite

в отличие от других интерфейсов api, таких как [GDI](/windows/desktop/gdi/windows-gdi), GDI+ или WPF, [Direct2D](./direct2d-portal.md) взаимодействует с другим API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), для обработки и отрисовки текста. В этом разделе описываются преимущества и взаимодействие этих отдельных компонентов.

В этом разделе содержатся следующие подразделы.

-   [Direct2D включает добавочное внедрение](#direct2d-enables-incremental-adoption)
-   [Текстовые службы и отрисовка текста](#text-services-versus-text-rendering)
-   [Глифы и текст](#glyphs-versus-text)
-   [DirectWrite и Direct2D](#directwrite-and-direct2d)
    -   [DrawText](#drawtextlayout)
    -   [дравтекстлайаут](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Рендеринг глифов](#glyph-rendering)
-   [Заключение](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D включает добавочное внедрение

Перемещение приложения из одного графического API в другой может быть сложным или ненужным по различным причинам. Это может быть вызвано тем, что необходимо поддерживать подключаемые модули, которые по-прежнему используют старые интерфейсы, так как само приложение слишком велико для переноса на новый API в одном выпуске или потому, что более старый API достаточно хорошо работает для других частей приложения.

поскольку [Direct2D](./direct2d-portal.md) и [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) реализуются как отдельные компоненты, можно обновить всю систему двухмерной графики или просто текстовую часть. например, можно обновить приложение так, чтобы оно использовало DirectWrite для текста, но по-прежнему использовало [GDI](/windows/desktop/gdi/windows-gdi) или GDI+ для отрисовки.

## <a name="text-services-versus-text-rendering"></a>Текстовые службы и отрисовка текста

По мере развития приложений требования к обработке текста были все еще сложны. В первую очередь, текст обычно ограничен статическим выходным ИНТЕРФЕЙСом, а текст был отображен в хорошо определенном поле, например на кнопке. По мере того, как приложения начали быть доступны на растущем количестве языков, этот подход стал труднее, так как ширина и высота переведенного текста могут значительно различаться в разных языках. Для адаптации приложения начали динамически размещать свой пользовательский интерфейс в зависимости от фактического размера отображаемого текста, а не наоборот.

чтобы помочь приложениям выполнить эту задачу, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) предоставляет интерфейс [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) . Этот API позволяет приложению указать часть текста со сложными характеристиками, такими как различные шрифты и размеры шрифтов, подчеркивания, зачеркивание, двунаправленный текст, эффекты, многоточие и даже встроенные символы, отличные от глифов (например, точечный значок или значок). Приложение может изменить различные характеристики текста по мере того, как оно последовательно определяет макет пользовательского интерфейса. многие из этих эффектов показаны в [примере DirectWrite Hello World](/samples/browse/?redirectedfrom=MSDN-samples), который показан на следующем рисунке и в разделе [учебник. начало работы с DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite) .

![снимок экрана примера "Hello World".](images/dwrite-hello-world.png)

Макет может расположить глифы в идеале на основе их ширины (как в WPF), или же можно привязать глифы к ближайшим позициям в пикселях (как в [GDI](/windows/desktop/gdi/windows-gdi) ).

Помимо получения текстовых измерений, приложение может выполнять проверку различных частей текста. Например, может потребоваться убедиться в том, что нажата гиперссылка в тексте. (Дополнительные сведения о проверке попадания см. в разделе [Проверка нажатия для разметки текста](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) .)

Интерфейс макета текста отделен от API отрисовки, используемого приложением, как показано на следующей схеме:

![Макет текста и диаграмма API графики.](images/direct2d-directwrite1.png)

это разделение возможно, так как DirectWrite предоставляет интерфейс отрисовки ([**идвритетекстрендерер**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)), который приложения могут реализовать для отображения текста с помощью любого нужного API. приложение, реализующее метод обратного вызова [**идвритетекстрендерер::D равглифрун**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) , вызывается DirectWrite при отрисовке макета текста. Этот метод отвечает за выполнение операций рисования или их передачу.

для рисования глифов [Direct2D](./direct2d-portal.md) предоставляет [**ID2D1RenderTarget::D равглифрун**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) для рисования на поверхности Direct2D и [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) предоставляет [**идвритебитмапрендертаржет::D равглифрун**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) для рисования на поверхность gdi, которую затем можно передать в окно с помощью GDI. **DrawGlyphRun** в Direct2D и DirectWrite имеют строго совместимые параметры для метода [**DrawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) , реализуемого приложением в [**идвритетекстрендерер**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer).

следуя подобным разделениям, функции для работы с текстом (например, перечисление и управление шрифтами, анализ глифов и т. д.) обрабатываются [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) вместо [Direct2D](./direct2d-portal.md). DirectWrite объекты принимаются непосредственно Direct2D. чтобы помочь существующим приложениям GDI воспользоваться преимуществами DirectWrite, он предоставляет интерфейс метода [**идвритегдиинтероп**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) с методами для выполнения следующих задач:

-   создание [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) шрифта из логического шрифта [GDI](/windows/desktop/gdi/windows-gdi) ([**креатефонтфромлогфонт**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   преобразование из [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) шрифта в логический шрифт [GDI](/windows/desktop/gdi/windows-gdi) ([**конвертфонтфацетологфонт**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   получение [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) шрифта, выбранного в параметре HDC. ([**Креатефонтфацефромхдк**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   создайте [DirectWriteный](/windows/desktop/DirectWrite/direct-write-portal) [**растровый объект прорисовки**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) в системной памяти ([**креатебитмапрендертаржет**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Глифы и текст

Текст — это набор кодовых позиций Юникода (символов) с различными модификаторами стилистического начертания (шрифты, веса, подчеркивания, зачеркивание и т. д.), которые располагаются в прямоугольнике. Глиф, напротив, является определенным индексом в определенном файле шрифта. Глиф определяет набор кривых, которые могут быть визуализированы, но не имеют текстового значения. Между глифами и символами существует потенциальное сопоставление типа «многие ко многим». Последовательность глифов, которая поступает из одной и той же гарнитуры шрифта и располагается последовательно в базовом плане, называется [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs). как [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) , так и [Direct2D](./direct2d-portal.md) вызывают свои наиболее точные [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) API рендеринга глифов и имеют очень похожие подписи. В следующем примере из [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) в Direct2D:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



И этот метод из [**идвритебитмапрендертаржет**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) в [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal):


```
STDMETHOD(DrawGlyphRun)(
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        IDWriteRenderingParams* renderingParams,
        COLORREF textColor,
        __out_opt RECT* blackBoxRect = NULL
        ) PURE;
```



версия [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) сохраняет исходный план, режим измерения и параметры запуска глифа и включает дополнительные параметры.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) также позволяет использовать пользовательский модуль визуализации для глифов путем реализации интерфейса [**идвритетекстрендерер**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) . Этот интерфейс также имеет метод **DrawGlyphRun** , как показано в следующем примере кода.


```
STDMETHOD(DrawGlyphRun)(
        __maybenull void* clientDrawingContext,
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
        __maybenull IUnknown* clientDrawingEffect
        ) PURE;
```



Эта версия содержит больше параметров, которые полезны при реализации пользовательского модуля [подготовки текста](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer). Последний параметр используется для реализованных приложением пользовательских эффектов рисования. (Дополнительные сведения о влиянии на рисование клиента см. в разделе [Добавление клиентских эффектов рисования в макет текста](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Каждый запуск глифа начинается в источнике и помещается в строку, начиная с этого источника. Глифы изменяются текущим преобразованием мира и выбранными параметрами отрисовки текста для связанного целевого объекта прорисовки. Этот API обычно вызывается напрямую только приложениями, которые выполняют собственный макет (например, текстовый процессор) или приложением, реализующим интерфейс [**идвритетекстрендерер**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) .

## <a name="directwrite-and-direct2d"></a>DirectWrite и Direct2D

[Direct2D](./direct2d-portal.md) предоставляет службы визуализации на уровне глифов через [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Однако для этого требуется, чтобы приложение реализовало сведения о отрисовке, что, по сути, повторно создает функциональные возможности API [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) из GDI.

Таким образом, [Direct2D](./direct2d-portal.md) предоставляет API-интерфейсы, которые принимают текст вместо Glyphs: [**ID2D1RenderTarget::D равтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) and [**ID2D1RenderTarget::D равтекст**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Оба метода подготавливаются к поверхности Direct2D. Для подготовки к просмотру на поверхности GDI предоставляется [**идвритебитмапрендертаржет::D равглифрун**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) . Однако для этого метода требуется, чтобы пользовательский модуль подготовки текста был реализован приложением. (Дополнительные сведения см. в разделе [Подготовка к поверхности GDI](/windows/desktop/DirectWrite/render-to-a-gdi-surface) .)

Использование текста приложением обычно начинается с простого: пошаговое нажатие кнопки " **ОК** " или **"Отмена"** на кнопке с фиксированным макетом. Однако со временем оно станет более сложным, так как используется Международная связь и добавляются другие компоненты. в конечном итоге многие приложения должны использовать объекты макета текста [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) и реализовать модуль подготовки текста.

Таким образом, [Direct2D](./direct2d-portal.md) предоставляет многоуровневые API, которые позволяют приложению запускаться просто и более сложным, не отвлекая и не отменяя рабочий код. Упрощенное представление показано на следующей схеме:

![Схема приложения DirectWrite и Direct2D.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>DrawText

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) — это самый простой из интерфейсов API для использования. Он принимает строку в Юникоде, кисть переднего плана, один объект форматирования и прямоугольник назначения. Она будет размещать и визуализировать всю строку в пределах прямоугольника макета и при необходимости обрезать ее. Это полезно при помещении простого фрагмента текста в элемент пользовательского интерфейса с фиксированной разметкой.

### <a name="drawtextlayout"></a>дравтекстлайаут

Создавая объект [**идвритетекстлайаут**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) , приложение может начать измерять и расположить текст и другие элементы пользовательского интерфейса, а также поддерживает несколько шрифтов, стилей, подчеркивания и зачеркивание. [Direct2D](./direct2d-portal.md) предоставляет API [**дравтекстлайаут**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) , который непосредственно принимает этот объект и визуализирует текст в заданной точке. (Ширина и высота предоставляются объектом макета). Помимо реализации всех ожидаемых функций макета текста, Direct2D будет интерпретировать любой объект Effect как кисть и применить эту кисть к выбранному диапазону глифов. Он также будет вызывать любые встроенные объекты. Приложение может затем вставлять в текст символы, не являющиеся глифами (значками). Еще одним преимуществом использования объекта макета текста является то, что позиции глифа кэшируются в нем. Таким образом, большой выигрыш в производительности можно сделать, повторно используя один и тот же объект макета для нескольких вызовов Draw и избегая повторного вычисления позиций глифа для каждого вызова. Эта возможность отсутствует для [**DRAWTEXT**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))GDI.

### <a name="drawglyphrun"></a>DrawGlyphRun

Наконец, приложение может реализовать интерфейс [**идвритетекстрендерер**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) и вызвать [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) и [**ФИЛЛРЕКТАНГЛЕ**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) , или любой другой API отрисовки. Все существующее взаимодействие с объектом макета текста останется неизменным.

Пример реализации пользовательского модуля подготовки отчетов см. в разделе Подготовка к просмотру [с помощью пользовательского текстового модуля подготовки](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) отчетов.

## <a name="glyph-rendering"></a>Рендеринг глифов

добавление [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) в существующее приложение GDI позволяет приложению использовать API [**идвритебитмапрендертаржет**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) для визуализации глифов. метод [**идвритебитмапрендертаржет::D равглифрун**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) , который DirectWrite предоставляет, выводит сплошной цвет в контроллер памяти, не требуя дополнительных api, таких как [Direct2D](./direct2d-portal.md).

Это позволяет приложению получать расширенные функции отрисовки текста, например следующие:

-   Технология ClearType в подпикселах позволяет приложению размещать глифы на позициях в пикселах, чтобы обеспечить визуализацию и макет глифов.
-   Сглаживание по оси Y обеспечивает более гладкую визуализацию кривых на более крупных глифах.

Приложение, перемещающееся в [Direct2D](./direct2d-portal.md) , также будет получать следующие возможности:

-   Аппаратное ускорение.
-   Возможность заполнения текста произвольной кистью [Direct2D](./direct2d-portal.md) , например радиальными градиентами, линейными градиентами и точечными рисунками.
-   Поддержка уровней и обрезки с помощью API-интерфейсов [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)), [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) и [**креатекомпатиблерендертаржет**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) .
-   Возможность поддержки отрисовки текста в градациях серого. Он правильно заполняет альфа-канал назначения в соответствии с непрозрачностью кисти текста и сглаживанием текста.

Для эффективной поддержки аппаратного ускорения [Direct2D](./direct2d-portal.md) использует слегка отличающееся приближение к гамме-коррекции, именуемое *корректировкой альфа-канала*. Это не требует от Direct2D проверки цветового пикселя целевого объекта прорисовки при отрисовке текста.

## <a name="conclusion"></a>Заключение

в этом разделе объясняются различия и сходства между [Direct2D](./direct2d-portal.md) и [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) и архитектурным мотивацией для предоставления их в виде отдельных интерфейсов api для совместной разработки.

 

 