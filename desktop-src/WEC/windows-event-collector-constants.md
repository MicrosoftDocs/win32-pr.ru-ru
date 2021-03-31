---
title: Константы сборщика событий Windows (Евколл. h)
description: Пакет SDK сборщика событий Windows содержит следующие константы.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800958"
---
# <a name="windows-event-collector-constants"></a><span data-ttu-id="84bd1-103">Константы сборщика событий Windows</span><span class="sxs-lookup"><span data-stu-id="84bd1-103">Windows Event Collector Constants</span></span>

<span data-ttu-id="84bd1-104">Пакет SDK сборщика событий Windows содержит следующие константы.</span><span class="sxs-lookup"><span data-stu-id="84bd1-104">The Windows Event Collector SDK contains the following constants.</span></span>

<dl> <dt>

<span data-ttu-id="84bd1-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ вариантный \_ тип \_ маски**</span><span class="sxs-lookup"><span data-stu-id="84bd1-105"><span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC\_VARIANT\_TYPE\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bd1-106">0x7F</span><span class="sxs-lookup"><span data-stu-id="84bd1-106">0x7f</span></span>
</dt> <dt>



<span data-ttu-id="84bd1-107">Используется для маскирования бита массива из свойства **Type** [**\_ варианта EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) , чтобы извлечь тип значения типа Variant.</span><span class="sxs-lookup"><span data-stu-id="84bd1-107">Used to mask out the array bit from the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) to extract the type of the variant value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84bd1-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC \_ \_ тип Variant \_ массива**</span><span class="sxs-lookup"><span data-stu-id="84bd1-108"><span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC\_VARIANT\_TYPE\_ARRAY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bd1-109">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="84bd1-109">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="84bd1-110">Если этот бит задан в свойстве **Type** [**\_ варианта EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), то объект Variant содержит указатель на массив значений, а не само значение.</span><span class="sxs-lookup"><span data-stu-id="84bd1-110">When this bit is set in the **Type** property of an [**EC\_VARIANT**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), the variant contains a pointer to an array of values, rather than the value itself.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84bd1-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC \_ доступ на чтение \_**</span><span class="sxs-lookup"><span data-stu-id="84bd1-111"><span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**EC\_READ\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bd1-112">1</span><span class="sxs-lookup"><span data-stu-id="84bd1-112">1</span></span>
</dt> <dt>



<span data-ttu-id="84bd1-113">Разрешение на управление доступом на чтение, позволяющее считывать данные из сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="84bd1-113">Read access control permission that allows information to be read from the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84bd1-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_доступ для записи EC \_**</span><span class="sxs-lookup"><span data-stu-id="84bd1-114"><span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**EC\_WRITE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bd1-115">2</span><span class="sxs-lookup"><span data-stu-id="84bd1-115">2</span></span>
</dt> <dt>



<span data-ttu-id="84bd1-116">Разрешение на запись контроля доступа, позволяющее записывать данные в сборщик событий.</span><span class="sxs-lookup"><span data-stu-id="84bd1-116">Write access control permission that allows information to be written to the event collector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84bd1-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ открыть \_ всегда**</span><span class="sxs-lookup"><span data-stu-id="84bd1-117"><span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC\_OPEN\_ALWAYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bd1-118">0</span><span class="sxs-lookup"><span data-stu-id="84bd1-118">0</span></span>
</dt> <dt>



<span data-ttu-id="84bd1-119">Открывает существующую подписку или создает подписку, если она не существует.</span><span class="sxs-lookup"><span data-stu-id="84bd1-119">Opens an existing subscription or creates the subscription if it does not exist.</span></span> <span data-ttu-id="84bd1-120">Используется методом [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .</span><span class="sxs-lookup"><span data-stu-id="84bd1-120">Used by the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84bd1-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ Создание \_ нового**</span><span class="sxs-lookup"><span data-stu-id="84bd1-121"><span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC\_CREATE\_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bd1-122">1</span><span class="sxs-lookup"><span data-stu-id="84bd1-122">1</span></span>
</dt> <dt>



<span data-ttu-id="84bd1-123">Флаг, передаваемый функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) , указывающий, что должна быть создана новая подписка.</span><span class="sxs-lookup"><span data-stu-id="84bd1-123">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that a new subscription should be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84bd1-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ открыть \_ существующий**</span><span class="sxs-lookup"><span data-stu-id="84bd1-124"><span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC\_OPEN\_EXISTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84bd1-125">2</span><span class="sxs-lookup"><span data-stu-id="84bd1-125">2</span></span>
</dt> <dt>



<span data-ttu-id="84bd1-126">Флаг, передаваемый функции [**екопенсубскриптион**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) , указывающий, что должна быть открыта существующая подписка.</span><span class="sxs-lookup"><span data-stu-id="84bd1-126">A flag passed to the [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) function specifying that an existing subscription should be opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84bd1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="84bd1-127">Requirements</span></span>



| <span data-ttu-id="84bd1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="84bd1-128">Requirement</span></span> | <span data-ttu-id="84bd1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="84bd1-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="84bd1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84bd1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84bd1-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84bd1-131">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="84bd1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84bd1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84bd1-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84bd1-133">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="84bd1-134">Header</span><span class="sxs-lookup"><span data-stu-id="84bd1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="84bd1-135"><dt>Евколл. h</dt></span><span class="sxs-lookup"><span data-stu-id="84bd1-135"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





