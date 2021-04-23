---
title: Изменение указателя в устройстве
description: Значения, которые могут быть переданы в параметре wParam сообщения WM_POINTERDEVICECHANGE.
ms.assetid: B95191D7-820B-445A-A3A4-811F9F1A8C4F
topic_type:
- apiref
api_name:
- PDC_ARRIVAL
- PDC_REMOVAL
- PDC_ORIENTATION_0
- PDC_ORIENTATION_90
- PDC_ORIENTATION_180
- PDC_ORIENTATION_270
- PDC_MODE_DEFAULT
- PDC_MODE_CENTERED
- PDC_MAPPING_CHANGE
- PDC_RESOLUTION
- PDC_ORIGIN
- PDC_MODE_ASPECTRATIOPRESERVED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5e4b85c17adcd2db7c0f2f672e27ca467b346b0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989025"
---
# <a name="pointer-device-change"></a><span data-ttu-id="3dae4-103">Изменение указателя в устройстве</span><span class="sxs-lookup"><span data-stu-id="3dae4-103">Pointer Device Change</span></span>

<span data-ttu-id="3dae4-104">Значения, которые могут быть переданы в параметре *wParam* сообщения [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="3dae4-104">Values that can be passed in the *wParam* parameter of the [**WM_POINTERDEVICECHANGE**](wm-pointerdevicechange.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="3dae4-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="3dae4-105"><span id="PDC_ARRIVAL"></span><span id="pdc_arrival"></span>**PDC_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-106">0x001</span><span class="sxs-lookup"><span data-stu-id="3dae4-106">0x001</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-107">Подключено новое устройство.</span><span class="sxs-lookup"><span data-stu-id="3dae4-107">A new device is attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span><span class="sxs-lookup"><span data-stu-id="3dae4-108"><span id="PDC_REMOVAL"></span><span id="pdc_removal"></span>**PDC_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-109">0x002</span><span class="sxs-lookup"><span data-stu-id="3dae4-109">0x002</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-110">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="3dae4-110">A device has been detached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span><span class="sxs-lookup"><span data-stu-id="3dae4-111"><span id="PDC_ORIENTATION_0"></span><span id="pdc_orientation_0"></span>**PDC_ORIENTATION_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-112">0x004</span><span class="sxs-lookup"><span data-stu-id="3dae4-112">0x004</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-113">Ориентация устройства.</span><span class="sxs-lookup"><span data-stu-id="3dae4-113">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span><span class="sxs-lookup"><span data-stu-id="3dae4-114"><span id="PDC_ORIENTATION_90"></span><span id="pdc_orientation_90"></span>**PDC_ORIENTATION_90**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-115">0x008</span><span class="sxs-lookup"><span data-stu-id="3dae4-115">0x008</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-116">Ориентация устройства.</span><span class="sxs-lookup"><span data-stu-id="3dae4-116">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span><span class="sxs-lookup"><span data-stu-id="3dae4-117"><span id="PDC_ORIENTATION_180"></span><span id="pdc_orientation_180"></span>**PDC_ORIENTATION_180**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-118">0x010</span><span class="sxs-lookup"><span data-stu-id="3dae4-118">0x010</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-119">Ориентация устройства.</span><span class="sxs-lookup"><span data-stu-id="3dae4-119">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span><span class="sxs-lookup"><span data-stu-id="3dae4-120"><span id="PDC_ORIENTATION_270"></span><span id="pdc_orientation_270"></span>**PDC_ORIENTATION_270**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-121">0x020</span><span class="sxs-lookup"><span data-stu-id="3dae4-121">0x020</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-122">Ориентация устройства.</span><span class="sxs-lookup"><span data-stu-id="3dae4-122">Orientation of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="3dae4-123"><span id="PDC_MODE_DEFAULT"></span><span id="pdc_mode_default"></span>**PDC_MODE_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-124">0x040</span><span class="sxs-lookup"><span data-stu-id="3dae4-124">0x040</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-125">Режим просмотра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3dae4-125">The default display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span><span class="sxs-lookup"><span data-stu-id="3dae4-126"><span id="PDC_MODE_CENTERED"></span><span id="pdc_mode_centered"></span>**PDC_MODE_CENTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-127">0x080</span><span class="sxs-lookup"><span data-stu-id="3dae4-127">0x080</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-128">Режим экрана по центру.</span><span class="sxs-lookup"><span data-stu-id="3dae4-128">Centered display mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="3dae4-129"><span id="PDC_MAPPING_CHANGE"></span><span id="pdc_mapping_change"></span>**PDC_MAPPING_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-130">0x100</span><span class="sxs-lookup"><span data-stu-id="3dae4-130">0x100</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-131">Изменение отображения в сопоставлении с дигитайзером.</span><span class="sxs-lookup"><span data-stu-id="3dae4-131">The change in display to digitizer mapping.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span><span class="sxs-lookup"><span data-stu-id="3dae4-132"><span id="PDC_RESOLUTION"></span><span id="pdc_resolution"></span>**PDC_RESOLUTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-133">0x200</span><span class="sxs-lookup"><span data-stu-id="3dae4-133">0x200</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-134">Разрешение экрана.</span><span class="sxs-lookup"><span data-stu-id="3dae4-134">Display resolution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span><span class="sxs-lookup"><span data-stu-id="3dae4-135"><span id="PDC_ORIGIN"></span><span id="pdc_origin"></span>**PDC_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-136">0x400</span><span class="sxs-lookup"><span data-stu-id="3dae4-136">0x400</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-137">Источник вывода.</span><span class="sxs-lookup"><span data-stu-id="3dae4-137">The display origin.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3dae4-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="3dae4-138"><span id="PDC_MODE_ASPECTRATIOPRESERVED"></span><span id="pdc_mode_aspectratiopreserved"></span>**PDC_MODE_ASPECTRATIOPRESERVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dae4-139">0x800</span><span class="sxs-lookup"><span data-stu-id="3dae4-139">0x800</span></span>
</dt> <dt>



<span data-ttu-id="3dae4-140">Пропорции дисплея.</span><span class="sxs-lookup"><span data-stu-id="3dae4-140">The display aspect ratio.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3dae4-141">Требования</span><span class="sxs-lookup"><span data-stu-id="3dae4-141">Requirements</span></span>



| <span data-ttu-id="3dae4-142">Требование</span><span class="sxs-lookup"><span data-stu-id="3dae4-142">Requirement</span></span> | <span data-ttu-id="3dae4-143">Значение</span><span class="sxs-lookup"><span data-stu-id="3dae4-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3dae4-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dae4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3dae4-145">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3dae4-145">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3dae4-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dae4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3dae4-147">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3dae4-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3dae4-148">Header</span><span class="sxs-lookup"><span data-stu-id="3dae4-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dae4-149"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dae4-149"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dae4-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dae4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dae4-151">Константы</span><span class="sxs-lookup"><span data-stu-id="3dae4-151">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="3dae4-152">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="3dae4-152">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





