---
description: В этом разделе описывается различие между полными типами мультимедиа и типами с частичными носителями.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Полные и частичные типы мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547391"
---
# <a name="complete-and-partial-media-types"></a><span data-ttu-id="4cbb0-103">Полные и частичные типы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="4cbb0-103">Complete and Partial Media Types</span></span>

<span data-ttu-id="4cbb0-104">В этом разделе описывается различие между полными типами мультимедиа и типами с частичными носителями.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-104">This topic describes the difference between complete media types and partial media types.</span></span>

## <a name="complete-media-types"></a><span data-ttu-id="4cbb0-105">Полные типы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="4cbb0-105">Complete Media Types</span></span>

<span data-ttu-id="4cbb0-106">*Полный* тип носителя — это тот, который полностью определяет формат потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-106">A *complete* media type is one that fully defines the format of the media stream.</span></span> <span data-ttu-id="4cbb0-107">При наличии полного типа носителя компонент конвейера может проанализировать потоковые данные, связанные с типом мультимедиа, без неоднозначности.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-107">Given a complete media type, a pipeline component can parse the stream data associated with the media type, with no ambiguity.</span></span>

<span data-ttu-id="4cbb0-108">Для несжатых форматов в следующих разделах определяются атрибуты, необходимые для полного типа носителя:</span><span class="sxs-lookup"><span data-stu-id="4cbb0-108">For uncompressed formats, the following topics define the attributes that are required for a complete media type:</span></span>

-   <span data-ttu-id="4cbb0-109">Аудио: [типы несжатых аудио мультимедиа](uncompressed-audio-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="4cbb0-109">Audio: [Uncompressed Audio Media Types](uncompressed-audio-media-types.md)</span></span>
-   <span data-ttu-id="4cbb0-110">Видео: [типы несжатых](uncompressed-video-media-types.md) видеоклипов</span><span class="sxs-lookup"><span data-stu-id="4cbb0-110">Video: [Uncompressed Video Media Types](uncompressed-video-media-types.md)</span></span>

<span data-ttu-id="4cbb0-111">Для сжатых (или *закодированных*) потоков определение полного типа носителя определяется кодеком.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-111">For compressed (or *encoded*) streams, the definition of a complete media type is defined by the codec.</span></span> <span data-ttu-id="4cbb0-112">Однако если для сжатого потока известны какие либо атрибуты несжатого типа, эти значения должны быть включены в тип носителя для сжатого потока.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-112">However, if any uncompressed type attributes are known for the compressed stream, these values should be included in the media type for the compressed stream.</span></span> <span data-ttu-id="4cbb0-113">Например, если известен размер кадра, установите атрибут [**\_ \_ \_ размера кадра MF MT**](mf-mt-frame-size-attribute.md) для типа носителя, даже если технически сжатый поток не имеет размера кадра.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-113">For example, if the frame size is known, set the [**MF\_MT\_FRAME\_SIZE**](mf-mt-frame-size-attribute.md) attribute on the media type, even though technically a compressed stream does not have a frame size.</span></span>

## <a name="partial-media-types"></a><span data-ttu-id="4cbb0-114">Типы частичных носителей</span><span class="sxs-lookup"><span data-stu-id="4cbb0-114">Partial Media Types</span></span>

<span data-ttu-id="4cbb0-115">В *частичном* типе носителя отсутствует один или несколько атрибутов, необходимых для полного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-115">A *partial* media type is lacks one or more of the attributes needed for a complete media type.</span></span> <span data-ttu-id="4cbb0-116">При перечислении возможных типов носителей компонент Microsoft Media Foundation может оставить значение неопределенным, чтобы указать, что он может обменяться любым значением.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-116">When enumerating possible media types, a Microsoft Media Foundation component may leave a value unset, to indicate that it can handle any value.</span></span> <span data-ttu-id="4cbb0-117">Например, обработчик видео может оставить атрибут [**\_ \_ \_ частоты кадров MF MT**](mf-mt-frame-rate-attribute.md) неизменным, чтобы указать, что он может обменяться любой частотой кадров, и при необходимости будет выполнять преобразование с частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-117">For example, a video processor might leave the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute unset, to indicate that it can handle any frame rate, and will perform a frame-rate conversion if necessary.</span></span>

<span data-ttu-id="4cbb0-118">При создании частичного типа носителя все равно следует включать как можно больше информации.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-118">If you create a partial media type, you should still include as much information as you know.</span></span> <span data-ttu-id="4cbb0-119">Однако тип мультимедиа не должен содержать неуверенные сведения.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-119">However, a media type must not include information that is uncertain.</span></span> <span data-ttu-id="4cbb0-120">Лучше, чтобы информация отсутствовала, чем ошибочная.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-120">It is better for information to be missing than wrong.</span></span>

<span data-ttu-id="4cbb0-121">Как минимум, частичный тип носителя должен содержать только два атрибута: [**\_ \_ основной \_ тип MF MT**](mf-mt-major-type-attribute.md) и [**\_ \_ подтип MF MT**](mf-mt-subtype-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="4cbb0-121">At a minimum, a partial media type should include just two attributes: [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) and [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md).</span></span>

<span data-ttu-id="4cbb0-122">Иногда Media Foundation компоненты должны предоставлять полные типы мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="4cbb0-122">Sometimes Media Foundation components must provide complete media types:</span></span>

-   <span data-ttu-id="4cbb0-123">Источники мультимедиа должны предоставлять полные типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-123">Media sources must provide complete output types.</span></span>
-   <span data-ttu-id="4cbb0-124">После установки типа входных данных декодеры должны предоставлять полные типы выходных данных.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-124">Decoders must provide complete output types, after the input type is set.</span></span> <span data-ttu-id="4cbb0-125">Перед установкой входного типа декодер может предоставить неполный выходной тип.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-125">Before the input type is set, a decoder might provide a partial output type.</span></span>
-   <span data-ttu-id="4cbb0-126">После установки типа выходных данных кодировщики должны предоставлять полные входные типы.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-126">Encoders must provide complete input types, after the output type is set.</span></span> <span data-ttu-id="4cbb0-127">Перед заданием типа выходных данных кодировщик может предоставить неполный входной тип.</span><span class="sxs-lookup"><span data-stu-id="4cbb0-127">Before the output type is set, an encoder might provide a partial input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cbb0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="4cbb0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cbb0-129">Типы носителей</span><span class="sxs-lookup"><span data-stu-id="4cbb0-129">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



