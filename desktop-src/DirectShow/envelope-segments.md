---
description: Сегменты конверта
ms.assetid: 1b59cd1c-7c37-4c70-a36c-2ee1f42b42c5
title: Сегменты конверта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bac997667f52ef9bbf14760584889fa16cbbd04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537379"
---
# <a name="envelope-segments"></a><span data-ttu-id="32ae5-103">Сегменты конверта</span><span class="sxs-lookup"><span data-stu-id="32ae5-103">Envelope Segments</span></span>

<span data-ttu-id="32ae5-104">Кривая параметра состоит из одного или нескольких сегментов конверта, определенных с помощью структуры [**\_ \_ сегмента конверта MP**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) .</span><span class="sxs-lookup"><span data-stu-id="32ae5-104">A parameter curve consists of one or more envelope segments, defined using the [**MP\_ENVELOPE\_SEGMENT**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_envelope_segment) structure.</span></span> <span data-ttu-id="32ae5-105">Эта структура содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="32ae5-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="32ae5-106">Время начала и окончания.</span><span class="sxs-lookup"><span data-stu-id="32ae5-106">The start and end times.</span></span>
-   <span data-ttu-id="32ae5-107">Начальное и конечное значения.</span><span class="sxs-lookup"><span data-stu-id="32ae5-107">The starting and ending values.</span></span>
-   <span data-ttu-id="32ae5-108">Тип кривой (линейный, квадратный и т. д.).</span><span class="sxs-lookup"><span data-stu-id="32ae5-108">The curve type (linear, square, and so forth).</span></span>
-   <span data-ttu-id="32ae5-109">Необязательные флаги, описанные в скором времени.</span><span class="sxs-lookup"><span data-stu-id="32ae5-109">Optional flags, described shortly.</span></span>

<span data-ttu-id="32ae5-110">Клиент добавляет сегменты конверта в параметр, вызывая метод [**имедиапарамс:: адденвелопе**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) и передавая массив **\_ \_ сегментов конверта MP** .</span><span class="sxs-lookup"><span data-stu-id="32ae5-110">The client adds envelope segments to a parameter by calling the [**IMediaParams::AddEnvelope**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-addenvelope) method and passing in an array of **MP\_ENVELOPE\_SEGMENT** structures.</span></span> <span data-ttu-id="32ae5-111">Клиент должен отсортировать сегменты в возрастающем порядке по времени перед вызовом метода.</span><span class="sxs-lookup"><span data-stu-id="32ae5-111">The client should sort the segments into ascending time order before calling the method.</span></span> <span data-ttu-id="32ae5-112">Так как DMO обрабатывает данные, вы можете представить параметр, передаваемых по каждому сегменту конверта, например автомобиль, посвященный ряду Хиллс.</span><span class="sxs-lookup"><span data-stu-id="32ae5-112">As the DMO processes data, you can imagine the parameter traveling over each envelope segment, like a car driving over a series of hills.</span></span> <span data-ttu-id="32ae5-113">Метод [**имедиапарамс:: param**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) Возвращает самое последнее значение.</span><span class="sxs-lookup"><span data-stu-id="32ae5-113">The [**IMediaParams::GetParam**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-getparam) method returns the most recent value.</span></span>

<span data-ttu-id="32ae5-114">Два смежных сегмента могут иметь разрыв между ними.</span><span class="sxs-lookup"><span data-stu-id="32ae5-114">Two adjacent segments can have a gap between them.</span></span> <span data-ttu-id="32ae5-115">Во время пропусков параметр оставляет свое предыдущее значение следующим образом:</span><span class="sxs-lookup"><span data-stu-id="32ae5-115">During gaps, the parameter retains its previous value, as follows:</span></span>

-   <span data-ttu-id="32ae5-116">Перед первым сегментом значением является нейтральное значение.</span><span class="sxs-lookup"><span data-stu-id="32ae5-116">Before the first segment, the value is the neutral value.</span></span>
-   <span data-ttu-id="32ae5-117">Между сегментами значение является конечным значением предыдущего сегмента.</span><span class="sxs-lookup"><span data-stu-id="32ae5-117">Between segments, the value is the ending value of the previous segment.</span></span>
-   <span data-ttu-id="32ae5-118">После последнего сегмента значение остается в конечном значении этого сегмента.</span><span class="sxs-lookup"><span data-stu-id="32ae5-118">After the last segment, the value remains at the ending value of that segment.</span></span>
-   <span data-ttu-id="32ae5-119">Если клиент очищает DMO, значение возвращается к нейтральному значению.</span><span class="sxs-lookup"><span data-stu-id="32ae5-119">If the client flushes the DMO, the value reverts to the neutral value.</span></span>

<span data-ttu-id="32ae5-120">Сегмент можно изменить, задав один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="32ae5-120">You can alter a segment by setting either of the following flags:</span></span>

-   <span data-ttu-id="32ae5-121">MPF \_ енвлп \_ Begin \_ куррентвал.</span><span class="sxs-lookup"><span data-stu-id="32ae5-121">MPF\_ENVLP\_BEGIN\_CURRENTVAL.</span></span> <span data-ttu-id="32ae5-122">Объект DMO использует самое последнее значение параметра в качестве начального значения для сегмента.</span><span class="sxs-lookup"><span data-stu-id="32ae5-122">The DMO uses the most recent value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="32ae5-123">Это может быть нейтральное значение или конечное значение из предыдущего сегмента.</span><span class="sxs-lookup"><span data-stu-id="32ae5-123">This might be the neutral value, or the ending value from the previous segment.</span></span> <span data-ttu-id="32ae5-124">DMO игнорирует элемент **валстарт** в структуре **\_ \_ сегмента конверта MP** .</span><span class="sxs-lookup"><span data-stu-id="32ae5-124">The DMO ignores the **valStart** member of the **MP\_ENVELOPE\_SEGMENT** structure.</span></span>
-   <span data-ttu-id="32ae5-125">MPF \_ енвлп \_ Begin \_ неутралвал.</span><span class="sxs-lookup"><span data-stu-id="32ae5-125">MPF\_ENVLP\_BEGIN\_NEUTRALVAL.</span></span> <span data-ttu-id="32ae5-126">Объект DMO использует нейтральное значение параметра в качестве начального значения для сегмента.</span><span class="sxs-lookup"><span data-stu-id="32ae5-126">The DMO uses the neutral value of the parameter as the starting value for the segment.</span></span> <span data-ttu-id="32ae5-127">Он игнорирует **валстарт**.</span><span class="sxs-lookup"><span data-stu-id="32ae5-127">It ignores **valStart**.</span></span>

<span data-ttu-id="32ae5-128">Эти флаги можно рассматривать как отправку начальной точки сегмента и перемещать их вверх или вниз, в то время как конечное значение остается фиксированным.</span><span class="sxs-lookup"><span data-stu-id="32ae5-128">You can think of these flags as grabbing the starting point of the segment and moving it up or down, while the ending value remains fixed.</span></span> <span data-ttu-id="32ae5-129">Сегмент будет растягиваться соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="32ae5-129">The segment will "stretch" accordingly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32ae5-130">См. также</span><span class="sxs-lookup"><span data-stu-id="32ae5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32ae5-131">Параметры носителя</span><span class="sxs-lookup"><span data-stu-id="32ae5-131">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



