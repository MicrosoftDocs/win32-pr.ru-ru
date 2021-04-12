---
description: Источники мультимедиа
ms.assetid: 65132e7d-22f6-4209-bc58-f5ea86ebd514
title: Источники мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd69b63679ba73bc4049f37207b1d07940edada
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104273244"
---
# <a name="media-sources"></a><span data-ttu-id="f559d-103">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f559d-103">Media Sources</span></span>

<span data-ttu-id="f559d-104">*Источники мультимедиа* — это объекты, которые создают данные мультимедиа в конвейере Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f559d-104">*Media sources* are objects that generate media data in the Media Foundation pipeline.</span></span> <span data-ttu-id="f559d-105">В этом разделе подробно описаны API-интерфейсы источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f559d-105">This section describes the media source APIs in detail.</span></span> <span data-ttu-id="f559d-106">Прочтите этот раздел, если вы реализуете пользовательский источник мультимедиа или используете источник мультимедиа за пределами конвейера Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f559d-106">Read this section if you are implementing a custom media source, or using a media source outside of the Media Foundation pipeline.</span></span>

<span data-ttu-id="f559d-107">Если приложение использует уровень элемента управления, он должен использовать только ограниченное подмножество API источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f559d-107">If your application uses the control layer, it needs to use only a limited subset of the media source APIs.</span></span> <span data-ttu-id="f559d-108">Дополнительные сведения см. в разделе [использование источников мультимедиа с сеансом мультимедиа](using-media-sources-with-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="f559d-108">For information, see the topic [Using Media Sources with the Media Session](using-media-sources-with-the-media-session.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f559d-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="f559d-109">In this section</span></span>



| <span data-ttu-id="f559d-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="f559d-110">Topic</span></span>                                                                                                 | <span data-ttu-id="f559d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f559d-111">Description</span></span>                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f559d-112">Объектная модель источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f559d-112">Media Source Object Model</span></span>](media-source-object-model.md)<br/>                                 | <span data-ttu-id="f559d-113">В этом разделе описывается объектная модель для источников мультимедиа в Microsoft Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f559d-113">This topic describes the object model for media sources in Microsoft Media Foundation</span></span><br/>                     |
| [<span data-ttu-id="f559d-114">Дескрипторы представления</span><span class="sxs-lookup"><span data-stu-id="f559d-114">Presentation Descriptors</span></span>](presentation-descriptors.md)<br/>                                   | <span data-ttu-id="f559d-115">*Дескриптор представления* — это объект, содержащий описание конкретной презентации.</span><span class="sxs-lookup"><span data-stu-id="f559d-115">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span><br/>      |
| [<span data-ttu-id="f559d-116">События источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f559d-116">Media Source Events</span></span>](media-source-events.md)<br/>                                             | <span data-ttu-id="f559d-117">В этом разделе перечислены события, отправляемые источниками мультимедиа и потоками мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f559d-117">This topic lists the events that are sent by media sources and media streams.</span></span><br/>                             |
| [<span data-ttu-id="f559d-118">Запись пользовательского источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f559d-118">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)<br/>                         | <span data-ttu-id="f559d-119">В этом разделе описано, как реализовать пользовательский источник мультимедиа в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f559d-119">This topic describes how to implement a custom media source in Media Foundation.</span></span><br/>                          |
| [<span data-ttu-id="f559d-120">Пример использования: источник мультимедиа MPEG-1</span><span class="sxs-lookup"><span data-stu-id="f559d-120">Case Study: MPEG-1 Media Source</span></span>](tutorial--writing-a-custom-media-source.md)<br/>             | <span data-ttu-id="f559d-121">В этом разделе приведен подробный обзор примера пакета SDK [MPEG-1 Media Source](mpeg1source-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="f559d-121">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span><br/>        |
| [<span data-ttu-id="f559d-122">Пользовательские поставщики метаданных для файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f559d-122">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)<br/> | <span data-ttu-id="f559d-123">В этом разделе описывается написание пользовательского обработчика свойств оболочки для Media Foundation источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f559d-123">This topic describes how to write a custom Shell property handler for a Media Foundation media source.</span></span><br/>    |
| [<span data-ttu-id="f559d-124">Сопоставитель источников</span><span class="sxs-lookup"><span data-stu-id="f559d-124">Source Resolver</span></span>](source-resolver.md)<br/>                                                     | <span data-ttu-id="f559d-125">Средство выбора источника принимает URL-адрес или поток байтов и создает соответствующий источник мультимедиа для этого контента.</span><span class="sxs-lookup"><span data-stu-id="f559d-125">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f559d-126">См. также</span><span class="sxs-lookup"><span data-stu-id="f559d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f559d-127">Конвейер Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f559d-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="f559d-128">Пользовательские поставщики метаданных для файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f559d-128">Custom Metadata Providers for Media Files</span></span>](custom-metadata-providers-for-media-files.md)
</dt> <dt>

[<span data-ttu-id="f559d-129">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f559d-129">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> </dl>

 

 




