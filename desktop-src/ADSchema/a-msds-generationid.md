---
title: Атрибут ms-DS-Generation-ID
description: Для обнаружения возобновления моментальных снимков виртуальной машины. Этот атрибут представляет идентификатор создания виртуальной машины.
ms.assetid: 48a454b7-b1dc-40d0-af10-d19c810f25a9
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-Generation-ID
- Схема AD атрибута msDS-GenerationId
topic_type:
- apiref
api_name:
- ms-DS-Generation-Id
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20a61a8a542a6ce56e58d2bde75d6982703c0f8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536047"
---
# <a name="ms-ds-generation-id-attribute"></a><span data-ttu-id="ed0d3-106">Атрибут ms-DS-Generation-ID</span><span class="sxs-lookup"><span data-stu-id="ed0d3-106">ms-DS-Generation-Id attribute</span></span>

<span data-ttu-id="ed0d3-107">Для обнаружения возобновления моментальных снимков виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed0d3-107">For virtual machine snapshot resuming detection.</span></span> <span data-ttu-id="ed0d3-108">Этот атрибут представляет идентификатор создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ed0d3-108">This attribute represents the VM Generation ID.</span></span>



| <span data-ttu-id="ed0d3-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed0d3-109">Entry</span></span> | <span data-ttu-id="ed0d3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ed0d3-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="ed0d3-111">CN</span><span class="sxs-lookup"><span data-stu-id="ed0d3-111">CN</span></span>                | <span data-ttu-id="ed0d3-112">MS-DS-Generation-ID</span><span class="sxs-lookup"><span data-stu-id="ed0d3-112">ms-DS-Generation-Id</span></span>                                   |
| <span data-ttu-id="ed0d3-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ed0d3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="ed0d3-114">msDS-GenerationId</span><span class="sxs-lookup"><span data-stu-id="ed0d3-114">msDS-GenerationId</span></span>                                     |
| <span data-ttu-id="ed0d3-115">Размер</span><span class="sxs-lookup"><span data-stu-id="ed0d3-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="ed0d3-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ed0d3-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="ed0d3-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ed0d3-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="ed0d3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ed0d3-118">Attribute-Id</span></span>      | <span data-ttu-id="ed0d3-119">1.2.840.113556.1.4.2166</span><span class="sxs-lookup"><span data-stu-id="ed0d3-119">1.2.840.113556.1.4.2166</span></span>                               |
| <span data-ttu-id="ed0d3-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ed0d3-120">System-Id-Guid</span></span>    | <span data-ttu-id="ed0d3-121">1e5d393d-8cb7-4b4f-840a-973b36cc09c3</span><span class="sxs-lookup"><span data-stu-id="ed0d3-121">1e5d393d-8cb7-4b4f-840a-973b36cc09c3</span></span>                  |
| <span data-ttu-id="ed0d3-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed0d3-122">Syntax</span></span>            | [<span data-ttu-id="ed0d3-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="ed0d3-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="ed0d3-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ed0d3-124">Implementations</span></span>

-   [<span data-ttu-id="ed0d3-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ed0d3-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="ed0d3-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ed0d3-126">Windows Server 2012</span></span>



| <span data-ttu-id="ed0d3-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="ed0d3-127">Entry</span></span> | <span data-ttu-id="ed0d3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ed0d3-128">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="ed0d3-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ed0d3-129">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="ed0d3-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ed0d3-130">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="ed0d3-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="ed0d3-131">System-Only</span></span>            | <span data-ttu-id="ed0d3-132">True</span><span class="sxs-lookup"><span data-stu-id="ed0d3-132">True</span></span>                                      |
| <span data-ttu-id="ed0d3-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ed0d3-133">Is-Single-Valued</span></span>       | <span data-ttu-id="ed0d3-134">True</span><span class="sxs-lookup"><span data-stu-id="ed0d3-134">True</span></span>                                      |
| <span data-ttu-id="ed0d3-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ed0d3-135">Is Indexed</span></span>             | <span data-ttu-id="ed0d3-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed0d3-136">False</span></span>                                     |
| <span data-ttu-id="ed0d3-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ed0d3-137">In Global Catalog</span></span>      | <span data-ttu-id="ed0d3-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="ed0d3-138">False</span></span>                                     |
| <span data-ttu-id="ed0d3-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ed0d3-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="ed0d3-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ed0d3-140">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="ed0d3-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ed0d3-141">Range-Lower</span></span>            | <span data-ttu-id="ed0d3-142">16</span><span class="sxs-lookup"><span data-stu-id="ed0d3-142">16</span></span>                                        |
| <span data-ttu-id="ed0d3-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ed0d3-143">Range-Upper</span></span>            | <span data-ttu-id="ed0d3-144">16</span><span class="sxs-lookup"><span data-stu-id="ed0d3-144">16</span></span>                                        |
| <span data-ttu-id="ed0d3-145">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ed0d3-145">Search-Flags</span></span>           | <span data-ttu-id="ed0d3-146">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ed0d3-146">0x00000000</span></span>                                |
| <span data-ttu-id="ed0d3-147">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ed0d3-147">System-Flags</span></span>           | <span data-ttu-id="ed0d3-148">0x00000011</span><span class="sxs-lookup"><span data-stu-id="ed0d3-148">0x00000011</span></span>                                |
| <span data-ttu-id="ed0d3-149">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ed0d3-149">Classes used in</span></span>        | [<span data-ttu-id="ed0d3-150">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="ed0d3-150">**Computer**</span></span>](c-computer.md)<br/> |



 

 





