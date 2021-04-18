---
description: Использование приемника мультимедиа Евр
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Использование приемника мультимедиа Евр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713302"
---
# <a name="using-the-evr-media-sink"></a><span data-ttu-id="d0c6c-103">Использование приемника мультимедиа Евр</span><span class="sxs-lookup"><span data-stu-id="d0c6c-103">Using the EVR Media Sink</span></span>

<span data-ttu-id="d0c6c-104">Расширенный приемник мультимедиа модуля подготовки видео (Евр) можно использовать в качестве отдельного компонента.</span><span class="sxs-lookup"><span data-stu-id="d0c6c-104">The enhanced video renderer (EVR) media sink can be used as a stand-alone component.</span></span> <span data-ttu-id="d0c6c-105">Тем не менее часто приложение создает приемник мультимедиа Евр в топологии, а затем использует сеанс мультимедиа для управления воспроизведением.</span><span class="sxs-lookup"><span data-stu-id="d0c6c-105">More often, however, an application will create the EVR media sink inside a topology, and then use the Media Session to control playback.</span></span>

<span data-ttu-id="d0c6c-106">Существует два способа создания приемника мультимедиа Евр.</span><span class="sxs-lookup"><span data-stu-id="d0c6c-106">There are two ways to create the EVR media sink:</span></span>

-   <span data-ttu-id="d0c6c-107">Функция [**мфкреатевидеорендерер**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) создает приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d0c6c-107">The [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) function creates the media sink.</span></span>

-   <span data-ttu-id="d0c6c-108">Функция [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) создает объект активации для приемника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d0c6c-108">The [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function creates an activation object for the media sink.</span></span>

<span data-ttu-id="d0c6c-109">Приемник носителя Евр изначально имеет один приемник потока, который соответствует потоку ссылок.</span><span class="sxs-lookup"><span data-stu-id="d0c6c-109">The EVR media sink initially has one stream sink, which corresponds to the reference stream.</span></span> <span data-ttu-id="d0c6c-110">Чтобы добавить новые приемники потока, вызовите метод [**имфмедиасинк:: аддстреамсинк**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span><span class="sxs-lookup"><span data-stu-id="d0c6c-110">To add new stream sinks, call [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0c6c-111">См. также</span><span class="sxs-lookup"><span data-stu-id="d0c6c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0c6c-112">Улучшенный модуль подготовки видео</span><span class="sxs-lookup"><span data-stu-id="d0c6c-112">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="d0c6c-113">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="d0c6c-113">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 



