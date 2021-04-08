---
description: Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в пути к видео приемника записи.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: Атрибут MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f5e297ddb5f06e71fe05a95df73aa205a7889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898362"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a><span data-ttu-id="4ed36-103">\_ \_ \_ \_ \_ \_ \_ Необработанный \_ атрибут выборки данных для приемника записей подсистемы захвата MF</span><span class="sxs-lookup"><span data-stu-id="4ed36-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="4ed36-104">Задает максимальное число необработанных выборок, которые могут быть помещены в буфер для обработки в пути к видео приемника записи.</span><span class="sxs-lookup"><span data-stu-id="4ed36-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ed36-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4ed36-105">Data type</span></span>

<span data-ttu-id="4ed36-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4ed36-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="4ed36-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ed36-107">Remarks</span></span>

<span data-ttu-id="4ed36-108">Чтобы настроить этот атрибут в подсистеме записи, добавьте его в параметр *паттрибутес* при вызове [**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="4ed36-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="4ed36-109">Максимальное значение для этого атрибута — 17.</span><span class="sxs-lookup"><span data-stu-id="4ed36-109">The maximum value for this attribute is 17.</span></span>

<span data-ttu-id="4ed36-110">После того как запись помещается в буфер на максимальное количество необработанных образцов, заданное с помощью \_ \_ приемника записей подсистемы записи MF, \_ \_ Максимальное число \_ \_ \_ необработанных \_ образцов, это снижает частоту кадров, удаляя образцы.</span><span class="sxs-lookup"><span data-stu-id="4ed36-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ed36-111">Требования</span><span class="sxs-lookup"><span data-stu-id="4ed36-111">Requirements</span></span>



| <span data-ttu-id="4ed36-112">Требование</span><span class="sxs-lookup"><span data-stu-id="4ed36-112">Requirement</span></span> | <span data-ttu-id="4ed36-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4ed36-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ed36-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ed36-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4ed36-115">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ed36-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="4ed36-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ed36-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4ed36-117">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ed36-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4ed36-118">Header</span><span class="sxs-lookup"><span data-stu-id="4ed36-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ed36-119"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ed36-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ed36-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ed36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ed36-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ed36-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ed36-122">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="4ed36-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ed36-123">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="4ed36-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




