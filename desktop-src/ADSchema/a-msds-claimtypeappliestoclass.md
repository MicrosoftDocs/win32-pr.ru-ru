---
title: атрибут применения MS-DS-ClaimSet-Type-to-Class
description: Для объекта типа утверждения этот связанный атрибут указывает на классы субъектов безопасности Active Directory, для которых должны выдаваться утверждения. (Например, ссылка на класс пользователя).
ms.assetid: 2323b120-c7b4-41ea-a04f-5791d6b55813
ms.tgt_platform: multiple
keywords:
- AD-DS-заявка-тип — применение схемы Active Directory к атрибуту
- Схема AD атрибута msDS-Клаимтипеапплиестокласс
topic_type:
- apiref
api_name:
- ms-DS-Claim-Type-Applies-To-Class
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72b5d440b492f5a9b120420bddba31375aec877b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655197"
---
# <a name="ms-ds-claim-type-applies-to-class-attribute"></a><span data-ttu-id="6ee13-106">атрибут применения MS-DS-ClaimSet-Type-to-Class</span><span class="sxs-lookup"><span data-stu-id="6ee13-106">ms-DS-Claim-Type-Applies-To-Class attribute</span></span>

<span data-ttu-id="6ee13-107">Для объекта типа утверждения этот связанный атрибут указывает на классы субъектов безопасности Active Directory, для которых должны выдаваться утверждения.</span><span class="sxs-lookup"><span data-stu-id="6ee13-107">For a claim type object, this linked attribute points to the AD security principal classes that for which claims should be issued.</span></span> <span data-ttu-id="6ee13-108">(Например, ссылка на класс пользователя).</span><span class="sxs-lookup"><span data-stu-id="6ee13-108">(For example, a link to the user class).</span></span>



| <span data-ttu-id="6ee13-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="6ee13-109">Entry</span></span> | <span data-ttu-id="6ee13-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6ee13-110">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="6ee13-111">CN</span><span class="sxs-lookup"><span data-stu-id="6ee13-111">CN</span></span>                | <span data-ttu-id="6ee13-112">MS-DS-заявка-тип — применяется к классу</span><span class="sxs-lookup"><span data-stu-id="6ee13-112">ms-DS-Claim-Type-Applies-To-Class</span></span>       |
| <span data-ttu-id="6ee13-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="6ee13-113">Ldap-Display-Name</span></span> | <span data-ttu-id="6ee13-114">msDS-Клаимтипеапплиестокласс</span><span class="sxs-lookup"><span data-stu-id="6ee13-114">msDS-ClaimTypeAppliesToClass</span></span>            |
| <span data-ttu-id="6ee13-115">Размер</span><span class="sxs-lookup"><span data-stu-id="6ee13-115">Size</span></span>              | \-                                      |
| <span data-ttu-id="6ee13-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="6ee13-116">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="6ee13-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="6ee13-117">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="6ee13-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6ee13-118">Attribute-Id</span></span>      | <span data-ttu-id="6ee13-119">1.2.840.113556.1.4.2100</span><span class="sxs-lookup"><span data-stu-id="6ee13-119">1.2.840.113556.1.4.2100</span></span>                 |
| <span data-ttu-id="6ee13-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="6ee13-120">System-Id-Guid</span></span>    | <span data-ttu-id="6ee13-121">6afb0e4c-d876-437c-aeb6-c3e41454c272</span><span class="sxs-lookup"><span data-stu-id="6ee13-121">6afb0e4c-d876-437c-aeb6-c3e41454c272</span></span>    |
| <span data-ttu-id="6ee13-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6ee13-122">Syntax</span></span>            | [<span data-ttu-id="6ee13-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="6ee13-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="6ee13-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="6ee13-124">Implementations</span></span>

-   [<span data-ttu-id="6ee13-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="6ee13-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="6ee13-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6ee13-126">Windows Server 2012</span></span>



| <span data-ttu-id="6ee13-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="6ee13-127">Entry</span></span> | <span data-ttu-id="6ee13-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6ee13-128">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="6ee13-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="6ee13-129">Link-Id</span></span>                | <span data-ttu-id="6ee13-130">2176</span><span class="sxs-lookup"><span data-stu-id="6ee13-130">2176</span></span>                                                    |
| <span data-ttu-id="6ee13-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6ee13-131">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="6ee13-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="6ee13-132">System-Only</span></span>            | <span data-ttu-id="6ee13-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="6ee13-133">False</span></span>                                                   |
| <span data-ttu-id="6ee13-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="6ee13-134">Is-Single-Valued</span></span>       | <span data-ttu-id="6ee13-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="6ee13-135">False</span></span>                                                   |
| <span data-ttu-id="6ee13-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="6ee13-136">Is Indexed</span></span>             | <span data-ttu-id="6ee13-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="6ee13-137">False</span></span>                                                   |
| <span data-ttu-id="6ee13-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="6ee13-138">In Global Catalog</span></span>      | <span data-ttu-id="6ee13-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="6ee13-139">False</span></span>                                                   |
| <span data-ttu-id="6ee13-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="6ee13-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="6ee13-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="6ee13-141">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="6ee13-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6ee13-142">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="6ee13-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6ee13-143">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="6ee13-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee13-144">Search-Flags</span></span>           | <span data-ttu-id="6ee13-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6ee13-145">0x00000000</span></span>                                              |
| <span data-ttu-id="6ee13-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6ee13-146">System-Flags</span></span>           | <span data-ttu-id="6ee13-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6ee13-147">0x00000010</span></span>                                              |
| <span data-ttu-id="6ee13-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="6ee13-148">Classes used in</span></span>        | [<span data-ttu-id="6ee13-149">**MS-DS-ClaimSet-тип**</span><span class="sxs-lookup"><span data-stu-id="6ee13-149">**ms-DS-Claim-Type**</span></span>](c-msds-claimtype.md)<br/> |



 

 





