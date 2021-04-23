---
description: Определяет, какой поток создал событие записи.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: Атрибут MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898365"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a><span data-ttu-id="67d07-103">\_ \_ \_ \_ Атрибут индекса потока событий для обработчика записи MF \_</span><span class="sxs-lookup"><span data-stu-id="67d07-103">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX attribute</span></span>

<span data-ttu-id="67d07-104">Определяет, какой поток создал событие записи.</span><span class="sxs-lookup"><span data-stu-id="67d07-104">Identifies which stream generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="67d07-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="67d07-105">Data type</span></span>

<span data-ttu-id="67d07-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="67d07-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="67d07-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="67d07-107">Get/set</span></span>

<span data-ttu-id="67d07-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="67d07-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="67d07-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67d07-109">Remarks</span></span>

<span data-ttu-id="67d07-110">Этот атрибут отображается для некоторых событий в подсистеме захвата.</span><span class="sxs-lookup"><span data-stu-id="67d07-110">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="67d07-111">Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) GetObject для объекта события.</span><span class="sxs-lookup"><span data-stu-id="67d07-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) on the event object.</span></span> <span data-ttu-id="67d07-112">Объект события передается в приложение через метод [**имфкаптурингинеоневенткаллбакк:: oneven**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .</span><span class="sxs-lookup"><span data-stu-id="67d07-112">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67d07-113">Требования</span><span class="sxs-lookup"><span data-stu-id="67d07-113">Requirements</span></span>



| <span data-ttu-id="67d07-114">Требование</span><span class="sxs-lookup"><span data-stu-id="67d07-114">Requirement</span></span> | <span data-ttu-id="67d07-115">Значение</span><span class="sxs-lookup"><span data-stu-id="67d07-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67d07-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67d07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="67d07-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="67d07-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="67d07-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67d07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="67d07-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="67d07-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="67d07-120">Header</span><span class="sxs-lookup"><span data-stu-id="67d07-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="67d07-121"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="67d07-121"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67d07-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67d07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67d07-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67d07-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="67d07-124">**Имфкаптурингинеоневенткаллбакк:: oneven**</span><span class="sxs-lookup"><span data-stu-id="67d07-124">**IMFCaptureEngineOnEventCallback::OnEvent**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




