---
description: Задает значение флага удаления кадра в заголовке группы рисунков (GOP).
ms.assetid: 37f8f5f6-ddcb-44ab-a727-632b78e6f599
title: Свойство Авенквидеохеадердропфраме (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 741911c400256f02f917e143dbc83bfa0eca04bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895090"
---
# <a name="avencvideoheaderdropframe-property"></a><span data-ttu-id="04f99-103">Авенквидеохеадердропфраме, свойство</span><span class="sxs-lookup"><span data-stu-id="04f99-103">AVEncVideoHeaderDropFrame property</span></span>

<span data-ttu-id="04f99-104">Задает значение флага удаления кадра в заголовке группы рисунков (GOP).</span><span class="sxs-lookup"><span data-stu-id="04f99-104">Specifies the value of drop-frame flag in the group of pictures (GOP) header.</span></span>

<span data-ttu-id="04f99-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="04f99-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="04f99-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="04f99-106">Data type</span></span>

<span data-ttu-id="04f99-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="04f99-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="04f99-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="04f99-108">Property GUID</span></span>

<span data-ttu-id="04f99-109">**КОДЕКАПИ \_ авенквидеохеадердропфраме**</span><span class="sxs-lookup"><span data-stu-id="04f99-109">**CODECAPI\_AVEncVideoHeaderDropFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="04f99-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="04f99-110">Property value</span></span>

<span data-ttu-id="04f99-111">Значение этого свойства может быть равно 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="04f99-111">The value of this property can be 0 or 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="04f99-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04f99-112">Remarks</span></span>

<span data-ttu-id="04f99-113">Режим перетаскивания кадров используется в видео NTSC для исправления расхождения между видео, которое составляет 29,97 кадров в секунду, и отображение кода времени — 30 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="04f99-113">Drop-frame mode is used in NTSC video to correct the discrepancy between the video, which is 29.97 frames per second, and the time code display, which is 30 frames per second.</span></span> <span data-ttu-id="04f99-114">В режиме переноса кадров номера кадров 00 и 01 пропускаются в начале каждой минуты, за исключением минут, которые еще кратны десяти (00, 10, 20 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="04f99-114">In drop-frame mode, frame numbers 00 and 01 are skipped at the start of each minute, except for minutes that are even multiples of ten (00, 10, 20, and so forth).</span></span> <span data-ttu-id="04f99-115">Удаляются только номера кадров в коде времени; фактические кадры не удаляются.</span><span class="sxs-lookup"><span data-stu-id="04f99-115">Only the frame numbers in the time code are dropped; no actual frames are dropped.</span></span>

## <a name="requirements"></a><span data-ttu-id="04f99-116">Требования</span><span class="sxs-lookup"><span data-stu-id="04f99-116">Requirements</span></span>



| <span data-ttu-id="04f99-117">Требование</span><span class="sxs-lookup"><span data-stu-id="04f99-117">Requirement</span></span> | <span data-ttu-id="04f99-118">Значение</span><span class="sxs-lookup"><span data-stu-id="04f99-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04f99-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04f99-119">Minimum supported client</span></span><br/> | <span data-ttu-id="04f99-120">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="04f99-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="04f99-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04f99-121">Minimum supported server</span></span><br/> | <span data-ttu-id="04f99-122">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="04f99-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="04f99-123">Header</span><span class="sxs-lookup"><span data-stu-id="04f99-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="04f99-124"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f99-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04f99-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04f99-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f99-126">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="04f99-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="04f99-127">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="04f99-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




