---
description: Помечает текущий кадр как кадр слева.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: Свойство CODECAPI_AVEncVideoMarkLTRFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539623"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a><span data-ttu-id="8c837-103">КОДЕКАПИ \_ авенквидеомарклтрфраме, свойство</span><span class="sxs-lookup"><span data-stu-id="8c837-103">CODECAPI\_AVEncVideoMarkLTRFrame property</span></span>

<span data-ttu-id="8c837-104">Помечает текущий кадр как кадр слева.</span><span class="sxs-lookup"><span data-stu-id="8c837-104">Marks the current frame as a LTR frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c837-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8c837-105">Data type</span></span>

<span data-ttu-id="8c837-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="8c837-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8c837-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="8c837-107">Property GUID</span></span>

<span data-ttu-id="8c837-108">**КОДЕКАПИ \_ авенквидеомарклтрфраме**</span><span class="sxs-lookup"><span data-stu-id="8c837-108">**CODECAPI\_AVEncVideoMarkLTRFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="8c837-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c837-109">Remarks</span></span>

<span data-ttu-id="8c837-110">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="8c837-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="8c837-111">Значением этого элемента управления является значение 264 синтаксиса H. *лонгтермфрамидкс* , связанное с текущим кадром.</span><span class="sxs-lookup"><span data-stu-id="8c837-111">The value of this control is the value of H.264 syntax *LongTermFramIdx* associated with the current frame.</span></span> <span data-ttu-id="8c837-112">Если текущий кадр не находится на базовом уровне, например, *темпоральный \_ идентификатор* элемента синтаксиса не равен 0, это свойство применяется к следующему базовому кадру слоя в порядке кодировки.</span><span class="sxs-lookup"><span data-stu-id="8c837-112">If the current frame is not in the base layer, for example syntax element *temporal\_id* is not equal to 0, this property applies to the next base layer frame in encoding order.</span></span>

<span data-ttu-id="8c837-113">Это свойство не должно вызываться, если отложенный вызов, помечающий кадр LTR, был выдан с помощью \_ Свойства кодекапи авенквидеомарклтрфраме, а кодировщик еще не пометил кадр как LTR.</span><span class="sxs-lookup"><span data-stu-id="8c837-113">This property should not be called if a pending call to mark an LTR frame has been issued using the CODECAPI\_AVEncVideoMarkLTRFrame property and the encoder has not yet marked a frame as LTR.</span></span> <span data-ttu-id="8c837-114">Иными словами, кодировщик не должен ставить в очередь запросы КОДЕКАПИ \_ авенквидеомарклтрфраме.</span><span class="sxs-lookup"><span data-stu-id="8c837-114">In other words, the encoder should not queue up CODECAPI\_AVEncVideoMarkLTRFrame requests.</span></span> <span data-ttu-id="8c837-115">Если запрос КОДЕКАПИ \_ авенквидеомарклтрфраме отправляется в то время, когда другой \_ запрос кодекапи авенквидеомарклтрфраме все еще находится в состоянии ожидания, старый запрос следует удалить.</span><span class="sxs-lookup"><span data-stu-id="8c837-115">If a CODECAPI\_AVEncVideoMarkLTRFrame request is submitted while another CODECAPI\_AVEncVideoMarkLTRFrame request is still pending, the older request should be dropped.</span></span>

<span data-ttu-id="8c837-116">Свойство КОДЕКАПИ \_ авенквидеомарклтрфраме является динамическим и может быть задано во время сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="8c837-116">The CODECAPI\_AVEncVideoMarkLTRFrame property is dynamic and can be set during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c837-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8c837-117">Requirements</span></span>



| <span data-ttu-id="8c837-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8c837-118">Requirement</span></span> | <span data-ttu-id="8c837-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8c837-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c837-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c837-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c837-121">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="8c837-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="8c837-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c837-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c837-123">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="8c837-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="8c837-124">Header</span><span class="sxs-lookup"><span data-stu-id="8c837-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c837-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c837-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c837-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c837-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c837-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c837-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




