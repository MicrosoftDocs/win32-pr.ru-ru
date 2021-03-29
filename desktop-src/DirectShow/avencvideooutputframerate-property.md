---
description: Указывает частоту кадров в потоке вывода кодировщика, в кадрах в секунду.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Свойство Авенквидеуутпутфрамерате (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805824"
---
# <a name="avencvideooutputframerate-property"></a><span data-ttu-id="313f2-103">Авенквидеуутпутфрамерате, свойство</span><span class="sxs-lookup"><span data-stu-id="313f2-103">AVEncVideoOutputFrameRate property</span></span>

<span data-ttu-id="313f2-104">Указывает частоту кадров в потоке вывода кодировщика, в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="313f2-104">Specifies the frame rate on the encoder's output stream, in frames per second.</span></span>

<span data-ttu-id="313f2-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="313f2-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="313f2-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="313f2-106">Data type</span></span>

<span data-ttu-id="313f2-107">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="313f2-107">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="313f2-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="313f2-108">Property GUID</span></span>

<span data-ttu-id="313f2-109">**КОДЕКАПИ \_ авенквидеуутпутфрамерате**</span><span class="sxs-lookup"><span data-stu-id="313f2-109">**CODECAPI\_AVEncVideoOutputFrameRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="313f2-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="313f2-110">Property value</span></span>

<span data-ttu-id="313f2-111">Значение этого свойства является отношением, определяющим частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="313f2-111">The value of this property is a ratio that defines the frame rate.</span></span> <span data-ttu-id="313f2-112">Верхние 32 бита содержат числитель, а младшие 32 биты содержат знаменатель.</span><span class="sxs-lookup"><span data-stu-id="313f2-112">The upper 32 bits contain the numerator, and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="313f2-113">В следующей таблице показаны распространенные частоты кадров в кадрах за секунду.</span><span class="sxs-lookup"><span data-stu-id="313f2-113">The following table shows common frame rates, in frames per second.</span></span>



| <span data-ttu-id="313f2-114">Частота кадров</span><span class="sxs-lookup"><span data-stu-id="313f2-114">Frame rate</span></span> | <span data-ttu-id="313f2-115">Соотношение</span><span class="sxs-lookup"><span data-stu-id="313f2-115">Ratio</span></span>      |
|------------|------------|
| <span data-ttu-id="313f2-116">23,97</span><span class="sxs-lookup"><span data-stu-id="313f2-116">23.97</span></span>      | <span data-ttu-id="313f2-117">24000/1001</span><span class="sxs-lookup"><span data-stu-id="313f2-117">24000/1001</span></span> |
| <span data-ttu-id="313f2-118">24</span><span class="sxs-lookup"><span data-stu-id="313f2-118">24</span></span>         | <span data-ttu-id="313f2-119">24/1</span><span class="sxs-lookup"><span data-stu-id="313f2-119">24/1</span></span>       |
| <span data-ttu-id="313f2-120">25</span><span class="sxs-lookup"><span data-stu-id="313f2-120">25</span></span>         | <span data-ttu-id="313f2-121">25/1</span><span class="sxs-lookup"><span data-stu-id="313f2-121">25/1</span></span>       |
| <span data-ttu-id="313f2-122">29,97</span><span class="sxs-lookup"><span data-stu-id="313f2-122">29.97</span></span>      | <span data-ttu-id="313f2-123">30000/1001</span><span class="sxs-lookup"><span data-stu-id="313f2-123">30000/1001</span></span> |
| <span data-ttu-id="313f2-124">30</span><span class="sxs-lookup"><span data-stu-id="313f2-124">30</span></span>         | <span data-ttu-id="313f2-125">30/1</span><span class="sxs-lookup"><span data-stu-id="313f2-125">30/1</span></span>       |
| <span data-ttu-id="313f2-126">50</span><span class="sxs-lookup"><span data-stu-id="313f2-126">50</span></span>         | <span data-ttu-id="313f2-127">50/1</span><span class="sxs-lookup"><span data-stu-id="313f2-127">50/1</span></span>       |
| <span data-ttu-id="313f2-128">59,94</span><span class="sxs-lookup"><span data-stu-id="313f2-128">59.94</span></span>      | <span data-ttu-id="313f2-129">60000/1001</span><span class="sxs-lookup"><span data-stu-id="313f2-129">60000/1001</span></span> |
| <span data-ttu-id="313f2-130">60</span><span class="sxs-lookup"><span data-stu-id="313f2-130">60</span></span>         | <span data-ttu-id="313f2-131">60/1</span><span class="sxs-lookup"><span data-stu-id="313f2-131">60/1</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="313f2-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="313f2-132">Remarks</span></span>

<span data-ttu-id="313f2-133">Приложения могут установить это свойство, чтобы указать частоту выходных кадров.</span><span class="sxs-lookup"><span data-stu-id="313f2-133">Applications can set this property to specify the output frame rate.</span></span> <span data-ttu-id="313f2-134">Кодировщики также могут возвращать это свойство как возможность.</span><span class="sxs-lookup"><span data-stu-id="313f2-134">Encoders can also return this property as a capability.</span></span> <span data-ttu-id="313f2-135">В зависимости от кодировщика значение может быть ограничено частотой входного кадра.</span><span class="sxs-lookup"><span data-stu-id="313f2-135">Depending on the encoder, the value might be restricted to the input frame rate.</span></span> <span data-ttu-id="313f2-136">В противном случае кодировщик может преобразовать частоту кадров внутри.</span><span class="sxs-lookup"><span data-stu-id="313f2-136">If not, the encoder is able to convert the frame rate internally.</span></span> <span data-ttu-id="313f2-137">См. раздел [**свойство авенквидеуутпутфрамератеконверсион**](avencvideooutputframerateconversion-property.md).</span><span class="sxs-lookup"><span data-stu-id="313f2-137">See [**AVEncVideoOutputFrameRateConversion Property**](avencvideooutputframerateconversion-property.md).</span></span>

<span data-ttu-id="313f2-138">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="313f2-138">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="313f2-139">Требования</span><span class="sxs-lookup"><span data-stu-id="313f2-139">Requirements</span></span>



| <span data-ttu-id="313f2-140">Требование</span><span class="sxs-lookup"><span data-stu-id="313f2-140">Requirement</span></span> | <span data-ttu-id="313f2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="313f2-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="313f2-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="313f2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="313f2-143">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="313f2-143">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="313f2-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="313f2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="313f2-145">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="313f2-145">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="313f2-146">Header</span><span class="sxs-lookup"><span data-stu-id="313f2-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="313f2-147"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="313f2-147"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313f2-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="313f2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313f2-149">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="313f2-149">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="313f2-150">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="313f2-150">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

