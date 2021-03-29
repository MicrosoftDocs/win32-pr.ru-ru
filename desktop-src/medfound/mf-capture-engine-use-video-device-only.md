---
description: Указывает, будет ли подсистема захвата записывать видео, но не аудио.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: Атрибут MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991483"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a><span data-ttu-id="f349f-103">\_Запись MF \_ Engine \_ использовать \_ \_ атрибут " \_ только видео устройства"</span><span class="sxs-lookup"><span data-stu-id="f349f-103">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="f349f-104">Указывает, будет ли подсистема захвата записывать видео, но не аудио.</span><span class="sxs-lookup"><span data-stu-id="f349f-104">Specifies whether the capture engine captures video but not audio.</span></span>

## <a name="data-type"></a><span data-ttu-id="f349f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f349f-105">Data type</span></span>

<span data-ttu-id="f349f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f349f-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f349f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f349f-107">Remarks</span></span>

<span data-ttu-id="f349f-108">Если этот атрибут имеет **значение true**, подсистема захвата не выбирает или не использует устройство аудиозаписи.</span><span class="sxs-lookup"><span data-stu-id="f349f-108">If this attribute is **TRUE**, the capture engine does not select or use an audio capture device.</span></span> <span data-ttu-id="f349f-109">Присвойте этому атрибуту **значение true** , если хотите записывать видео без звука.</span><span class="sxs-lookup"><span data-stu-id="f349f-109">Set this attribute to **TRUE** if you want to capture video without audio.</span></span> <span data-ttu-id="f349f-110">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="f349f-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f349f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f349f-111">Requirements</span></span>



| <span data-ttu-id="f349f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f349f-112">Requirement</span></span> | <span data-ttu-id="f349f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f349f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f349f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f349f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f349f-115">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f349f-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f349f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f349f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f349f-117">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f349f-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f349f-118">Header</span><span class="sxs-lookup"><span data-stu-id="f349f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f349f-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f349f-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f349f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f349f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f349f-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f349f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f349f-122">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="f349f-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="f349f-123">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="f349f-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




