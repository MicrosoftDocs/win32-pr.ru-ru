---
description: Интерфейсы потоковой передачи DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Интерфейсы потоковой передачи DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072233"
---
# <a name="directdraw-streaming-interfaces"></a><span data-ttu-id="fe827-103">Интерфейсы потоковой передачи DirectDraw</span><span class="sxs-lookup"><span data-stu-id="fe827-103">DirectDraw Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="fe827-104">Эти API-интерфейсы являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="fe827-104">These APIs are deprecated.</span></span> <span data-ttu-id="fe827-105">Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fe827-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="fe827-106">При использовании в потоках форматов видео, поддерживаемых DirectDraw, следующие интерфейсы предоставляют более мощный контроль над данными, чем более универсальные базовые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="fe827-106">If you use DirectDraw-supported video formats in your streams, the following interfaces give you more powerful control over the data than the more generic base interfaces.</span></span>



| <span data-ttu-id="fe827-107">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="fe827-107">Interface</span></span>                                                  | <span data-ttu-id="fe827-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fe827-108">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe827-109">**идиректдравмедиастреам**</span><span class="sxs-lookup"><span data-stu-id="fe827-109">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="fe827-110">Задает и получает формат потока и объект DirectDraw, связанный с потоком мультимедиа. Этот интерфейс является производным от [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span><span class="sxs-lookup"><span data-stu-id="fe827-110">Sets and retrieves the stream format and the DirectDraw object associated with the media stream; this interface derives from [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span></span> <span data-ttu-id="fe827-111">Этот интерфейс также можно использовать для создания видеороликов.</span><span class="sxs-lookup"><span data-stu-id="fe827-111">You can also use this interface to create video samples.</span></span> |
| [<span data-ttu-id="fe827-112">**идиректдравстреамсампле**</span><span class="sxs-lookup"><span data-stu-id="fe827-112">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="fe827-113">Позволяет подключать образцы видео к поверхности DirectDraw; Этот интерфейс является производным от интерфейса [**истреамсампле**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) .</span><span class="sxs-lookup"><span data-stu-id="fe827-113">Enables you to attach video samples to DirectDraw surfaces; this interface derives from the [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface.</span></span> <span data-ttu-id="fe827-114">Каждая Присоединенная область содержит прямоугольник обрезки для упрощения отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fe827-114">Each attached surface includes a clipping rectangle to make rendering easier.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fe827-115">См. также</span><span class="sxs-lookup"><span data-stu-id="fe827-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe827-116">Список интерфейсов потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fe827-116">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



