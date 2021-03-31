---
description: Демонстрирует, как реализовать видео-эффекты в виде Media Foundation преобразования (MFT).
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: Пример MFT_Grayscale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155355"
---
# <a name="mft_grayscale-sample"></a><span data-ttu-id="0c755-103">\_Пример использования градаций серого в MFT</span><span class="sxs-lookup"><span data-stu-id="0c755-103">MFT\_Grayscale Sample</span></span>

<span data-ttu-id="0c755-104">Демонстрирует, как реализовать видео-эффекты в виде Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="0c755-104">Shows how to implement a video effect as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="0c755-105">Файловая таблица в градациях серого преобразует видео YUV в градации серого, устанавливая значения чрома в видео как нейтральные.</span><span class="sxs-lookup"><span data-stu-id="0c755-105">The grayscale MFT converts YUV video to grayscale by setting the chroma values in the video to neutral.</span></span> <span data-ttu-id="0c755-106">Файл MFT принимает несжатое видео в форматах UYVY, YUY2 или NV12.</span><span class="sxs-lookup"><span data-stu-id="0c755-106">The MFT accepts uncompressed video in UYVY, YUY2, or NV12 formats.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="0c755-107">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="0c755-107">APIs Demonstrated</span></span>

<span data-ttu-id="0c755-108">В этом образце демонстрируются следующие интерфейсы Microsoft Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="0c755-108">This sample demonstrates the following Microsoft Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="0c755-109">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="0c755-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a><span data-ttu-id="0c755-110">Использование</span><span class="sxs-lookup"><span data-stu-id="0c755-110">Usage</span></span>

<span data-ttu-id="0c755-111">\_Пример для MFT градации серого строит библиотеку DLL, которая является сервером COM для MFT.</span><span class="sxs-lookup"><span data-stu-id="0c755-111">The MFT\_GrayScale sample builds a DLL that is a COM server for the MFT.</span></span> <span data-ttu-id="0c755-112">Перед использованием MFT необходимо зарегистрировать библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="0c755-112">Before using the MFT, you must register the DLL.</span></span>

<span data-ttu-id="0c755-113">Чтобы просмотреть таблицу MFT в оттенках серого, запустите [Пример плайбаккфкс](/previous-versions//bb970336(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c755-113">To see the grayscale MFT in use, run the [PlaybackFX Sample](/previous-versions//bb970336(v=vs.85)).</span></span> <span data-ttu-id="0c755-114">Кроме того, с помощью средства Топоедит можно создать топологию, включающую основную таблицу файлов в градациях серого.</span><span class="sxs-lookup"><span data-stu-id="0c755-114">You can also use the TopoEdit tool to build a topology that includes the grayscale MFT.</span></span> <span data-ttu-id="0c755-115">Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="0c755-115">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c755-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0c755-116">Requirements</span></span>



| <span data-ttu-id="0c755-117">Продукт</span><span class="sxs-lookup"><span data-stu-id="0c755-117">Product</span></span>                                                        | <span data-ttu-id="0c755-118">Version</span><span class="sxs-lookup"><span data-stu-id="0c755-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="0c755-119">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0c755-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="0c755-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c755-120">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="0c755-121">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="0c755-121">Downloading the Sample</span></span>

<span data-ttu-id="0c755-122">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span><span class="sxs-lookup"><span data-stu-id="0c755-122">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c755-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0c755-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c755-124">Видео о YUV</span><span class="sxs-lookup"><span data-stu-id="0c755-124">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="0c755-125">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c755-125">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="0c755-126">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c755-126">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="0c755-127">\_Пример АУДИОДЕЛАЙ MFT</span><span class="sxs-lookup"><span data-stu-id="0c755-127">MFT\_AudioDelay Sample</span></span>](mft-audiodelay-sample.md)
</dt> <dt>

[<span data-ttu-id="0c755-128">Запись пользовательского MFT</span><span class="sxs-lookup"><span data-stu-id="0c755-128">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
