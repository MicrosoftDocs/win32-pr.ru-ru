---
description: В этом разделе рассматриваются источники растровых изображений — основной компонент Windows Imaging Component (WIC), представляющий растровые пикселы изображения.
ms.assetid: cff0c088-ca22-4d55-9cf0-9cbe9803923e
title: Обзор источников точечных рисунков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910bfc253798058639b98a1d1beaacec9bd4d1bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497337"
---
# <a name="bitmap-sources-overview"></a>Обзор источников точечных рисунков

В этом разделе рассматриваются источники растровых изображений — основной компонент Windows Imaging Component (WIC), представляющий растровые пикселы изображения.

В этом разделе содержатся следующие подразделы.

-   [Источники точечных рисунков](#bitmap-sources-overview)
-   [Кадры точечного рисунка](#bitmap-frames)
-   [Растровые изображения](#bitmap-sources-overview)
-   [Преобразование источников битовой карты](#transform-bitmap-sources)
-   [Преобразователи контекста формата пикселей и цвета](#pixel-format-and-color-context-converters)
-   [Рисование источников точечных рисунков](#drawing-bitmap-sources)
-   [См. также](#related-topics)

## <a name="bitmap-sources"></a>Источники точечных рисунков

Компонент [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) является базовым стандартным блоком WIC и представляет один набор пикселей. Источником точечных рисунков может быть отдельный кадр многокадрового изображения или результат преобразования, выполняемого в источнике точечного рисунка. Интерфейс **IWICBitmapSource** — это основа многих основных ИНТЕРФЕЙСов WIC, таких как кадр декодера [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) и источники точечных рисунков преобразования, такие как [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).

В следующей таблице описаны различные компоненты источника битовой карты, предоставляемые компонентом WIC.



| Источники точечных рисунков                                                    | Описание                                                          |
|-------------------------------------------------------------------|----------------------------------------------------------------------|
| [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) | Представляет кадр изображения декодера.                                    |
| [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                       | Предоставляет записи и представление в памяти для источников битовой карты. |
| [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)         | Вырезает исходный точечный рисунок в нужный прямоугольник.                        |
| [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) | Переворачивает и (или) поворачивает источник точечного рисунка до нужной ориентации.       |
| [**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)           | Масштабирует источник точечного рисунка до нужного размера.                            |
| [**ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)       | Преобразует цветовой контекст источника точечного рисунка.                     |
| [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)     | Преобразует формат пикселей исходного растрового изображения.                        |



 

## <a name="bitmap-frames"></a>Кадры точечного рисунка

Наиболее распространенным [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) является [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Этот интерфейс используется для доступа к реальным данным точечного рисунка формата изображения. Многие форматы изображений поддерживают только один кадр точечного рисунка, а другие форматы, такие как GIF и TIFF, поддерживают несколько кадров на изображение.

Пример получения кадров точечного рисунка из изображения см. в разделе [Получение кадров изображения](https://www.bing.com/search?q=How+to+Retrieve+the+Frames+of+an+Image) .

## <a name="bitmaps"></a>Растровые изображения

[**Ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) добавляет основные понятия записи и статические в памяти источники битовой карты. Растровые изображения WIC позволяют пользователям напрямую обращаться к пикселям источника точечного рисунка. Этот прямой доступ предоставляется методом [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) и поддерживает любое сочетание прав на чтение и запись в пикселах растрового изображения. Метод **Lock** блокирует указанный прямоугольник точечного рисунка и предоставляет объект [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) для доступа к пикселям.

Пример использования объектов [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) и [**ивикбитмаплокк**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock) см. в разделе [Изменение пикселов исходного растрового изображения](-wic-bitmapsources-howto-modifypixels.md) .

## <a name="transform-bitmap-sources"></a>Преобразование источников битовой карты

Компонент WIC предоставляет несколько интерфейсов [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) , которые преобразуют данные пикселей. В частности, WIC предоставляет исходные растровые преобразования для масштабирования, обрезки, поворота и зеркального отображения данных пикселей. Эти преобразования источника точечных рисунков — [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)и [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator). Каждый из этих источников точечных рисунков имеет метод для инициализации и создания нового преобразованного источника точечного рисунка. Например, **ивикбитмапклиппер** включает метод [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapclipper-initialize) . Этот метод инициализирует источник битовой карты Clipper с обрезанными данными пикселя входного источника битовой карты в заданном [**викрект**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect).

В следующих разделах рассматриваются различные способы использования источников растрового изображения преобразования.

-   [Масштабирование источника точечного рисунка](-wic-bitmapsources-howto-scale.md)
-   [Как обрезать источник точечного рисунка](-wic-bitmapsources-howto-clip.md)
-   [Отражение и поворот исходного растрового изображения](-wic-bitmapsources-howto-flipandrotate.md)

## <a name="pixel-format-and-color-context-converters"></a>Преобразователи контекста формата пикселей и цвета

WIC также предоставляет источники растровых изображений, которые позволяют преобразовать формат пикселей и контекст цвета источника точечного рисунка. Компонент WIC предоставляет [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) и [**ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) для этих операций.

[**Ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) Преобразует заданный исходный точечный рисунок из одного формата пикселей в другой.

Пример использования [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)см. в разделе [как нарисовать растровый источник с помощью Direct2D](-wic-bitmapsources-howto-drawusingd2d.md) .

## <a name="drawing-bitmap-sources"></a>Рисование источников точечных рисунков

Компонент WIC по-прежнему представляет собой технологию кодеков изображений и используется для управления данными и метаданными изображений и не предоставляет способа визуализации изображений. Однако источники точечных рисунков можно изобразить с помощью нескольких графических технологий Windows, таких как Direct2D, Windows интерфейс графических устройств (GDI) и Windows GDI+. Каждая из этих технологий имеет разный уровень взаимодействия с WIC. Direct2D обеспечивает прямое взаимодействие через интерфейс [ID2D1Bitmap](../direct2d/render-targets-overview.md) и метод [ID2D1RenderTarget:: креатебитмапфромвикбитмап](../direct2d/id2d1rendertarget-createbitmapfromwicbitmap.md) , в то время как GDI и GDI+ требует, чтобы пользователи скопировали исходные Пиксели растрового изображения в [точечные рисунки](../gdi/bitmaps.md).

В следующем примере демонстрируется рисование растровых источников с помощью Direct2D.

-   [Рисование исходного растрового изображения с помощью Direct2D](-wic-bitmapsources-howto-drawusingd2d.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Общие сведения о кодировке](-wic-creating-encoder.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
