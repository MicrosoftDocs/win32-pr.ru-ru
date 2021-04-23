---
description: Указывает компромисс между движениями и по-прежнему образами. Это свойство применяется только к режиму управления постоянной скоростью (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Свойство Авенквидеокбрмотионтрадеофф (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103990220"
---
# <a name="avencvideocbrmotiontradeoff-property"></a><span data-ttu-id="6b8da-104">Авенквидеокбрмотионтрадеофф, свойство</span><span class="sxs-lookup"><span data-stu-id="6b8da-104">AVEncVideoCBRMotionTradeoff property</span></span>

<span data-ttu-id="6b8da-105">Указывает компромисс между движениями и по-прежнему образами.</span><span class="sxs-lookup"><span data-stu-id="6b8da-105">Specifies the tradeoff between motion and still images.</span></span> <span data-ttu-id="6b8da-106">Это свойство применяется только к режиму управления постоянной скоростью (CBR).</span><span class="sxs-lookup"><span data-stu-id="6b8da-106">This property applies only to constant bit rate (CBR) control mode.</span></span>

<span data-ttu-id="6b8da-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6b8da-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b8da-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6b8da-108">Data type</span></span>

<span data-ttu-id="6b8da-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="6b8da-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6b8da-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="6b8da-110">Property GUID</span></span>

<span data-ttu-id="6b8da-111">**КОДЕКАПИ \_ авенквидеокбрмотионтрадеофф**</span><span class="sxs-lookup"><span data-stu-id="6b8da-111">**CODECAPI\_AVEncVideoCBRMotionTradeoff**</span></span>

## <a name="property-value"></a><span data-ttu-id="6b8da-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6b8da-112">Property value</span></span>

<span data-ttu-id="6b8da-113">Значение этого свойства имеет следующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="6b8da-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="6b8da-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6b8da-114">Value</span></span> | <span data-ttu-id="6b8da-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6b8da-115">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="6b8da-116">0</span><span class="sxs-lookup"><span data-stu-id="6b8da-116">0</span></span>     | <span data-ttu-id="6b8da-117">Оптимизировать для изображений по-прежнему</span><span class="sxs-lookup"><span data-stu-id="6b8da-117">Optimize for still images</span></span> |
| <span data-ttu-id="6b8da-118">100</span><span class="sxs-lookup"><span data-stu-id="6b8da-118">100</span></span>   | <span data-ttu-id="6b8da-119">Оптимизировать для движения.</span><span class="sxs-lookup"><span data-stu-id="6b8da-119">Optimize for motion.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="6b8da-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6b8da-120">Requirements</span></span>



| <span data-ttu-id="6b8da-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6b8da-121">Requirement</span></span> | <span data-ttu-id="6b8da-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6b8da-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8da-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b8da-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8da-124">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6b8da-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="6b8da-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b8da-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8da-126">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="6b8da-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6b8da-127">Header</span><span class="sxs-lookup"><span data-stu-id="6b8da-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b8da-128"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8da-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8da-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b8da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8da-130">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="6b8da-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="6b8da-131">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="6b8da-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




