---
title: MS-DS-заявка-имеет значение, ограниченное пространством, атрибутом
description: Для типа утверждения этот атрибут определяет, может ли пользователь вводить значения, отличные от описанных в msDS-Клаимпоссиблевалуес в приложениях.
ms.assetid: 6a965b2f-ab3f-4429-8e2d-2fc21eefbb5e
ms.tgt_platform: multiple
keywords:
- MS-DS-заявка — это схема AD атрибута с ограниченным пространством значений
- Схема AD атрибута msDS-Клаимисвалуеспацерестриктед
topic_type:
- apiref
api_name:
- ms-DS-Claim-Is-Value-Space-Restricted
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b4ea4e81033d7f4ce889bf7fd593c91f8bb2b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655201"
---
# <a name="ms-ds-claim-is-value-space-restricted-attribute"></a><span data-ttu-id="9ab7b-105">MS-DS-заявка-имеет значение, ограниченное пространством, атрибутом</span><span class="sxs-lookup"><span data-stu-id="9ab7b-105">ms-DS-Claim-Is-Value-Space-Restricted attribute</span></span>

<span data-ttu-id="9ab7b-106">Для типа утверждения этот атрибут определяет, может ли пользователь вводить значения, отличные от описанных в msDS-Клаимпоссиблевалуес в приложениях.</span><span class="sxs-lookup"><span data-stu-id="9ab7b-106">For a claim type, this attribute identifies whether a user can input values other than those described in the msDS-ClaimPossibleValues in applications.</span></span>



| <span data-ttu-id="9ab7b-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab7b-107">Entry</span></span> | <span data-ttu-id="9ab7b-108">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab7b-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="9ab7b-109">CN</span><span class="sxs-lookup"><span data-stu-id="9ab7b-109">CN</span></span>                | <span data-ttu-id="9ab7b-110">MS-DS-заявка--"-значение-пространство — ограничено"</span><span class="sxs-lookup"><span data-stu-id="9ab7b-110">ms-DS-Claim-Is-Value-Space-Restricted</span></span> |
| <span data-ttu-id="9ab7b-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9ab7b-111">Ldap-Display-Name</span></span> | <span data-ttu-id="9ab7b-112">msDS-Клаимисвалуеспацерестриктед</span><span class="sxs-lookup"><span data-stu-id="9ab7b-112">msDS-ClaimIsValueSpaceRestricted</span></span>      |
| <span data-ttu-id="9ab7b-113">Размер</span><span class="sxs-lookup"><span data-stu-id="9ab7b-113">Size</span></span>              | \-                                    |
| <span data-ttu-id="9ab7b-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9ab7b-114">Update Privilege</span></span>  | \-                                    |
| <span data-ttu-id="9ab7b-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9ab7b-115">Update Frequency</span></span>  | \-                                    |
| <span data-ttu-id="9ab7b-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ab7b-116">Attribute-Id</span></span>      | <span data-ttu-id="9ab7b-117">1.2.840.113556.1.4.2159</span><span class="sxs-lookup"><span data-stu-id="9ab7b-117">1.2.840.113556.1.4.2159</span></span>               |
| <span data-ttu-id="9ab7b-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9ab7b-118">System-Id-Guid</span></span>    | <span data-ttu-id="9ab7b-119">0c2ce4c7-f1c3-4482-8578-c60d4bb74422</span><span class="sxs-lookup"><span data-stu-id="9ab7b-119">0c2ce4c7-f1c3-4482-8578-c60d4bb74422</span></span>  |
| <span data-ttu-id="9ab7b-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ab7b-120">Syntax</span></span>            | [<span data-ttu-id="9ab7b-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="9ab7b-121">**Boolean**</span></span>](s-boolean.md)          |



## <a name="implementations"></a><span data-ttu-id="9ab7b-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9ab7b-122">Implementations</span></span>

-   [<span data-ttu-id="9ab7b-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ab7b-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="9ab7b-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ab7b-124">Windows Server 2012</span></span>



| <span data-ttu-id="9ab7b-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ab7b-125">Entry</span></span> | <span data-ttu-id="9ab7b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab7b-126">Value</span></span> |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab7b-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ab7b-127">Link-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="9ab7b-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ab7b-128">MAPI-Id</span></span>                | \-                                                                                                              |
| <span data-ttu-id="9ab7b-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ab7b-129">System-Only</span></span>            | <span data-ttu-id="9ab7b-130">True</span><span class="sxs-lookup"><span data-stu-id="9ab7b-130">True</span></span>                                                                                                            |
| <span data-ttu-id="9ab7b-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ab7b-131">Is-Single-Valued</span></span>       | <span data-ttu-id="9ab7b-132">True</span><span class="sxs-lookup"><span data-stu-id="9ab7b-132">True</span></span>                                                                                                            |
| <span data-ttu-id="9ab7b-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ab7b-133">Is Indexed</span></span>             | <span data-ttu-id="9ab7b-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab7b-134">False</span></span>                                                                                                           |
| <span data-ttu-id="9ab7b-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ab7b-135">In Global Catalog</span></span>      | <span data-ttu-id="9ab7b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ab7b-136">False</span></span>                                                                                                           |
| <span data-ttu-id="9ab7b-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ab7b-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ab7b-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ab7b-138">O:BAG:BAD:S:</span></span>                                                                                                    |
| <span data-ttu-id="9ab7b-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ab7b-139">Range-Lower</span></span>            | \-                                                                                                              |
| <span data-ttu-id="9ab7b-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ab7b-140">Range-Upper</span></span>            | \-                                                                                                              |
| <span data-ttu-id="9ab7b-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab7b-141">Search-Flags</span></span>           | <span data-ttu-id="9ab7b-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9ab7b-142">0x00000000</span></span>                                                                                                      |
| <span data-ttu-id="9ab7b-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ab7b-143">System-Flags</span></span>           | <span data-ttu-id="9ab7b-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ab7b-144">0x00000010</span></span>                                                                                                      |
| <span data-ttu-id="9ab7b-145">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ab7b-145">Classes used in</span></span>        | [<span data-ttu-id="9ab7b-146">**MS-DS-ClaimSet-тип**</span><span class="sxs-lookup"><span data-stu-id="9ab7b-146">**ms-DS-Claim-Type**</span></span>](c-msds-claimtype.md)<br/> [<span data-ttu-id="9ab7b-147">**MS-DS-value-type**</span><span class="sxs-lookup"><span data-stu-id="9ab7b-147">**ms-DS-Value-Type**</span></span>](c-msds-valuetype.md)<br/> |



 

 





