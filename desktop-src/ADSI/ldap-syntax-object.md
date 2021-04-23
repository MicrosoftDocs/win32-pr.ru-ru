---
title: Объект синтаксиса LDAP
description: Поставщик LDAP использует следующее сопоставление между синтаксисом LDAP и синтаксисом ADSI.
ms.assetid: a82cf8ab-9591-4489-87a6-ccfab0e01d61
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, поставщики служб, сопоставление синтаксиса с синтаксисом LDAP
- Сопоставление синтаксиса ADSI с синтаксисом LDAP в ADSI
- синтаксис и сопоставление из ADSI с LDAP ADSI
- Поставщик служб LDAP ADSI, сопоставление синтаксиса ADSI с синтаксисом LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2272a0805ec32fd7ade9c4584feefb64fb1467f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132802"
---
# <a name="ldap-syntax-object"></a><span data-ttu-id="7c772-107">Объект синтаксиса LDAP</span><span class="sxs-lookup"><span data-stu-id="7c772-107">LDAP Syntax Object</span></span>

<span data-ttu-id="7c772-108">Поставщик LDAP использует следующее сопоставление между синтаксисом LDAP и синтаксисом ADSI.</span><span class="sxs-lookup"><span data-stu-id="7c772-108">The LDAP provider uses the following mapping between the LDAP syntax and ADSI syntax.</span></span>



| <span data-ttu-id="7c772-109">Синтаксис LDAP</span><span class="sxs-lookup"><span data-stu-id="7c772-109">LDAP Syntax</span></span>   | <span data-ttu-id="7c772-110">Синтаксис ADSI (автоматизация)</span><span class="sxs-lookup"><span data-stu-id="7c772-110">ADSI Syntax (Automation)</span></span>            |
|---------------|-------------------------------------|
| <span data-ttu-id="7c772-111">Действитель</span><span class="sxs-lookup"><span data-stu-id="7c772-111">ADsPath</span></span>       | <span data-ttu-id="7c772-112">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-112">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="7c772-113">Boolean</span></span>       | <span data-ttu-id="7c772-114">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="7c772-114">VT\_BOOL</span></span>                            |
| <span data-ttu-id="7c772-115">Счетчик</span><span class="sxs-lookup"><span data-stu-id="7c772-115">Counter</span></span>       | <span data-ttu-id="7c772-116">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7c772-116">VT\_I4</span></span>                              |
| <span data-ttu-id="7c772-117">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7c772-117">EmailAddress</span></span>  | <span data-ttu-id="7c772-118">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-118">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-119">факснумбер</span><span class="sxs-lookup"><span data-stu-id="7c772-119">FaxNumber</span></span>     | <span data-ttu-id="7c772-120">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-120">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-121">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="7c772-121">Integer</span></span>       | <span data-ttu-id="7c772-122">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7c772-122">VT\_I4</span></span>                              |
| <span data-ttu-id="7c772-123">Интервал</span><span class="sxs-lookup"><span data-stu-id="7c772-123">Interval</span></span>      | <span data-ttu-id="7c772-124">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7c772-124">VT\_I4</span></span>                              |
| <span data-ttu-id="7c772-125">Список</span><span class="sxs-lookup"><span data-stu-id="7c772-125">List</span></span>          | <span data-ttu-id="7c772-126">VT \_ Variant ( \_ массив VT \| BSTR \_ )</span><span class="sxs-lookup"><span data-stu-id="7c772-126">VT\_VARIANT (VT\_BSTR \| VT\_ARRAY)</span></span> |
| <span data-ttu-id="7c772-127">нетаддресс</span><span class="sxs-lookup"><span data-stu-id="7c772-127">NetAddress</span></span>    | <span data-ttu-id="7c772-128">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-128">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-129">октетстринг</span><span class="sxs-lookup"><span data-stu-id="7c772-129">OctetString</span></span>   | <span data-ttu-id="7c772-130">\_вариант VT</span><span class="sxs-lookup"><span data-stu-id="7c772-130">VT\_VARIANT</span></span>                         |
| <span data-ttu-id="7c772-131">Путь</span><span class="sxs-lookup"><span data-stu-id="7c772-131">Path</span></span>          | <span data-ttu-id="7c772-132">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-132">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-133">PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="7c772-133">PhoneNumber</span></span>   | <span data-ttu-id="7c772-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-134">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-135">PostalAddress</span><span class="sxs-lookup"><span data-stu-id="7c772-135">PostalAddress</span></span> | <span data-ttu-id="7c772-136">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-136">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-137">смаллинтервал</span><span class="sxs-lookup"><span data-stu-id="7c772-137">SmallInterval</span></span> | <span data-ttu-id="7c772-138">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7c772-138">VT\_I4</span></span>                              |
| <span data-ttu-id="7c772-139">Строка</span><span class="sxs-lookup"><span data-stu-id="7c772-139">String</span></span>        | <span data-ttu-id="7c772-140">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="7c772-140">VT\_BSTR</span></span>                            |
| <span data-ttu-id="7c772-141">Время</span><span class="sxs-lookup"><span data-stu-id="7c772-141">Time</span></span>          | <span data-ttu-id="7c772-142">\_Дата VT</span><span class="sxs-lookup"><span data-stu-id="7c772-142">VT\_DATE</span></span>                            |



 

 

 




