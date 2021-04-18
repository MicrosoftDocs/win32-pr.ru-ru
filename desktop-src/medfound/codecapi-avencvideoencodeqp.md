---
description: Указывает параметр дискретизация (QP) для кодирования видео.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Свойство CODECAPI_AVEncVideoEncodeQP (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701330"
---
# <a name="codecapi_avencvideoencodeqp-property"></a><span data-ttu-id="d44eb-103">КОДЕКАПИ \_ авенквидеоенкодекп, свойство</span><span class="sxs-lookup"><span data-stu-id="d44eb-103">CODECAPI\_AVEncVideoEncodeQP property</span></span>

<span data-ttu-id="d44eb-104">Указывает параметр дискретизация (QP) для кодирования видео.</span><span class="sxs-lookup"><span data-stu-id="d44eb-104">Specifies the quantization parameter (QP) for video encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="d44eb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d44eb-105">Data type</span></span>

<span data-ttu-id="d44eb-106">**Улонглонг** (VT \_ UI8)</span><span class="sxs-lookup"><span data-stu-id="d44eb-106">**ULONGLONG** (VT\_UI8)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d44eb-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="d44eb-107">Property GUID</span></span>

<span data-ttu-id="d44eb-108">**КОДЕКАПИ \_ авенквидеоенкодекп**</span><span class="sxs-lookup"><span data-stu-id="d44eb-108">**CODECAPI\_AVEncVideoEncodeQP**</span></span>

## <a name="property-value"></a><span data-ttu-id="d44eb-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d44eb-109">Property value</span></span>

<span data-ttu-id="d44eb-110">Набор из 4 16 битовых полей, используемых для указания кадра QPs в кодировке fixed-QP.</span><span class="sxs-lookup"><span data-stu-id="d44eb-110">A set of four 16-bit fields used to specify the frame QPs in fixed-QP encoding.</span></span>

<span data-ttu-id="d44eb-111">Поля:</span><span class="sxs-lookup"><span data-stu-id="d44eb-111">The fields are:</span></span>

-   <span data-ttu-id="d44eb-112">BITS 0-15: служба QP по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d44eb-112">Bits 0-15: Default QP</span></span>
-   <span data-ttu-id="d44eb-113">BITS 16-31: обработчики запросов, используемые для кадров I</span><span class="sxs-lookup"><span data-stu-id="d44eb-113">Bits 16-31: QP used for I frames</span></span>
-   <span data-ttu-id="d44eb-114">BITS 32-47: служба QP, используемая для кадров P</span><span class="sxs-lookup"><span data-stu-id="d44eb-114">Bits 32-47: QP used for P frames</span></span>
-   <span data-ttu-id="d44eb-115">BITS 48-63: служба QP, используемая для кадров B</span><span class="sxs-lookup"><span data-stu-id="d44eb-115">Bits 48-63: QP used for B frames</span></span>

## <a name="remarks"></a><span data-ttu-id="d44eb-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d44eb-116">Remarks</span></span>

<span data-ttu-id="d44eb-117">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="d44eb-117">This property is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

<span data-ttu-id="d44eb-118">Чтобы обеспечить согласованное использование в разных кодировщиках, необходимо предположить, что кодировщики будут рассматривать только обработчики запросов по умолчанию и могут игнорировать значения QP для изображений I/P/B.</span><span class="sxs-lookup"><span data-stu-id="d44eb-118">To insure consistent usage across different encoders, you should assume encoders will only look at the default QP and can ignore QP values for I/P/B pictures.</span></span>

## <a name="requirements"></a><span data-ttu-id="d44eb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d44eb-119">Requirements</span></span>



| <span data-ttu-id="d44eb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d44eb-120">Requirement</span></span> | <span data-ttu-id="d44eb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d44eb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d44eb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d44eb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d44eb-123">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="d44eb-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d44eb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d44eb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d44eb-125">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d44eb-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d44eb-126">Header</span><span class="sxs-lookup"><span data-stu-id="d44eb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d44eb-127"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d44eb-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d44eb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d44eb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d44eb-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d44eb-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d44eb-130">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="d44eb-130">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

