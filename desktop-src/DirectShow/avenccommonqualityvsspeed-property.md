---
description: Задает компромисс между качеством и скоростью кодирования. Это свойство допустимо во всех режимах управления скоростью.
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: Свойство Авенккоммонкуалитивсспид (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140482"
---
# <a name="avenccommonqualityvsspeed-property"></a><span data-ttu-id="d46d6-104">Авенккоммонкуалитивсспид, свойство</span><span class="sxs-lookup"><span data-stu-id="d46d6-104">AVEncCommonQualityVsSpeed property</span></span>

<span data-ttu-id="d46d6-105">Задает компромисс между качеством и скоростью кодирования.</span><span class="sxs-lookup"><span data-stu-id="d46d6-105">Specifies the tradeoff between encoding quality and speed.</span></span> <span data-ttu-id="d46d6-106">Это свойство допустимо во всех режимах управления скоростью.</span><span class="sxs-lookup"><span data-stu-id="d46d6-106">This property is valid in all rate control modes.</span></span>

<span data-ttu-id="d46d6-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d46d6-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="d46d6-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d46d6-108">Data type</span></span>

<span data-ttu-id="d46d6-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d46d6-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d46d6-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="d46d6-110">Property GUID</span></span>

<span data-ttu-id="d46d6-111">**КОДЕКАПИ \_ авенккоммонкуалитивсспид**</span><span class="sxs-lookup"><span data-stu-id="d46d6-111">**CODECAPI\_AVEncCommonQualityVsSpeed**</span></span>

## <a name="property-value"></a><span data-ttu-id="d46d6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d46d6-112">Property value</span></span>

<span data-ttu-id="d46d6-113">Значение этого свойства имеет следующий диапазон.</span><span class="sxs-lookup"><span data-stu-id="d46d6-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="d46d6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d46d6-114">Value</span></span> | <span data-ttu-id="d46d6-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d46d6-115">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="d46d6-116">0</span><span class="sxs-lookup"><span data-stu-id="d46d6-116">0</span></span>     | <span data-ttu-id="d46d6-117">Более низкое качество, более быстрая кодировка.</span><span class="sxs-lookup"><span data-stu-id="d46d6-117">Lower quality, faster encoding.</span></span>  |
| <span data-ttu-id="d46d6-118">100</span><span class="sxs-lookup"><span data-stu-id="d46d6-118">100</span></span>   | <span data-ttu-id="d46d6-119">Более высокое качество, медленная кодировка.</span><span class="sxs-lookup"><span data-stu-id="d46d6-119">Higher quality, slower encoding.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d46d6-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d46d6-120">Requirements</span></span>



| <span data-ttu-id="d46d6-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d46d6-121">Requirement</span></span> | <span data-ttu-id="d46d6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d46d6-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d46d6-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d46d6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d46d6-124">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d46d6-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d46d6-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d46d6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d46d6-126">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="d46d6-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d46d6-127">Header</span><span class="sxs-lookup"><span data-stu-id="d46d6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d46d6-128"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d46d6-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d46d6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d46d6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d46d6-130">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="d46d6-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d46d6-131">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="d46d6-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




