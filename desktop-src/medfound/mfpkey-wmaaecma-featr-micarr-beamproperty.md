---
description: Указывает, какой образ используется для записи голоса, используемой DSP для обработки массива микрофона.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Свойство MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692602"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a><span data-ttu-id="2f535-103">МФПКЭЙ \_ вмааекма \_ феатр \_ микарр, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="2f535-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_BEAM Property</span></span>

<span data-ttu-id="2f535-104">Указывает, какой образ используется для записи голоса, используемой DSP для обработки массива микрофона.</span><span class="sxs-lookup"><span data-stu-id="2f535-104">Specifies which beam the Voice Capture DSP uses for microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2f535-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="2f535-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2f535-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2f535-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2f535-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2f535-107">Data Type</span></span>

<span data-ttu-id="2f535-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2f535-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="2f535-109">Применение</span><span class="sxs-lookup"><span data-stu-id="2f535-109">Applies To</span></span>

-   [<span data-ttu-id="2f535-110">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="2f535-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="2f535-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2f535-111">Remarks</span></span>

<span data-ttu-id="2f535-112">Задайте это свойство, если свойство [мфпкэй \_ вмааекма \_ феатр \_ \_ mode микарр](mfpkey-wmaaecma-featr-micarr-modeproperty.md) имеет значение микаррай \_ extern \_ .</span><span class="sxs-lookup"><span data-stu-id="2f535-112">Set this property if the value of the [MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) property is MICARRAY\_EXTERN\_BEAM.</span></span>

<span data-ttu-id="2f535-113">Если значение [**мфпкэй \_ вмааекма \_ феатр \_ микарр \_ mode**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) равно микаррай Single- \_ \_ лучевой, можно прочитать это свойство, чтобы запросить, какую форму он выбрал в DSP.</span><span class="sxs-lookup"><span data-stu-id="2f535-113">If the value of [**MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) is MICARRAY\_SINGLE\_BEAM, you can read this property to query which beam was selected by the DSP.</span></span>

<span data-ttu-id="2f535-114">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="2f535-114">This property can have the following values.</span></span> <span data-ttu-id="2f535-115">Значения находятся в градусах по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="2f535-115">Values are in degrees horizontal.</span></span>



| <span data-ttu-id="2f535-116">Значение</span><span class="sxs-lookup"><span data-stu-id="2f535-116">Value</span></span> | <span data-ttu-id="2f535-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2f535-117">Description</span></span>              |
|-------|--------------------------|
| <span data-ttu-id="2f535-118">0</span><span class="sxs-lookup"><span data-stu-id="2f535-118">0</span></span>     | <span data-ttu-id="2f535-119">-50 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-119">-50 degrees.</span></span>             |
| <span data-ttu-id="2f535-120">1</span><span class="sxs-lookup"><span data-stu-id="2f535-120">1</span></span>     | <span data-ttu-id="2f535-121">-40 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-121">-40 degrees.</span></span>             |
| <span data-ttu-id="2f535-122">2</span><span class="sxs-lookup"><span data-stu-id="2f535-122">2</span></span>     | <span data-ttu-id="2f535-123">– 30 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-123">-30 degrees.</span></span>             |
| <span data-ttu-id="2f535-124">3</span><span class="sxs-lookup"><span data-stu-id="2f535-124">3</span></span>     | <span data-ttu-id="2f535-125">-20 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-125">-20 degrees.</span></span>             |
| <span data-ttu-id="2f535-126">4</span><span class="sxs-lookup"><span data-stu-id="2f535-126">4</span></span>     | <span data-ttu-id="2f535-127">-10 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-127">-10 degrees.</span></span>             |
| <span data-ttu-id="2f535-128">5</span><span class="sxs-lookup"><span data-stu-id="2f535-128">5</span></span>     | <span data-ttu-id="2f535-129">0 градусов (Центральная наобразная).</span><span class="sxs-lookup"><span data-stu-id="2f535-129">0 degrees (center beam).</span></span> |
| <span data-ttu-id="2f535-130">6</span><span class="sxs-lookup"><span data-stu-id="2f535-130">6</span></span>     | <span data-ttu-id="2f535-131">10 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-131">10 degrees.</span></span>              |
| <span data-ttu-id="2f535-132">7</span><span class="sxs-lookup"><span data-stu-id="2f535-132">7</span></span>     | <span data-ttu-id="2f535-133">20 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-133">20 degrees.</span></span>              |
| <span data-ttu-id="2f535-134">8</span><span class="sxs-lookup"><span data-stu-id="2f535-134">8</span></span>     | <span data-ttu-id="2f535-135">30 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-135">30 degrees.</span></span>              |
| <span data-ttu-id="2f535-136">9</span><span class="sxs-lookup"><span data-stu-id="2f535-136">9</span></span>     | <span data-ttu-id="2f535-137">40 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-137">40 degrees.</span></span>              |
| <span data-ttu-id="2f535-138">10</span><span class="sxs-lookup"><span data-stu-id="2f535-138">10</span></span>    | <span data-ttu-id="2f535-139">50 градусов.</span><span class="sxs-lookup"><span data-stu-id="2f535-139">50 degrees.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="2f535-140">Требования</span><span class="sxs-lookup"><span data-stu-id="2f535-140">Requirements</span></span>



| <span data-ttu-id="2f535-141">Требование</span><span class="sxs-lookup"><span data-stu-id="2f535-141">Requirement</span></span> | <span data-ttu-id="2f535-142">Значение</span><span class="sxs-lookup"><span data-stu-id="2f535-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f535-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f535-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2f535-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f535-144">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2f535-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f535-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2f535-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f535-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f535-147">Header</span><span class="sxs-lookup"><span data-stu-id="2f535-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f535-148"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f535-148"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f535-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f535-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f535-150">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f535-150">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="2f535-151">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="2f535-151">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
