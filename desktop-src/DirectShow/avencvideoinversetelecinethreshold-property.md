---
description: Задает пороговое значение, при котором кодировщик считает поле видео избыточным.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Свойство АвенквидеоинверсетелеЦинесрешолд (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805393"
---
# <a name="avencvideoinversetelecinethreshold-property"></a><span data-ttu-id="3ee7d-103">АвенквидеоинверсетелеЦинесрешолд, свойство</span><span class="sxs-lookup"><span data-stu-id="3ee7d-103">AVEncVideoInverseTelecineThreshold property</span></span>

<span data-ttu-id="3ee7d-104">Задает пороговое значение, при котором кодировщик считает поле видео избыточным.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-104">Sets the threshold at which the encoder considers a video field redundant.</span></span>

<span data-ttu-id="3ee7d-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ee7d-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3ee7d-106">Data type</span></span>

<span data-ttu-id="3ee7d-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="3ee7d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3ee7d-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="3ee7d-108">Property GUID</span></span>

<span data-ttu-id="3ee7d-109">**КОДЕКАПИ \_ авенквидеоинверсетелеЦинесрешолд**</span><span class="sxs-lookup"><span data-stu-id="3ee7d-109">**CODECAPI\_AVEncVideoInverseTelecineThreshold**</span></span>

## <a name="property-value"></a><span data-ttu-id="3ee7d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3ee7d-110">Property value</span></span>

<span data-ttu-id="3ee7d-111">Значение этого свойства имеет следующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="3ee7d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="3ee7d-112">Value</span></span> | <span data-ttu-id="3ee7d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="3ee7d-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="3ee7d-114">0</span><span class="sxs-lookup"><span data-stu-id="3ee7d-114">0</span></span>     | <span data-ttu-id="3ee7d-115">Менее вероятно, что кодировщику следует считать поля видео избыточными.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-115">The encoder is less likely to consider video fields redundant.</span></span> |
| <span data-ttu-id="3ee7d-116">100</span><span class="sxs-lookup"><span data-stu-id="3ee7d-116">100</span></span>   | <span data-ttu-id="3ee7d-117">Более вероятно, что кодировщик может считать поля видео избыточными.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-117">The encoder is more likely to consider video fields redundant.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3ee7d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ee7d-118">Remarks</span></span>

<span data-ttu-id="3ee7d-119">Задайте это свойство, если кодировщик выполняет обратную чересстрочности с аналоговым источником видео.</span><span class="sxs-lookup"><span data-stu-id="3ee7d-119">Set this property if the encoder is performing inverse telecine with an analog video source.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ee7d-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3ee7d-120">Requirements</span></span>



| <span data-ttu-id="3ee7d-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3ee7d-121">Requirement</span></span> | <span data-ttu-id="3ee7d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3ee7d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee7d-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ee7d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee7d-124">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3ee7d-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3ee7d-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ee7d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee7d-126">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="3ee7d-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3ee7d-127">Header</span><span class="sxs-lookup"><span data-stu-id="3ee7d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ee7d-128"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ee7d-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ee7d-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ee7d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee7d-130">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="3ee7d-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3ee7d-131">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="3ee7d-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




