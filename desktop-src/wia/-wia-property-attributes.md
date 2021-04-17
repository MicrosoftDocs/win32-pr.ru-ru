---
description: Все объекты элементов имеют свойства.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Атрибуты свойств (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497547"
---
# <a name="property-attributes-wia"></a><span data-ttu-id="700ec-103">Атрибуты свойств (WIA)</span><span class="sxs-lookup"><span data-stu-id="700ec-103">Property Attributes (WIA)</span></span>

<span data-ttu-id="700ec-104">Все объекты элементов имеют свойства.</span><span class="sxs-lookup"><span data-stu-id="700ec-104">All item objects have properties.</span></span> <span data-ttu-id="700ec-105">Свойства имеют атрибуты.</span><span class="sxs-lookup"><span data-stu-id="700ec-105">The properties have attributes.</span></span> <span data-ttu-id="700ec-106">Например, атрибуты свойства указывают, считывается ли свойство из, записывается в или удаляется.</span><span class="sxs-lookup"><span data-stu-id="700ec-106">For instance, property attributes indicate whether a property is read from, written to, or deleted.</span></span> <span data-ttu-id="700ec-107">Они также указывают допустимые значения свойств.</span><span class="sxs-lookup"><span data-stu-id="700ec-107">They also indicate the valid property values.</span></span> <span data-ttu-id="700ec-108">Следующие константы являются допустимыми атрибутами свойств:</span><span class="sxs-lookup"><span data-stu-id="700ec-108">The following constants are valid property attributes:</span></span> 

| <span data-ttu-id="700ec-109">Атрибут свойства</span><span class="sxs-lookup"><span data-stu-id="700ec-109">Property Attribute</span></span>        | <span data-ttu-id="700ec-110">Значение</span><span class="sxs-lookup"><span data-stu-id="700ec-110">Meaning</span></span>                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="700ec-111">\_ \_ кэширование свойства WIA</span><span class="sxs-lookup"><span data-stu-id="700ec-111">WIA\_PROP\_CACHEABLE</span></span>      | <span data-ttu-id="700ec-112">Устройство может кэшировать значение свойства.</span><span class="sxs-lookup"><span data-stu-id="700ec-112">The device can cache the property's value.</span></span>                                                               |
| <span data-ttu-id="700ec-113">\_флаг prop для WIA \_</span><span class="sxs-lookup"><span data-stu-id="700ec-113">WIA\_PROP\_FLAG</span></span>           | <span data-ttu-id="700ec-114">Свойство содержит список допустимых значений флагов.</span><span class="sxs-lookup"><span data-stu-id="700ec-114">The property has a list of legal flag values.</span></span> <span data-ttu-id="700ec-115">Значения флагов объединяются с помощью побитовой операции **или** .</span><span class="sxs-lookup"><span data-stu-id="700ec-115">Flag values are combined using a bitwise **OR** operation.</span></span> |
| <span data-ttu-id="700ec-116">\_список свойств \_ WIA</span><span class="sxs-lookup"><span data-stu-id="700ec-116">WIA\_PROP\_LIST</span></span>           | <span data-ttu-id="700ec-117">Свойство содержит список допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="700ec-117">The property has a list of legal values.</span></span>                                                                 |
| <span data-ttu-id="700ec-118">WIA \_ prop \_ None</span><span class="sxs-lookup"><span data-stu-id="700ec-118">WIA\_PROP\_NONE</span></span>           | <span data-ttu-id="700ec-119">С этим свойством не связаны допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="700ec-119">The property does not have any valid values associated with it.</span></span>                                          |
| <span data-ttu-id="700ec-120">\_диапазон prop для WIA \_</span><span class="sxs-lookup"><span data-stu-id="700ec-120">WIA\_PROP\_RANGE</span></span>          | <span data-ttu-id="700ec-121">Свойство имеет диапазон допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="700ec-121">The property has a range of valid values.</span></span>                                                                |
| <span data-ttu-id="700ec-122">чтение свойства "WIA" \_ \_</span><span class="sxs-lookup"><span data-stu-id="700ec-122">WIA\_PROP\_READ</span></span>           | <span data-ttu-id="700ec-123">Приложение может считывать значение свойства.</span><span class="sxs-lookup"><span data-stu-id="700ec-123">The application can read the property's value.</span></span>                                                           |
| <span data-ttu-id="700ec-124">WIA \_ prop \_ RW</span><span class="sxs-lookup"><span data-stu-id="700ec-124">WIA\_PROP\_RW</span></span>             | <span data-ttu-id="700ec-125">Приложение может считывать и записывать значение свойства.</span><span class="sxs-lookup"><span data-stu-id="700ec-125">The application can read and write the property's value.</span></span>                                                 |
| <span data-ttu-id="700ec-126">\_ \_ требуется синхронизация свойства "WIA" \_</span><span class="sxs-lookup"><span data-stu-id="700ec-126">WIA\_PROP\_SYNC\_REQUIRED</span></span> | <span data-ttu-id="700ec-127">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="700ec-127">Do not use.</span></span>                                                                                              |
| <span data-ttu-id="700ec-128">запись свойства "WIA \_ prop" \_</span><span class="sxs-lookup"><span data-stu-id="700ec-128">WIA\_PROP\_WRITE</span></span>          | <span data-ttu-id="700ec-129">Приложение может записать значение свойства.</span><span class="sxs-lookup"><span data-stu-id="700ec-129">The application can write the property's value.</span></span>                                                          |



 

 

 



