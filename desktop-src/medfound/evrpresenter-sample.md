---
description: Пример Еврпресентер
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Пример Еврпресентер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143111"
---
# <a name="evrpresenter-sample"></a><span data-ttu-id="47b73-103">Пример Еврпресентер</span><span class="sxs-lookup"><span data-stu-id="47b73-103">EVRPresenter Sample</span></span>

<span data-ttu-id="47b73-104">Показывает, как реализовать пользовательский объект Presenter для [расширенного модуля подготовки видео](enhanced-video-renderer.md) (Евр).</span><span class="sxs-lookup"><span data-stu-id="47b73-104">Shows how to implement a custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="47b73-105">Пользовательский Presenter можно использовать с фильтром DirectShow Евр или с приемником Microsoft Media Foundation Евр.</span><span class="sxs-lookup"><span data-stu-id="47b73-105">The custom presenter can be used with either the DirectShow EVR filter or the Microsoft Media Foundation EVR sink.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="47b73-106">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="47b73-106">APIs Demonstrated</span></span>

<span data-ttu-id="47b73-107">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="47b73-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="47b73-108">**имфклоккстатесинк**</span><span class="sxs-lookup"><span data-stu-id="47b73-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="47b73-109">**имфратесуппорт**</span><span class="sxs-lookup"><span data-stu-id="47b73-109">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="47b73-110">**имфтопологисервицелукупклиент**</span><span class="sxs-lookup"><span data-stu-id="47b73-110">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [<span data-ttu-id="47b73-111">**имфвидеодевицеид**</span><span class="sxs-lookup"><span data-stu-id="47b73-111">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [<span data-ttu-id="47b73-112">**имфвидеодисплайконтрол**</span><span class="sxs-lookup"><span data-stu-id="47b73-112">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [<span data-ttu-id="47b73-113">**имфвидеопресентер**</span><span class="sxs-lookup"><span data-stu-id="47b73-113">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a><span data-ttu-id="47b73-114">Использование</span><span class="sxs-lookup"><span data-stu-id="47b73-114">Usage</span></span>

<span data-ttu-id="47b73-115">В примере Еврпресентер создается библиотека DLL, которая является COM-сервером для выступающего.</span><span class="sxs-lookup"><span data-stu-id="47b73-115">The EVRPresenter sample builds a DLL that is a COM server for the presenter.</span></span> <span data-ttu-id="47b73-116">Перед использованием пользовательского Presenter необходимо зарегистрировать библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="47b73-116">Before using the custom presenter, you must register the DLL.</span></span>

<span data-ttu-id="47b73-117">Чтобы использовать этот пример в Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="47b73-117">To use this sample in Media Foundation:</span></span>

1.  <span data-ttu-id="47b73-118">Выполните сборку примера.</span><span class="sxs-lookup"><span data-stu-id="47b73-118">Build the sample.</span></span>
2.  <span data-ttu-id="47b73-119">EvrPresenter.dll regsvr32.</span><span class="sxs-lookup"><span data-stu-id="47b73-119">Regsvr32 EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="47b73-120">Выполните сборку и запустите [Пример мфплайер](/previous-versions//bb970516(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="47b73-120">Build and run the [MFPlayer Sample](/previous-versions//bb970516(v=vs.85)).</span></span>
4.  <span data-ttu-id="47b73-121">В меню **файл** выберите **Открыть** файл.</span><span class="sxs-lookup"><span data-stu-id="47b73-121">From the **File** menu, select **Open** File.</span></span>
5.  <span data-ttu-id="47b73-122">В диалоговом окне **Открытие файла** выберите **Custom Евр Presenter (пользовательский выступающий).**</span><span class="sxs-lookup"><span data-stu-id="47b73-122">In the **Open File** dialog box, select **Custom EVR Presenter.**</span></span>
6.  <span data-ttu-id="47b73-123">Выберите файл для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="47b73-123">Select a file for playback.</span></span>

<span data-ttu-id="47b73-124">Чтобы использовать этот пример в DirectShow, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="47b73-124">To use this sample in DirectShow:</span></span>

1.  <span data-ttu-id="47b73-125">Выполните сборку примера.</span><span class="sxs-lookup"><span data-stu-id="47b73-125">Build the sample.</span></span>
2.  <span data-ttu-id="47b73-126">Зарегистрируйте EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="47b73-126">Register EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="47b73-127">Выполните сборку и запустите пример Еврплайер.</span><span class="sxs-lookup"><span data-stu-id="47b73-127">Build and run the EVRPlayer sample.</span></span> <span data-ttu-id="47b73-128">Этот пример включен в примеры DirectShow в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="47b73-128">This sample is included with the DirectShow samples in the Windows SDK.</span></span>
4.  <span data-ttu-id="47b73-129">В меню **файл** выберите **Евр Presenter**.</span><span class="sxs-lookup"><span data-stu-id="47b73-129">From the **File** menu, select **EVR Presenter**.</span></span>
5.  <span data-ttu-id="47b73-130">Выберите файл для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="47b73-130">Select a file for playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="47b73-131">Требования</span><span class="sxs-lookup"><span data-stu-id="47b73-131">Requirements</span></span>



| <span data-ttu-id="47b73-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="47b73-132">Product</span></span>                                                        | <span data-ttu-id="47b73-133">Version</span><span class="sxs-lookup"><span data-stu-id="47b73-133">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="47b73-134">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="47b73-134">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="47b73-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="47b73-135">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="47b73-136">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="47b73-136">Downloading the Sample</span></span>

<span data-ttu-id="47b73-137">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="47b73-137">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47b73-138">См. также</span><span class="sxs-lookup"><span data-stu-id="47b73-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47b73-139">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="47b73-139">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="47b73-140">Написание выступающего Евр</span><span class="sxs-lookup"><span data-stu-id="47b73-140">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="47b73-141">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47b73-141">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
