---
description: Значение, определяющее единицы для значения глубины в видеокадре.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: Атрибут MF_MT_DEPTH_VALUE_UNIT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711555"
---
# <a name="mf_mt_depth_value_unit-attribute"></a><span data-ttu-id="86305-103">\_ \_ \_ Атрибут единицы значения глубины MF Book \_</span><span class="sxs-lookup"><span data-stu-id="86305-103">MF\_MT\_DEPTH\_VALUE\_UNIT attribute</span></span>

<span data-ttu-id="86305-104">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="86305-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="86305-105">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="86305-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="86305-106">Значение, определяющее единицы для значения глубины в видеокадре.</span><span class="sxs-lookup"><span data-stu-id="86305-106">A value that defines the units for a depth value in a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="86305-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="86305-107">Data type</span></span>

<span data-ttu-id="86305-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="86305-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="86305-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="86305-109">Remarks</span></span>

<span data-ttu-id="86305-110">Значение единицы измерения представляет собой значение UINT64 в метрах в диапазоне от 1E до 9 метров.</span><span class="sxs-lookup"><span data-stu-id="86305-110">The unit value is a UINT64 value in nanometers, in the range 1e - 9 meters.</span></span> <span data-ttu-id="86305-111">Если это значение отсутствует, значением по умолчанию для единицы является 1E-3, что означает, что каждый уровень пикселя измеряется в физическом пространстве в 1 миллиметр.</span><span class="sxs-lookup"><span data-stu-id="86305-111">If this value is not present, the default value of the unit is 1e-3, which indicates each pixel level is measured in 1 millimeter in physical space.</span></span>

<span data-ttu-id="86305-112">Камеры глубины не могут понять глубину всех пикселов.</span><span class="sxs-lookup"><span data-stu-id="86305-112">Depth cameras cannot sense the depth of all pixels.</span></span> <span data-ttu-id="86305-113">Если достоверность пикселя мала, из-за материала, перекрытия или вне диапазона и т. д. значение глубины на этом пикселе может быть недопустимым.</span><span class="sxs-lookup"><span data-stu-id="86305-113">When the confidence of a pixel is low, because of material, occlusion, or out of range etc, the depth value on that pixel can be invalid.</span></span>

<span data-ttu-id="86305-114">Если значение в пикселях глубины равно 0, пиксель является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="86305-114">When a depth pixel value is 0, the pixel is invalid.</span></span>

<span data-ttu-id="86305-115">Некоторые камеры с глубиной присоединяют метаданные битовой маски для каждого пикселя в дополнение к значению глубины, представляющему причину недопустимой глубины пикселя из-за материала, перекрытия или вне диапазона и т. д. Мы рекомендуем не присоединять такие метаданные как биты в значении глубины, так как они обычно приводят к сложности при использовании таких значений в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="86305-115">Some depth cameras attach bitmask metadata for each pixel in addition to the depth value to represent the reason why the depth of pixel is invalid, due to material, occlusion or out of range etc. We recommend that you avoid attaching such metadata as bits in depth value, because it will typically lead to difficulty when using such values in pixel shader.</span></span> <span data-ttu-id="86305-116">Используйте.</span><span class="sxs-lookup"><span data-stu-id="86305-116">Instead.</span></span> <span data-ttu-id="86305-117">рекомендуется использовать отдельный буфер образа 8 бит с тем же разрешением и присоединить его как атрибут [**имфсампле**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span><span class="sxs-lookup"><span data-stu-id="86305-117">we recommend that you use a separate 8bit image buffer with same resolution and attach it as attribute of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).</span></span> <span data-ttu-id="86305-118">Такие метаданные зависят от поставщика камеры и не стандартизированы платформой.</span><span class="sxs-lookup"><span data-stu-id="86305-118">Such metadata varies for each camera vendor and is not standardized by the platform.</span></span> <span data-ttu-id="86305-119">Мы рекомендуем использовать полные 16 бит для значения глубины, чтобы упростить обработку и использовать фиксированное значение, например 0 для недействительности.</span><span class="sxs-lookup"><span data-stu-id="86305-119">We recommend using full 16 bits for the depth value for easier processing downstream and using a fixed value such as 0 for invalidation.</span></span>

## <a name="requirements"></a><span data-ttu-id="86305-120">Требования</span><span class="sxs-lookup"><span data-stu-id="86305-120">Requirements</span></span>



| <span data-ttu-id="86305-121">Требование</span><span class="sxs-lookup"><span data-stu-id="86305-121">Requirement</span></span> | <span data-ttu-id="86305-122">Значение</span><span class="sxs-lookup"><span data-stu-id="86305-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86305-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86305-123">Minimum supported client</span></span><br/> | <span data-ttu-id="86305-124">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="86305-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="86305-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86305-125">Minimum supported server</span></span><br/> | <span data-ttu-id="86305-126">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="86305-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="86305-127">Header</span><span class="sxs-lookup"><span data-stu-id="86305-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="86305-128"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="86305-128"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




