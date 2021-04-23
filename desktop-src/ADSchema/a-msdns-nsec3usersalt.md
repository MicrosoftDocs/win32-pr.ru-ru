---
title: атрибут MS-DNS-NSEC3-User-Salt
description: Атрибут, определяющий указанную пользователем строку NSEC3, используемую при подписывании зоны DNS. Если значение пустое, будет использоваться случайная соль.
ms.assetid: b9829732-8a79-4f07-8644-9fe4ba05ba8f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DNS-NSEC3-User-соли
- msDN — схема AD атрибута NSEC3UserSalt
topic_type:
- apiref
api_name:
- ms-DNS-NSEC3-User-Salt
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d28acb28dec95ef13afc37f9d7f26d713d5cf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804715"
---
# <a name="ms-dns-nsec3-user-salt-attribute"></a><span data-ttu-id="8092b-106">атрибут MS-DNS-NSEC3-User-Salt</span><span class="sxs-lookup"><span data-stu-id="8092b-106">ms-DNS-NSEC3-User-Salt attribute</span></span>

<span data-ttu-id="8092b-107">Атрибут, определяющий указанную пользователем строку NSEC3, используемую при подписывании зоны DNS.</span><span class="sxs-lookup"><span data-stu-id="8092b-107">An attribute that defines a user-specified NSEC3 salt string to use when signing the DNS zone.</span></span> <span data-ttu-id="8092b-108">Если значение пустое, будет использоваться случайная соль.</span><span class="sxs-lookup"><span data-stu-id="8092b-108">If empty, random salt will be used.</span></span>



| <span data-ttu-id="8092b-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8092b-109">Entry</span></span> | <span data-ttu-id="8092b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8092b-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="8092b-111">CN</span><span class="sxs-lookup"><span data-stu-id="8092b-111">CN</span></span>                | <span data-ttu-id="8092b-112">MS-DNS-NSEC3-User-Salt</span><span class="sxs-lookup"><span data-stu-id="8092b-112">ms-DNS-NSEC3-User-Salt</span></span>                      |
| <span data-ttu-id="8092b-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8092b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8092b-114">msDN — NSEC3UserSalt</span><span class="sxs-lookup"><span data-stu-id="8092b-114">msDNS-NSEC3UserSalt</span></span>                         |
| <span data-ttu-id="8092b-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8092b-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="8092b-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8092b-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="8092b-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8092b-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="8092b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8092b-118">Attribute-Id</span></span>      | <span data-ttu-id="8092b-119">1.2.840.113556.1.4.2148</span><span class="sxs-lookup"><span data-stu-id="8092b-119">1.2.840.113556.1.4.2148</span></span>                     |
| <span data-ttu-id="8092b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8092b-120">System-Id-Guid</span></span>    | <span data-ttu-id="8092b-121">aff16770-9622-4fbc-a128-3088777605b9</span><span class="sxs-lookup"><span data-stu-id="8092b-121">aff16770-9622-4fbc-a128-3088777605b9</span></span>        |
| <span data-ttu-id="8092b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8092b-122">Syntax</span></span>            | [<span data-ttu-id="8092b-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="8092b-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="8092b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8092b-124">Implementations</span></span>

-   [<span data-ttu-id="8092b-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8092b-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="8092b-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8092b-126">Windows Server 2012</span></span>



| <span data-ttu-id="8092b-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="8092b-127">Entry</span></span> | <span data-ttu-id="8092b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8092b-128">Value</span></span> |
|------------------------|------------------------------------------|
| <span data-ttu-id="8092b-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8092b-129">Link-Id</span></span>                | \-                                       |
| <span data-ttu-id="8092b-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8092b-130">MAPI-Id</span></span>                | \-                                       |
| <span data-ttu-id="8092b-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="8092b-131">System-Only</span></span>            | <span data-ttu-id="8092b-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="8092b-132">False</span></span>                                    |
| <span data-ttu-id="8092b-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8092b-133">Is-Single-Valued</span></span>       | <span data-ttu-id="8092b-134">True</span><span class="sxs-lookup"><span data-stu-id="8092b-134">True</span></span>                                     |
| <span data-ttu-id="8092b-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8092b-135">Is Indexed</span></span>             | <span data-ttu-id="8092b-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="8092b-136">False</span></span>                                    |
| <span data-ttu-id="8092b-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8092b-137">In Global Catalog</span></span>      | <span data-ttu-id="8092b-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="8092b-138">False</span></span>                                    |
| <span data-ttu-id="8092b-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8092b-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="8092b-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8092b-140">O:BAG:BAD:S:</span></span>                             |
| <span data-ttu-id="8092b-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8092b-141">Range-Lower</span></span>            | <span data-ttu-id="8092b-142">0</span><span class="sxs-lookup"><span data-stu-id="8092b-142">0</span></span>                                        |
| <span data-ttu-id="8092b-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8092b-143">Range-Upper</span></span>            | <span data-ttu-id="8092b-144">510</span><span class="sxs-lookup"><span data-stu-id="8092b-144">510</span></span>                                      |
| <span data-ttu-id="8092b-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8092b-145">Search-Flags</span></span>           | <span data-ttu-id="8092b-146">0x00000008</span><span class="sxs-lookup"><span data-stu-id="8092b-146">0x00000008</span></span>                               |
| <span data-ttu-id="8092b-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8092b-147">System-Flags</span></span>           | <span data-ttu-id="8092b-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8092b-148">0x00000010</span></span>                               |
| <span data-ttu-id="8092b-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8092b-149">Classes used in</span></span>        | [<span data-ttu-id="8092b-150">**DNS — зона**</span><span class="sxs-lookup"><span data-stu-id="8092b-150">**Dns-Zone**</span></span>](c-dnszone.md)<br/> |



 

 





