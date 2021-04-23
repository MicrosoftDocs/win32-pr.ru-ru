---
description: Указывает, будет ли кодек использовать оптимизацию масштабирования видео.
ms.assetid: a21d0100-e020-4e74-b8e3-bb7071194828
title: Свойство MFPKEY_VIDEOSCALING (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 555cec22533b7817c509d5419391039b10c92576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898750"
---
# <a name="mfpkey_videoscaling-property"></a><span data-ttu-id="940f6-103">МФПКЭЙ \_ видеоскалинг, свойство</span><span class="sxs-lookup"><span data-stu-id="940f6-103">MFPKEY\_VIDEOSCALING Property</span></span>

<span data-ttu-id="940f6-104">Указывает, будет ли кодек использовать оптимизацию масштабирования видео.</span><span class="sxs-lookup"><span data-stu-id="940f6-104">Specifies whether the codec will use video scaling optimization.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="940f6-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="940f6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="940f6-106">g \_ всзвмвквидеоскалинг</span><span class="sxs-lookup"><span data-stu-id="940f6-106">g\_wszWMVCVideoScaling</span></span>

## <a name="data-type"></a><span data-ttu-id="940f6-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="940f6-107">Data Type</span></span>

<span data-ttu-id="940f6-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="940f6-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="940f6-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="940f6-109">Default Value</span></span>

<span data-ttu-id="940f6-110">0</span><span class="sxs-lookup"><span data-stu-id="940f6-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="940f6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="940f6-111">Remarks</span></span>

<span data-ttu-id="940f6-112">Масштабирование видео — это тип оптимизации искусственного, который может улучшить качество визуального изображения в кодировке с низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="940f6-112">Video scaling is a type of perceptual optimization that can improve the visual quality of video encoded at low bit rates.</span></span> <span data-ttu-id="940f6-113">Оптимизация масштабирования видео сокращает произносит производимые артефакты, но может пожертвовать деталями изображения.</span><span class="sxs-lookup"><span data-stu-id="940f6-113">The video scaling optimization reduces pronounced artifacts, but can sacrifice image detail.</span></span> <span data-ttu-id="940f6-114">Эта оптимизация влияет на диапазон яркости в кодированном видео, как описано ниже, но не влияет на физическое разрешение выходного видео.</span><span class="sxs-lookup"><span data-stu-id="940f6-114">This optimization affects the luma range of the encoded video as described below but does not affect the physical resolution of the output video.</span></span>

<span data-ttu-id="940f6-115">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="940f6-115">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="940f6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="940f6-116">Value</span></span> | <span data-ttu-id="940f6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="940f6-117">Description</span></span>                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="940f6-118">0</span><span class="sxs-lookup"><span data-stu-id="940f6-118">0</span></span>     | <span data-ttu-id="940f6-119">Масштабирование видео не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="940f6-119">Video scaling will not be used.</span></span>                                                                                       |
| <span data-ttu-id="940f6-120">1</span><span class="sxs-lookup"><span data-stu-id="940f6-120">1</span></span>     | <span data-ttu-id="940f6-121">Кодировщик будет использовать консервативную оптимизацию масштабирования видео.</span><span class="sxs-lookup"><span data-stu-id="940f6-121">The encoder will use conservative video scaling optimization.</span></span> <span data-ttu-id="940f6-122">Диапазон яркости будет масштабироваться от 0... 255 до 26... 229.</span><span class="sxs-lookup"><span data-stu-id="940f6-122">The luma range will be scaled from 0...255 to 26...229.</span></span> |
| <span data-ttu-id="940f6-123">2</span><span class="sxs-lookup"><span data-stu-id="940f6-123">2</span></span>     | <span data-ttu-id="940f6-124">Кодировщик будет использовать агрессивную оптимизацию масштабирования видео.</span><span class="sxs-lookup"><span data-stu-id="940f6-124">The encoder will use aggressive video scaling optimization.</span></span> <span data-ttu-id="940f6-125">Диапазон яркости будет масштабироваться от 0... 255 до 31... 224.</span><span class="sxs-lookup"><span data-stu-id="940f6-125">The luma range will be scaled from 0...255 to 31...224.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="940f6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="940f6-126">Requirements</span></span>



| <span data-ttu-id="940f6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="940f6-127">Requirement</span></span> | <span data-ttu-id="940f6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="940f6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="940f6-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="940f6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="940f6-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="940f6-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="940f6-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="940f6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="940f6-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="940f6-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="940f6-133">Header</span><span class="sxs-lookup"><span data-stu-id="940f6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="940f6-134"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="940f6-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="940f6-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="940f6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="940f6-136">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="940f6-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




