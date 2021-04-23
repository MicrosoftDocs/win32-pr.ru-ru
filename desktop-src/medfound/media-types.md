---
description: Типы носителей
ms.assetid: 690fda6e-dcbd-44dc-968d-cc949126da81
title: Типы носителей (Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acbfb1b637eef6acb664d3d95a0488f155c6916
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351622"
---
# <a name="media-types-media-foundation"></a><span data-ttu-id="dc209-103">Типы носителей (Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="dc209-103">Media Types (Media Foundation)</span></span>

<span data-ttu-id="dc209-104">*Тип мультимедиа* — это способ описания формата потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dc209-104">A *media type* is a way to describe the format of a media stream.</span></span> <span data-ttu-id="dc209-105">В Media Foundation типы мультимедиа представлены интерфейсом [**имфмедиатипе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="dc209-105">In Media Foundation, media types are represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="dc209-106">Приложения используют типы мультимедиа для обнаружения формата файла мультимедиа или потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dc209-106">Applications use media types to discover the format of a media file or media stream.</span></span> <span data-ttu-id="dc209-107">Объекты в конвейере Media Foundation используют типы мультимедиа для согласования форматов, которые они будут доставлять или получать.</span><span class="sxs-lookup"><span data-stu-id="dc209-107">Objects in the Media Foundation pipeline use media types to negotiate the formats they will deliver or receive.</span></span>

<span data-ttu-id="dc209-108">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="dc209-108">This section contains the following topics.</span></span>



| <span data-ttu-id="dc209-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="dc209-109">Topic</span></span>                                                                    | <span data-ttu-id="dc209-110">Описание</span><span class="sxs-lookup"><span data-stu-id="dc209-110">Description</span></span>                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="dc209-111">О типах носителей</span><span class="sxs-lookup"><span data-stu-id="dc209-111">About Media Types</span></span>](about-media-types.md)                               | <span data-ttu-id="dc209-112">Общие сведения о типах носителей в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="dc209-112">General overview of media types in Media Foundation.</span></span>                             |
| [<span data-ttu-id="dc209-113">GUID типа носителя</span><span class="sxs-lookup"><span data-stu-id="dc209-113">Media Type GUIDs</span></span>](media-type-guids.md)                                 | <span data-ttu-id="dc209-114">Перечисляет определенные идентификаторы GUID для основных типов и подтипов.</span><span class="sxs-lookup"><span data-stu-id="dc209-114">Lists the defined GUIDs for major types and subtypes.</span></span>                            |
| [<span data-ttu-id="dc209-115">Типы звуковых носителей</span><span class="sxs-lookup"><span data-stu-id="dc209-115">Audio Media Types</span></span>](audio-media-types.md)                               | <span data-ttu-id="dc209-116">Создание типов мультимедиа для звуковых форматов.</span><span class="sxs-lookup"><span data-stu-id="dc209-116">How to create media types for audio formats.</span></span>                                     |
| [<span data-ttu-id="dc209-117">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="dc209-117">Video Media Types</span></span>](video-media-types.md)                               | <span data-ttu-id="dc209-118">Создание типов мультимедиа для форматов видео.</span><span class="sxs-lookup"><span data-stu-id="dc209-118">How to create media types for video formats.</span></span>                                     |
| [<span data-ttu-id="dc209-119">Полные и частичные типы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dc209-119">Complete and Partial Media Types</span></span>](complete-and-partial-media-types.md) | <span data-ttu-id="dc209-120">Описание различий между полными типами мультимедиа и частичными типами носителей.</span><span class="sxs-lookup"><span data-stu-id="dc209-120">Describes the difference between complete media types and partial media types.</span></span>   |
| [<span data-ttu-id="dc209-121">Преобразования типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dc209-121">Media Type Conversions</span></span>](media-type-conversions.md)                     | <span data-ttu-id="dc209-122">Преобразование между Media Foundationными типами носителей и более старыми структурами формата.</span><span class="sxs-lookup"><span data-stu-id="dc209-122">How to convert between Media Foundation media types and older format structures.</span></span> |
| [<span data-ttu-id="dc209-123">Вспомогательные функции типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dc209-123">Media Type Helper Functions</span></span>](media-type-helper-functions.md)           | <span data-ttu-id="dc209-124">Список функций, которые управляют или получают информацию из типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dc209-124">A list of functions that manipulate or get information from a media type.</span></span>        |
| [<span data-ttu-id="dc209-125">Код отладки типа носителя</span><span class="sxs-lookup"><span data-stu-id="dc209-125">Media Type Debugging Code</span></span>](media-type-debugging-code.md)               | <span data-ttu-id="dc209-126">Пример кода, демонстрирующий Просмотр типа мультимедиа во время отладки.</span><span class="sxs-lookup"><span data-stu-id="dc209-126">Example code that shows how to view a media type while debugging.</span></span>                |



 

## <a name="related-topics"></a><span data-ttu-id="dc209-127">См. также</span><span class="sxs-lookup"><span data-stu-id="dc209-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc209-128">Примитивы Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dc209-128">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> <dt>

[<span data-ttu-id="dc209-129">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dc209-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 



