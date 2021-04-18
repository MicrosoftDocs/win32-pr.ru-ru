---
description: Уровень конвейера в Microsoft Media Foundation — это уровень архитектуры, который непосредственно создает или обрабатывает данные мультимедиа.
ms.assetid: d6396246-ddc4-4e24-9371-35ddbef59b8a
title: Конвейер Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f307049d7f88ca6b50479bdb261c75ba20f9b41e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720022"
---
# <a name="media-foundation-pipeline"></a><span data-ttu-id="cce48-103">Конвейер Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cce48-103">Media Foundation Pipeline</span></span>

<span data-ttu-id="cce48-104">Уровень *конвейера* в Microsoft Media Foundation — это уровень архитектуры, который непосредственно создает или обрабатывает данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cce48-104">The *pipeline* layer in Microsoft Media Foundation is the layer of the architecture that directly generates or processes media data.</span></span>

<span data-ttu-id="cce48-105">Большинство приложений не вызывают методы непосредственно в компонентах конвейера, хотя это можно сделать.</span><span class="sxs-lookup"><span data-stu-id="cce48-105">Most applications do not call methods directly on the pipeline components, although it is possible to do so.</span></span> <span data-ttu-id="cce48-106">Прочтите эти разделы при написании пользовательского компонента конвейера.</span><span class="sxs-lookup"><span data-stu-id="cce48-106">Read these topics if you are writing a custom pipeline component.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cce48-107">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="cce48-107">In this section</span></span>



| <span data-ttu-id="cce48-108">Раздел</span><span class="sxs-lookup"><span data-stu-id="cce48-108">Topic</span></span>                                                                     | <span data-ttu-id="cce48-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cce48-109">Description</span></span>                                                                                                                           |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cce48-110">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cce48-110">Media Sources</span></span>](media-sources.md)<br/>                             | <span data-ttu-id="cce48-111">Источники мультимедиа создают данные мультимедиа, обычно из файла, устройства записи или сетевого потока.</span><span class="sxs-lookup"><span data-stu-id="cce48-111">Media sources generate media data, typically from a file, capture device, or network stream.</span></span> <br/>                              |
| [<span data-ttu-id="cce48-112">Преобразования Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cce48-112">Media Foundation Transforms</span></span>](media-foundation-transforms.md)<br/> | <span data-ttu-id="cce48-113">Media Foundation преобразования (МФТС) обработка данных мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cce48-113">Media Foundation transforms (MFTs) process media data.</span></span> <span data-ttu-id="cce48-114">Например, кодеки в Media Foundation реализуются как МФТС.</span><span class="sxs-lookup"><span data-stu-id="cce48-114">For example, codecs in Media Foundation are implemented as MFTs.</span></span> <br/>   |
| [<span data-ttu-id="cce48-115">Приемники носителей</span><span class="sxs-lookup"><span data-stu-id="cce48-115">Media Sinks</span></span>](media-sinks.md)<br/>                                 | <span data-ttu-id="cce48-116">Приемники носителей используют данные мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cce48-116">Media sinks consume media data.</span></span> <span data-ttu-id="cce48-117">Например, приемник мультимедиа может записать данные в файл или отправить данные по сети.</span><span class="sxs-lookup"><span data-stu-id="cce48-117">For example, a media sink might write the data to a file, or send the data over a network.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="cce48-118">См. также</span><span class="sxs-lookup"><span data-stu-id="cce48-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cce48-119">Media Foundation и COM</span><span class="sxs-lookup"><span data-stu-id="cce48-119">Media Foundation and COM</span></span>](media-foundation-and-com.md)
</dt> <dt>

[<span data-ttu-id="cce48-120">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cce48-120">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




