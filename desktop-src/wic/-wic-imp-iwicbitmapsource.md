---
description: Реализация IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Реализация IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ffd73271e8e159eea825ed40c24347ec2af98f0edbfa9ecc0d5ac584df23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965023"
---
# <a name="implementing-iwicbitmapsource"></a>Реализация IWICBitmapSource

## <a name="iwicbitmapsource"></a>IWICBitmapSource

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) важен для работы с образами с точки зрения приложения. он представляет абстракцию наивысшего уровня для источника изображения, а все интерфейсы компонента обработки изображений Windows (WIC), представляющие изображение, включая [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), и все интерфейсы преобразования ([**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)и [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) являются производными от него. В любой конкретный момент времени объект **IWICBitmapSource** может или не может поддерживаться фактическим растровым изображением в памяти. Это обеспечивает очень эффективную обработку приложением, поскольку образ может быть обработано как абстракция. Операции преобразования могут быть объединены в конвейер преобразований без использования ресурсов памяти, пока приложение не будет готово к отображению или печати изображения, при этом он вызывает метод [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) в последнем преобразовании, чтобы получить точечный рисунок в памяти изображения с примененными преобразованиями.

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
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

С точки зрения кодека методы [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) реализуются на объекте декодера Frame. Эти методы описаны в разделе Реализация IWICBitmapSource вместе с другими методами в [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), которые являются производными от **IWICBitmapSource**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Reference**
</dt> <dt>

[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Зрения**
</dt> <dt>

[Реализация Ивикбитмапкодекпрогресснотификатион (декодер)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Реализация IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



