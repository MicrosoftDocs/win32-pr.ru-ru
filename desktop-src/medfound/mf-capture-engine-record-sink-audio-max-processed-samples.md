---
description: Задает максимальное число обработанных выборок, которые могут быть помещены в буфер звукового пути приемника записи.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: Атрибут MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d1ce4d649c75106545eb2ff39d4f3ea742e6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542567"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a><span data-ttu-id="c6967-103">\_Атрибут сбора данных о \_ \_ \_ приемнике для записи \_ \_ \_ обработчика MF \_</span><span class="sxs-lookup"><span data-stu-id="c6967-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="c6967-104">Задает максимальное число обработанных выборок, которые могут быть помещены в буфер звукового пути приемника записи.</span><span class="sxs-lookup"><span data-stu-id="c6967-104">Sets the maximum number of processed samples that can be buffered in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6967-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c6967-105">Data type</span></span>

<span data-ttu-id="c6967-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c6967-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c6967-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6967-107">Remarks</span></span>

<span data-ttu-id="c6967-108">Чтобы настроить этот атрибут в подсистеме записи, добавьте его в параметр *паттрибутес* при вызове [**Имфкаптурингине:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span><span class="sxs-lookup"><span data-stu-id="c6967-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="c6967-109">Максимальное значение для этого атрибута — 100.</span><span class="sxs-lookup"><span data-stu-id="c6967-109">The maximum value for this attribute is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6967-110">Требования</span><span class="sxs-lookup"><span data-stu-id="c6967-110">Requirements</span></span>



| <span data-ttu-id="c6967-111">Требование</span><span class="sxs-lookup"><span data-stu-id="c6967-111">Requirement</span></span> | <span data-ttu-id="c6967-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c6967-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6967-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6967-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c6967-114">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c6967-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c6967-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6967-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c6967-116">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c6967-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6967-117">Header</span><span class="sxs-lookup"><span data-stu-id="c6967-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6967-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6967-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6967-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6967-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6967-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6967-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6967-121">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="c6967-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6967-122">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="c6967-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




