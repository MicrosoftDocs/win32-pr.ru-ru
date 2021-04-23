---
description: Пример Вавсинк
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Пример Вавсинк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692765"
---
# <a name="wavsink-sample"></a><span data-ttu-id="03de7-103">Пример Вавсинк</span><span class="sxs-lookup"><span data-stu-id="03de7-103">WavSink Sample</span></span>

<span data-ttu-id="03de7-104">Показывает, как реализовать пользовательский приемник мультимедиа в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="03de7-104">Shows how to implement a custom media sink in Microsoft Media Foundation.</span></span> <span data-ttu-id="03de7-105">В примере реализуется приемник архива, записывающий несжатый аудиопоток PCM в WAV-файл.</span><span class="sxs-lookup"><span data-stu-id="03de7-105">The sample implements an archive sink that writes uncompressed PCM audio to a .wav file.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="03de7-106">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="03de7-106">APIs Demonstrated</span></span>

<span data-ttu-id="03de7-107">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="03de7-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="03de7-108">**имфклоккстатесинк**</span><span class="sxs-lookup"><span data-stu-id="03de7-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="03de7-109">**имффинализаблемедиасинк**</span><span class="sxs-lookup"><span data-stu-id="03de7-109">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [<span data-ttu-id="03de7-110">**имфмедиасинк**</span><span class="sxs-lookup"><span data-stu-id="03de7-110">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [<span data-ttu-id="03de7-111">**имфмедиатипехандлер**</span><span class="sxs-lookup"><span data-stu-id="03de7-111">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [<span data-ttu-id="03de7-112">**имфстреамсинк**</span><span class="sxs-lookup"><span data-stu-id="03de7-112">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a><span data-ttu-id="03de7-113">Использование</span><span class="sxs-lookup"><span data-stu-id="03de7-113">Usage</span></span>

<span data-ttu-id="03de7-114">Пример Вавсинк содержит два проекта Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="03de7-114">The WavSink sample contains two Visual Studio projects:</span></span>

-   <span data-ttu-id="03de7-115">Вавсинк. vcproj строит статическую библиотеку, которая содержит реализацию приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="03de7-115">WavSink.vcproj builds a static library that contains the media sink implementation.</span></span>
-   <span data-ttu-id="03de7-116">Вритевавфиле. vcproj создает консольное приложение, использующее приемник мультимедиа для создания WAV-файла.</span><span class="sxs-lookup"><span data-stu-id="03de7-116">WriteWavFile.vcproj builds a console application that uses the media sink to produce a .wav file.</span></span> <span data-ttu-id="03de7-117">Это приложение связывается с библиотекой, созданной проектом Вавсинк.</span><span class="sxs-lookup"><span data-stu-id="03de7-117">This application links to the library created by the WavSink project.</span></span>

## <a name="requirements"></a><span data-ttu-id="03de7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="03de7-118">Requirements</span></span>



| <span data-ttu-id="03de7-119">Продукт</span><span class="sxs-lookup"><span data-stu-id="03de7-119">Product</span></span>                                                        | <span data-ttu-id="03de7-120">Version</span><span class="sxs-lookup"><span data-stu-id="03de7-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="03de7-121">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="03de7-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="03de7-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03de7-122">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="03de7-123">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="03de7-123">Downloading the Sample</span></span>

<span data-ttu-id="03de7-124">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span><span class="sxs-lookup"><span data-stu-id="03de7-124">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03de7-125">См. также</span><span class="sxs-lookup"><span data-stu-id="03de7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03de7-126">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03de7-126">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="03de7-127">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="03de7-127">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



