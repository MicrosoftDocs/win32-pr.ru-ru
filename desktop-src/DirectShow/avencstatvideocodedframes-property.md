---
description: Возвращает число закодированных видеокадров.
ms.assetid: ade9fe69-b3dd-44aa-856b-75d4a7e4c680
title: Свойство Авенкстатвидеокодедфрамес (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aed3ed0a06003807a6bd0db90b8978282042daf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140190"
---
# <a name="avencstatvideocodedframes-property"></a><span data-ttu-id="5941c-103">Авенкстатвидеокодедфрамес, свойство</span><span class="sxs-lookup"><span data-stu-id="5941c-103">AVEncStatVideoCodedFrames property</span></span>

<span data-ttu-id="5941c-104">Возвращает число закодированных видеокадров.</span><span class="sxs-lookup"><span data-stu-id="5941c-104">Returns the number of video frames that were encoded.</span></span>

<span data-ttu-id="5941c-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5941c-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="5941c-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5941c-106">Data type</span></span>

<span data-ttu-id="5941c-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="5941c-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5941c-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="5941c-108">Property GUID</span></span>

<span data-ttu-id="5941c-109">**КОДЕКАПИ \_ авенкстатвидеокодедфрамес**</span><span class="sxs-lookup"><span data-stu-id="5941c-109">**CODECAPI\_AVEncStatVideoCodedFrames**</span></span>

## <a name="remarks"></a><span data-ttu-id="5941c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5941c-110">Remarks</span></span>

<span data-ttu-id="5941c-111">Это свойство доступно после завершения кодирования.</span><span class="sxs-lookup"><span data-stu-id="5941c-111">This property is available after the encoding is completed.</span></span>

<span data-ttu-id="5941c-112">Значение этого свойства равно значению свойства [**авенкстатвидеототалфрамес**](avencstatvideototalframes-property.md) минус число пропущенных кадров.</span><span class="sxs-lookup"><span data-stu-id="5941c-112">The value of this property is equal to the [**AVEncStatVideoTotalFrames**](avencstatvideototalframes-property.md) property minus the number of dropped frames.</span></span> <span data-ttu-id="5941c-113">Кодировщик может удалить кадры, чтобы остаться в заданных ограничениях скорости.</span><span class="sxs-lookup"><span data-stu-id="5941c-113">The encoder might drop frames to stay within the specified bit rate constraints.</span></span> <span data-ttu-id="5941c-114">Он также может удалять кадры в конце потока (см. свойство [**авенккоммонстреамендхандлинг**](avenccommonstreamendhandling-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="5941c-114">It might also drop frames at the end of the stream (see [**AVEncCommonStreamEndHandling**](avenccommonstreamendhandling-property.md) property).</span></span>

## <a name="requirements"></a><span data-ttu-id="5941c-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5941c-115">Requirements</span></span>



| <span data-ttu-id="5941c-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5941c-116">Requirement</span></span> | <span data-ttu-id="5941c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5941c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5941c-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5941c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5941c-119">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5941c-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5941c-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5941c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5941c-121">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="5941c-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5941c-122">Header</span><span class="sxs-lookup"><span data-stu-id="5941c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5941c-123"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5941c-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5941c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5941c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5941c-125">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="5941c-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="5941c-126">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="5941c-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




