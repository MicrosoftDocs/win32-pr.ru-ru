---
description: Указывает логику, которую кодек будет использовать для обнаружения чередующихся исходных видео.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: Свойство MFPKEY_VTYPE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898209"
---
# <a name="mfpkey_vtype-property"></a><span data-ttu-id="7c0dd-103">МФПКЭЙ \_ втипе, свойство</span><span class="sxs-lookup"><span data-stu-id="7c0dd-103">MFPKEY\_VTYPE Property</span></span>

<span data-ttu-id="7c0dd-104">Указывает логику, которую кодек будет использовать для обнаружения чередующихся исходных видео.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-104">Specifies the logic that the codec will use to detect interlaced source video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7c0dd-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="7c0dd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7c0dd-106">g \_ всзвмвквтипе</span><span class="sxs-lookup"><span data-stu-id="7c0dd-106">g\_wszWMVCVType</span></span>

## <a name="data-type"></a><span data-ttu-id="7c0dd-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7c0dd-107">Data Type</span></span>

<span data-ttu-id="7c0dd-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7c0dd-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="7c0dd-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7c0dd-109">Default Value</span></span>

<span data-ttu-id="7c0dd-110">0</span><span class="sxs-lookup"><span data-stu-id="7c0dd-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="7c0dd-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c0dd-111">Remarks</span></span>

<span data-ttu-id="7c0dd-112">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="7c0dd-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7c0dd-113">Value</span></span> | <span data-ttu-id="7c0dd-114">Описание</span><span class="sxs-lookup"><span data-stu-id="7c0dd-114">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0dd-115">0</span><span class="sxs-lookup"><span data-stu-id="7c0dd-115">0</span></span>     | <span data-ttu-id="7c0dd-116">Кодек будет использовать стандартную логику обнаружения типов кадров.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-116">The codec will use the standard frame-type detection logic.</span></span>                                                                                 |
| <span data-ttu-id="7c0dd-117">1</span><span class="sxs-lookup"><span data-stu-id="7c0dd-117">1</span></span>     | <span data-ttu-id="7c0dd-118">Кодек будет обрабатывать все исходные видеоматериалы как чередующиеся кадры.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-118">The codec will treat all source video frames as interlaced frames.</span></span>                                                                          |
| <span data-ttu-id="7c0dd-119">2</span><span class="sxs-lookup"><span data-stu-id="7c0dd-119">2</span></span>     | <span data-ttu-id="7c0dd-120">Кодек будет обрабатывать все исходные видеоматериалы как поля с чередованием видео.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-120">The codec will treat all source video frames as fields of interlaced video.</span></span>                                                                 |
| <span data-ttu-id="7c0dd-121">3</span><span class="sxs-lookup"><span data-stu-id="7c0dd-121">3</span></span>     | <span data-ttu-id="7c0dd-122">Кодек автоматически определит, являются ли входные видеокадры перечередованием кадров или поля с чередованием видео.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-122">The codec will automatically determine whether input video frames are interlaced frames or fields of interlaced video.</span></span>                      |
| <span data-ttu-id="7c0dd-123">4</span><span class="sxs-lookup"><span data-stu-id="7c0dd-123">4</span></span>     | <span data-ttu-id="7c0dd-124">Кодек автоматически определит, являются ли входные видеокадры последовательными кадрами, чередованием кадров или полями с чередованием видео.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-124">The codec will automatically determine whether input video frames are progressive frames, interlaced frames, or fields of interlaced video.</span></span> |



 

<span data-ttu-id="7c0dd-125">Это свойство определяет метод кодирования изображения, используемый для последовательной или чередования кодирования видео.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-125">This property determines the picture encoding method used for progressive or interlaced video encoding.</span></span>

<span data-ttu-id="7c0dd-126">Если тип видео не указан, кодек будет использовать прогрессивную кодировку кадров для сеансов прогрессивной кодировки и поле с чередованием кодирования для сеансов кодирования с чередованием.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-126">If no video type is specified, the codec will use progressive frame encoding for progressive encoding sessions, and field interlaced encoding for interlaced encoding sessions.</span></span> <span data-ttu-id="7c0dd-127">Тип сеанса кодирования видео (прогрессивный или с чередованием) задается с помощью свойства [мфпкэй \_ интерлацедкодинженаблед](mfpkey-interlacedcodingenabledproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="7c0dd-127">The type of video encoding session (progressive or interlaced) is set by using the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="7c0dd-128">Для создания чередующихся выходных данных свойство [мфпкэй \_ интерлацедкодинженаблед](mfpkey-interlacedcodingenabledproperty.md) должно иметь значение Variant \_ true. в противном случае установка свойства мпфкэй втипе не \_ будет действовать.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-128">The [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property must be set to VARIANT\_TRUE in order to produce interlaced output; otherwise, setting the MPFKEY\_VTYPE property will have no effect.</span></span>

 

<span data-ttu-id="7c0dd-129">При кодировании видео с чередованием можно указать несколько методов кодирования изображений.</span><span class="sxs-lookup"><span data-stu-id="7c0dd-129">When interlaced video is being encoded, it is possible to specify several picture encoding methods.</span></span> <span data-ttu-id="7c0dd-130">Как правило, самый эффективный способ кодирования видео с чередованием — использовать метод с чередованием (2).</span><span class="sxs-lookup"><span data-stu-id="7c0dd-130">Typically the most efficient way to encode interlaced video is to use the field interlaced method (2).</span></span> <span data-ttu-id="7c0dd-131">Если исходное видео содержит очень малое движение, то может оказаться более подходящим метод с чередованием кадров (1) или методом автоматического кадра/поля (2).</span><span class="sxs-lookup"><span data-stu-id="7c0dd-131">If the source video contains very little motion, the frame interlaced method (1) or the auto frame/field method (2) might be more suitable.</span></span>

<span data-ttu-id="7c0dd-132">При кодировании смешанного содержимого (содержащего как прогрессивные, так и чередующиеся кадры) лучше использовать значение автокадров/поле/прогрессивный метод (4).</span><span class="sxs-lookup"><span data-stu-id="7c0dd-132">When encoding mixed content (containing both progressive and interlaced frames), it's best to use the value auto frame/field/progressive method (4).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c0dd-133">Требования</span><span class="sxs-lookup"><span data-stu-id="7c0dd-133">Requirements</span></span>



| <span data-ttu-id="7c0dd-134">Требование</span><span class="sxs-lookup"><span data-stu-id="7c0dd-134">Requirement</span></span> | <span data-ttu-id="7c0dd-135">Значение</span><span class="sxs-lookup"><span data-stu-id="7c0dd-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c0dd-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c0dd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7c0dd-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7c0dd-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7c0dd-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c0dd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7c0dd-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c0dd-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c0dd-140">Header</span><span class="sxs-lookup"><span data-stu-id="7c0dd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c0dd-141"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c0dd-141"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c0dd-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c0dd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c0dd-143">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c0dd-143">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




