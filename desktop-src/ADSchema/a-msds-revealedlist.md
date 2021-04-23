---
title: Атрибут ms-DS-выводит список
description: Определяет субъекты безопасности, чьи текущие пароли учетных записей компьютеров были реплицированы на RODC.
ms.assetid: 10100719-4d03-4954-bcb6-d4ca635d00f7
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута "MS-DS-выобъявлено-список"
- Схема AD атрибута msDS-Ревеаледлист
topic_type:
- apiref
api_name:
- ms-DS-Revealed-List
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf8c5dc2e308b69ce142c7345957d25510168ab
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804979"
---
# <a name="ms-ds-revealed-list-attribute"></a><span data-ttu-id="36738-105">Атрибут ms-DS-выводит список</span><span class="sxs-lookup"><span data-stu-id="36738-105">ms-DS-Revealed-List attribute</span></span>

<span data-ttu-id="36738-106">Определяет субъекты безопасности, чьи текущие пароли учетных записей компьютеров были реплицированы на RODC.</span><span class="sxs-lookup"><span data-stu-id="36738-106">Identifies security principals whose current computer account passwords have been replicated to the RODC.</span></span>



| <span data-ttu-id="36738-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="36738-107">Entry</span></span> | <span data-ttu-id="36738-108">Значение</span><span class="sxs-lookup"><span data-stu-id="36738-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="36738-109">CN</span><span class="sxs-lookup"><span data-stu-id="36738-109">CN</span></span>                | <span data-ttu-id="36738-110">MS-DS-выявили список</span><span class="sxs-lookup"><span data-stu-id="36738-110">ms-DS-Revealed-List</span></span>                                   |
| <span data-ttu-id="36738-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="36738-111">Ldap-Display-Name</span></span> | <span data-ttu-id="36738-112">msDS-Ревеаледлист</span><span class="sxs-lookup"><span data-stu-id="36738-112">msDS-RevealedList</span></span>                                     |
| <span data-ttu-id="36738-113">Размер</span><span class="sxs-lookup"><span data-stu-id="36738-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="36738-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="36738-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="36738-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="36738-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="36738-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="36738-116">Attribute-Id</span></span>      | <span data-ttu-id="36738-117">1.2.840.113556.1.4.1940</span><span class="sxs-lookup"><span data-stu-id="36738-117">1.2.840.113556.1.4.1940</span></span>                               |
| <span data-ttu-id="36738-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="36738-118">System-Id-Guid</span></span>    | <span data-ttu-id="36738-119">cbdad11c-7fec-387b-6219-3a0627d9af81</span><span class="sxs-lookup"><span data-stu-id="36738-119">cbdad11c-7fec-387b-6219-3a0627d9af81</span></span>                  |
| <span data-ttu-id="36738-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36738-120">Syntax</span></span>            | [<span data-ttu-id="36738-121">**Object(точка_доступа)**</span><span class="sxs-lookup"><span data-stu-id="36738-121">**Object(Access-Point)**</span></span>](s-object-access-point.md) |



## <a name="implementations"></a><span data-ttu-id="36738-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="36738-122">Implementations</span></span>

