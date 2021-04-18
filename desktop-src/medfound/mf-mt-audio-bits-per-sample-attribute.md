---
description: Число битов на аудио в типе звукового носителя.
ms.assetid: d78a8c4d-377e-45eb-9cf6-2d61b34e82d6
title: Атрибут MF_MT_AUDIO_BITS_PER_SAMPLE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 896e77c937269b63208cb4bff73482a8df8596aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692660"
---
# <a name="mf_mt_audio_bits_per_sample-attribute"></a><span data-ttu-id="81ce0-103">\_ \_ Звуковой бит MF \_ MT \_ на \_ образец атрибута</span><span class="sxs-lookup"><span data-stu-id="81ce0-103">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="81ce0-104">Число битов на аудио в типе звукового носителя.</span><span class="sxs-lookup"><span data-stu-id="81ce0-104">Number of bits per audio sample in an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="81ce0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="81ce0-105">Data type</span></span>

<span data-ttu-id="81ce0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="81ce0-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="81ce0-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81ce0-107">Remarks</span></span>

<span data-ttu-id="81ce0-108">Этот атрибут соответствует элементу **вбитсперсампле** структуры [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="81ce0-108">This attribute corresponds to the **wBitsPerSample** member of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

<span data-ttu-id="81ce0-109">Если в некоторых битах содержится заполнение, задайте для атрибута номер версии [**MF \_ MT \_ Audio \_ Valid \_ \_ \_**](mf-mt-audio-valid-bits-per-sample-attribute.md) для каждого образца, чтобы указать число битов допустимых звуковых данных в каждом примере.</span><span class="sxs-lookup"><span data-stu-id="81ce0-109">If some bits contain padding, set the [**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md) attribute to specify the number of bits of valid audio data in each sample.</span></span>

<span data-ttu-id="81ce0-110">Если в аудио содержится 8 бит на пример, то звуковые примеры являются неподписанными значениями.</span><span class="sxs-lookup"><span data-stu-id="81ce0-110">If the audio contains 8 bits per sample, the audio samples are unsigned values.</span></span> <span data-ttu-id="81ce0-111">(Каждый звуковой образец имеет диапазон от 0 до 255.) Если звук содержит 16 бит на выборку или выше, то звуковые примеры являются значениями со знаком.</span><span class="sxs-lookup"><span data-stu-id="81ce0-111">(Each audio sample has the range 0–255.) If the audio contains 16 bits per sample or higher, the audio samples are signed values.</span></span>

<span data-ttu-id="81ce0-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="81ce0-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ce0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="81ce0-113">Requirements</span></span>



| <span data-ttu-id="81ce0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="81ce0-114">Requirement</span></span> | <span data-ttu-id="81ce0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="81ce0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81ce0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81ce0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="81ce0-117">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="81ce0-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="81ce0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81ce0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="81ce0-119">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="81ce0-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="81ce0-120">Header</span><span class="sxs-lookup"><span data-stu-id="81ce0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="81ce0-121"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="81ce0-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81ce0-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81ce0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ce0-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81ce0-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="81ce0-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="81ce0-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="81ce0-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="81ce0-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="81ce0-126">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="81ce0-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="81ce0-127">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="81ce0-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
