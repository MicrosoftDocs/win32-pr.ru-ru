---
description: Указывает диапазон, используемый при поиске движения.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: Свойство MFPKEY_MOTIONSEARCHRANGE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263988"
---
# <a name="mfpkey_motionsearchrange-property"></a><span data-ttu-id="3559d-103">МФПКЭЙ \_ мотионсеарчранже, свойство</span><span class="sxs-lookup"><span data-stu-id="3559d-103">MFPKEY\_MOTIONSEARCHRANGE Property</span></span>

<span data-ttu-id="3559d-104">Указывает диапазон, используемый при поиске движения.</span><span class="sxs-lookup"><span data-stu-id="3559d-104">Specifies the range used in motion searches.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3559d-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="3559d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3559d-106">g \_ всзвмвкмотионсеарчранже</span><span class="sxs-lookup"><span data-stu-id="3559d-106">g\_wszWMVCMotionSearchRange</span></span>

## <a name="data-type"></a><span data-ttu-id="3559d-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3559d-107">Data Type</span></span>

<span data-ttu-id="3559d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3559d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="3559d-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3559d-109">Default Value</span></span>

<span data-ttu-id="3559d-110">0</span><span class="sxs-lookup"><span data-stu-id="3559d-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="3559d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3559d-111">Remarks</span></span>

<span data-ttu-id="3559d-112">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3559d-112">This property may be set to one of the following values.</span></span> <span data-ttu-id="3559d-113">H обозначает горизонтальный диапазон, а V означает вертикальный диапазон.</span><span class="sxs-lookup"><span data-stu-id="3559d-113">H denotes horizontal range and V denotes vertical range.</span></span> <span data-ttu-id="3559d-114">Все диапазоны задаются в пикселях.</span><span class="sxs-lookup"><span data-stu-id="3559d-114">All ranges are given in pixels.</span></span>



| <span data-ttu-id="3559d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3559d-115">Value</span></span> | <span data-ttu-id="3559d-116">Диапазон</span><span class="sxs-lookup"><span data-stu-id="3559d-116">Range</span></span>                                |
|-------|--------------------------------------|
| <span data-ttu-id="3559d-117">0</span><span class="sxs-lookup"><span data-stu-id="3559d-117">0</span></span>     | <span data-ttu-id="3559d-118">+ 63.75/-64.0» H, + 31.75/-32.0 V</span><span class="sxs-lookup"><span data-stu-id="3559d-118">+63.75/-64.0 H, +31.75/-32.0 V</span></span>       |
| <span data-ttu-id="3559d-119">1</span><span class="sxs-lookup"><span data-stu-id="3559d-119">1</span></span>     | <span data-ttu-id="3559d-120">+127.75/-128.0 H, +63.75/-64.0 V</span><span class="sxs-lookup"><span data-stu-id="3559d-120">+127.75/-128.0 H, +63.75/-64.0 V</span></span>     |
| <span data-ttu-id="3559d-121">2</span><span class="sxs-lookup"><span data-stu-id="3559d-121">2</span></span>     | <span data-ttu-id="3559d-122">+ 511.75/-512.0 H, + 127.75/-128.0 V</span><span class="sxs-lookup"><span data-stu-id="3559d-122">+511.75/-512.0 H, +127.75/-128.0 V</span></span>   |
| <span data-ttu-id="3559d-123">3</span><span class="sxs-lookup"><span data-stu-id="3559d-123">3</span></span>     | <span data-ttu-id="3559d-124">+ 1023.75/-1024.0 H, + 255.75/-256.0 V</span><span class="sxs-lookup"><span data-stu-id="3559d-124">+1023.75/-1024.0 H, +255.75/-256.0 V</span></span> |
| <span data-ttu-id="3559d-125">-1</span><span class="sxs-lookup"><span data-stu-id="3559d-125">-1</span></span>    | <span data-ttu-id="3559d-126">Макроблокк — адаптивный (автоматический)</span><span class="sxs-lookup"><span data-stu-id="3559d-126">Macroblock-adaptive (automatic)</span></span>      |



 

<span data-ttu-id="3559d-127">Это свойство управляет размером области кадров, которую кодек будет искать элемент, который может иметь продвижение между кадрами.</span><span class="sxs-lookup"><span data-stu-id="3559d-127">This property controls the size of the frame area that the codec will search for an element that may have exhibited motion between frames.</span></span> <span data-ttu-id="3559d-128">Более крупное окно поиска поможет быстро найти более быстрое движение, но потребует больше времени ЦП.</span><span class="sxs-lookup"><span data-stu-id="3559d-128">A larger search window will help find faster motion but will require more CPU time.</span></span> <span data-ttu-id="3559d-129">Требования к ЦП задаются примерно вдвое на каждом уровне.</span><span class="sxs-lookup"><span data-stu-id="3559d-129">The CPU requirements are approximately doubled at each level.</span></span>

<span data-ttu-id="3559d-130">В автоматическом режиме (-1) будет динамически выбран наиболее эффективный режим.</span><span class="sxs-lookup"><span data-stu-id="3559d-130">The automatic mode (-1) will dynamically select the most efficient mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="3559d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="3559d-131">Requirements</span></span>



| <span data-ttu-id="3559d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="3559d-132">Requirement</span></span> | <span data-ttu-id="3559d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3559d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3559d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3559d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3559d-135">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3559d-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3559d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3559d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3559d-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3559d-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3559d-138">Header</span><span class="sxs-lookup"><span data-stu-id="3559d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3559d-139"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3559d-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3559d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3559d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3559d-141">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3559d-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




