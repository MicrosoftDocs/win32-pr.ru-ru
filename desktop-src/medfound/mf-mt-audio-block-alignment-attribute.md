---
description: Выравнивание блокировки (в байтах) для типа звукового носителя. Выравнивание блока — это минимальная атомарная единица данных для звукового формата.
ms.assetid: 7d304826-ad81-4243-a675-2f55b668b348
title: Атрибут MF_MT_AUDIO_BLOCK_ALIGNMENT (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21efb14cbb89d1773fe9bc3b5ade8d0a50555a1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702495"
---
# <a name="mf_mt_audio_block_alignment-attribute"></a><span data-ttu-id="f6755-104">\_ \_ \_ Атрибут выравнивания звукового блока MF MT \_</span><span class="sxs-lookup"><span data-stu-id="f6755-104">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT attribute</span></span>

<span data-ttu-id="f6755-105">Выравнивание блокировки (в байтах) для типа звукового носителя.</span><span class="sxs-lookup"><span data-stu-id="f6755-105">Block alignment, in bytes, for an audio media type.</span></span> <span data-ttu-id="f6755-106">Выравнивание блока — это минимальная атомарная единица данных для звукового формата.</span><span class="sxs-lookup"><span data-stu-id="f6755-106">The block alignment is the minimum atomic unit of data for the audio format.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6755-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f6755-107">Data type</span></span>

<span data-ttu-id="f6755-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6755-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f6755-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6755-109">Remarks</span></span>

<span data-ttu-id="f6755-110">Для звуковых форматов PCM выравнивание блока равно числу звуковых каналов, умноженному на число байтов на каждый образец звука.</span><span class="sxs-lookup"><span data-stu-id="f6755-110">For PCM audio formats, the block alignment is equal to the number of audio channels multiplied by the number of bytes per audio sample.</span></span>

<span data-ttu-id="f6755-111">Этот атрибут соответствует элементу **нблоккалигн** структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f6755-111">This attribute corresponds to the **nBlockAlign** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="f6755-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="f6755-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6755-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f6755-113">Requirements</span></span>



| <span data-ttu-id="f6755-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f6755-114">Requirement</span></span> | <span data-ttu-id="f6755-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f6755-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6755-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6755-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f6755-117">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f6755-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f6755-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6755-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f6755-119">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f6755-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f6755-120">Header</span><span class="sxs-lookup"><span data-stu-id="f6755-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6755-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6755-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6755-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6755-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6755-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6755-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6755-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6755-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f6755-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f6755-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f6755-126">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="f6755-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f6755-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f6755-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
