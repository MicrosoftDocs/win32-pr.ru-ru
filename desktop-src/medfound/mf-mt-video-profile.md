---
description: Задает профиль кодирования видео для выходного типа носителя. Это псевдоним \_ \_ атрибута профиля MF MT MPEG2 \_ .
ms.assetid: 29D1CCCA-CC11-46F1-A094-8BA8F74F7EE9
title: Атрибут MF_MT_VIDEO_PROFILE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6dbf8d324c7a451c1d2affb9f348a3ef2e1806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712863"
---
# <a name="mf_mt_video_profile-attribute"></a><span data-ttu-id="44844-104">\_ \_ Атрибут профиля видео MF MT \_</span><span class="sxs-lookup"><span data-stu-id="44844-104">MF\_MT\_VIDEO\_PROFILE attribute</span></span>

<span data-ttu-id="44844-105">Задает профиль кодирования видео для выходного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="44844-105">Specifies the profile of video encoding on the output media type.</span></span> <span data-ttu-id="44844-106">Это псевдоним атрибута [ \_ \_ \_ профиля MF MT MPEG2](mf-mt-mpeg2-profile-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="44844-106">This is an alias of [MF\_MT\_MPEG2\_PROFILE](mf-mt-mpeg2-profile-attribute.md) attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="44844-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="44844-107">Data type</span></span>

<span data-ttu-id="44844-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="44844-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="44844-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44844-109">Remarks</span></span>

<span data-ttu-id="44844-110">**Кодировщики H. 264:**</span><span class="sxs-lookup"><span data-stu-id="44844-110">**H.264 encoders:**</span></span>

<span data-ttu-id="44844-111">В число поддерживаемых профилей входят [**eAVEncH264VProfile \_ Констраинедбасе**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) и **eAVEncH264VProfile \_ констраинедхигх**.</span><span class="sxs-lookup"><span data-stu-id="44844-111">Supported profiles are exceeded to include [**eAVEncH264VProfile\_ConstrainedBase**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) and **eAVEncH264VProfile\_ConstrainedHigh**.</span></span>

<span data-ttu-id="44844-112">Кодировщики должны поддерживать методы [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) и [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) для этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="44844-112">Encoders shall support both [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) and [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) for this attribute.</span></span>

<span data-ttu-id="44844-113">Это статические, поэтому видеокодировщики необходимо настроить перед запуском потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="44844-113">This is static, so video encoders must be configured before the streaming starts.</span></span> <span data-ttu-id="44844-114">Если приложение задает профиль, который не поддерживает кодировщик, кодировщик должен отклонить тип носителя.</span><span class="sxs-lookup"><span data-stu-id="44844-114">If the application sets a profile which the encoder does not support, the encoder shall reject the media type.</span></span>

<span data-ttu-id="44844-115">Рекомендуемое значение по умолчанию: [**\_ основной профиль eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) .</span><span class="sxs-lookup"><span data-stu-id="44844-115">Recommended default: [**eAVEncH264VProfile\_Main**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="44844-116">Требования</span><span class="sxs-lookup"><span data-stu-id="44844-116">Requirements</span></span>



| <span data-ttu-id="44844-117">Требование</span><span class="sxs-lookup"><span data-stu-id="44844-117">Requirement</span></span> | <span data-ttu-id="44844-118">Значение</span><span class="sxs-lookup"><span data-stu-id="44844-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44844-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44844-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44844-120">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44844-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="44844-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44844-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44844-122">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="44844-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="44844-123">Header</span><span class="sxs-lookup"><span data-stu-id="44844-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44844-124"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="44844-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44844-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44844-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44844-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44844-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
