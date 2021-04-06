---
description: Содержит метку времени из драйвера устройства.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: Атрибут MFSampleExtension_DeviceTimestamp (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898741"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a><span data-ttu-id="6e41b-103">Мфсампликстенсион \_ DeviceTimestamp, атрибут</span><span class="sxs-lookup"><span data-stu-id="6e41b-103">MFSampleExtension\_DeviceTimestamp attribute</span></span>

<span data-ttu-id="6e41b-104">Содержит метку времени из драйвера устройства.</span><span class="sxs-lookup"><span data-stu-id="6e41b-104">Contains the time stamp from the device driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="6e41b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6e41b-105">Data type</span></span>

<span data-ttu-id="6e41b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="6e41b-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="6e41b-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="6e41b-107">Get/set</span></span>

<span data-ttu-id="6e41b-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="6e41b-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="6e41b-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="6e41b-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="6e41b-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="6e41b-110">Applies to</span></span>

[<span data-ttu-id="6e41b-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="6e41b-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="6e41b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e41b-112">Remarks</span></span>

<span data-ttu-id="6e41b-113">Этот атрибут задается в примерах носителей, созданных источником мультимедиа для устройства записи.</span><span class="sxs-lookup"><span data-stu-id="6e41b-113">This attribute is set on media samples created by a media source for a capture device.</span></span> <span data-ttu-id="6e41b-114">Значение этого атрибута находится в домене [**мфтиме**](mftime.md) , которому предоставляется общий доступ к эпохе со счетчиком производительности запросов (QPC) и всегда выражается в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="6e41b-114">This attribute's value is in the [**MFTIME**](mftime.md) domain, sharing an epoch with query performance counter (QPC) time and always expressed in 100ns units.</span></span> <span data-ttu-id="6e41b-115">Этот атрибут доступен для МФТС, вставленного в конвейер захвата.</span><span class="sxs-lookup"><span data-stu-id="6e41b-115">This attribute is available for MFTs inserted into the capture pipeline.</span></span>

<span data-ttu-id="6e41b-116">Чтобы получить отметку времени относительно начала потоковой передачи, вызовите метод [**имфсампле:: жетсамплетиме**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .</span><span class="sxs-lookup"><span data-stu-id="6e41b-116">To get the time stamp relative to the start of streaming, call the [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) method.</span></span>

<span data-ttu-id="6e41b-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="6e41b-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e41b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6e41b-118">Requirements</span></span>



| <span data-ttu-id="6e41b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6e41b-119">Requirement</span></span> | <span data-ttu-id="6e41b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6e41b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e41b-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e41b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e41b-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6e41b-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6e41b-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e41b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e41b-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e41b-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6e41b-125">Header</span><span class="sxs-lookup"><span data-stu-id="6e41b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e41b-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e41b-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e41b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e41b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e41b-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e41b-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6e41b-129">Видеозапись Аудио/видео в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6e41b-129">Audio/Video Capture in Media Foundation</span></span>](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="6e41b-130">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="6e41b-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




