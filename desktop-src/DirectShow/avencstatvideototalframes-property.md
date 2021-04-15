---
description: Возвращает число кадров видео, полученных кодировщиком.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Свойство Авенкстатвидеототалфрамес (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655581"
---
# <a name="avencstatvideototalframes-property"></a><span data-ttu-id="7e8d2-103">Авенкстатвидеототалфрамес, свойство</span><span class="sxs-lookup"><span data-stu-id="7e8d2-103">AVEncStatVideoTotalFrames property</span></span>

<span data-ttu-id="7e8d2-104">Возвращает число кадров видео, полученных кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="7e8d2-104">Returns the number of video frames that the encoder received.</span></span>

<span data-ttu-id="7e8d2-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7e8d2-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7e8d2-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7e8d2-106">Data type</span></span>

<span data-ttu-id="7e8d2-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="7e8d2-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7e8d2-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="7e8d2-108">Property GUID</span></span>

<span data-ttu-id="7e8d2-109">**КОДЕКАПИ \_ авенкстатвидеототалфрамес**</span><span class="sxs-lookup"><span data-stu-id="7e8d2-109">**CODECAPI\_AVEncStatVideoTotalFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="7e8d2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e8d2-110">Remarks</span></span>

<span data-ttu-id="7e8d2-111">Это свойство доступно после завершения кодирования.</span><span class="sxs-lookup"><span data-stu-id="7e8d2-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="7e8d2-112">Значением этого свойства является общее число кадров, отправленных кодировщику, включая пропущенные кадры.</span><span class="sxs-lookup"><span data-stu-id="7e8d2-112">The value of this property is the total number of frames sent to the encoder, including frames that were dropped.</span></span> <span data-ttu-id="7e8d2-113">Чтобы получить количество закодированных кадров, прочитайте свойство [**авенкстатвидеокодедфрамес**](avencstatvideocodedframes-property.md) .</span><span class="sxs-lookup"><span data-stu-id="7e8d2-113">To get the number of encoded frames, read the [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e8d2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7e8d2-114">Requirements</span></span>



| <span data-ttu-id="7e8d2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7e8d2-115">Requirement</span></span> | <span data-ttu-id="7e8d2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7e8d2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8d2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7e8d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7e8d2-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7e8d2-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7e8d2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7e8d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7e8d2-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="7e8d2-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7e8d2-121">Header</span><span class="sxs-lookup"><span data-stu-id="7e8d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e8d2-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e8d2-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e8d2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e8d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e8d2-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="7e8d2-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7e8d2-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="7e8d2-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




