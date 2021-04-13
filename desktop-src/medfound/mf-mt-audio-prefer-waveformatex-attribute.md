---
description: Указывает предпочтительную структуру устаревшего формата, используемую при преобразовании типа аудио Media.
ms.assetid: 9bb045a2-be5b-468b-b30b-aedcb7849945
title: Атрибут MF_MT_AUDIO_PREFER_WAVEFORMATEX (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be5f5ac0aadfb2a4d8d2b8394a06f270e1b4d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544351"
---
# <a name="mf_mt_audio_prefer_waveformatex-attribute"></a><span data-ttu-id="f6d50-103">\_АУДИОРАЗЪЕМ MF \_ , \_ предпочтительный \_ атрибут вавеформатекс</span><span class="sxs-lookup"><span data-stu-id="f6d50-103">MF\_MT\_AUDIO\_PREFER\_WAVEFORMATEX attribute</span></span>

<span data-ttu-id="f6d50-104">Указывает предпочтительную структуру устаревшего формата, используемую при преобразовании типа аудио Media.</span><span class="sxs-lookup"><span data-stu-id="f6d50-104">Specifies the preferred legacy format structure to use when converting an audio media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6d50-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f6d50-105">Data type</span></span>

<span data-ttu-id="f6d50-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6d50-106">**UINT32**</span></span>

<span data-ttu-id="f6d50-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="f6d50-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6d50-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6d50-108">Remarks</span></span>

<span data-ttu-id="f6d50-109">Этот атрибут предоставляет указание для функции [**мфкреатевавеформатексфроммфмедиатипе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) .</span><span class="sxs-lookup"><span data-stu-id="f6d50-109">This attribute provides a hint to the [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype) function.</span></span> <span data-ttu-id="f6d50-110">Если атрибут имеет **значение true**, функция по возможности преобразует тип звукового носителя в структуру [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) , вместо того чтобы преобразовывать ее в структуру [**вавеформатекстенсибле**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f6d50-110">If the attribute is **TRUE**, the function converts the audio media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure whenever possible, instead of converting it to a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span>

<span data-ttu-id="f6d50-111">Функция [**мфинитмедиатипефромвавеформатекс**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) задает этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="f6d50-111">The [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) function sets this attribute.</span></span> <span data-ttu-id="f6d50-112">Значение этого атрибута можно переопределить, но установка этого атрибута в **значение true** не гарантирует, что тип звукового носителя можно преобразовать в [**вавеформатекс**](/previous-versions/dd757713(v=vs.85)) форму.</span><span class="sxs-lookup"><span data-stu-id="f6d50-112">You can override the value of this attribute, but setting this attribute to **TRUE** does not guarantee that an audio media type can be converted to [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) form.</span></span>

<span data-ttu-id="f6d50-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="f6d50-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d50-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f6d50-114">Requirements</span></span>



| <span data-ttu-id="f6d50-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f6d50-115">Requirement</span></span> | <span data-ttu-id="f6d50-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f6d50-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d50-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6d50-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d50-118">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="f6d50-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f6d50-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6d50-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d50-120">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="f6d50-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f6d50-121">Header</span><span class="sxs-lookup"><span data-stu-id="f6d50-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6d50-122"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6d50-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d50-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6d50-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d50-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6d50-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6d50-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6d50-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f6d50-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f6d50-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f6d50-127">**имфмедиатипе**</span><span class="sxs-lookup"><span data-stu-id="f6d50-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="f6d50-128">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f6d50-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
