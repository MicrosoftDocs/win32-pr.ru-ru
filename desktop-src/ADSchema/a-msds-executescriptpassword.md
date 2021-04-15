---
title: Атрибут ms-DS-Ексекутескриптпассворд
description: Используется при переименовании домена. Это значение не может быть записано или прочитано с помощью LDAP.
ms.assetid: 381c3676-0a11-4e53-8093-f04dbf156250
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-Ексекутескриптпассворд
- Схема AD атрибута msDS-Ексекутескриптпассворд
topic_type:
- apiref
api_name:
- ms-DS-ExecuteScriptPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01ebb231404188235236442df1d4916814f0636
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655194"
---
# <a name="ms-ds-executescriptpassword-attribute"></a><span data-ttu-id="4f79d-106">Атрибут ms-DS-Ексекутескриптпассворд</span><span class="sxs-lookup"><span data-stu-id="4f79d-106">ms-DS-ExecuteScriptPassword attribute</span></span>

<span data-ttu-id="4f79d-107">Используется при переименовании домена.</span><span class="sxs-lookup"><span data-stu-id="4f79d-107">Used during domain rename.</span></span> <span data-ttu-id="4f79d-108">Это значение не может быть записано или прочитано с помощью LDAP.</span><span class="sxs-lookup"><span data-stu-id="4f79d-108">This value cannot be written to or read from by using LDAP.</span></span>