-   [<span data-ttu-id="36738-123">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="36738-123">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="36738-124">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="36738-124">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="36738-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="36738-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="36738-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36738-126">Windows Server 2008</span></span>



| <span data-ttu-id="36738-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="36738-127">Entry</span></span> | <span data-ttu-id="36738-128">Значение</span><span class="sxs-lookup"><span data-stu-id="36738-128">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36738-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36738-129">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36738-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36738-130">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36738-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="36738-131">System-Only</span></span>            | <span data-ttu-id="36738-132">True</span><span class="sxs-lookup"><span data-stu-id="36738-132">True</span></span>                                      |
| <span data-ttu-id="36738-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36738-133">Is-Single-Valued</span></span>       | <span data-ttu-id="36738-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-134">False</span></span>                                     |
| <span data-ttu-id="36738-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36738-135">Is Indexed</span></span>             | <span data-ttu-id="36738-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-136">False</span></span>                                     |
| <span data-ttu-id="36738-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36738-137">In Global Catalog</span></span>      | <span data-ttu-id="36738-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-138">False</span></span>                                     |
| <span data-ttu-id="36738-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36738-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="36738-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36738-140">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36738-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36738-141">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36738-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36738-142">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36738-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36738-143">Search-Flags</span></span>           | <span data-ttu-id="36738-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36738-144">0x00000000</span></span>                                |
| <span data-ttu-id="36738-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36738-145">System-Flags</span></span>           | <span data-ttu-id="36738-146">0x00000014</span><span class="sxs-lookup"><span data-stu-id="36738-146">0x00000014</span></span>                                |
| <span data-ttu-id="36738-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36738-147">Classes used in</span></span>        | [<span data-ttu-id="36738-148">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="36738-148">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="36738-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36738-149">Windows Server 2008 R2</span></span>



| <span data-ttu-id="36738-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="36738-150">Entry</span></span> | <span data-ttu-id="36738-151">Значение</span><span class="sxs-lookup"><span data-stu-id="36738-151">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36738-152">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36738-152">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36738-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36738-153">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36738-154">System-Only</span><span class="sxs-lookup"><span data-stu-id="36738-154">System-Only</span></span>            | <span data-ttu-id="36738-155">True</span><span class="sxs-lookup"><span data-stu-id="36738-155">True</span></span>                                      |
| <span data-ttu-id="36738-156">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36738-156">Is-Single-Valued</span></span>       | <span data-ttu-id="36738-157">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-157">False</span></span>                                     |
| <span data-ttu-id="36738-158">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36738-158">Is Indexed</span></span>             | <span data-ttu-id="36738-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-159">False</span></span>                                     |
| <span data-ttu-id="36738-160">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36738-160">In Global Catalog</span></span>      | <span data-ttu-id="36738-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-161">False</span></span>                                     |
| <span data-ttu-id="36738-162">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36738-162">NT-Security-Descriptor</span></span> | <span data-ttu-id="36738-163">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36738-163">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36738-164">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36738-164">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36738-165">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36738-165">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36738-166">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36738-166">Search-Flags</span></span>           | <span data-ttu-id="36738-167">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36738-167">0x00000000</span></span>                                |
| <span data-ttu-id="36738-168">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36738-168">System-Flags</span></span>           | <span data-ttu-id="36738-169">0x00000014</span><span class="sxs-lookup"><span data-stu-id="36738-169">0x00000014</span></span>                                |
| <span data-ttu-id="36738-170">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36738-170">Classes used in</span></span>        | [<span data-ttu-id="36738-171">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="36738-171">**Computer**</span></span>](c-computer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="36738-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="36738-172">Windows Server 2012</span></span>



| <span data-ttu-id="36738-173">Ввод</span><span class="sxs-lookup"><span data-stu-id="36738-173">Entry</span></span> | <span data-ttu-id="36738-174">Значение</span><span class="sxs-lookup"><span data-stu-id="36738-174">Value</span></span> |
|------------------------|-------------------------------------------|
| <span data-ttu-id="36738-175">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="36738-175">Link-Id</span></span>                | \-                                        |
| <span data-ttu-id="36738-176">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="36738-176">MAPI-Id</span></span>                | \-                                        |
| <span data-ttu-id="36738-177">System-Only</span><span class="sxs-lookup"><span data-stu-id="36738-177">System-Only</span></span>            | <span data-ttu-id="36738-178">True</span><span class="sxs-lookup"><span data-stu-id="36738-178">True</span></span>                                      |
| <span data-ttu-id="36738-179">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="36738-179">Is-Single-Valued</span></span>       | <span data-ttu-id="36738-180">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-180">False</span></span>                                     |
| <span data-ttu-id="36738-181">Индексируется</span><span class="sxs-lookup"><span data-stu-id="36738-181">Is Indexed</span></span>             | <span data-ttu-id="36738-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-182">False</span></span>                                     |
| <span data-ttu-id="36738-183">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="36738-183">In Global Catalog</span></span>      | <span data-ttu-id="36738-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="36738-184">False</span></span>                                     |
| <span data-ttu-id="36738-185">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="36738-185">NT-Security-Descriptor</span></span> | <span data-ttu-id="36738-186">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="36738-186">O:BAG:BAD:S:</span></span>                              |
| <span data-ttu-id="36738-187">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="36738-187">Range-Lower</span></span>            | \-                                        |
| <span data-ttu-id="36738-188">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="36738-188">Range-Upper</span></span>            | \-                                        |
| <span data-ttu-id="36738-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="36738-189">Search-Flags</span></span>           | <span data-ttu-id="36738-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="36738-190">0x00000000</span></span>                                |
| <span data-ttu-id="36738-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="36738-191">System-Flags</span></span>           | <span data-ttu-id="36738-192">0x00000014</span><span class="sxs-lookup"><span data-stu-id="36738-192">0x00000014</span></span>                                |
| <span data-ttu-id="36738-193">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="36738-193">Classes used in</span></span>        | [<span data-ttu-id="36738-194">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="36738-194">**Computer**</span></span>](c-computer.md)<br/> |



 

 





