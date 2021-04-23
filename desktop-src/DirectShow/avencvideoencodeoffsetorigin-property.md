---
description: Задает левый и верхний углы прямоугольника обрезки, если видео обрезано.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Свойство Авенквидеоенкодеоффсеторигин (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139803"
---
# <a name="avencvideoencodeoffsetorigin-property"></a><span data-ttu-id="c2ebd-103">Авенквидеоенкодеоффсеторигин, свойство</span><span class="sxs-lookup"><span data-stu-id="c2ebd-103">AVEncVideoEncodeOffsetOrigin property</span></span>

<span data-ttu-id="c2ebd-104">Задает левый и верхний углы прямоугольника обрезки, если видео обрезано.</span><span class="sxs-lookup"><span data-stu-id="c2ebd-104">Specifies the left and top corners of the clipping rectangle, if the video is cropped.</span></span>

<span data-ttu-id="c2ebd-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c2ebd-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c2ebd-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c2ebd-106">Data type</span></span>

<span data-ttu-id="c2ebd-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="c2ebd-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c2ebd-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="c2ebd-108">Property GUID</span></span>

<span data-ttu-id="c2ebd-109">**КОДЕКАПИ \_ авенквидеоенкодеоффсеторигин**</span><span class="sxs-lookup"><span data-stu-id="c2ebd-109">**CODECAPI\_AVEncVideoEncodeOffsetOrigin**</span></span>

## <a name="property-value"></a><span data-ttu-id="c2ebd-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c2ebd-110">Property value</span></span>

<span data-ttu-id="c2ebd-111">Верхние 16 разрядов значения содержат смещение от левого края входного кадра в пикселях.</span><span class="sxs-lookup"><span data-stu-id="c2ebd-111">The upper 16 bits of the value contain the offset from the left edge of the input frame, in pixels.</span></span> <span data-ttu-id="c2ebd-112">Младшие 16 бит содержат смещение от верхнего края входного кадра (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="c2ebd-112">The lower 16 bits contain the offset from the top edge of the input frame, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ebd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2ebd-113">Remarks</span></span>

<span data-ttu-id="c2ebd-114">Приложения могут задать это свойство, чтобы обрезать входное видео.</span><span class="sxs-lookup"><span data-stu-id="c2ebd-114">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="c2ebd-115">Используйте свойство [**авенквидеоенкодедименсион**](avencvideoencodedimension-property.md) , чтобы указать ширину и высоту прямоугольника обрезки.</span><span class="sxs-lookup"><span data-stu-id="c2ebd-115">Use the [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) property to specify the width and height of the clipping rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ebd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c2ebd-116">Requirements</span></span>



| <span data-ttu-id="c2ebd-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c2ebd-117">Requirement</span></span> | <span data-ttu-id="c2ebd-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c2ebd-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2ebd-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2ebd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c2ebd-120">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c2ebd-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c2ebd-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2ebd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c2ebd-122">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="c2ebd-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c2ebd-123">Header</span><span class="sxs-lookup"><span data-stu-id="c2ebd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2ebd-124"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2ebd-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2ebd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2ebd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ebd-126">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="c2ebd-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c2ebd-127">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="c2ebd-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




