---
title: Атрибут по умолчанию — локальный — политика объекта
description: Ссылка на объект политики, определяющий локальную политику для объекта узла.
ms.assetid: baed2be8-db3e-458f-a6da-2fa522b95d29
ms.tgt_platform: multiple
keywords:
- Default — локальная политика — атрибут объекта AD
- Схема AD атрибута Дефаултлокалполициобжект
topic_type:
- apiref
api_name:
- Default-Local-Policy-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c2bfc4797dbda7aff5e2fadec16de8b87854824
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105654882"
---
# <a name="default-local-policy-object-attribute"></a><span data-ttu-id="c96e8-105">Атрибут по умолчанию — локальный — политика объекта</span><span class="sxs-lookup"><span data-stu-id="c96e8-105">Default-Local-Policy-Object attribute</span></span>

<span data-ttu-id="c96e8-106">Ссылка на объект политики, определяющий локальную политику для объекта узла.</span><span class="sxs-lookup"><span data-stu-id="c96e8-106">A reference to a Policy object that defines the local policy for the host object.</span></span>



| <span data-ttu-id="c96e8-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="c96e8-107">Entry</span></span> | <span data-ttu-id="c96e8-108">Значение</span><span class="sxs-lookup"><span data-stu-id="c96e8-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="c96e8-109">CN</span><span class="sxs-lookup"><span data-stu-id="c96e8-109">CN</span></span>                | <span data-ttu-id="c96e8-110">По умолчанию — локальная политика — объект</span><span class="sxs-lookup"><span data-stu-id="c96e8-110">Default-Local-Policy-Object</span></span>             |
| <span data-ttu-id="c96e8-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="c96e8-111">Ldap-Display-Name</span></span> | <span data-ttu-id="c96e8-112">дефаултлокалполициобжект</span><span class="sxs-lookup"><span data-stu-id="c96e8-112">defaultLocalPolicyObject</span></span>                |
| <span data-ttu-id="c96e8-113">Размер</span><span class="sxs-lookup"><span data-stu-id="c96e8-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="c96e8-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="c96e8-114">Update Privilege</span></span>  | \-                                      |
| <span data-ttu-id="c96e8-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="c96e8-115">Update Frequency</span></span>  | \-                                      |
| <span data-ttu-id="c96e8-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c96e8-116">Attribute-Id</span></span>      | <span data-ttu-id="c96e8-117">1.2.840.113556.1.4.57</span><span class="sxs-lookup"><span data-stu-id="c96e8-117">1.2.840.113556.1.4.57</span></span>                   |
| <span data-ttu-id="c96e8-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="c96e8-118">System-Id-Guid</span></span>    | <span data-ttu-id="c96e8-119">bf96799f-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="c96e8-119">bf96799f-0de6-11d0-a285-00aa003049e2</span></span>    |
| <span data-ttu-id="c96e8-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c96e8-120">Syntax</span></span>            | [<span data-ttu-id="c96e8-121">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="c96e8-121">**Object(DS-DN)**</span></span>](s-object-ds-dn.md) |



## <a name="implementations"></a><span data-ttu-id="c96e8-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="c96e8-122">Implementations</span></span>

