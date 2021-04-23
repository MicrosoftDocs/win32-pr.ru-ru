---
description: Количество звуковых образцов, содержащихся в одном сжатом блоке звуковых данных. Этот атрибут может использоваться в сжатых звуковых форматах с фиксированным числом выборок в каждом блоке.
ms.assetid: 6ae31548-4d78-4e38-9cfc-01b611a6022d
title: Атрибут MF_MT_AUDIO_SAMPLES_PER_BLOCK (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c453fa4daeaa310b5e41add44b63b0fb45372d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712409"
---
# <a name="mf_mt_audio_samples_per_block-attribute"></a><span data-ttu-id="1a553-104">\_ \_ Звуковые образцы MF MT \_ \_ для каждого \_ атрибута блока</span><span class="sxs-lookup"><span data-stu-id="1a553-104">MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK attribute</span></span>

<span data-ttu-id="1a553-105">Количество звуковых образцов, содержащихся в одном сжатом блоке звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="1a553-105">Number of audio samples contained in one compressed block of audio data.</span></span> <span data-ttu-id="1a553-106">Этот атрибут может использоваться в сжатых звуковых форматах с фиксированным числом выборок в каждом блоке.</span><span class="sxs-lookup"><span data-stu-id="1a553-106">This attribute can be used in compressed audio formats that have a fixed number of samples within each block.</span></span>

## <a name="data-type"></a><span data-ttu-id="1a553-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1a553-107">Data type</span></span>

<span data-ttu-id="1a553-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1a553-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1a553-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a553-109">Remarks</span></span>

<span data-ttu-id="1a553-110">Этот атрибут соответствует элементу **всамплесперблокк** структуры [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1a553-110">This attribute corresponds to the **wSamplesPerBlock** member of the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="1a553-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="1a553-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a553-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1a553-112">Requirements</span></span>



| <span data-ttu-id="1a553-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1a553-113">Requirement</span></span> | <span data-ttu-id="1a553-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1a553-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a553-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a553-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1a553-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="1a553-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1a553-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a553-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1a553-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="1a553-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1a553-119">Header</span><span class="sxs-lookup"><span data-stu-id="1a553-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a553-120"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a553-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a553-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a553-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a553-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1a553-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1a553-123">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="1a553-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1a553-124">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="1a553-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1a553-125">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="1a553-125">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="1a553-126">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1a553-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
