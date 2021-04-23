---
description: Задает ширину и высоту закодированного видео, если видео обрезано.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Свойство Авенквидеоенкодедименсион (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662005"
---
# <a name="avencvideoencodedimension-property"></a><span data-ttu-id="70e1e-103">Авенквидеоенкодедименсион, свойство</span><span class="sxs-lookup"><span data-stu-id="70e1e-103">AVEncVideoEncodeDimension property</span></span>

<span data-ttu-id="70e1e-104">Задает ширину и высоту закодированного видео, если видео обрезано.</span><span class="sxs-lookup"><span data-stu-id="70e1e-104">Specifies the width and height of the encoded video, if the video is cropped.</span></span>

<span data-ttu-id="70e1e-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="70e1e-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="70e1e-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="70e1e-106">Data type</span></span>

<span data-ttu-id="70e1e-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="70e1e-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="70e1e-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="70e1e-108">Property GUID</span></span>

<span data-ttu-id="70e1e-109">**КОДЕКАПИ \_ авенквидеоенкодедименсион**</span><span class="sxs-lookup"><span data-stu-id="70e1e-109">**CODECAPI\_AVEncVideoEncodeDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="70e1e-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="70e1e-110">Property value</span></span>

<span data-ttu-id="70e1e-111">Верхние 16 разрядов значения содержат ширину в пикселях, а младшие 16 бит содержат высоту в пикселях.</span><span class="sxs-lookup"><span data-stu-id="70e1e-111">The upper 16 bits of the value contain the width in pixels, and the lower 16 bits contain the height in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e1e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70e1e-112">Remarks</span></span>

<span data-ttu-id="70e1e-113">Приложения могут задать это свойство, чтобы обрезать входное видео.</span><span class="sxs-lookup"><span data-stu-id="70e1e-113">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="70e1e-114">Указанный размер должен быть меньше размера входных кадров видео.</span><span class="sxs-lookup"><span data-stu-id="70e1e-114">The specified size must be less than the size of the input video frames.</span></span> <span data-ttu-id="70e1e-115">Используйте свойство [**авенквидеоенкодеоффсеторигин**](avencvideoencodeoffsetorigin-property.md) , чтобы указать левый и верхний углы прямоугольника обрезки.</span><span class="sxs-lookup"><span data-stu-id="70e1e-115">Use the [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) property to specify the left and top corners of the clipping rectangle.</span></span>

<span data-ttu-id="70e1e-116">Кодировщики могут возвращать это свойство как возможность.</span><span class="sxs-lookup"><span data-stu-id="70e1e-116">Encoders can return this property as a capability.</span></span>

<span data-ttu-id="70e1e-117">Это свойство также используется с [кодировщиками камер H. 264 увк 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="70e1e-117">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="70e1e-118">Для кодировщиков камер УВК 1,5 не поддерживается [авенквидеоенкодеоффсеторигин](avencvideoencodeoffsetorigin-property.md) .</span><span class="sxs-lookup"><span data-stu-id="70e1e-118">For UVC 1.5 camera encoders, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="70e1e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="70e1e-119">Requirements</span></span>



| <span data-ttu-id="70e1e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="70e1e-120">Requirement</span></span> | <span data-ttu-id="70e1e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="70e1e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70e1e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70e1e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="70e1e-123">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="70e1e-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="70e1e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70e1e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="70e1e-125">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="70e1e-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="70e1e-126">Header</span><span class="sxs-lookup"><span data-stu-id="70e1e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e1e-127"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e1e-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e1e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70e1e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e1e-129">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="70e1e-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="70e1e-130">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="70e1e-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

