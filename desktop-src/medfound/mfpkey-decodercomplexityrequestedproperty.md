---
description: Указывает шаблон соответствия устройств, который вы хотите использовать для кодирования видео.
ms.assetid: cd2c068a-dbbc-42c5-bc92-bbb73f0259d1
title: Свойство MFPKEY_DECODERCOMPLEXITYREQUESTED (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e017361d7e8267d33ecb2cfdbce2a6e79758fac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692856"
---
# <a name="mfpkey_decodercomplexityrequested-property"></a><span data-ttu-id="863a6-103">МФПКЭЙ \_ декодеркомплекситирекуестед, свойство</span><span class="sxs-lookup"><span data-stu-id="863a6-103">MFPKEY\_DECODERCOMPLEXITYREQUESTED Property</span></span>

<span data-ttu-id="863a6-104">Указывает шаблон соответствия устройств, который вы хотите использовать для кодирования видео.</span><span class="sxs-lookup"><span data-stu-id="863a6-104">Specifies the device conformance template that you want to use for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="863a6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="863a6-105">Data Type</span></span>

<span data-ttu-id="863a6-106">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="863a6-106">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="863a6-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="863a6-107">Default Value</span></span>

<span data-ttu-id="863a6-108">1</span><span class="sxs-lookup"><span data-stu-id="863a6-108">1</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="863a6-109">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="863a6-109">Constant for IPropertyBag</span></span>

<span data-ttu-id="863a6-110">g \_ всзвмвкдекодеркомплекситирекуестед</span><span class="sxs-lookup"><span data-stu-id="863a6-110">g\_wszWMVCDecoderComplexityRequested</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="863a6-111">Тип данных для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="863a6-111">Data Type for IPropertyBag</span></span>

<span data-ttu-id="863a6-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="863a6-112">VT\_BSTR</span></span>

## <a name="default-value-for-ipropertybag"></a><span data-ttu-id="863a6-113">Значение по умолчанию для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="863a6-113">Default Value for IPropertyBag</span></span>

<span data-ttu-id="863a6-114">МВ</span><span class="sxs-lookup"><span data-stu-id="863a6-114">"MP"</span></span>

## <a name="remarks"></a><span data-ttu-id="863a6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="863a6-115">Remarks</span></span>

<span data-ttu-id="863a6-116">Кодек попытается закодировать содержимое с помощью шаблона соответствия устройства, указанного в этом значении.</span><span class="sxs-lookup"><span data-stu-id="863a6-116">The codec will attempt to encode the content using the device conformance template specified by this value.</span></span> <span data-ttu-id="863a6-117">Фактический шаблон, которому можно получить закодированное содержимое, из свойства [мфпкэй \_ декодеркомплекситипрофиле](mfpkey-decodercomplexityprofileproperty.md) после кодировки.</span><span class="sxs-lookup"><span data-stu-id="863a6-117">The actual template to which the encoded content conforms can be retrieved from the [MFPKEY\_DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md) property after encoding.</span></span>

<span data-ttu-id="863a6-118">Это свойство должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="863a6-118">This property must be one of the following values.</span></span>



| <span data-ttu-id="863a6-119">Значение для Ипропертисторе</span><span class="sxs-lookup"><span data-stu-id="863a6-119">Value for IPropertyStore</span></span> | <span data-ttu-id="863a6-120">Значение для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="863a6-120">Value for IPropertyBag</span></span> | <span data-ttu-id="863a6-121">Описание</span><span class="sxs-lookup"><span data-stu-id="863a6-121">Description</span></span>         |
|--------------------------|------------------------|---------------------|
| <span data-ttu-id="863a6-122">0</span><span class="sxs-lookup"><span data-stu-id="863a6-122">0</span></span>                        | <span data-ttu-id="863a6-123">ПОРТОВ</span><span class="sxs-lookup"><span data-stu-id="863a6-123">"SP"</span></span>                   | <span data-ttu-id="863a6-124">простой профиль</span><span class="sxs-lookup"><span data-stu-id="863a6-124">simple profile</span></span>      |
| <span data-ttu-id="863a6-125">1</span><span class="sxs-lookup"><span data-stu-id="863a6-125">1</span></span>                        | <span data-ttu-id="863a6-126">МВ</span><span class="sxs-lookup"><span data-stu-id="863a6-126">"MP"</span></span>                   | <span data-ttu-id="863a6-127">Основной профиль</span><span class="sxs-lookup"><span data-stu-id="863a6-127">main profile</span></span>        |
| <span data-ttu-id="863a6-128">2</span><span class="sxs-lookup"><span data-stu-id="863a6-128">2</span></span>                        | <span data-ttu-id="863a6-129">CP</span><span class="sxs-lookup"><span data-stu-id="863a6-129">"CP"</span></span>                   | <span data-ttu-id="863a6-130">больше не поддерживается</span><span class="sxs-lookup"><span data-stu-id="863a6-130">no longer supported</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="863a6-131">Требования</span><span class="sxs-lookup"><span data-stu-id="863a6-131">Requirements</span></span>



| <span data-ttu-id="863a6-132">Требование</span><span class="sxs-lookup"><span data-stu-id="863a6-132">Requirement</span></span> | <span data-ttu-id="863a6-133">Значение</span><span class="sxs-lookup"><span data-stu-id="863a6-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="863a6-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="863a6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="863a6-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="863a6-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="863a6-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="863a6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="863a6-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="863a6-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="863a6-138">Header</span><span class="sxs-lookup"><span data-stu-id="863a6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="863a6-139"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="863a6-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="863a6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="863a6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="863a6-141">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="863a6-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