| <span data-ttu-id="4f79d-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="4f79d-109">Entry</span></span> | <span data-ttu-id="4f79d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4f79d-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="4f79d-111">CN</span><span class="sxs-lookup"><span data-stu-id="4f79d-111">CN</span></span>                | <span data-ttu-id="4f79d-112">MS-DS-Ексекутескриптпассворд</span><span class="sxs-lookup"><span data-stu-id="4f79d-112">ms-DS-ExecuteScriptPassword</span></span>                           |
| <span data-ttu-id="4f79d-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4f79d-113">Ldap-Display-Name</span></span> | <span data-ttu-id="4f79d-114">msDS-Ексекутескриптпассворд</span><span class="sxs-lookup"><span data-stu-id="4f79d-114">msDS-ExecuteScriptPassword</span></span>                            |
| <span data-ttu-id="4f79d-115">Размер</span><span class="sxs-lookup"><span data-stu-id="4f79d-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="4f79d-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4f79d-116">Update Privilege</span></span>  | <span data-ttu-id="4f79d-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="4f79d-117">This value is set by the system.</span></span>                      |
| <span data-ttu-id="4f79d-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4f79d-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="4f79d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4f79d-119">Attribute-Id</span></span>      | <span data-ttu-id="4f79d-120">1.2.840.113556.1.4.1783</span><span class="sxs-lookup"><span data-stu-id="4f79d-120">1.2.840.113556.1.4.1783</span></span>                               |
| <span data-ttu-id="4f79d-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4f79d-121">System-Id-Guid</span></span>    | <span data-ttu-id="4f79d-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span><span class="sxs-lookup"><span data-stu-id="4f79d-122">9d054a5a-d187-46c1-9d85-42dfc44a56dd</span></span>                  |
| <span data-ttu-id="4f79d-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f79d-123">Syntax</span></span>            | [<span data-ttu-id="4f79d-124">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="4f79d-124">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="4f79d-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4f79d-125">Implementations</span></span>

-   [<span data-ttu-id="4f79d-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="4f79d-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="4f79d-127">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4f79d-127">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="4f79d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="4f79d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="4f79d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="4f79d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="4f79d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="4f79d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="4f79d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="4f79d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="4f79d-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4f79d-132">Windows Server 2003</span></span>



| <span data-ttu-id="4f79d-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="4f79d-133">Entry</span></span> | <span data-ttu-id="4f79d-134">Значение</span><span class="sxs-lookup"><span data-stu-id="4f79d-134">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4f79d-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4f79d-135">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4f79d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f79d-136">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4f79d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f79d-137">System-Only</span></span>            | <span data-ttu-id="4f79d-138">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-138">True</span></span>                                                          |
| <span data-ttu-id="4f79d-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4f79d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="4f79d-140">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-140">True</span></span>                                                          |
| <span data-ttu-id="4f79d-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4f79d-141">Is Indexed</span></span>             | <span data-ttu-id="4f79d-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-142">False</span></span>                                                         |
| <span data-ttu-id="4f79d-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4f79d-143">In Global Catalog</span></span>      | <span data-ttu-id="4f79d-144">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-144">False</span></span>                                                         |
| <span data-ttu-id="4f79d-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4f79d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f79d-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4f79d-146">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4f79d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f79d-147">Range-Lower</span></span>            | <span data-ttu-id="4f79d-148">0</span><span class="sxs-lookup"><span data-stu-id="4f79d-148">0</span></span>                                                             |
| <span data-ttu-id="4f79d-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f79d-149">Range-Upper</span></span>            | <span data-ttu-id="4f79d-150">64</span><span class="sxs-lookup"><span data-stu-id="4f79d-150">64</span></span>                                                            |
| <span data-ttu-id="4f79d-151">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-151">Search-Flags</span></span>           | <span data-ttu-id="4f79d-152">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f79d-152">0x00000000</span></span>                                                    |
| <span data-ttu-id="4f79d-153">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-153">System-Flags</span></span>           | <span data-ttu-id="4f79d-154">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4f79d-154">0x00000011</span></span>                                                    |
| <span data-ttu-id="4f79d-155">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4f79d-155">Classes used in</span></span>        | [<span data-ttu-id="4f79d-156">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="4f79d-156">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="adam"></a><span data-ttu-id="4f79d-157">ADAM</span><span class="sxs-lookup"><span data-stu-id="4f79d-157">ADAM</span></span>



| <span data-ttu-id="4f79d-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="4f79d-158">Entry</span></span> | <span data-ttu-id="4f79d-159">Значение</span><span class="sxs-lookup"><span data-stu-id="4f79d-159">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4f79d-160">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4f79d-160">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4f79d-161">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f79d-161">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4f79d-162">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f79d-162">System-Only</span></span>            | <span data-ttu-id="4f79d-163">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-163">True</span></span>                                                          |
| <span data-ttu-id="4f79d-164">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4f79d-164">Is-Single-Valued</span></span>       | <span data-ttu-id="4f79d-165">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-165">True</span></span>                                                          |
| <span data-ttu-id="4f79d-166">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4f79d-166">Is Indexed</span></span>             | <span data-ttu-id="4f79d-167">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-167">False</span></span>                                                         |
| <span data-ttu-id="4f79d-168">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4f79d-168">In Global Catalog</span></span>      | <span data-ttu-id="4f79d-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-169">False</span></span>                                                         |
| <span data-ttu-id="4f79d-170">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4f79d-170">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f79d-171">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4f79d-171">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4f79d-172">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f79d-172">Range-Lower</span></span>            | <span data-ttu-id="4f79d-173">0</span><span class="sxs-lookup"><span data-stu-id="4f79d-173">0</span></span>                                                             |
| <span data-ttu-id="4f79d-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f79d-174">Range-Upper</span></span>            | <span data-ttu-id="4f79d-175">64</span><span class="sxs-lookup"><span data-stu-id="4f79d-175">64</span></span>                                                            |
| <span data-ttu-id="4f79d-176">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-176">Search-Flags</span></span>           | <span data-ttu-id="4f79d-177">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f79d-177">0x00000000</span></span>                                                    |
| <span data-ttu-id="4f79d-178">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-178">System-Flags</span></span>           | <span data-ttu-id="4f79d-179">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4f79d-179">0x00000011</span></span>                                                    |
| <span data-ttu-id="4f79d-180">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4f79d-180">Classes used in</span></span>        | [<span data-ttu-id="4f79d-181">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="4f79d-181">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="4f79d-182">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="4f79d-182">Windows Server 2003 R2</span></span>



| <span data-ttu-id="4f79d-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="4f79d-183">Entry</span></span> | <span data-ttu-id="4f79d-184">Значение</span><span class="sxs-lookup"><span data-stu-id="4f79d-184">Value</span></span> |
|------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4f79d-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4f79d-185">Link-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4f79d-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f79d-186">MAPI-Id</span></span>                | \-                                                            |
| <span data-ttu-id="4f79d-187">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f79d-187">System-Only</span></span>            | <span data-ttu-id="4f79d-188">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-188">True</span></span>                                                          |
| <span data-ttu-id="4f79d-189">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4f79d-189">Is-Single-Valued</span></span>       | <span data-ttu-id="4f79d-190">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-190">True</span></span>                                                          |
| <span data-ttu-id="4f79d-191">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4f79d-191">Is Indexed</span></span>             | <span data-ttu-id="4f79d-192">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-192">False</span></span>                                                         |
| <span data-ttu-id="4f79d-193">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4f79d-193">In Global Catalog</span></span>      | <span data-ttu-id="4f79d-194">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-194">False</span></span>                                                         |
| <span data-ttu-id="4f79d-195">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4f79d-195">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f79d-196">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4f79d-196">O:BAG:BAD:S:</span></span>                                                  |
| <span data-ttu-id="4f79d-197">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f79d-197">Range-Lower</span></span>            | <span data-ttu-id="4f79d-198">0</span><span class="sxs-lookup"><span data-stu-id="4f79d-198">0</span></span>                                                             |
| <span data-ttu-id="4f79d-199">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f79d-199">Range-Upper</span></span>            | <span data-ttu-id="4f79d-200">64</span><span class="sxs-lookup"><span data-stu-id="4f79d-200">64</span></span>                                                            |
| <span data-ttu-id="4f79d-201">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-201">Search-Flags</span></span>           | <span data-ttu-id="4f79d-202">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f79d-202">0x00000000</span></span>                                                    |
| <span data-ttu-id="4f79d-203">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-203">System-Flags</span></span>           | <span data-ttu-id="4f79d-204">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4f79d-204">0x00000011</span></span>                                                    |
| <span data-ttu-id="4f79d-205">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4f79d-205">Classes used in</span></span>        | [<span data-ttu-id="4f79d-206">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="4f79d-206">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="4f79d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f79d-207">Windows Server 2008</span></span>



| <span data-ttu-id="4f79d-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="4f79d-208">Entry</span></span> | <span data-ttu-id="4f79d-209">Значение</span><span class="sxs-lookup"><span data-stu-id="4f79d-209">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f79d-210">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4f79d-210">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="4f79d-211">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f79d-211">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="4f79d-212">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f79d-212">System-Only</span></span>            | <span data-ttu-id="4f79d-213">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-213">True</span></span>                                                                                                    |
| <span data-ttu-id="4f79d-214">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4f79d-214">Is-Single-Valued</span></span>       | <span data-ttu-id="4f79d-215">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-215">True</span></span>                                                                                                    |
| <span data-ttu-id="4f79d-216">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4f79d-216">Is Indexed</span></span>             | <span data-ttu-id="4f79d-217">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-217">False</span></span>                                                                                                   |
| <span data-ttu-id="4f79d-218">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4f79d-218">In Global Catalog</span></span>      | <span data-ttu-id="4f79d-219">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-219">False</span></span>                                                                                                   |
| <span data-ttu-id="4f79d-220">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4f79d-220">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f79d-221">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4f79d-221">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="4f79d-222">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f79d-222">Range-Lower</span></span>            | <span data-ttu-id="4f79d-223">0</span><span class="sxs-lookup"><span data-stu-id="4f79d-223">0</span></span>                                                                                                       |
| <span data-ttu-id="4f79d-224">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f79d-224">Range-Upper</span></span>            | <span data-ttu-id="4f79d-225">64</span><span class="sxs-lookup"><span data-stu-id="4f79d-225">64</span></span>                                                                                                      |
| <span data-ttu-id="4f79d-226">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-226">Search-Flags</span></span>           | <span data-ttu-id="4f79d-227">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f79d-227">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="4f79d-228">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-228">System-Flags</span></span>           | <span data-ttu-id="4f79d-229">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4f79d-229">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="4f79d-230">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4f79d-230">Classes used in</span></span>        | [<span data-ttu-id="4f79d-231">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="4f79d-231">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4f79d-232">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="4f79d-232">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="4f79d-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f79d-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="4f79d-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="4f79d-234">Entry</span></span> | <span data-ttu-id="4f79d-235">Значение</span><span class="sxs-lookup"><span data-stu-id="4f79d-235">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f79d-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4f79d-236">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="4f79d-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f79d-237">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="4f79d-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f79d-238">System-Only</span></span>            | <span data-ttu-id="4f79d-239">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-239">True</span></span>                                                                                                    |
| <span data-ttu-id="4f79d-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4f79d-240">Is-Single-Valued</span></span>       | <span data-ttu-id="4f79d-241">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-241">True</span></span>                                                                                                    |
| <span data-ttu-id="4f79d-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4f79d-242">Is Indexed</span></span>             | <span data-ttu-id="4f79d-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-243">False</span></span>                                                                                                   |
| <span data-ttu-id="4f79d-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4f79d-244">In Global Catalog</span></span>      | <span data-ttu-id="4f79d-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-245">False</span></span>                                                                                                   |
| <span data-ttu-id="4f79d-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4f79d-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f79d-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4f79d-247">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="4f79d-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f79d-248">Range-Lower</span></span>            | <span data-ttu-id="4f79d-249">0</span><span class="sxs-lookup"><span data-stu-id="4f79d-249">0</span></span>                                                                                                       |
| <span data-ttu-id="4f79d-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f79d-250">Range-Upper</span></span>            | <span data-ttu-id="4f79d-251">64</span><span class="sxs-lookup"><span data-stu-id="4f79d-251">64</span></span>                                                                                                      |
| <span data-ttu-id="4f79d-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-252">Search-Flags</span></span>           | <span data-ttu-id="4f79d-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f79d-253">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="4f79d-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-254">System-Flags</span></span>           | <span data-ttu-id="4f79d-255">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4f79d-255">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="4f79d-256">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4f79d-256">Classes used in</span></span>        | [<span data-ttu-id="4f79d-257">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="4f79d-257">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4f79d-258">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="4f79d-258">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="4f79d-259">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4f79d-259">Windows Server 2012</span></span>



| <span data-ttu-id="4f79d-260">Ввод</span><span class="sxs-lookup"><span data-stu-id="4f79d-260">Entry</span></span> | <span data-ttu-id="4f79d-261">Значение</span><span class="sxs-lookup"><span data-stu-id="4f79d-261">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f79d-262">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4f79d-262">Link-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="4f79d-263">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4f79d-263">MAPI-Id</span></span>                | \-                                                                                                      |
| <span data-ttu-id="4f79d-264">System-Only</span><span class="sxs-lookup"><span data-stu-id="4f79d-264">System-Only</span></span>            | <span data-ttu-id="4f79d-265">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-265">True</span></span>                                                                                                    |
| <span data-ttu-id="4f79d-266">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4f79d-266">Is-Single-Valued</span></span>       | <span data-ttu-id="4f79d-267">True</span><span class="sxs-lookup"><span data-stu-id="4f79d-267">True</span></span>                                                                                                    |
| <span data-ttu-id="4f79d-268">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4f79d-268">Is Indexed</span></span>             | <span data-ttu-id="4f79d-269">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-269">False</span></span>                                                                                                   |
| <span data-ttu-id="4f79d-270">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4f79d-270">In Global Catalog</span></span>      | <span data-ttu-id="4f79d-271">Неверно</span><span class="sxs-lookup"><span data-stu-id="4f79d-271">False</span></span>                                                                                                   |
| <span data-ttu-id="4f79d-272">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4f79d-272">NT-Security-Descriptor</span></span> | <span data-ttu-id="4f79d-273">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4f79d-273">O:BAG:BAD:S:</span></span>                                                                                            |
| <span data-ttu-id="4f79d-274">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4f79d-274">Range-Lower</span></span>            | <span data-ttu-id="4f79d-275">0</span><span class="sxs-lookup"><span data-stu-id="4f79d-275">0</span></span>                                                                                                       |
| <span data-ttu-id="4f79d-276">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4f79d-276">Range-Upper</span></span>            | <span data-ttu-id="4f79d-277">64</span><span class="sxs-lookup"><span data-stu-id="4f79d-277">64</span></span>                                                                                                      |
| <span data-ttu-id="4f79d-278">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-278">Search-Flags</span></span>           | <span data-ttu-id="4f79d-279">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4f79d-279">0x00000000</span></span>                                                                                              |
| <span data-ttu-id="4f79d-280">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4f79d-280">System-Flags</span></span>           | <span data-ttu-id="4f79d-281">0x00000011</span><span class="sxs-lookup"><span data-stu-id="4f79d-281">0x00000011</span></span>                                                                                              |
| <span data-ttu-id="4f79d-282">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4f79d-282">Classes used in</span></span>        | [<span data-ttu-id="4f79d-283">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="4f79d-283">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="4f79d-284">**Перекрестные ссылки на контейнеры**</span><span class="sxs-lookup"><span data-stu-id="4f79d-284">**Cross-Ref-Container**</span></span>](c-crossrefcontainer.md)<br/> |



 

 





