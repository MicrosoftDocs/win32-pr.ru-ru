---
description: Показывает, как написать декодер для Microsoft Media Foundation.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Пример декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990836"
---
# <a name="decoder-sample"></a><span data-ttu-id="0e00f-103">Пример декодера</span><span class="sxs-lookup"><span data-stu-id="0e00f-103">Decoder Sample</span></span>

<span data-ttu-id="0e00f-104">Показывает, как написать декодер для Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0e00f-104">Shows how to write a decoder for Microsoft Media Foundation.</span></span>

<span data-ttu-id="0e00f-105">В этом примере реализуется макет видеодекодера MPEG-1, который отображает код времени для каждого кадра видео.</span><span class="sxs-lookup"><span data-stu-id="0e00f-105">This sample implements a mock MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="0e00f-106">На самом деле он не расшифровывает битовый поток MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="0e00f-106">It does not actually decode the MPEG-1 bitstream.</span></span> <span data-ttu-id="0e00f-107">На следующем рисунке показан вывод видео из декодера.</span><span class="sxs-lookup"><span data-stu-id="0e00f-107">The following image shows the video output from the decoder.</span></span>

![снимок экрана видеокадра из декодера](images/decodersample.png)

> [!Note]  
> <span data-ttu-id="0e00f-109">До Windows SDK для Windows 7 этот пример был включен как часть [примера MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="0e00f-109">Prior to the Windows SDK for Windows 7, this sample was included as part of the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

 

## <a name="apis-demonstrated"></a><span data-ttu-id="0e00f-110">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="0e00f-110">APIs Demonstrated</span></span>

<span data-ttu-id="0e00f-111">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="0e00f-111">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="0e00f-112">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="0e00f-112">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a><span data-ttu-id="0e00f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0e00f-113">Requirements</span></span>



| <span data-ttu-id="0e00f-114">Продукт</span><span class="sxs-lookup"><span data-stu-id="0e00f-114">Product</span></span>                                                        | <span data-ttu-id="0e00f-115">Version</span><span class="sxs-lookup"><span data-stu-id="0e00f-115">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0e00f-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0e00f-116">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0e00f-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0e00f-117">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0e00f-118">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0e00f-118">Downloading the Sample</span></span>

<span data-ttu-id="0e00f-119">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span><span class="sxs-lookup"><span data-stu-id="0e00f-119">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e00f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0e00f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e00f-121">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e00f-121">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="0e00f-122">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e00f-122">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="0e00f-123">Запись пользовательского MFT</span><span class="sxs-lookup"><span data-stu-id="0e00f-123">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



