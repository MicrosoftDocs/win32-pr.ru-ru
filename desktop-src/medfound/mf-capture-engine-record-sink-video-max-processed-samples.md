---
description: Задает максимальное число обработанных выборок, которые могут быть помещены в буфер видеоролика приемника записи.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: Атрибут MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810492"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a><span data-ttu-id="98af2-103">\_Атрибут сбора данных о \_ \_ \_ приемнике записей модуля \_ \_ \_ \_ записи MF для видео</span><span class="sxs-lookup"><span data-stu-id="98af2-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="98af2-104">Задает максимальное число обработанных выборок, которые могут быть помещены в буфер видеоролика приемника записи.</span><span class="sxs-lookup"><span data-stu-id="98af2-104">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="98af2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="98af2-105">Data type</span></span>

<span data-ttu-id="98af2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="98af2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="98af2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98af2-107">Remarks</span></span>

<span data-ttu-id="98af2-108">Чтобы настроить этот атрибут в подсистеме записи, добавьте его в параметр *паттрибутес* при вызове [**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="98af2-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="98af2-109">Максимальное значение для этого атрибута — 17.</span><span class="sxs-lookup"><span data-stu-id="98af2-109">The maximum value for this attribute is 17.</span></span>

## <a name="requirements"></a><span data-ttu-id="98af2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="98af2-110">Requirements</span></span>



| <span data-ttu-id="98af2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="98af2-111">Requirement</span></span> | <span data-ttu-id="98af2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="98af2-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="98af2-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98af2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="98af2-114">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="98af2-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="98af2-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98af2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="98af2-116">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="98af2-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="98af2-117">Header</span><span class="sxs-lookup"><span data-stu-id="98af2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="98af2-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="98af2-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98af2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98af2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98af2-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98af2-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="98af2-121">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="98af2-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="98af2-122">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="98af2-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




