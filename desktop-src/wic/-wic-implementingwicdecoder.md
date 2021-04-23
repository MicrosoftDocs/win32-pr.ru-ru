---
description: 'Дополнительные сведения: реализация декодера WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Реализация декодера WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911380"
---
# <a name="implementing-a-wic-enabled-decoder"></a><span data-ttu-id="def6b-103">Реализация декодера WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="def6b-103">Implementing a WIC-Enabled Decoder</span></span>


<span data-ttu-id="def6b-104">Для реализации декодера компонента обработки изображений Windows (WIC) требуется написание двух классов.</span><span class="sxs-lookup"><span data-stu-id="def6b-104">Implementing a Windows Imaging Component (WIC) decoder requires writing two classes.</span></span> <span data-ttu-id="def6b-105">Интерфейсы в этих классах непосредственно соответствуют обязанностям декодера, описанным в разделе [декодирование](-wic-howwicworks.md) [принципа работы компонента Windows Imaging](-wic-howwicworks.md).</span><span class="sxs-lookup"><span data-stu-id="def6b-105">The interfaces on these classes correspond directly to the decoder responsibilities outlined in the [Decoding](-wic-howwicworks.md) section of [How The Windows Imaging Component Works](-wic-howwicworks.md).</span></span>

<span data-ttu-id="def6b-106">Один из классов предоставляет службы уровня контейнера и реализует интерфейс [ивикбитмапдекодер](-wic-imp-iwicbitmapdecoder.md) .</span><span class="sxs-lookup"><span data-stu-id="def6b-106">One of the classes provides container-level services and implements the [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) interface.</span></span> <span data-ttu-id="def6b-107">Если формат изображения поддерживает метаданные уровня контейнера, необходимо также реализовать интерфейс [ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md) для этого класса.</span><span class="sxs-lookup"><span data-stu-id="def6b-107">If your image format supports container-level metadata, you must also implement the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface on this class.</span></span> <span data-ttu-id="def6b-108">Рекомендуется поддерживать интерфейс [ивикбитмапкодекпрогресснотификатион](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) как для декодера, так и для кодировщика, чтобы обеспечить лучшее взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="def6b-108">It is recommended that you support the [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) interface on both the decoder and encoder to support a better user experience.</span></span>

<span data-ttu-id="def6b-109">Другой класс, который вы реализуете, предоставляет службы на уровне кадров и выполняет фактическое декодирование битов изображения для каждого кадра в контейнере.</span><span class="sxs-lookup"><span data-stu-id="def6b-109">The other class you will implement provides frame-level services and does the actual decoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="def6b-110">Этот класс реализует интерфейс [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) и интерфейс [ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md) .</span><span class="sxs-lookup"><span data-stu-id="def6b-110">This class implements the [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) interface and the [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) interface.</span></span> <span data-ttu-id="def6b-111">При написании декодера для необработанного формата в этом классе также реализуется интерфейс [ивикдевелоправ](-wic-imp-iwicdevelopraw.md) .</span><span class="sxs-lookup"><span data-stu-id="def6b-111">If you are writing a decoder for a raw format, you also implement the [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) interface on this class.</span></span> <span data-ttu-id="def6b-112">В дополнение к необходимым интерфейсам настоятельно рекомендуется реализовать интерфейс [ивикбитмапсаурцетрансформ](-wic-imp-iwicmetadatablockreader.md) для этого класса, чтобы обеспечить наилучшую производительность для вашего формата изображения.</span><span class="sxs-lookup"><span data-stu-id="def6b-112">In addition to the required interfaces, it is highly recommended that you implement the [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) interface on this class to enable the best possible performance for your image format.</span></span>

<span data-ttu-id="def6b-113">Одним из объектов, предоставляемых компонентом WIC, является [**имагингфактори**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="def6b-113">One of the objects provided by WIC is the [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span> <span data-ttu-id="def6b-114">Интерфейс [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) для этого объекта часто используется для создания различных компонентов.</span><span class="sxs-lookup"><span data-stu-id="def6b-114">You frequently use the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) interface on this object to create various components.</span></span> <span data-ttu-id="def6b-115">Так как он часто используется, следует ссылаться на него как на свойство члена в классах декодера и кодировщика.</span><span class="sxs-lookup"><span data-stu-id="def6b-115">Because it is used frequently, you should keep a reference to it as a member property on both your decoder and encoder classes.</span></span>


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a><span data-ttu-id="def6b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="def6b-116">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="def6b-117">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="def6b-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="def6b-118">Принцип работы компонента Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="def6b-118">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

[<span data-ttu-id="def6b-119">Интерфейсы декодера</span><span class="sxs-lookup"><span data-stu-id="def6b-119">Decoder Interfaces</span></span>](-wic-decoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="def6b-120">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="def6b-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="def6b-121">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="def6b-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="def6b-122">Общие сведения о метаданных компонента WIC</span><span class="sxs-lookup"><span data-stu-id="def6b-122">WIC Metadata Overview</span></span>](-wic-about-metadata.md)
</dt> <dt>

[<span data-ttu-id="def6b-123">Общие сведения о кодировке</span><span class="sxs-lookup"><span data-stu-id="def6b-123">Encoding Overview</span></span>](-wic-creating-encoder.md)
</dt> </dl>

 

 



