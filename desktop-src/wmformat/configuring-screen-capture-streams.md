---
title: Настройка потоков снимка экрана
description: Настройка потоков снимка экрана
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- потоки, Настройка потоков захвата экрана
- кодеки, Настройка потоков захвата экрана
- потоки снимка экрана
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987172"
---
# <a name="configuring-screen-capture-streams"></a><span data-ttu-id="0a847-106">Настройка потоков снимка экрана</span><span class="sxs-lookup"><span data-stu-id="0a847-106">Configuring Screen Capture Streams</span></span>

<span data-ttu-id="0a847-107">Потоки, использующие экранный кодек Windows Media® Video 9, настраиваются приложениями таким же образом, как и обычные видеопотоки.</span><span class="sxs-lookup"><span data-stu-id="0a847-107">Streams that use the Windows Media® Video 9 Screen codec are configured by applications in the same way as normal video streams.</span></span> <span data-ttu-id="0a847-108">Однако если задать уровень сложности видео равным 0, то модуль записи будет игнорировать любое значение качества видео, заданное с помощью [**ивмвидеомедиапропс:: сеткуалити**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span><span class="sxs-lookup"><span data-stu-id="0a847-108">However, if you set the video complexity level to 0, the writer will ignore any video quality value set with [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span></span> <span data-ttu-id="0a847-109">Дополнительные сведения см. [в разделе Получение хороших результатов с помощью экранного видеокодека Windows Media видео 9](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span><span class="sxs-lookup"><span data-stu-id="0a847-109">For more information, see [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a847-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0a847-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a847-111">**Настройка потоков**</span><span class="sxs-lookup"><span data-stu-id="0a847-111">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="0a847-112">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="0a847-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="0a847-113">**Настройка потоков видео**</span><span class="sxs-lookup"><span data-stu-id="0a847-113">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




