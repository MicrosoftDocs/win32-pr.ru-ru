---
title: Атрибут ms-DS-ClaimSet-Source
description: Для типа утверждения этот атрибут указывает источник типа утверждения. Например, источником может быть Certificate.
ms.assetid: ec6d8565-e628-47a4-be84-c07b12cd9aec
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-ClaimSet-Source
- Схема AD атрибута msDS-Клаимсаурце
topic_type:
- apiref
api_name:
- ms-DS-Claim-Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90e8668d79e22107cd4338762340e55cc2a60af3
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804702"
---
# <a name="ms-ds-claim-source-attribute"></a><span data-ttu-id="0b8ad-106">Атрибут ms-DS-ClaimSet-Source</span><span class="sxs-lookup"><span data-stu-id="0b8ad-106">ms-DS-Claim-Source attribute</span></span>

<span data-ttu-id="0b8ad-107">Для типа утверждения этот атрибут указывает источник типа утверждения.</span><span class="sxs-lookup"><span data-stu-id="0b8ad-107">For a claim type, this attribute indicates the source of the claim type.</span></span> <span data-ttu-id="0b8ad-108">Например, источником может быть Certificate.</span><span class="sxs-lookup"><span data-stu-id="0b8ad-108">For example, the source can be certificate.</span></span>



| <span data-ttu-id="0b8ad-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b8ad-109">Entry</span></span> | <span data-ttu-id="0b8ad-110">Значение</span><span class="sxs-lookup"><span data-stu-id="0b8ad-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="0b8ad-111">CN</span><span class="sxs-lookup"><span data-stu-id="0b8ad-111">CN</span></span>                | <span data-ttu-id="0b8ad-112">MS-DS-заявка-источник</span><span class="sxs-lookup"><span data-stu-id="0b8ad-112">ms-DS-Claim-Source</span></span>                          |
| <span data-ttu-id="0b8ad-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="0b8ad-113">Ldap-Display-Name</span></span> | <span data-ttu-id="0b8ad-114">msDS-Клаимсаурце</span><span class="sxs-lookup"><span data-stu-id="0b8ad-114">msDS-ClaimSource</span></span>                            |
| <span data-ttu-id="0b8ad-115">Размер</span><span class="sxs-lookup"><span data-stu-id="0b8ad-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="0b8ad-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="0b8ad-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="0b8ad-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="0b8ad-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="0b8ad-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="0b8ad-118">Attribute-Id</span></span>      | <span data-ttu-id="0b8ad-119">1.2.840.113556.1.4.2157</span><span class="sxs-lookup"><span data-stu-id="0b8ad-119">1.2.840.113556.1.4.2157</span></span>                     |
| <span data-ttu-id="0b8ad-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="0b8ad-120">System-Id-Guid</span></span>    | <span data-ttu-id="0b8ad-121">fa32f2a6-f28b-47d0-bf91-663e8f910a72</span><span class="sxs-lookup"><span data-stu-id="0b8ad-121">fa32f2a6-f28b-47d0-bf91-663e8f910a72</span></span>        |
| <span data-ttu-id="0b8ad-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b8ad-122">Syntax</span></span>            | [<span data-ttu-id="0b8ad-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="0b8ad-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="0b8ad-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="0b8ad-124">Implementations</span></span>

-   [<span data-ttu-id="0b8ad-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="0b8ad-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="0b8ad-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b8ad-126">Windows Server 2012</span></span>



| <span data-ttu-id="0b8ad-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="0b8ad-127">Entry</span></span> | <span data-ttu-id="0b8ad-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0b8ad-128">Value</span></span> |
|------------------------|---------------------------------------------------------|
| <span data-ttu-id="0b8ad-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="0b8ad-129">Link-Id</span></span>                | \-                                                      |
| <span data-ttu-id="0b8ad-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="0b8ad-130">MAPI-Id</span></span>                | \-                                                      |
| <span data-ttu-id="0b8ad-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="0b8ad-131">System-Only</span></span>            | <span data-ttu-id="0b8ad-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b8ad-132">False</span></span>                                                   |
| <span data-ttu-id="0b8ad-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="0b8ad-133">Is-Single-Valued</span></span>       | <span data-ttu-id="0b8ad-134">True</span><span class="sxs-lookup"><span data-stu-id="0b8ad-134">True</span></span>                                                    |
| <span data-ttu-id="0b8ad-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="0b8ad-135">Is Indexed</span></span>             | <span data-ttu-id="0b8ad-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b8ad-136">False</span></span>                                                   |
| <span data-ttu-id="0b8ad-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="0b8ad-137">In Global Catalog</span></span>      | <span data-ttu-id="0b8ad-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="0b8ad-138">False</span></span>                                                   |
| <span data-ttu-id="0b8ad-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="0b8ad-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="0b8ad-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="0b8ad-140">O:BAG:BAD:S:</span></span>                                            |
| <span data-ttu-id="0b8ad-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="0b8ad-141">Range-Lower</span></span>            | \-                                                      |
| <span data-ttu-id="0b8ad-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="0b8ad-142">Range-Upper</span></span>            | \-                                                      |
| <span data-ttu-id="0b8ad-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8ad-143">Search-Flags</span></span>           | <span data-ttu-id="0b8ad-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="0b8ad-144">0x00000000</span></span>                                              |
| <span data-ttu-id="0b8ad-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="0b8ad-145">System-Flags</span></span>           | <span data-ttu-id="0b8ad-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="0b8ad-146">0x00000010</span></span>                                              |
| <span data-ttu-id="0b8ad-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="0b8ad-147">Classes used in</span></span>        | [<span data-ttu-id="0b8ad-148">**MS-DS-ClaimSet-тип**</span><span class="sxs-lookup"><span data-stu-id="0b8ad-148">**ms-DS-Claim-Type**</span></span>](c-msds-claimtype.md)<br/> |



 

 





