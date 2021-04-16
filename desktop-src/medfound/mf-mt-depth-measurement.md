---
description: Значение, определяющее систему измерения для значения глубины в видеокадре.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: Атрибут MF_MT_DEPTH_MEASUREMENT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567218"
---
# <a name="mf_mt_depth_measurement-attribute"></a><span data-ttu-id="55a42-103">\_ \_ \_ Атрибут измерения глубины MT</span><span class="sxs-lookup"><span data-stu-id="55a42-103">MF\_MT\_DEPTH\_MEASUREMENT attribute</span></span>

<span data-ttu-id="55a42-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="55a42-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="55a42-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="55a42-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="55a42-106">Значение, определяющее систему измерения для значения глубины в видеокадре.</span><span class="sxs-lookup"><span data-stu-id="55a42-106">A value that defines the measurement system for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="55a42-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="55a42-107">Data type</span></span>

<span data-ttu-id="55a42-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="55a42-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="55a42-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55a42-109">Remarks</span></span>

<span data-ttu-id="55a42-110">Это значение является членом перечисления [**\_ мфдепсмеасуремент**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)</span><span class="sxs-lookup"><span data-stu-id="55a42-110">This value is a member of the [**\_MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement) enumeration</span></span>

<span data-ttu-id="55a42-111">Если этот атрибут отсутствует, предполагается, что он является **дистанцетофокалплане**.</span><span class="sxs-lookup"><span data-stu-id="55a42-111">If this attribute is not present it is assumed to be **DistanceToFocalPlane**.</span></span> <span data-ttu-id="55a42-112">Расстояние до фокальной плоскости обычно проще использовать в трехмерной евклидовой системе координат.</span><span class="sxs-lookup"><span data-stu-id="55a42-112">The distance to focal plane is typically easier to consume in a 3D Euclidian coordinate system.</span></span>

![Иллюстрация дистанцетофокалплане](images/distance-to-focal-plane.png)

<span data-ttu-id="55a42-114">Расстояние до центра фокуса — это обычно необработанные данные от датчика, например время видеокамер.</span><span class="sxs-lookup"><span data-stu-id="55a42-114">The distance to focal center format is typically raw data from sensor such as time of flight cameras.</span></span>

![Иллюстрация дистанцетуптикалцентер](images/distance-to-optical-center.png)

<span data-ttu-id="55a42-116">Камеры глубины не могут понять глубину всех пикселов.</span><span class="sxs-lookup"><span data-stu-id="55a42-116">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="55a42-117">Если достоверность пикселя мала, из-за материала, перекрытия или вне диапазона и т. д. значение глубины на этом пикселе может быть недопустимым.</span><span class="sxs-lookup"><span data-stu-id="55a42-117">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="55a42-118">Если значение в пикселях глубины равно 0, пиксель является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="55a42-118">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="55a42-119">Некоторые камеры с глубиной присоединяют метаданные битовой маски для каждого пикселя в дополнение к значению глубины, представляющему причину недопустимой глубины пикселя из-за материала, перекрытия или вне диапазона и т. д. Мы рекомендуем не присоединять такие метаданные как биты в значении глубины, так как они обычно приводят к сложности при использовании таких значений в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="55a42-119">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="55a42-120">Используйте.</span><span class="sxs-lookup"><span data-stu-id="55a42-120">Instead.</span></span> <span data-ttu-id="55a42-121">рекомендуется использовать отдельный буфер образа 8 бит с тем же разрешением и присоединить его как атрибут [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="55a42-121">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="55a42-122">Такие метаданные зависят от поставщика камеры и не стандартизированы платформой.</span><span class="sxs-lookup"><span data-stu-id="55a42-122">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="55a42-123">Мы рекомендуем использовать полные 16 бит для значения глубины, чтобы упростить обработку и использовать фиксированное значение, например 0 для недействительности.</span><span class="sxs-lookup"><span data-stu-id="55a42-123">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a42-124">Требования</span><span class="sxs-lookup"><span data-stu-id="55a42-124">Requirements</span></span>



| <span data-ttu-id="55a42-125">Требование</span><span class="sxs-lookup"><span data-stu-id="55a42-125">Requirement</span></span> | <span data-ttu-id="55a42-126">Значение</span><span class="sxs-lookup"><span data-stu-id="55a42-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55a42-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55a42-127">Minimum supported client</span></span><br/> | <span data-ttu-id="55a42-128">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="55a42-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="55a42-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55a42-129">Minimum supported server</span></span><br/> | <span data-ttu-id="55a42-130">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="55a42-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="55a42-131">Header</span><span class="sxs-lookup"><span data-stu-id="55a42-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="55a42-132"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="55a42-132"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