-   [<span data-ttu-id="c96e8-123">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c96e8-123">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c96e8-124">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c96e8-124">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c96e8-125">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c96e8-125">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c96e8-126">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c96e8-126">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c96e8-127">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c96e8-127">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c96e8-128">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c96e8-128">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c96e8-129">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c96e8-129">Windows 2000 Server</span></span>



| <span data-ttu-id="c96e8-130">Ввод</span><span class="sxs-lookup"><span data-stu-id="c96e8-130">Entry</span></span> | <span data-ttu-id="c96e8-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c96e8-131">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96e8-132">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c96e8-132">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-133">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c96e8-133">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="c96e8-134">System-Only</span></span>            | <span data-ttu-id="c96e8-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-135">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c96e8-136">Is-Single-Valued</span></span>       | <span data-ttu-id="c96e8-137">True</span><span class="sxs-lookup"><span data-stu-id="c96e8-137">True</span></span>                                                                                                                                      |
| <span data-ttu-id="c96e8-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c96e8-138">Is Indexed</span></span>             | <span data-ttu-id="c96e8-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-139">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c96e8-140">In Global Catalog</span></span>      | <span data-ttu-id="c96e8-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-141">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c96e8-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="c96e8-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c96e8-143">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="c96e8-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c96e8-144">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-145">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c96e8-145">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-146">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-146">Search-Flags</span></span>           | <span data-ttu-id="c96e8-147">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c96e8-147">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-148">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-148">System-Flags</span></span>           | <span data-ttu-id="c96e8-149">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c96e8-149">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-150">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c96e8-150">Classes used in</span></span>        | [<span data-ttu-id="c96e8-151">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c96e8-151">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c96e8-152">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c96e8-152">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c96e8-153">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="c96e8-153">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c96e8-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c96e8-154">Windows Server 2003</span></span>



| <span data-ttu-id="c96e8-155">Ввод</span><span class="sxs-lookup"><span data-stu-id="c96e8-155">Entry</span></span> | <span data-ttu-id="c96e8-156">Значение</span><span class="sxs-lookup"><span data-stu-id="c96e8-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96e8-157">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c96e8-157">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c96e8-158">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="c96e8-159">System-Only</span></span>            | <span data-ttu-id="c96e8-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-160">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-161">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c96e8-161">Is-Single-Valued</span></span>       | <span data-ttu-id="c96e8-162">True</span><span class="sxs-lookup"><span data-stu-id="c96e8-162">True</span></span>                                                                                                                                      |
| <span data-ttu-id="c96e8-163">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c96e8-163">Is Indexed</span></span>             | <span data-ttu-id="c96e8-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-164">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-165">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c96e8-165">In Global Catalog</span></span>      | <span data-ttu-id="c96e8-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-166">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-167">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c96e8-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="c96e8-168">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c96e8-168">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="c96e8-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c96e8-169">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c96e8-170">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-171">Search-Flags</span></span>           | <span data-ttu-id="c96e8-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c96e8-172">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-173">System-Flags</span></span>           | <span data-ttu-id="c96e8-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c96e8-174">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-175">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c96e8-175">Classes used in</span></span>        | [<span data-ttu-id="c96e8-176">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c96e8-176">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c96e8-177">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c96e8-177">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c96e8-178">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="c96e8-178">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c96e8-179">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c96e8-179">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c96e8-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="c96e8-180">Entry</span></span> | <span data-ttu-id="c96e8-181">Значение</span><span class="sxs-lookup"><span data-stu-id="c96e8-181">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96e8-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c96e8-182">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c96e8-183">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="c96e8-184">System-Only</span></span>            | <span data-ttu-id="c96e8-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-185">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c96e8-186">Is-Single-Valued</span></span>       | <span data-ttu-id="c96e8-187">True</span><span class="sxs-lookup"><span data-stu-id="c96e8-187">True</span></span>                                                                                                                                      |
| <span data-ttu-id="c96e8-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c96e8-188">Is Indexed</span></span>             | <span data-ttu-id="c96e8-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-189">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c96e8-190">In Global Catalog</span></span>      | <span data-ttu-id="c96e8-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-191">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c96e8-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="c96e8-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c96e8-193">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="c96e8-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c96e8-194">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c96e8-195">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-196">Search-Flags</span></span>           | <span data-ttu-id="c96e8-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c96e8-197">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-198">System-Flags</span></span>           | <span data-ttu-id="c96e8-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c96e8-199">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c96e8-200">Classes used in</span></span>        | [<span data-ttu-id="c96e8-201">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c96e8-201">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c96e8-202">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c96e8-202">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c96e8-203">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="c96e8-203">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c96e8-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c96e8-204">Windows Server 2008</span></span>



| <span data-ttu-id="c96e8-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="c96e8-205">Entry</span></span> | <span data-ttu-id="c96e8-206">Значение</span><span class="sxs-lookup"><span data-stu-id="c96e8-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96e8-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c96e8-207">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c96e8-208">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="c96e8-209">System-Only</span></span>            | <span data-ttu-id="c96e8-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-210">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c96e8-211">Is-Single-Valued</span></span>       | <span data-ttu-id="c96e8-212">True</span><span class="sxs-lookup"><span data-stu-id="c96e8-212">True</span></span>                                                                                                                                      |
| <span data-ttu-id="c96e8-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c96e8-213">Is Indexed</span></span>             | <span data-ttu-id="c96e8-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-214">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c96e8-215">In Global Catalog</span></span>      | <span data-ttu-id="c96e8-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-216">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c96e8-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="c96e8-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c96e8-218">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="c96e8-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c96e8-219">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c96e8-220">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-221">Search-Flags</span></span>           | <span data-ttu-id="c96e8-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c96e8-222">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-223">System-Flags</span></span>           | <span data-ttu-id="c96e8-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c96e8-224">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c96e8-225">Classes used in</span></span>        | [<span data-ttu-id="c96e8-226">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c96e8-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c96e8-227">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c96e8-227">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c96e8-228">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="c96e8-228">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c96e8-229">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c96e8-229">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c96e8-230">Ввод</span><span class="sxs-lookup"><span data-stu-id="c96e8-230">Entry</span></span> | <span data-ttu-id="c96e8-231">Значение</span><span class="sxs-lookup"><span data-stu-id="c96e8-231">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96e8-232">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c96e8-232">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-233">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c96e8-233">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-234">System-Only</span><span class="sxs-lookup"><span data-stu-id="c96e8-234">System-Only</span></span>            | <span data-ttu-id="c96e8-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-235">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-236">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c96e8-236">Is-Single-Valued</span></span>       | <span data-ttu-id="c96e8-237">True</span><span class="sxs-lookup"><span data-stu-id="c96e8-237">True</span></span>                                                                                                                                      |
| <span data-ttu-id="c96e8-238">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c96e8-238">Is Indexed</span></span>             | <span data-ttu-id="c96e8-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-239">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-240">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c96e8-240">In Global Catalog</span></span>      | <span data-ttu-id="c96e8-241">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-241">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-242">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c96e8-242">NT-Security-Descriptor</span></span> | <span data-ttu-id="c96e8-243">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c96e8-243">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="c96e8-244">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c96e8-244">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-245">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c96e8-245">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-246">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-246">Search-Flags</span></span>           | <span data-ttu-id="c96e8-247">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c96e8-247">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-248">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-248">System-Flags</span></span>           | <span data-ttu-id="c96e8-249">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c96e8-249">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-250">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c96e8-250">Classes used in</span></span>        | [<span data-ttu-id="c96e8-251">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c96e8-251">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c96e8-252">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c96e8-252">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c96e8-253">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="c96e8-253">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c96e8-254">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c96e8-254">Windows Server 2012</span></span>



| <span data-ttu-id="c96e8-255">Ввод</span><span class="sxs-lookup"><span data-stu-id="c96e8-255">Entry</span></span> | <span data-ttu-id="c96e8-256">Значение</span><span class="sxs-lookup"><span data-stu-id="c96e8-256">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96e8-257">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="c96e8-257">Link-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-258">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c96e8-258">MAPI-Id</span></span>                | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-259">System-Only</span><span class="sxs-lookup"><span data-stu-id="c96e8-259">System-Only</span></span>            | <span data-ttu-id="c96e8-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-260">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-261">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="c96e8-261">Is-Single-Valued</span></span>       | <span data-ttu-id="c96e8-262">True</span><span class="sxs-lookup"><span data-stu-id="c96e8-262">True</span></span>                                                                                                                                      |
| <span data-ttu-id="c96e8-263">Индексируется</span><span class="sxs-lookup"><span data-stu-id="c96e8-263">Is Indexed</span></span>             | <span data-ttu-id="c96e8-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-264">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-265">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="c96e8-265">In Global Catalog</span></span>      | <span data-ttu-id="c96e8-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="c96e8-266">False</span></span>                                                                                                                                     |
| <span data-ttu-id="c96e8-267">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="c96e8-267">NT-Security-Descriptor</span></span> | <span data-ttu-id="c96e8-268">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="c96e8-268">O:BAG:BAD:S:</span></span>                                                                                                                              |
| <span data-ttu-id="c96e8-269">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c96e8-269">Range-Lower</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-270">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c96e8-270">Range-Upper</span></span>            | \-                                                                                                                                        |
| <span data-ttu-id="c96e8-271">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-271">Search-Flags</span></span>           | <span data-ttu-id="c96e8-272">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c96e8-272">0x00000000</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-273">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c96e8-273">System-Flags</span></span>           | <span data-ttu-id="c96e8-274">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c96e8-274">0x00000010</span></span>                                                                                                                                |
| <span data-ttu-id="c96e8-275">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="c96e8-275">Classes used in</span></span>        | [<span data-ttu-id="c96e8-276">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c96e8-276">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="c96e8-277">**Политика домена**</span><span class="sxs-lookup"><span data-stu-id="c96e8-277">**Domain-Policy**</span></span>](c-domainpolicy.md)<br/> [<span data-ttu-id="c96e8-278">**SAM-домен**</span><span class="sxs-lookup"><span data-stu-id="c96e8-278">**Sam-Domain**</span></span>](c-samdomain.md)<br/> |



 

 





