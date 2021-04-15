---
title: MS-authz-эффективные-безопасность-атрибут политики
description: Для централизованного правила доступа этот атрибут определяет разрешение, которое применяется к целевым ресурсам в централизованном правиле доступа.
ms.assetid: 0b7e14b7-9f5d-4437-a0a7-a6ec329c4f80
ms.tgt_platform: multiple
keywords:
- MS-authz-эффективные-безопасность — схема AD атрибута политики
- Схема AD атрибута Мсаусз-Еффективесекуритиполици
topic_type:
- apiref
api_name:
- ms-Authz-Effective-Security-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c78d6e3cb23c16f289fc280f07a3a4418d5383
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654892"
---
# <a name="ms-authz-effective-security-policy-attribute"></a><span data-ttu-id="66ddb-105">MS-authz-эффективные-безопасность-атрибут политики</span><span class="sxs-lookup"><span data-stu-id="66ddb-105">ms-Authz-Effective-Security-Policy attribute</span></span>

<span data-ttu-id="66ddb-106">Для централизованного правила доступа этот атрибут определяет разрешение, которое применяется к целевым ресурсам в централизованном правиле доступа.</span><span class="sxs-lookup"><span data-stu-id="66ddb-106">For a central access rule, this attribute defines the permission that is applying to the target resources on the central access rule.</span></span>



| <span data-ttu-id="66ddb-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="66ddb-107">Entry</span></span> | <span data-ttu-id="66ddb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="66ddb-108">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="66ddb-109">CN</span><span class="sxs-lookup"><span data-stu-id="66ddb-109">CN</span></span>                | <span data-ttu-id="66ddb-110">MS-authz-эффективные-безопасность — политика</span><span class="sxs-lookup"><span data-stu-id="66ddb-110">ms-Authz-Effective-Security-Policy</span></span>          |
| <span data-ttu-id="66ddb-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="66ddb-111">Ldap-Display-Name</span></span> | <span data-ttu-id="66ddb-112">Мсаусз — Еффективесекуритиполици</span><span class="sxs-lookup"><span data-stu-id="66ddb-112">msAuthz-EffectiveSecurityPolicy</span></span>             |
| <span data-ttu-id="66ddb-113">Размер</span><span class="sxs-lookup"><span data-stu-id="66ddb-113">Size</span></span>              | \-                                          |
| <span data-ttu-id="66ddb-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="66ddb-114">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="66ddb-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="66ddb-115">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="66ddb-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="66ddb-116">Attribute-Id</span></span>      | <span data-ttu-id="66ddb-117">1.2.840.113556.1.4.2150</span><span class="sxs-lookup"><span data-stu-id="66ddb-117">1.2.840.113556.1.4.2150</span></span>                     |
| <span data-ttu-id="66ddb-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="66ddb-118">System-Id-Guid</span></span>    | <span data-ttu-id="66ddb-119">07831919-8f94-4fb6-8a42-91545dccdad3</span><span class="sxs-lookup"><span data-stu-id="66ddb-119">07831919-8f94-4fb6-8a42-91545dccdad3</span></span>        |
| <span data-ttu-id="66ddb-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66ddb-120">Syntax</span></span>            | [<span data-ttu-id="66ddb-121">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="66ddb-121">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="66ddb-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="66ddb-122">Implementations</span></span>

-   [<span data-ttu-id="66ddb-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="66ddb-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="66ddb-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66ddb-124">Windows Server 2012</span></span>



| <span data-ttu-id="66ddb-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="66ddb-125">Entry</span></span> | <span data-ttu-id="66ddb-126">Значение</span><span class="sxs-lookup"><span data-stu-id="66ddb-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="66ddb-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="66ddb-127">Link-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="66ddb-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="66ddb-128">MAPI-Id</span></span>                | \-                                                                             |
| <span data-ttu-id="66ddb-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="66ddb-129">System-Only</span></span>            | <span data-ttu-id="66ddb-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="66ddb-130">False</span></span>                                                                          |
| <span data-ttu-id="66ddb-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="66ddb-131">Is-Single-Valued</span></span>       | <span data-ttu-id="66ddb-132">True</span><span class="sxs-lookup"><span data-stu-id="66ddb-132">True</span></span>                                                                           |
| <span data-ttu-id="66ddb-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="66ddb-133">Is Indexed</span></span>             | <span data-ttu-id="66ddb-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="66ddb-134">False</span></span>                                                                          |
| <span data-ttu-id="66ddb-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="66ddb-135">In Global Catalog</span></span>      | <span data-ttu-id="66ddb-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="66ddb-136">False</span></span>                                                                          |
| <span data-ttu-id="66ddb-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="66ddb-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="66ddb-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="66ddb-138">O:BAG:BAD:S:</span></span>                                                                   |
| <span data-ttu-id="66ddb-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="66ddb-139">Range-Lower</span></span>            | \-                                                                             |
| <span data-ttu-id="66ddb-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="66ddb-140">Range-Upper</span></span>            | \-                                                                             |
| <span data-ttu-id="66ddb-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="66ddb-141">Search-Flags</span></span>           | <span data-ttu-id="66ddb-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="66ddb-142">0x00000000</span></span>                                                                     |
| <span data-ttu-id="66ddb-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="66ddb-143">System-Flags</span></span>           | <span data-ttu-id="66ddb-144">0x00000010</span><span class="sxs-lookup"><span data-stu-id="66ddb-144">0x00000010</span></span>                                                                     |
| <span data-ttu-id="66ddb-145">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="66ddb-145">Classes used in</span></span>        | [<span data-ttu-id="66ddb-146">**MS-authz-центральный-доступ — правило**</span><span class="sxs-lookup"><span data-stu-id="66ddb-146">**ms-Authz-Central-Access-Rule**</span></span>](c-msauthz-centralaccessrule.md)<br/> |



 

 





