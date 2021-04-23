---
title: Нетбут-Machine-File-путь атрибут
description: Этот атрибут указывает сервер, который отвечает клиенту. Начиная с операционной системы Windows Server 2003, она может указывать Startrom.com, которые получает клиент.
ms.assetid: 8706bf38-8027-4260-b382-4d4c2a6e0f6e
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута нетбут-Machine-File-Path
- Схема AD атрибута Нетбутмачинефилепас
topic_type:
- apiref
api_name:
- Netboot-Machine-File-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d03ead4f307b7c0b524192d9c865ee437fbd9d2
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655109"
---
# <a name="netboot-machine-file-path-attribute"></a><span data-ttu-id="552b7-106">Нетбут-Machine-File-путь атрибут</span><span class="sxs-lookup"><span data-stu-id="552b7-106">Netboot-Machine-File-Path attribute</span></span>

<span data-ttu-id="552b7-107">Этот атрибут указывает сервер, который отвечает клиенту.</span><span class="sxs-lookup"><span data-stu-id="552b7-107">This attribute specifies the server that answers the client.</span></span> <span data-ttu-id="552b7-108">Начиная с операционной системы Windows Server 2003, она может указывать Startrom.com, которые получает клиент.</span><span class="sxs-lookup"><span data-stu-id="552b7-108">Beginning with the Windows Server 2003 operating system, it can indicate the Startrom.com that the client gets.</span></span>



| <span data-ttu-id="552b7-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="552b7-109">Entry</span></span> | <span data-ttu-id="552b7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="552b7-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="552b7-111">CN</span><span class="sxs-lookup"><span data-stu-id="552b7-111">CN</span></span>                | <span data-ttu-id="552b7-112">Нетбут-Machine-File-Path</span><span class="sxs-lookup"><span data-stu-id="552b7-112">Netboot-Machine-File-Path</span></span>                   |
| <span data-ttu-id="552b7-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="552b7-113">Ldap-Display-Name</span></span> | <span data-ttu-id="552b7-114">нетбутмачинефилепас</span><span class="sxs-lookup"><span data-stu-id="552b7-114">netbootMachineFilePath</span></span>                      |
| <span data-ttu-id="552b7-115">Размер</span><span class="sxs-lookup"><span data-stu-id="552b7-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="552b7-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="552b7-116">Update Privilege</span></span>  | <span data-ttu-id="552b7-117">Это значение задается системой.</span><span class="sxs-lookup"><span data-stu-id="552b7-117">This value is set by the system.</span></span>            |
| <span data-ttu-id="552b7-118">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="552b7-118">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="552b7-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="552b7-119">Attribute-Id</span></span>      | <span data-ttu-id="552b7-120">1.2.840.113556.1.4.361</span><span class="sxs-lookup"><span data-stu-id="552b7-120">1.2.840.113556.1.4.361</span></span>                      |
| <span data-ttu-id="552b7-121">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="552b7-121">System-Id-Guid</span></span>    | <span data-ttu-id="552b7-122">3e978923-8c01-11d0-afda-00c04fd930c9</span><span class="sxs-lookup"><span data-stu-id="552b7-122">3e978923-8c01-11d0-afda-00c04fd930c9</span></span>        |
| <span data-ttu-id="552b7-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="552b7-123">Syntax</span></span>            | [<span data-ttu-id="552b7-124">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="552b7-124">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="552b7-125">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="552b7-125">Implementations</span></span>

