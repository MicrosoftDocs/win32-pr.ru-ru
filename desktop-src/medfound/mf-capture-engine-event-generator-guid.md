---
description: Определяет компонент, создавший событие записи.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: Атрибут MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701655"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a><span data-ttu-id="64574-103">\_ \_ \_ \_ Атрибут GUID генератора событий ядра записи MF \_</span><span class="sxs-lookup"><span data-stu-id="64574-103">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID attribute</span></span>

<span data-ttu-id="64574-104">Определяет компонент, создавший событие записи.</span><span class="sxs-lookup"><span data-stu-id="64574-104">Identifies the component that generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="64574-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="64574-105">Data type</span></span>

<span data-ttu-id="64574-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="64574-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="64574-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="64574-107">Remarks</span></span>

<span data-ttu-id="64574-108">Этот атрибут отображается для некоторых событий в подсистеме захвата.</span><span class="sxs-lookup"><span data-stu-id="64574-108">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="64574-109">Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) GetObject в объекте события.</span><span class="sxs-lookup"><span data-stu-id="64574-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) on the event object.</span></span> <span data-ttu-id="64574-110">Объект события передается в приложение через метод [**имфкаптурингинеоневенткаллбакк:: oneven**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="64574-110">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

<span data-ttu-id="64574-111">Значение представляет собой идентификатор интерфейса для компонента, создавшего событие.</span><span class="sxs-lookup"><span data-stu-id="64574-111">The value is an interface identifier for the component that generated the event.</span></span> <span data-ttu-id="64574-112">Например, значение **IID \_ имфкаптурепревиевсинк** указывает на приемник предварительной версии ([**имфкаптурепревиевсинк**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span><span class="sxs-lookup"><span data-stu-id="64574-112">For example, the value **IID\_IMFCapturePreviewSink** indicates the preview sink ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span></span> <span data-ttu-id="64574-113">Не все события захвата содержат этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="64574-113">Not every capture event contains this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="64574-114">Требования</span><span class="sxs-lookup"><span data-stu-id="64574-114">Requirements</span></span>



| <span data-ttu-id="64574-115">Требование</span><span class="sxs-lookup"><span data-stu-id="64574-115">Requirement</span></span> | <span data-ttu-id="64574-116">Значение</span><span class="sxs-lookup"><span data-stu-id="64574-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="64574-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="64574-117">Minimum supported client</span></span><br/> | <span data-ttu-id="64574-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="64574-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="64574-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="64574-119">Minimum supported server</span></span><br/> | <span data-ttu-id="64574-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="64574-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64574-121">Header</span><span class="sxs-lookup"><span data-stu-id="64574-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="64574-122"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="64574-122"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64574-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="64574-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64574-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="64574-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="64574-125">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="64574-125">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="64574-126">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="64574-126">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




