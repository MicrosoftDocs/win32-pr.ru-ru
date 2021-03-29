---
description: Включает или отключает аппаратное ускорение для декодирования видео MPEG-2.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: Свойство AVDecVideoAcceleration_MPEG2 (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806587"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a><span data-ttu-id="f749a-103">Авдеквидеоакцелератион, \_ свойство MPEG2</span><span class="sxs-lookup"><span data-stu-id="f749a-103">AVDecVideoAcceleration\_MPEG2 property</span></span>

<span data-ttu-id="f749a-104">Включает или отключает аппаратное ускорение для декодирования видео MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f749a-104">Enables or disables hardware acceleration for MPEG-2 video decoding.</span></span>

<span data-ttu-id="f749a-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f749a-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="f749a-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f749a-106">Data type</span></span>

<span data-ttu-id="f749a-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="f749a-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f749a-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="f749a-108">Property GUID</span></span>

<span data-ttu-id="f749a-109">**КОДЕКАПИ \_ авдеквидеоакцелератион \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="f749a-109">**CODECAPI\_AVDecVideoAcceleration\_MPEG2**</span></span>

## <a name="remarks"></a><span data-ttu-id="f749a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f749a-110">Remarks</span></span>

<span data-ttu-id="f749a-111">Если значение равно нулю, декодер не использует ускорение видео DirectX (ДКСВА) для декодирования видео MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="f749a-111">If the value is zero, the decoder does not use DirectX Video Acceleration (DXVA) for MPEG-2 video decoding.</span></span> <span data-ttu-id="f749a-112">Для фильтров DirectShow установите это свойство перед подключением выходного ПИН-кода декодера.</span><span class="sxs-lookup"><span data-stu-id="f749a-112">For DirectShow filters, set this property before the decoder's output pin is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="f749a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f749a-113">Requirements</span></span>



| <span data-ttu-id="f749a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f749a-114">Requirement</span></span> | <span data-ttu-id="f749a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f749a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f749a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f749a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f749a-117">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f749a-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f749a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f749a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f749a-119">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="f749a-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f749a-120">Header</span><span class="sxs-lookup"><span data-stu-id="f749a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f749a-121"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f749a-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f749a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f749a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f749a-123">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="f749a-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="f749a-124">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="f749a-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




