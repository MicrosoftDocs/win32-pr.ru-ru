---
description: Интерфейсы потоковой передачи аудио
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Интерфейсы потоковой передачи аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538015"
---
# <a name="audio-streaming-interfaces"></a><span data-ttu-id="89c2b-103">Интерфейсы потоковой передачи аудио</span><span class="sxs-lookup"><span data-stu-id="89c2b-103">Audio Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="89c2b-104">Эти API-интерфейсы являются устаревшими.</span><span class="sxs-lookup"><span data-stu-id="89c2b-104">These APIs are deprecated.</span></span> <span data-ttu-id="89c2b-105">Приложения должны использовать [**образец фильтра захвата**](sample-grabber-filter.md) или реализовать настраиваемый фильтр для получения данных из графа фильтра DirectShow.</span><span class="sxs-lookup"><span data-stu-id="89c2b-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 



| <span data-ttu-id="89c2b-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="89c2b-106">Interface</span></span>                                        | <span data-ttu-id="89c2b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="89c2b-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89c2b-108">**иаудиомедиастреам**</span><span class="sxs-lookup"><span data-stu-id="89c2b-108">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | <span data-ttu-id="89c2b-109">Управляет потоками аудио мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="89c2b-109">Controls audio media streams.</span></span> <span data-ttu-id="89c2b-110">Этот интерфейс наследуется от интерфейса [**имедиастреам**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) и используется для создания одного или нескольких объектов [**иаудиостреамсампле**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="89c2b-110">This interface inherits from the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and is used to create one or more [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) objects.</span></span> <span data-ttu-id="89c2b-111">Он также используется для задания и получения текущего формата потоковых данных.</span><span class="sxs-lookup"><span data-stu-id="89c2b-111">It is also used to set and retrieve the current format of the stream data.</span></span>                                                                                                            |
| [<span data-ttu-id="89c2b-112">**иаудиостреамсампле**</span><span class="sxs-lookup"><span data-stu-id="89c2b-112">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | <span data-ttu-id="89c2b-113">Получает сведения из базовых объектов данных [**иаудиодата**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) .</span><span class="sxs-lookup"><span data-stu-id="89c2b-113">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="89c2b-114">**имеморидата**</span><span class="sxs-lookup"><span data-stu-id="89c2b-114">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | <span data-ttu-id="89c2b-115">Содержит методы, которые устанавливают и извлекают данные памяти для объектов звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="89c2b-115">Contains methods that set and retrieve memory data on audio data objects.</span></span> <span data-ttu-id="89c2b-116">Объекты звуковых данных предоставляют базовые данные, доступ к которым осуществляется с помощью Streaming Samples.</span><span class="sxs-lookup"><span data-stu-id="89c2b-116">Audio data objects provide the underlying data that stream samples access.</span></span> <span data-ttu-id="89c2b-117">Этот интерфейс предоставляет способ инициализации буферов памяти и установки фактических объемов звуковых данных в объектах.</span><span class="sxs-lookup"><span data-stu-id="89c2b-117">This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects.</span></span> <span data-ttu-id="89c2b-118">Кроме того, метод [**имеморидата:: info**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) можно использовать для получения данных о звуковой памяти.</span><span class="sxs-lookup"><span data-stu-id="89c2b-118">Additionally, the [**IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) method can be used to retrieve audio memory data.</span></span> |
| [<span data-ttu-id="89c2b-119">**иаудиодата**</span><span class="sxs-lookup"><span data-stu-id="89c2b-119">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | <span data-ttu-id="89c2b-120">Предоставляет методы, позволяющие приложениям устанавливать и получать базовые звуковые данные, на которые будут ссылаться звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="89c2b-120">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span> <span data-ttu-id="89c2b-121">Формат звуковых данных задается в структуре [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="89c2b-121">The audio data format is set in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="89c2b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="89c2b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89c2b-123">Список интерфейсов потоковой передачи мультимедиа</span><span class="sxs-lookup"><span data-stu-id="89c2b-123">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
