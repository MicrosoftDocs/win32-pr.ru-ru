---
description: Количество допустимых битов звуковых данных в каждом звуковом примере.
ms.assetid: b5b97700-c98a-4394-a184-661852add0b4
title: Атрибут MF_MT_AUDIO_VALID_BITS_PER_SAMPLE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4e5efb41bf3b79d4feded2872b601eea43723a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349922"
---
# <a name="mf_mt_audio_valid_bits_per_sample-attribute"></a><span data-ttu-id="6acd7-103">\_ \_ \_ Допустимый бит MF \_ \_ на \_ примере атрибута</span><span class="sxs-lookup"><span data-stu-id="6acd7-103">MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="6acd7-104">Количество допустимых битов звуковых данных в каждом звуковом примере.</span><span class="sxs-lookup"><span data-stu-id="6acd7-104">Number of valid bits of audio data in each audio sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="6acd7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6acd7-105">Data type</span></span>

<span data-ttu-id="6acd7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6acd7-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6acd7-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6acd7-107">Remarks</span></span>

<span data-ttu-id="6acd7-108">Для звуковых форматов, содержащих заполнение после каждого аудио-образца, используется звуковая подложка **MF \_ MT. \_ \_ Допустимые \_ биты \_ на \_ Пример** атрибута.</span><span class="sxs-lookup"><span data-stu-id="6acd7-108">The **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is used for audio formats that contain padding after each audio sample.</span></span> <span data-ttu-id="6acd7-109">Общий размер каждого образца звука, включая биты заполнения, задается в атрибуте [**MF \_ \_ Audio \_ бит \_ \_**](mf-mt-audio-bits-per-sample-attribute.md) в указанном примере.</span><span class="sxs-lookup"><span data-stu-id="6acd7-109">The total size of each audio sample, including padding bits, is given in the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="6acd7-110">Если для образца атрибута не задано **допустимое количество аудио-файлов MF \_ MT на \_ \_ \_ \_ \_ выборку** , то для определения числа допустимых битов на выборку используйте номер [**MF \_ MT Audio- \_ \_ бит \_ на \_ Пример**](mf-mt-audio-bits-per-sample-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6acd7-110">If the **MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE** attribute is not set, use the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute to find the number of valid bits per sample.</span></span>

<span data-ttu-id="6acd7-111">Если формат аудио не содержит никаких битов заполнения, то этот атрибут не должен быть установлен или должен иметь то же значение, что и [**\_ \_ звуковый бит MF MT \_ \_ на каждый \_ Пример**](mf-mt-audio-bits-per-sample-attribute.md) атрибута.</span><span class="sxs-lookup"><span data-stu-id="6acd7-111">If an audio format does not contain any padding bits, then this attribute should not be set, or should be set to the same value as the [**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md) attribute.</span></span>

<span data-ttu-id="6acd7-112">Этот атрибут соответствует элементу **ввалидбитсперсампле** структуры [**вавеформатекстенсибле**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) .</span><span class="sxs-lookup"><span data-stu-id="6acd7-112">This attribute corresponds to the **wValidBitsPerSample** member of the [**WAVEFORMATEXTENSIBLE**](/windows/win32/api/mmreg/ns-mmreg-waveformatextensible) structure.</span></span>

<span data-ttu-id="6acd7-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="6acd7-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6acd7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6acd7-114">Requirements</span></span>



| <span data-ttu-id="6acd7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6acd7-115">Requirement</span></span> | <span data-ttu-id="6acd7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6acd7-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6acd7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6acd7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6acd7-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="6acd7-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6acd7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6acd7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6acd7-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="6acd7-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6acd7-121">Header</span><span class="sxs-lookup"><span data-stu-id="6acd7-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6acd7-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6acd7-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6acd7-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6acd7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6acd7-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6acd7-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6acd7-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="6acd7-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6acd7-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="6acd7-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6acd7-127">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="6acd7-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6acd7-128">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="6acd7-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
