---
description: Реализация IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Реализация IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b49e3636f5d81202b1060d868ecb40bb99d095dd9f26b6afd0d40c5f5fd0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205768"
---
# <a name="implementing-iwicbitmapframedecode"></a>Реализация IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) — это интерфейс уровня кадров, предоставляющий доступ к реальным битам изображения. Этот интерфейс реализуется для класса декодирования на уровне кадров. Так как он является производным от [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), ваша реализация **IWICBitmapFrameDecode** будет включать реализацию методов **IWICBitmapSource** . Дополнительные методы в **IWICBitmapFrameDecode** обеспечивают доступ к эскизу на уровне кадров, любому цветному контексту для изображения и считывателю запросов метаданных для рамки.

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [GetThumbnail](#getthumbnail)
-   [жетколорконтекстс](#getcolorcontexts)
-   [жетметадатакуериреадер](#getmetadataqueryreader)
-   [Метод Жетпикселформат и метод.](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [копипалетте](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

Параметр " [**эскиз**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) " возвращает эскиз текущего кадра. По соображениям производительности эскизы чаще всего кодируются в формате JPEG. Точно так же, как и в предварительной версии декодера, не обязательно и не рекомендуется предоставлять собственный декодер JPEG для эскизов. вместо этого следует делегировать декодеру JPEG, предоставляемому компонентом Windows imaging (WIC).

Дополнительные сведения о эскизах см. в описании метода [сетсумбнаил](-wic-imp-iwicbitmapframeencode.md) для [реализации ивикбитмапфраминкоде](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>жетколорконтекстс

[**Жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) возвращает допустимые контексты цвета (также известные как цветовые профили), связанные с изображением в этом кадре. В большинстве случаев это будет только один, но бывают случаи, когда есть два или, редко и больше. Вызывающий объект передаст один или несколько объектов [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , устанавливая параметр *учетная запись* , чтобы указать, сколько их передается. Этот метод заполняет объекты **ивикколорконтекст** фактическими данными контекста цвета для цветовых профилей, связанных с изображением. Задайте для параметра *пкактуалкаунт* фактическое количество цветовых контекстов, связанных с изображением, даже если оно больше числа, которое можно вернуть. (В случае, если доступно больше контекстов, чем количество объектов **ивикколорконтекст** , переданных вызывающей стороной, это указывает вызывающей стороне, что есть доступ к одному или нескольким другим.)

### <a name="getmetadataqueryreader"></a>жетметадатакуериреадер

[**Жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) возвращает [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , который приложение может использовать для получения метаданных из фрейма изображения. Этот интерфейс реализуется обработчиком метаданных и позволяет приложению запрашивать определенные свойства метаданных, принадлежащие определенному формату метаданных. Дополнительные сведения см. в разделе [Реализация ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md).

Чтобы создать экземпляр [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), вызовите [**креатекуериреадерфромблоккреадер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) в [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>Метод Жетпикселформат и метод.

Метод [**жетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) [**и метод**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)- [**разрешение**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) говорят сами за себя и возвращают запрошенные свойства изображения.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) — это метод, который вызывается приложением, когда требуется создать точечный рисунок в памяти, который может быть визуализирован на дисплее или на принтере. Это метод, который выполняет фактическое декодирование битов изображения. Параметры — это прямоугольник, который представляет область, представляющую интерес в исходном изображении для копирования в память; шаг, указывающий число байтов в одной строке просмотра; Размер буфера в памяти, выделенного приложением; и указатель на буфер, в который должны копироваться запрошенные биты изображения. (Чтобы предотвратить потенциальные переполнения буфера от внедрения уязвимостей безопасности, необходимо скопировать в буфер только столько данных образа, сколько указывает параметр *кббуфферсизе* .)

### <a name="copypalette"></a>копипалетте

Только кодеки, имеющие Индексированные форматы пикселей, должны реализовывать метод [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) . Если изображение использует индексированный формат, используйте этот метод для возврата палитры цветов, используемых в изображении. Если у кодека нет индексированного формата, возвратите ВИНКОДЕК \_ Err \_ палеттеунаваилабле.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Зрения**
</dt> <dt>

[Реализация IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Реализация Ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



