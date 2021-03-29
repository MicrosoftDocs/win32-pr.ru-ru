---
description: Декодирование
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Декодирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911936"
---
# <a name="decoding"></a><span data-ttu-id="9dac7-103">Декодирование</span><span class="sxs-lookup"><span data-stu-id="9dac7-103">Decoding</span></span>

<span data-ttu-id="9dac7-104">Для правильной поддержки метаданных авторы декодера должны выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="9dac7-104">To properly support metadata, decoder authors must do the following:</span></span>

-   <span data-ttu-id="9dac7-105">Реализуйте интерфейсы [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .</span><span class="sxs-lookup"><span data-stu-id="9dac7-105">Implement [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) interfaces.</span></span>
-   <span data-ttu-id="9dac7-106">Реализуйте [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) в декодере кадров.</span><span class="sxs-lookup"><span data-stu-id="9dac7-106">Implement [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on the frame decoder.</span></span> <span data-ttu-id="9dac7-107">Если кодек поддерживает метаданные уровня контейнера, этот интерфейс должен быть реализован в декодере уровня контейнера, а также в декодере кадров.</span><span class="sxs-lookup"><span data-stu-id="9dac7-107">If the codec supports container-level metadata, this interface must be implemented on the container-level decoder as well as on the frame decoder.</span></span>
-   <span data-ttu-id="9dac7-108">При декодировании потока изображения вызовите [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**креатеметадатареадерфромконтаинер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) , чтобы создать экземпляр модуля чтения метаданных для каждого блока метаданных.</span><span class="sxs-lookup"><span data-stu-id="9dac7-108">While decoding the image stream, call [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) to instantiate a metadata reader for each metadata block.</span></span> <span data-ttu-id="9dac7-109">(Все новые читатели метаданных, реализуемые кодеком, должны быть зарегистрированы в WIC.)</span><span class="sxs-lookup"><span data-stu-id="9dac7-109">(Any new metadata readers that the codec implements must be registered with WIC.)</span></span>

    <span data-ttu-id="9dac7-110">Декодер не должен создавать модули чтения метаданных самостоятельно, а использует WIC для создания их на основе блоков метаданных в потоке.</span><span class="sxs-lookup"><span data-stu-id="9dac7-110">The decoder should not create metadata readers on its own, but rather use WIC to create them based on the metadata blocks in the stream.</span></span> <span data-ttu-id="9dac7-111">Декодер должен сделать это на всех найденных блоках, даже если они не известны докодер, так как в системе могут быть установлены средства чтения метаданных, которые понимают, как обрабатывать эти блоки метаданных.</span><span class="sxs-lookup"><span data-stu-id="9dac7-111">The decoder must do this on all blocks that it finds, even if they are not natively known to the docoder, because future metadata readers might be installed on the system that do understand how to handle these metadata blocks.</span></span>

-   <span data-ttu-id="9dac7-112">Если обработчик метаданных для блока отсутствует, создайте экземпляр модуля чтения неизвестных метаданных с помощью параметров создания метаданных.</span><span class="sxs-lookup"><span data-stu-id="9dac7-112">If there is no metadata handler for a block, instantiate the unknown metadata reader by using the metadata creation options.</span></span>
-   <span data-ttu-id="9dac7-113">Предоставьте коллекцию средств чтения метаданных через интерфейс [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="9dac7-113">Expose the collection of metadata readers through the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dac7-114">См. также</span><span class="sxs-lookup"><span data-stu-id="9dac7-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9dac7-115">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9dac7-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9dac7-116">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="9dac7-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="9dac7-117">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="9dac7-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="9dac7-118">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="9dac7-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



