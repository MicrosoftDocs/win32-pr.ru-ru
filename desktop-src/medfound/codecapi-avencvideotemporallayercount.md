---
description: Задает число временных слоев видео для кодировщика видео.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: Свойство CODECAPI_AVEncVideoTemporalLayerCount (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496839"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a><span data-ttu-id="f7d2d-103">КОДЕКАПИ \_ авенквидеотемпораллайеркаунт, свойство</span><span class="sxs-lookup"><span data-stu-id="f7d2d-103">CODECAPI\_AVEncVideoTemporalLayerCount property</span></span>

<span data-ttu-id="f7d2d-104">Задает число временных слоев видео для кодировщика видео.</span><span class="sxs-lookup"><span data-stu-id="f7d2d-104">Sets the video temporal layer count for a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="f7d2d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f7d2d-105">Data type</span></span>

<span data-ttu-id="f7d2d-106">**ULONG (VT \_ UI4)**</span><span class="sxs-lookup"><span data-stu-id="f7d2d-106">**ULONG (VT\_UI4)**</span></span>

## <a name="property-guid"></a><span data-ttu-id="f7d2d-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="f7d2d-107">Property GUID</span></span>

<span data-ttu-id="f7d2d-108">**КОДЕКАПИ \_ авенквидеотемпораллайеркаунт**</span><span class="sxs-lookup"><span data-stu-id="f7d2d-108">**CODECAPI\_AVEncVideoTemporalLayerCount**</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d2d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f7d2d-109">Remarks</span></span>

<span data-ttu-id="f7d2d-110">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="f7d2d-110">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="f7d2d-111">КОДЕКАПИ \_ авенквидеотемпораллайеркаунт, [кодекапи \_ авенквидеаусаже](codecapi-avencvideousage.md)и [кодекапи \_ авенккоммонратеконтролмоде](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) являются статическими свойствами кодировщика.</span><span class="sxs-lookup"><span data-stu-id="f7d2d-111">CODECAPI\_AVEncVideoTemporalLayerCount, [CODECAPI\_AVEncVideoUsage](codecapi-avencvideousage.md), and [CODECAPI\_AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) are static encoder properties.</span></span> <span data-ttu-id="f7d2d-112">После установки они вступят в силу только после того, как на закрепление выходных данных камеры будет вызван тип набора носителей.</span><span class="sxs-lookup"><span data-stu-id="f7d2d-112">Once set, these will only take effect after a set media type is called on the camera s output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d2d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f7d2d-113">Requirements</span></span>



| <span data-ttu-id="f7d2d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f7d2d-114">Requirement</span></span> | <span data-ttu-id="f7d2d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f7d2d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d2d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7d2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d2d-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="f7d2d-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="f7d2d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7d2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d2d-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f7d2d-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f7d2d-120">Header</span><span class="sxs-lookup"><span data-stu-id="f7d2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d2d-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2d-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d2d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7d2d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d2d-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f7d2d-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