-   [<span data-ttu-id="552b7-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="552b7-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="552b7-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="552b7-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="552b7-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="552b7-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="552b7-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="552b7-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="552b7-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="552b7-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="552b7-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="552b7-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="552b7-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="552b7-132">Windows 2000 Server</span></span>



| <span data-ttu-id="552b7-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="552b7-133">Entry</span></span> | <span data-ttu-id="552b7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="552b7-134">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552b7-135">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="552b7-135">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="552b7-136">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="552b7-137">System-Only</span></span>            | <span data-ttu-id="552b7-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-138">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-139">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="552b7-139">Is-Single-Valued</span></span>       | <span data-ttu-id="552b7-140">True</span><span class="sxs-lookup"><span data-stu-id="552b7-140">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-141">Индексируется</span><span class="sxs-lookup"><span data-stu-id="552b7-141">Is Indexed</span></span>             | <span data-ttu-id="552b7-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-142">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-143">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="552b7-143">In Global Catalog</span></span>      | <span data-ttu-id="552b7-144">True</span><span class="sxs-lookup"><span data-stu-id="552b7-144">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-145">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="552b7-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="552b7-146">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="552b7-146">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="552b7-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="552b7-147">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="552b7-148">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-149">Search-Flags</span></span>           | <span data-ttu-id="552b7-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="552b7-150">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="552b7-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-151">System-Flags</span></span>           | <span data-ttu-id="552b7-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="552b7-152">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="552b7-153">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="552b7-153">Classes used in</span></span>        | [<span data-ttu-id="552b7-154">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="552b7-154">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="552b7-155">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="552b7-155">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="552b7-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="552b7-156">Windows Server 2003</span></span>



| <span data-ttu-id="552b7-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="552b7-157">Entry</span></span> | <span data-ttu-id="552b7-158">Значение</span><span class="sxs-lookup"><span data-stu-id="552b7-158">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552b7-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="552b7-159">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="552b7-160">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="552b7-161">System-Only</span></span>            | <span data-ttu-id="552b7-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-162">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="552b7-163">Is-Single-Valued</span></span>       | <span data-ttu-id="552b7-164">True</span><span class="sxs-lookup"><span data-stu-id="552b7-164">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="552b7-165">Is Indexed</span></span>             | <span data-ttu-id="552b7-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-166">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="552b7-167">In Global Catalog</span></span>      | <span data-ttu-id="552b7-168">True</span><span class="sxs-lookup"><span data-stu-id="552b7-168">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="552b7-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="552b7-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="552b7-170">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="552b7-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="552b7-171">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="552b7-172">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-173">Search-Flags</span></span>           | <span data-ttu-id="552b7-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="552b7-174">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="552b7-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-175">System-Flags</span></span>           | <span data-ttu-id="552b7-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="552b7-176">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="552b7-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="552b7-177">Classes used in</span></span>        | [<span data-ttu-id="552b7-178">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="552b7-178">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="552b7-179">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="552b7-179">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="552b7-180">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="552b7-180">Windows Server 2003 R2</span></span>



| <span data-ttu-id="552b7-181">Ввод</span><span class="sxs-lookup"><span data-stu-id="552b7-181">Entry</span></span> | <span data-ttu-id="552b7-182">Значение</span><span class="sxs-lookup"><span data-stu-id="552b7-182">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552b7-183">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="552b7-183">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-184">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="552b7-184">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-185">System-Only</span><span class="sxs-lookup"><span data-stu-id="552b7-185">System-Only</span></span>            | <span data-ttu-id="552b7-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-186">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-187">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="552b7-187">Is-Single-Valued</span></span>       | <span data-ttu-id="552b7-188">True</span><span class="sxs-lookup"><span data-stu-id="552b7-188">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-189">Индексируется</span><span class="sxs-lookup"><span data-stu-id="552b7-189">Is Indexed</span></span>             | <span data-ttu-id="552b7-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-190">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-191">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="552b7-191">In Global Catalog</span></span>      | <span data-ttu-id="552b7-192">True</span><span class="sxs-lookup"><span data-stu-id="552b7-192">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-193">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="552b7-193">NT-Security-Descriptor</span></span> | <span data-ttu-id="552b7-194">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="552b7-194">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="552b7-195">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="552b7-195">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-196">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="552b7-196">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-197">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-197">Search-Flags</span></span>           | <span data-ttu-id="552b7-198">0x00000000</span><span class="sxs-lookup"><span data-stu-id="552b7-198">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="552b7-199">System-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-199">System-Flags</span></span>           | <span data-ttu-id="552b7-200">0x00000010</span><span class="sxs-lookup"><span data-stu-id="552b7-200">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="552b7-201">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="552b7-201">Classes used in</span></span>        | [<span data-ttu-id="552b7-202">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="552b7-202">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="552b7-203">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="552b7-203">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="552b7-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="552b7-204">Windows Server 2008</span></span>



| <span data-ttu-id="552b7-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="552b7-205">Entry</span></span> | <span data-ttu-id="552b7-206">Значение</span><span class="sxs-lookup"><span data-stu-id="552b7-206">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552b7-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="552b7-207">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="552b7-208">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="552b7-209">System-Only</span></span>            | <span data-ttu-id="552b7-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-210">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="552b7-211">Is-Single-Valued</span></span>       | <span data-ttu-id="552b7-212">True</span><span class="sxs-lookup"><span data-stu-id="552b7-212">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="552b7-213">Is Indexed</span></span>             | <span data-ttu-id="552b7-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-214">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="552b7-215">In Global Catalog</span></span>      | <span data-ttu-id="552b7-216">True</span><span class="sxs-lookup"><span data-stu-id="552b7-216">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="552b7-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="552b7-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="552b7-218">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="552b7-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="552b7-219">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="552b7-220">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-221">Search-Flags</span></span>           | <span data-ttu-id="552b7-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="552b7-222">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="552b7-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-223">System-Flags</span></span>           | <span data-ttu-id="552b7-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="552b7-224">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="552b7-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="552b7-225">Classes used in</span></span>        | [<span data-ttu-id="552b7-226">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="552b7-226">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="552b7-227">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="552b7-227">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="552b7-228">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="552b7-228">Windows Server 2008 R2</span></span>



| <span data-ttu-id="552b7-229">Ввод</span><span class="sxs-lookup"><span data-stu-id="552b7-229">Entry</span></span> | <span data-ttu-id="552b7-230">Значение</span><span class="sxs-lookup"><span data-stu-id="552b7-230">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552b7-231">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="552b7-231">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-232">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="552b7-232">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-233">System-Only</span><span class="sxs-lookup"><span data-stu-id="552b7-233">System-Only</span></span>            | <span data-ttu-id="552b7-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-234">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-235">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="552b7-235">Is-Single-Valued</span></span>       | <span data-ttu-id="552b7-236">True</span><span class="sxs-lookup"><span data-stu-id="552b7-236">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-237">Индексируется</span><span class="sxs-lookup"><span data-stu-id="552b7-237">Is Indexed</span></span>             | <span data-ttu-id="552b7-238">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-238">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-239">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="552b7-239">In Global Catalog</span></span>      | <span data-ttu-id="552b7-240">True</span><span class="sxs-lookup"><span data-stu-id="552b7-240">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-241">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="552b7-241">NT-Security-Descriptor</span></span> | <span data-ttu-id="552b7-242">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="552b7-242">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="552b7-243">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="552b7-243">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-244">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="552b7-244">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-245">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-245">Search-Flags</span></span>           | <span data-ttu-id="552b7-246">0x00000000</span><span class="sxs-lookup"><span data-stu-id="552b7-246">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="552b7-247">System-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-247">System-Flags</span></span>           | <span data-ttu-id="552b7-248">0x00000010</span><span class="sxs-lookup"><span data-stu-id="552b7-248">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="552b7-249">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="552b7-249">Classes used in</span></span>        | [<span data-ttu-id="552b7-250">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="552b7-250">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="552b7-251">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="552b7-251">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="552b7-252">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="552b7-252">Windows Server 2012</span></span>



| <span data-ttu-id="552b7-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="552b7-253">Entry</span></span> | <span data-ttu-id="552b7-254">Значение</span><span class="sxs-lookup"><span data-stu-id="552b7-254">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552b7-255">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="552b7-255">Link-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-256">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="552b7-256">MAPI-Id</span></span>                | \-                                                                                                   |
| <span data-ttu-id="552b7-257">System-Only</span><span class="sxs-lookup"><span data-stu-id="552b7-257">System-Only</span></span>            | <span data-ttu-id="552b7-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-258">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-259">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="552b7-259">Is-Single-Valued</span></span>       | <span data-ttu-id="552b7-260">True</span><span class="sxs-lookup"><span data-stu-id="552b7-260">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-261">Индексируется</span><span class="sxs-lookup"><span data-stu-id="552b7-261">Is Indexed</span></span>             | <span data-ttu-id="552b7-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="552b7-262">False</span></span>                                                                                                |
| <span data-ttu-id="552b7-263">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="552b7-263">In Global Catalog</span></span>      | <span data-ttu-id="552b7-264">True</span><span class="sxs-lookup"><span data-stu-id="552b7-264">True</span></span>                                                                                                 |
| <span data-ttu-id="552b7-265">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="552b7-265">NT-Security-Descriptor</span></span> | <span data-ttu-id="552b7-266">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="552b7-266">O:BAG:BAD:S:</span></span>                                                                                         |
| <span data-ttu-id="552b7-267">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="552b7-267">Range-Lower</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-268">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="552b7-268">Range-Upper</span></span>            | \-                                                                                                   |
| <span data-ttu-id="552b7-269">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-269">Search-Flags</span></span>           | <span data-ttu-id="552b7-270">0x00000000</span><span class="sxs-lookup"><span data-stu-id="552b7-270">0x00000000</span></span>                                                                                           |
| <span data-ttu-id="552b7-271">System-Flags</span><span class="sxs-lookup"><span data-stu-id="552b7-271">System-Flags</span></span>           | <span data-ttu-id="552b7-272">0x00000010</span><span class="sxs-lookup"><span data-stu-id="552b7-272">0x00000010</span></span>                                                                                           |
| <span data-ttu-id="552b7-273">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="552b7-273">Classes used in</span></span>        | [<span data-ttu-id="552b7-274">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="552b7-274">**Computer**</span></span>](c-computer.md)<br/> [<span data-ttu-id="552b7-275">**IntelliMirror — SCP**</span><span class="sxs-lookup"><span data-stu-id="552b7-275">**Intellimirror-SCP**</span></span>](c-intellimirrorscp.md)<br/> |



 

 





