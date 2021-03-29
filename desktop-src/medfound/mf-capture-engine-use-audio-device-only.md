---
description: Указывает, захватывает ли подсистема захвата аудио, но не видео.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: Атрибут MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991237"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a><span data-ttu-id="208b8-103">\_Система записи \_ MF \_ использует \_ атрибут "только звуковое \_ устройство \_ "</span><span class="sxs-lookup"><span data-stu-id="208b8-103">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="208b8-104">Указывает, захватывает ли подсистема захвата аудио, но не видео.</span><span class="sxs-lookup"><span data-stu-id="208b8-104">Specifies whether the capture engine captures audio but not video.</span></span>

## <a name="data-type"></a><span data-ttu-id="208b8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="208b8-105">Data type</span></span>

<span data-ttu-id="208b8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="208b8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="208b8-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="208b8-107">Remarks</span></span>

<span data-ttu-id="208b8-108">Если этот атрибут имеет **значение true**, подсистема захвата не выбирает или не использует устройство видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="208b8-108">If this attribute is **TRUE**, the capture engine does not select or use a video capture device.</span></span> <span data-ttu-id="208b8-109">Присвойте этому атрибуту **значение true** , если хотите записывать звук без видео.</span><span class="sxs-lookup"><span data-stu-id="208b8-109">Set this attribute to **TRUE** if you want to capture audio without video.</span></span> <span data-ttu-id="208b8-110">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="208b8-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="208b8-111">Требования</span><span class="sxs-lookup"><span data-stu-id="208b8-111">Requirements</span></span>



| <span data-ttu-id="208b8-112">Требование</span><span class="sxs-lookup"><span data-stu-id="208b8-112">Requirement</span></span> | <span data-ttu-id="208b8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="208b8-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="208b8-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="208b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="208b8-115">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="208b8-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="208b8-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="208b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="208b8-117">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="208b8-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="208b8-118">Header</span><span class="sxs-lookup"><span data-stu-id="208b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="208b8-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="208b8-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="208b8-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="208b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208b8-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="208b8-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="208b8-122">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="208b8-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="208b8-123">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="208b8-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




