---
title: Атрибут Instance-Type
description: Значение битов, определяющее способ создания объекта на определенном сервере.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Instance-Type
- Схема AD атрибута instanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804775"
---
# <a name="instance-type-attribute"></a><span data-ttu-id="9ca2a-105">Атрибут Instance-Type</span><span class="sxs-lookup"><span data-stu-id="9ca2a-105">Instance-Type attribute</span></span>

<span data-ttu-id="9ca2a-106">Значение битов, определяющее способ создания объекта на определенном сервере.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-106">A bitfield that dictates how the object is instantiated on a particular server.</span></span> <span data-ttu-id="9ca2a-107">Значение этого атрибута может отличаться в разных репликах, даже если реплики синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-107">The value of this attribute can differ on different replicas even if the replicas are in sync.</span></span>

<span data-ttu-id="9ca2a-108">Этот атрибут может быть нулевым или сочетанием одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-108">This attribute can be zero or a combination of one or more of the following values.</span></span>

| <span data-ttu-id="9ca2a-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-109">Value</span></span>      | <span data-ttu-id="9ca2a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9ca2a-110">Description</span></span>                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca2a-111">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9ca2a-111">0x00000001</span></span> | <span data-ttu-id="9ca2a-112">Заголовок контекста именования.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-112">The head of naming context.</span></span>                                                                        |
| <span data-ttu-id="9ca2a-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9ca2a-113">0x00000002</span></span> | <span data-ttu-id="9ca2a-114">Экземпляр этой реплики не создан.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-114">This replica is not instantiated.</span></span>                                                                  |
| <span data-ttu-id="9ca2a-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9ca2a-115">0x00000004</span></span> | <span data-ttu-id="9ca2a-116">Объект доступен для записи в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-116">The object is writable on this directory.</span></span>                                                          |
| <span data-ttu-id="9ca2a-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-117">0x00000008</span></span> | <span data-ttu-id="9ca2a-118">Контекст именования, приведенный выше в этом каталоге, удерживается.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-118">The naming context above this one on this directory is held.</span></span>                                       |
| <span data-ttu-id="9ca2a-119">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9ca2a-119">0x00000010</span></span> | <span data-ttu-id="9ca2a-120">Контекст именования находится в процессе, который создается в первый раз с помощью репликации.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-120">The naming context is in the process of being constructed for the first time by using replication.</span></span> |
| <span data-ttu-id="9ca2a-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="9ca2a-121">0x00000020</span></span> | <span data-ttu-id="9ca2a-122">Контекст именования находится в процессе удаления из локального DSA.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-122">The naming context is in the process of being removed from the local DSA.</span></span>                          |



 



| <span data-ttu-id="9ca2a-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-123">Entry</span></span> | <span data-ttu-id="9ca2a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-124">Value</span></span> |
|-------------------|------------------------------------------------|
| <span data-ttu-id="9ca2a-125">CN</span><span class="sxs-lookup"><span data-stu-id="9ca2a-125">CN</span></span>                | <span data-ttu-id="9ca2a-126">Instance-Type</span><span class="sxs-lookup"><span data-stu-id="9ca2a-126">Instance-Type</span></span>                                  |
| <span data-ttu-id="9ca2a-127">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9ca2a-127">Ldap-Display-Name</span></span> | <span data-ttu-id="9ca2a-128">instanceType</span><span class="sxs-lookup"><span data-stu-id="9ca2a-128">instanceType</span></span>                                   |
| <span data-ttu-id="9ca2a-129">Размер</span><span class="sxs-lookup"><span data-stu-id="9ca2a-129">Size</span></span>              | <span data-ttu-id="9ca2a-130">4 байта.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-130">4 bytes.</span></span>                                       |
| <span data-ttu-id="9ca2a-131">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9ca2a-131">Update Privilege</span></span>  | <span data-ttu-id="9ca2a-132">Это значение задается администратором схемы.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-132">This value is set by the schema administrator.</span></span> |
| <span data-ttu-id="9ca2a-133">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9ca2a-133">Update Frequency</span></span>  | <span data-ttu-id="9ca2a-134">При создании объекта.</span><span class="sxs-lookup"><span data-stu-id="9ca2a-134">When the object is created.</span></span>                    |
| <span data-ttu-id="9ca2a-135">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-135">Attribute-Id</span></span>      | <span data-ttu-id="9ca2a-136">1.2.840.113556.1.2.1</span><span class="sxs-lookup"><span data-stu-id="9ca2a-136">1.2.840.113556.1.2.1</span></span>                           |
| <span data-ttu-id="9ca2a-137">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9ca2a-137">System-Id-Guid</span></span>    | <span data-ttu-id="9ca2a-138">bf96798c-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="9ca2a-138">bf96798c-0de6-11d0-a285-00aa003049e2</span></span>           |
| <span data-ttu-id="9ca2a-139">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ca2a-139">Syntax</span></span>            | [<span data-ttu-id="9ca2a-140">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-140">**Enumeration**</span></span>](s-enumeration.md)           |



