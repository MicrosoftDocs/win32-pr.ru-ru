---
description: В поле Тип звукового носителя указывает назначение звуковых каналов для позиционирования динамиков.
ms.assetid: fa5f6baa-0a21-4162-8870-38e71763aba0
title: Атрибут MF_MT_AUDIO_CHANNEL_MASK (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5293f5387a2c293b97ee32db54fcfb3f3ff304d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080482"
---
# <a name="mf_mt_audio_channel_mask-attribute"></a><span data-ttu-id="ab04c-103">\_ \_ \_ Атрибут маски канала MF MT Audio \_</span><span class="sxs-lookup"><span data-stu-id="ab04c-103">MF\_MT\_AUDIO\_CHANNEL\_MASK attribute</span></span>

<span data-ttu-id="ab04c-104">В поле Тип звукового носителя указывает назначение звуковых каналов для позиционирования динамиков.</span><span class="sxs-lookup"><span data-stu-id="ab04c-104">In an audio media type, specifies the assignment of audio channels to speaker positions.</span></span>

## <a name="data-type"></a><span data-ttu-id="ab04c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ab04c-105">Data type</span></span>

<span data-ttu-id="ab04c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ab04c-106">**UINT32**</span></span>

<span data-ttu-id="ab04c-107">Значение этого атрибута является побитовым оператором **или** для следующих флагов, которые определены в файле заголовка ммрег. h.</span><span class="sxs-lookup"><span data-stu-id="ab04c-107">The value of this attribute is a bitwise **OR** of the following flags, which are defined in the header file mmreg.h.</span></span>

<dl> <dt>

<span data-ttu-id="ab04c-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**Докладчик \_ ПЕРЕДНИй \_ левый** (0x1)</span><span class="sxs-lookup"><span data-stu-id="ab04c-108"><span id="SPEAKER_FRONT_LEFT"></span><span id="speaker_front_left"></span>**SPEAKER\_FRONT\_LEFT** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**Докладчик \_ ПЕРЕДНИй \_ правый** (0x2)</span><span class="sxs-lookup"><span data-stu-id="ab04c-109"><span id="SPEAKER_FRONT_RIGHT"></span><span id="speaker_front_right"></span>**SPEAKER\_FRONT\_RIGHT** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**Докладчик \_ ПЕРЕДНИй \_ Центральный центр** (0x4)</span><span class="sxs-lookup"><span data-stu-id="ab04c-110"><span id="SPEAKER_FRONT_CENTER"></span><span id="speaker_front_center"></span>**SPEAKER\_FRONT\_CENTER** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**Докладчик \_ НИЗКАЯ \_ Частота** (0x8)</span><span class="sxs-lookup"><span data-stu-id="ab04c-111"><span id="SPEAKER_LOW_FREQUENCY"></span><span id="speaker_low_frequency"></span>**SPEAKER\_LOW\_FREQUENCY** (0x8)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**Докладчик \_ НАЗАД \_ влево** (0x10)</span><span class="sxs-lookup"><span data-stu-id="ab04c-112"><span id="SPEAKER_BACK_LEFT"></span><span id="speaker_back_left"></span>**SPEAKER\_BACK\_LEFT** (0x10)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**Докладчик \_ ЗАДНий \_ правый** (0x20)</span><span class="sxs-lookup"><span data-stu-id="ab04c-113"><span id="SPEAKER_BACK_RIGHT"></span><span id="speaker_back_right"></span>**SPEAKER\_BACK\_RIGHT** (0x20)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**Докладчик \_ ПЕРЕДНИй \_ левый \_ от \_ центра Center** (0x40)</span><span class="sxs-lookup"><span data-stu-id="ab04c-114"><span id="SPEAKER_FRONT_LEFT_OF_CENTER"></span><span id="speaker_front_left_of_center"></span>**SPEAKER\_FRONT\_LEFT\_OF\_CENTER** (0x40)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**Докладчик \_ ПЕРЕДНИй \_ правый \_ \_ центра** (0x80)</span><span class="sxs-lookup"><span data-stu-id="ab04c-115"><span id="SPEAKER_FRONT_RIGHT_OF_CENTER"></span><span id="speaker_front_right_of_center"></span>**SPEAKER\_FRONT\_RIGHT\_OF\_CENTER** (0x80)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**Докладчик \_ ЗАДНЯЯ \_ центр** (0x100)</span><span class="sxs-lookup"><span data-stu-id="ab04c-116"><span id="SPEAKER_BACK_CENTER"></span><span id="speaker_back_center"></span>**SPEAKER\_BACK\_CENTER** (0x100)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**Докладчик \_ БОКОВая \_ слева** (0x200)</span><span class="sxs-lookup"><span data-stu-id="ab04c-117"><span id="SPEAKER_SIDE_LEFT"></span><span id="speaker_side_left"></span>**SPEAKER\_SIDE\_LEFT** (0x200)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**Докладчик \_ \_Справа** (0x400)</span><span class="sxs-lookup"><span data-stu-id="ab04c-118"><span id="SPEAKER_SIDE_RIGHT"></span><span id="speaker_side_right"></span>**SPEAKER\_SIDE\_RIGHT** (0x400)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**Докладчик \_ \_Центр вверху** (0x800)</span><span class="sxs-lookup"><span data-stu-id="ab04c-119"><span id="SPEAKER_TOP_CENTER"></span><span id="speaker_top_center"></span>**SPEAKER\_TOP\_CENTER** (0x800)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**Докладчик \_ СВЕРХУ \_ спереди \_ слева** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="ab04c-120"><span id="SPEAKER_TOP_FRONT_LEFT"></span><span id="speaker_top_front_left"></span>**SPEAKER\_TOP\_FRONT\_LEFT** (0x1000)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**Докладчик \_ ВЕРХНИЙ \_ передний \_ Центральный центр** (0x2000)</span><span class="sxs-lookup"><span data-stu-id="ab04c-121"><span id="SPEAKER_TOP_FRONT_CENTER"></span><span id="speaker_top_front_center"></span>**SPEAKER\_TOP\_FRONT\_CENTER** (0x2000)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**Докладчик \_ ВЕРХНИЙ \_ передний \_ правый** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="ab04c-122"><span id="SPEAKER_TOP_FRONT_RIGHT"></span><span id="speaker_top_front_right"></span>**SPEAKER\_TOP\_FRONT\_RIGHT** (0x4000)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**Докладчик \_ Верхний \_ задний \_ левый край** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="ab04c-123"><span id="SPEAKER_TOP_BACK_LEFT"></span><span id="speaker_top_back_left"></span>**SPEAKER\_TOP\_BACK\_LEFT** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**Докладчик \_ ВЕРХНИЙ \_ задний \_ центр** (0x10000)</span><span class="sxs-lookup"><span data-stu-id="ab04c-124"><span id="SPEAKER_TOP_BACK_CENTER"></span><span id="speaker_top_back_center"></span>**SPEAKER\_TOP\_BACK\_CENTER** (0x10000)</span></span>
</dt> <dt>

<span data-ttu-id="ab04c-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**Докладчик \_ ВЕРХНИЙ \_ задний \_ правый** (0x20000)</span><span class="sxs-lookup"><span data-stu-id="ab04c-125"><span id="SPEAKER_TOP_BACK_RIGHT"></span><span id="speaker_top_back_right"></span>**SPEAKER\_TOP\_BACK\_RIGHT** (0x20000)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ab04c-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab04c-126">Remarks</span></span>

<span data-ttu-id="ab04c-127">Этот атрибут соответствует элементу **двчаннелмаск** структуры [**вавеформатекстенсибле**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="ab04c-127">This attribute corresponds to the **dwChannelMask** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="ab04c-128">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ab04c-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab04c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="ab04c-129">Requirements</span></span>



| <span data-ttu-id="ab04c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="ab04c-130">Requirement</span></span> | <span data-ttu-id="ab04c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="ab04c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab04c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab04c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ab04c-133">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="ab04c-133">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ab04c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab04c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ab04c-135">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ab04c-135">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ab04c-136">Header</span><span class="sxs-lookup"><span data-stu-id="ab04c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab04c-137"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab04c-137"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab04c-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab04c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab04c-139">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab04c-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ab04c-140">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="ab04c-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ab04c-141">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ab04c-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ab04c-142">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="ab04c-142">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="ab04c-143">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ab04c-143">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
