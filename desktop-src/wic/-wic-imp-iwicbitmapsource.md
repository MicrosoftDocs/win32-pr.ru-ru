---
description: Реализация IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Реализация IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816089"
---
# <a name="implementing-iwicbitmapsource"></a><span data-ttu-id="0ed38-103">Реализация IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="0ed38-103">Implementing IWICBitmapSource</span></span>

## <a name="iwicbitmapsource"></a><span data-ttu-id="0ed38-104">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="0ed38-104">IWICBitmapSource</span></span>

<span data-ttu-id="0ed38-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) важен для работы с образами с точки зрения приложения.</span><span class="sxs-lookup"><span data-stu-id="0ed38-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is important for working with images from an application perspective.</span></span> <span data-ttu-id="0ed38-106">Он представляет абстракцию наивысшего уровня для источника изображения, и все интерфейсы компонента Windows Imaging Component (WIC), представляющие образ, включая [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**ивикбитмап**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)и все интерфейсы преобразования ([**ивикбитмапскалер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**ивикбитмапклиппер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**ивикбитмапфлипротатор**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)и [**ивикформатконвертер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)), являются производными от него.</span><span class="sxs-lookup"><span data-stu-id="0ed38-106">It represents the highest level abstraction for an image source, and all Windows Imaging Component (WIC) interfaces that represent an image, including [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), and all the transform interfaces ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) are derived from it.</span></span> <span data-ttu-id="0ed38-107">В любой конкретный момент времени объект **IWICBitmapSource** может или не может поддерживаться фактическим растровым изображением в памяти.</span><span class="sxs-lookup"><span data-stu-id="0ed38-107">At any specific time, an **IWICBitmapSource** object may or may not be backed by an actual bitmap in memory.</span></span> <span data-ttu-id="0ed38-108">Это обеспечивает очень эффективную обработку приложением, поскольку образ может быть обработано как абстракция.</span><span class="sxs-lookup"><span data-stu-id="0ed38-108">This enables very efficient processing by an application, because an image can be dealt with as an abstraction.</span></span> <span data-ttu-id="0ed38-109">Операции преобразования могут быть объединены в конвейер преобразований без использования ресурсов памяти, пока приложение не будет готово к отображению или печати изображения, при этом он вызывает метод [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) в последнем преобразовании, чтобы получить точечный рисунок в памяти изображения с примененными преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="0ed38-109">Transform operations can be chained in a transform pipeline without consuming memory resources until the application is ready to render or print the image, at which time it invokes the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the final transform to get a bitmap in memory of the image with the selected transforms applied.</span></span>

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

<span data-ttu-id="0ed38-110">С точки зрения кодека методы [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) реализуются на объекте декодера Frame.</span><span class="sxs-lookup"><span data-stu-id="0ed38-110">From a codec perspective, the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) methods are implemented on the frame decoder object.</span></span> <span data-ttu-id="0ed38-111">Эти методы описаны в разделе Реализация IWICBitmapSource вместе с другими методами в [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), которые являются производными от **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="0ed38-111">These methods are described in Implementing IWICBitmapSource, along with the other methods on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), which is derived from **IWICBitmapSource**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ed38-112">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0ed38-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0ed38-113">**Reference**</span><span class="sxs-lookup"><span data-stu-id="0ed38-113">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0ed38-114">**ивикбитмапдекодер**</span><span class="sxs-lookup"><span data-stu-id="0ed38-114">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="0ed38-115">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="0ed38-115">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="0ed38-116">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="0ed38-116">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="0ed38-117">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="0ed38-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0ed38-118">Реализация Ивикбитмапкодекпрогресснотификатион (декодер)</span><span class="sxs-lookup"><span data-stu-id="0ed38-118">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="0ed38-119">Реализация IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="0ed38-119">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="0ed38-120">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="0ed38-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="0ed38-121">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="0ed38-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