## <a name="implementations"></a><span data-ttu-id="9ca2a-141">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9ca2a-141">Implementations</span></span>

-   [<span data-ttu-id="9ca2a-142">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-142">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="9ca2a-143">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-143">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9ca2a-144">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-144">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="9ca2a-145">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-145">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9ca2a-146">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-146">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9ca2a-147">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-147">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9ca2a-148">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-148">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="9ca2a-149">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9ca2a-149">Windows 2000 Server</span></span>



| <span data-ttu-id="9ca2a-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-150">Entry</span></span> | <span data-ttu-id="9ca2a-151">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-151">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9ca2a-152">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ca2a-152">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9ca2a-153">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-153">MAPI-Id</span></span>                | <span data-ttu-id="9ca2a-154">0x80BD</span><span class="sxs-lookup"><span data-stu-id="9ca2a-154">0x80BD</span></span>                          |
| <span data-ttu-id="9ca2a-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ca2a-155">System-Only</span></span>            | <span data-ttu-id="9ca2a-156">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-156">True</span></span>                            |
| <span data-ttu-id="9ca2a-157">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ca2a-157">Is-Single-Valued</span></span>       | <span data-ttu-id="9ca2a-158">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-158">True</span></span>                            |
| <span data-ttu-id="9ca2a-159">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ca2a-159">Is Indexed</span></span>             | <span data-ttu-id="9ca2a-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ca2a-160">False</span></span>                           |
| <span data-ttu-id="9ca2a-161">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ca2a-161">In Global Catalog</span></span>      | <span data-ttu-id="9ca2a-162">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-162">True</span></span>                            |
| <span data-ttu-id="9ca2a-163">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ca2a-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ca2a-164">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ca2a-164">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9ca2a-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ca2a-165">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ca2a-166">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-167">Search-Flags</span></span>           | <span data-ttu-id="9ca2a-168">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-168">0x00000008</span></span>                      |
| <span data-ttu-id="9ca2a-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-169">System-Flags</span></span>           | <span data-ttu-id="9ca2a-170">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-170">0x00000012</span></span>                      |
| <span data-ttu-id="9ca2a-171">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ca2a-171">Classes used in</span></span>        | [<span data-ttu-id="9ca2a-172">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-172">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="9ca2a-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9ca2a-173">Windows Server 2003</span></span>



| <span data-ttu-id="9ca2a-174">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-174">Entry</span></span> | <span data-ttu-id="9ca2a-175">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-175">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9ca2a-176">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ca2a-176">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9ca2a-177">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-177">MAPI-Id</span></span>                | <span data-ttu-id="9ca2a-178">0x80BD</span><span class="sxs-lookup"><span data-stu-id="9ca2a-178">0x80BD</span></span>                          |
| <span data-ttu-id="9ca2a-179">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ca2a-179">System-Only</span></span>            | <span data-ttu-id="9ca2a-180">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-180">True</span></span>                            |
| <span data-ttu-id="9ca2a-181">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ca2a-181">Is-Single-Valued</span></span>       | <span data-ttu-id="9ca2a-182">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-182">True</span></span>                            |
| <span data-ttu-id="9ca2a-183">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ca2a-183">Is Indexed</span></span>             | <span data-ttu-id="9ca2a-184">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ca2a-184">False</span></span>                           |
| <span data-ttu-id="9ca2a-185">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ca2a-185">In Global Catalog</span></span>      | <span data-ttu-id="9ca2a-186">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-186">True</span></span>                            |
| <span data-ttu-id="9ca2a-187">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ca2a-187">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ca2a-188">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ca2a-188">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9ca2a-189">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ca2a-189">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-190">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ca2a-190">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-191">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-191">Search-Flags</span></span>           | <span data-ttu-id="9ca2a-192">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-192">0x00000008</span></span>                      |
| <span data-ttu-id="9ca2a-193">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-193">System-Flags</span></span>           | <span data-ttu-id="9ca2a-194">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-194">0x00000012</span></span>                      |
| <span data-ttu-id="9ca2a-195">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ca2a-195">Classes used in</span></span>        | [<span data-ttu-id="9ca2a-196">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-196">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="9ca2a-197">ADAM</span><span class="sxs-lookup"><span data-stu-id="9ca2a-197">ADAM</span></span>



| <span data-ttu-id="9ca2a-198">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-198">Entry</span></span> | <span data-ttu-id="9ca2a-199">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-199">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9ca2a-200">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ca2a-200">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9ca2a-201">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-201">MAPI-Id</span></span>                | <span data-ttu-id="9ca2a-202">0x80BD</span><span class="sxs-lookup"><span data-stu-id="9ca2a-202">0x80BD</span></span>                          |
| <span data-ttu-id="9ca2a-203">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ca2a-203">System-Only</span></span>            | <span data-ttu-id="9ca2a-204">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-204">True</span></span>                            |
| <span data-ttu-id="9ca2a-205">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ca2a-205">Is-Single-Valued</span></span>       | <span data-ttu-id="9ca2a-206">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-206">True</span></span>                            |
| <span data-ttu-id="9ca2a-207">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ca2a-207">Is Indexed</span></span>             | <span data-ttu-id="9ca2a-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ca2a-208">False</span></span>                           |
| <span data-ttu-id="9ca2a-209">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ca2a-209">In Global Catalog</span></span>      | <span data-ttu-id="9ca2a-210">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-210">True</span></span>                            |
| <span data-ttu-id="9ca2a-211">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ca2a-211">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ca2a-212">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ca2a-212">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9ca2a-213">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ca2a-213">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-214">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ca2a-214">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-215">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-215">Search-Flags</span></span>           | <span data-ttu-id="9ca2a-216">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-216">0x00000008</span></span>                      |
| <span data-ttu-id="9ca2a-217">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-217">System-Flags</span></span>           | <span data-ttu-id="9ca2a-218">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-218">0x00000012</span></span>                      |
| <span data-ttu-id="9ca2a-219">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ca2a-219">Classes used in</span></span>        | [<span data-ttu-id="9ca2a-220">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-220">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9ca2a-221">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9ca2a-221">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9ca2a-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-222">Entry</span></span> | <span data-ttu-id="9ca2a-223">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-223">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9ca2a-224">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ca2a-224">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9ca2a-225">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-225">MAPI-Id</span></span>                | <span data-ttu-id="9ca2a-226">0x80BD</span><span class="sxs-lookup"><span data-stu-id="9ca2a-226">0x80BD</span></span>                          |
| <span data-ttu-id="9ca2a-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ca2a-227">System-Only</span></span>            | <span data-ttu-id="9ca2a-228">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-228">True</span></span>                            |
| <span data-ttu-id="9ca2a-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ca2a-229">Is-Single-Valued</span></span>       | <span data-ttu-id="9ca2a-230">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-230">True</span></span>                            |
| <span data-ttu-id="9ca2a-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ca2a-231">Is Indexed</span></span>             | <span data-ttu-id="9ca2a-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ca2a-232">False</span></span>                           |
| <span data-ttu-id="9ca2a-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ca2a-233">In Global Catalog</span></span>      | <span data-ttu-id="9ca2a-234">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-234">True</span></span>                            |
| <span data-ttu-id="9ca2a-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ca2a-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ca2a-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ca2a-236">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9ca2a-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ca2a-237">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ca2a-238">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-239">Search-Flags</span></span>           | <span data-ttu-id="9ca2a-240">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-240">0x00000008</span></span>                      |
| <span data-ttu-id="9ca2a-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-241">System-Flags</span></span>           | <span data-ttu-id="9ca2a-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-242">0x00000012</span></span>                      |
| <span data-ttu-id="9ca2a-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ca2a-243">Classes used in</span></span>        | [<span data-ttu-id="9ca2a-244">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9ca2a-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-245">Windows Server 2008</span></span>



| <span data-ttu-id="9ca2a-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-246">Entry</span></span> | <span data-ttu-id="9ca2a-247">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9ca2a-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ca2a-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9ca2a-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-249">MAPI-Id</span></span>                | <span data-ttu-id="9ca2a-250">0x80BD</span><span class="sxs-lookup"><span data-stu-id="9ca2a-250">0x80BD</span></span>                          |
| <span data-ttu-id="9ca2a-251">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ca2a-251">System-Only</span></span>            | <span data-ttu-id="9ca2a-252">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-252">True</span></span>                            |
| <span data-ttu-id="9ca2a-253">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ca2a-253">Is-Single-Valued</span></span>       | <span data-ttu-id="9ca2a-254">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-254">True</span></span>                            |
| <span data-ttu-id="9ca2a-255">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ca2a-255">Is Indexed</span></span>             | <span data-ttu-id="9ca2a-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ca2a-256">False</span></span>                           |
| <span data-ttu-id="9ca2a-257">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ca2a-257">In Global Catalog</span></span>      | <span data-ttu-id="9ca2a-258">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-258">True</span></span>                            |
| <span data-ttu-id="9ca2a-259">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ca2a-259">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ca2a-260">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ca2a-260">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9ca2a-261">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ca2a-261">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ca2a-262">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-263">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-263">Search-Flags</span></span>           | <span data-ttu-id="9ca2a-264">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-264">0x00000008</span></span>                      |
| <span data-ttu-id="9ca2a-265">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-265">System-Flags</span></span>           | <span data-ttu-id="9ca2a-266">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-266">0x00000012</span></span>                      |
| <span data-ttu-id="9ca2a-267">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ca2a-267">Classes used in</span></span>        | [<span data-ttu-id="9ca2a-268">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-268">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9ca2a-269">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ca2a-269">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9ca2a-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-270">Entry</span></span> | <span data-ttu-id="9ca2a-271">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-271">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9ca2a-272">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ca2a-272">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9ca2a-273">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-273">MAPI-Id</span></span>                | <span data-ttu-id="9ca2a-274">0x80BD</span><span class="sxs-lookup"><span data-stu-id="9ca2a-274">0x80BD</span></span>                          |
| <span data-ttu-id="9ca2a-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ca2a-275">System-Only</span></span>            | <span data-ttu-id="9ca2a-276">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-276">True</span></span>                            |
| <span data-ttu-id="9ca2a-277">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ca2a-277">Is-Single-Valued</span></span>       | <span data-ttu-id="9ca2a-278">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-278">True</span></span>                            |
| <span data-ttu-id="9ca2a-279">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ca2a-279">Is Indexed</span></span>             | <span data-ttu-id="9ca2a-280">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ca2a-280">False</span></span>                           |
| <span data-ttu-id="9ca2a-281">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ca2a-281">In Global Catalog</span></span>      | <span data-ttu-id="9ca2a-282">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-282">True</span></span>                            |
| <span data-ttu-id="9ca2a-283">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ca2a-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ca2a-284">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ca2a-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9ca2a-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ca2a-285">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-286">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ca2a-286">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-287">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-287">Search-Flags</span></span>           | <span data-ttu-id="9ca2a-288">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-288">0x00000008</span></span>                      |
| <span data-ttu-id="9ca2a-289">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-289">System-Flags</span></span>           | <span data-ttu-id="9ca2a-290">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-290">0x00000012</span></span>                      |
| <span data-ttu-id="9ca2a-291">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ca2a-291">Classes used in</span></span>        | [<span data-ttu-id="9ca2a-292">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-292">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9ca2a-293">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-293">Windows Server 2012</span></span>



| <span data-ttu-id="9ca2a-294">Ввод</span><span class="sxs-lookup"><span data-stu-id="9ca2a-294">Entry</span></span> | <span data-ttu-id="9ca2a-295">Значение</span><span class="sxs-lookup"><span data-stu-id="9ca2a-295">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="9ca2a-296">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9ca2a-296">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="9ca2a-297">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9ca2a-297">MAPI-Id</span></span>                | <span data-ttu-id="9ca2a-298">0x80BD</span><span class="sxs-lookup"><span data-stu-id="9ca2a-298">0x80BD</span></span>                          |
| <span data-ttu-id="9ca2a-299">System-Only</span><span class="sxs-lookup"><span data-stu-id="9ca2a-299">System-Only</span></span>            | <span data-ttu-id="9ca2a-300">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-300">True</span></span>                            |
| <span data-ttu-id="9ca2a-301">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9ca2a-301">Is-Single-Valued</span></span>       | <span data-ttu-id="9ca2a-302">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-302">True</span></span>                            |
| <span data-ttu-id="9ca2a-303">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9ca2a-303">Is Indexed</span></span>             | <span data-ttu-id="9ca2a-304">Неверно</span><span class="sxs-lookup"><span data-stu-id="9ca2a-304">False</span></span>                           |
| <span data-ttu-id="9ca2a-305">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9ca2a-305">In Global Catalog</span></span>      | <span data-ttu-id="9ca2a-306">True</span><span class="sxs-lookup"><span data-stu-id="9ca2a-306">True</span></span>                            |
| <span data-ttu-id="9ca2a-307">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9ca2a-307">NT-Security-Descriptor</span></span> | <span data-ttu-id="9ca2a-308">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9ca2a-308">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="9ca2a-309">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9ca2a-309">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-310">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9ca2a-310">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="9ca2a-311">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-311">Search-Flags</span></span>           | <span data-ttu-id="9ca2a-312">0x00000008</span><span class="sxs-lookup"><span data-stu-id="9ca2a-312">0x00000008</span></span>                      |
| <span data-ttu-id="9ca2a-313">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9ca2a-313">System-Flags</span></span>           | <span data-ttu-id="9ca2a-314">0x00000012</span><span class="sxs-lookup"><span data-stu-id="9ca2a-314">0x00000012</span></span>                      |
| <span data-ttu-id="9ca2a-315">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9ca2a-315">Classes used in</span></span>        | [<span data-ttu-id="9ca2a-316">**Вверх**</span><span class="sxs-lookup"><span data-stu-id="9ca2a-316">**Top**</span></span>](c-top.md)<br/> |



 

 





