---
title: Флаги создания списка изображений (Шлобж. h)
description: Набор битовых флагов, указывающих тип создаваемого списка изображений. Этот параметр может быть сочетанием следующих значений, но может включать только одно из \_ значений цвета ILC. Используется для \_ инициализации ImageList Create и IImageList2.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490209"
---
# <a name="image-list-creation-flags"></a><span data-ttu-id="1b017-105">Флаги создания списка изображений</span><span class="sxs-lookup"><span data-stu-id="1b017-105">Image List Creation Flags</span></span>

<span data-ttu-id="1b017-106">Набор битовых флагов, указывающих тип создаваемого списка изображений.</span><span class="sxs-lookup"><span data-stu-id="1b017-106">The set of bit flags that specifies the type of image list to create.</span></span> <span data-ttu-id="1b017-107">Этот параметр может быть сочетанием следующих значений, но может включать только одно из \_ значений цвета ILC.</span><span class="sxs-lookup"><span data-stu-id="1b017-107">This parameter can be a combination of the following values, but it can include only one of the ILC\_COLOR values.</span></span> <span data-ttu-id="1b017-108">Используется в [**ImageList \_ CREATE**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) и [**IImageList2:: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span><span class="sxs-lookup"><span data-stu-id="1b017-108">Used by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) and [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span></span>



| <span data-ttu-id="1b017-109">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="1b017-109">Constant/value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="1b017-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1b017-110">Description</span></span>                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <span data-ttu-id="1b017-111"><dt>**ILC \_ Маска**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-111"><dt>**ILC\_MASK**</dt> <dt>0x00000001</dt></span></span> </dl>                                     | <span data-ttu-id="1b017-112">Использовать маску.</span><span class="sxs-lookup"><span data-stu-id="1b017-112">Use a mask.</span></span> <span data-ttu-id="1b017-113">Список изображений содержит два точечных рисунка, один из которых является монохромным точечным рисунком, используемым в качестве маски.</span><span class="sxs-lookup"><span data-stu-id="1b017-113">The image list contains two bitmaps, one of which is a monochrome bitmap used as a mask.</span></span> <span data-ttu-id="1b017-114">Если это значение не включено, список изображений содержит только одно растровое изображение.</span><span class="sxs-lookup"><span data-stu-id="1b017-114">If this value is not included, the image list contains only one bitmap.</span></span><br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <span data-ttu-id="1b017-115"><dt>**ILC \_ ЦВЕТ**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-115"><dt>**ILC\_COLOR**</dt> <dt>0x00000000</dt></span></span> </dl>                                  | <span data-ttu-id="1b017-116">Используйте поведение по умолчанию, если не задан ни один из других \_ флагов ILC колоркс.</span><span class="sxs-lookup"><span data-stu-id="1b017-116">Use the default behavior if none of the other ILC\_COLORx flags is specified.</span></span> <span data-ttu-id="1b017-117">Как правило, значение по умолчанию — ILC \_ COLOR4, но для старых видеодрайверов значение по умолчанию — ILC \_ колорддб.</span><span class="sxs-lookup"><span data-stu-id="1b017-117">Typically, the default is ILC\_COLOR4, but for older display drivers, the default is ILC\_COLORDDB.</span></span><br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <span data-ttu-id="1b017-118"><dt>**ILC \_ КОЛОРДДБ**</dt> <dt>0x000000FE</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-118"><dt>**ILC\_COLORDDB**</dt> <dt>0x000000FE</dt></span></span> </dl>                         | <span data-ttu-id="1b017-119">Используйте зависимый от устройства точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="1b017-119">Use a device-dependent bitmap.</span></span><br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <span data-ttu-id="1b017-120"><dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-120"><dt>**ILC\_COLOR4**</dt> <dt>0x00000004</dt></span></span> </dl>                               | <span data-ttu-id="1b017-121">Используйте 4-разрядный (16-цветный) раздел DIB (BMP) в качестве точечного рисунка для списка изображений.</span><span class="sxs-lookup"><span data-stu-id="1b017-121">Use a 4-bit (16-color) device-independent bitmap (DIB) section as the bitmap for the image list.</span></span><br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <span data-ttu-id="1b017-122"><dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-122"><dt>**ILC\_COLOR8**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="1b017-123">Используйте 8-разрядный раздел DIB.</span><span class="sxs-lookup"><span data-stu-id="1b017-123">Use an 8-bit DIB section.</span></span> <span data-ttu-id="1b017-124">Цвета, используемые для таблицы цветов, имеют те же цвета, что и палитра полутонов.</span><span class="sxs-lookup"><span data-stu-id="1b017-124">The colors used for the color table are the same colors as the halftone palette.</span></span><br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <span data-ttu-id="1b017-125"><dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-125"><dt>**ILC\_COLOR16**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="1b017-126">Используйте 16-разрядный (32/64k-цветной) раздел DIB.</span><span class="sxs-lookup"><span data-stu-id="1b017-126">Use a 16-bit (32/64k-color) DIB section.</span></span><br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <span data-ttu-id="1b017-127"><dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-127"><dt>**ILC\_COLOR24**</dt> <dt>0x00000018</dt></span></span> </dl>                            | <span data-ttu-id="1b017-128">Используйте 24-разрядный раздел DIB.</span><span class="sxs-lookup"><span data-stu-id="1b017-128">Use a 24-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <span data-ttu-id="1b017-129"><dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-129"><dt>**ILC\_COLOR32**</dt> <dt>0x00000020</dt></span></span> </dl>                            | <span data-ttu-id="1b017-130">Используйте 32-разрядный раздел DIB.</span><span class="sxs-lookup"><span data-stu-id="1b017-130">Use a 32-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <span data-ttu-id="1b017-131"><dt>**ILC \_ ПАЛИТРа**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-131"><dt>**ILC\_PALETTE**</dt> <dt>0x00000800</dt></span></span> </dl>                            | <span data-ttu-id="1b017-132">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="1b017-132">Not implemented.</span></span><br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <span data-ttu-id="1b017-133"><dt>**ILC \_ ЗЕРКАЛЬный**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-133"><dt>**ILC\_MIRROR**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="1b017-134">Зеркальное отображение содержащихся значков, если процесс зеркально отражен</span><span class="sxs-lookup"><span data-stu-id="1b017-134">Mirror the icons contained, if the process is mirrored</span></span><br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <span data-ttu-id="1b017-135"><dt>**ILC \_ ПЕРИТЕММИРРОР**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-135"><dt>**ILC\_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span></span> </dl>          | <span data-ttu-id="1b017-136">Приводит к тому, что код зеркального отображения зеркально отражает каждый элемент при вставке набора изображений, а не на всю полосу.</span><span class="sxs-lookup"><span data-stu-id="1b017-136">Causes the mirroring code to mirror each item when inserting a set of images, versus the whole strip.</span></span><br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <span data-ttu-id="1b017-137"><dt>**ILC \_ ОРИГИНАЛСИЗЕ**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-137"><dt>**ILC\_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="1b017-138">**Windows Vista и более поздние версии.**</span><span class="sxs-lookup"><span data-stu-id="1b017-138">**Windows Vista and later.**</span></span> <span data-ttu-id="1b017-139">Список ImageList должен принимать меньшее значение, чем установленные изображения, и применять исходный размер на основе добавленного образа.</span><span class="sxs-lookup"><span data-stu-id="1b017-139">Imagelist should accept smaller than set images and apply original size based on image added.</span></span><br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <span data-ttu-id="1b017-140"><dt>**ILC \_ ХИГХКУАЛИТИСКАЛЕ**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-140"><dt>**ILC\_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="1b017-141">**Windows Vista и более поздние версии.**</span><span class="sxs-lookup"><span data-stu-id="1b017-141">**Windows Vista and later.**</span></span> <span data-ttu-id="1b017-142">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="1b017-142">Reserved.</span></span><br/>                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="1b017-143">Требования</span><span class="sxs-lookup"><span data-stu-id="1b017-143">Requirements</span></span>



| <span data-ttu-id="1b017-144">Требование</span><span class="sxs-lookup"><span data-stu-id="1b017-144">Requirement</span></span> | <span data-ttu-id="1b017-145">Значение</span><span class="sxs-lookup"><span data-stu-id="1b017-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b017-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b017-146">Minimum supported client</span></span><br/> | <span data-ttu-id="1b017-147">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b017-147">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1b017-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b017-148">Minimum supported server</span></span><br/> | <span data-ttu-id="1b017-149">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1b017-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1b017-150">Header</span><span class="sxs-lookup"><span data-stu-id="1b017-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b017-151"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b017-151"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





