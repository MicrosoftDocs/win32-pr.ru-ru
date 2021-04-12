---
description: Посылается конвейером кодировщику МФТС по последовательному каналу с примерами мультимедиа через Имфтрансформ::P Роцессевент.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Событие Минкодингпараметерс (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263649"
---
# <a name="meencodingparameters-event"></a><span data-ttu-id="f96a9-103">Событие Минкодингпараметерс</span><span class="sxs-lookup"><span data-stu-id="f96a9-103">MEEncodingParameters event</span></span>

<span data-ttu-id="f96a9-104">Посылается конвейером кодировщику МФТС по последовательному каналу с примерами мультимедиа через [**имфтрансформ::P роцессевент**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="f96a9-104">Sent by the pipeline to encoder MFTs serially with media samples via [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="event-values"></a><span data-ttu-id="f96a9-105">Значения событий</span><span class="sxs-lookup"><span data-stu-id="f96a9-105">Event values</span></span>

<span data-ttu-id="f96a9-106">Возможные значения, полученные из [**имфмедиаевент:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) , включают следующее.</span><span class="sxs-lookup"><span data-stu-id="f96a9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f96a9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f96a9-107">VARTYPE</span></span>              | <span data-ttu-id="f96a9-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f96a9-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="f96a9-109">VT \_ пуст</span><span class="sxs-lookup"><span data-stu-id="f96a9-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f96a9-110">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="f96a9-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="f96a9-111">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f96a9-111">Attributes</span></span>

<span data-ttu-id="f96a9-112">Для этого события определены следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f96a9-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="f96a9-113">attribute</span><span class="sxs-lookup"><span data-stu-id="f96a9-113">Attribute</span></span>                                         | <span data-ttu-id="f96a9-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f96a9-114">Description</span></span>                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f96a9-115">**имфаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="f96a9-115">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | <span data-ttu-id="f96a9-116">Содержит новые параметры на основе Икодекапи, которые кодировщик должен применять к последующим входящим примерам.</span><span class="sxs-lookup"><span data-stu-id="f96a9-116">Contains the new ICodecAPI-based settings that the encoder should apply on subsequent incoming samples.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="f96a9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f96a9-117">Remarks</span></span>

<span data-ttu-id="f96a9-118">Полезные данные события — это хранилище атрибутов (указатель Имфаттрибутес), которое содержит новые параметры на основе Икодекапи///, которые кодировщик должен применять к последующим входящим примерам.</span><span class="sxs-lookup"><span data-stu-id="f96a9-118">Event payload is an attribute store (IMFAttributes pointer) that contains the new ICodecAPI-based /// settings that the encoder should apply on subsequent incoming samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96a9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f96a9-119">Requirements</span></span>



| <span data-ttu-id="f96a9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f96a9-120">Requirement</span></span> | <span data-ttu-id="f96a9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f96a9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96a9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f96a9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f96a9-123">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f96a9-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f96a9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f96a9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f96a9-125">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f96a9-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="f96a9-126">Header</span><span class="sxs-lookup"><span data-stu-id="f96a9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f96a9-127"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f96a9-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f96a9-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f96a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96a9-129">События Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f96a9-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




