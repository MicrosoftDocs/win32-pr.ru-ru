---
title: атрибут MS-TAPI-Conference-BLOB
description: Двоичный BLOB-объект данных, описывающий различные свойства многоадресной конференции TAPI. Его формат и содержимое определяются значением атрибута Protocol-Id в том же объекте. Как правило, данные в этом большом двоичном объекте преобразуются в RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TAPI-Conference-BLOB
- Схема AD атрибута Мстапи-Конференцеблоб
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655363"
---
# <a name="ms-tapi-conference-blob-attribute"></a><span data-ttu-id="9fde9-107">атрибут MS-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="9fde9-107">ms-TAPI-Conference-Blob attribute</span></span>

<span data-ttu-id="9fde9-108">Двоичный BLOB-объект данных, описывающий различные свойства многоадресной конференции TAPI.</span><span class="sxs-lookup"><span data-stu-id="9fde9-108">A binary BLOB of data that describes various properties of a TAPI multicast conference.</span></span> <span data-ttu-id="9fde9-109">Его формат и содержимое определяются значением атрибута Protocol-Id в том же объекте.</span><span class="sxs-lookup"><span data-stu-id="9fde9-109">Its format and content are determined by the value of the attribute Protocol-Id in the same object.</span></span> <span data-ttu-id="9fde9-110">Как правило, данные в этом большом двоичном объекте преобразуются в RFC2327.</span><span class="sxs-lookup"><span data-stu-id="9fde9-110">Typically, the data in this BLOB conforms to RFC2327.</span></span>



| <span data-ttu-id="9fde9-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fde9-111">Entry</span></span> | <span data-ttu-id="9fde9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9fde9-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fde9-113">CN</span><span class="sxs-lookup"><span data-stu-id="9fde9-113">CN</span></span>                | <span data-ttu-id="9fde9-114">MS-TAPI-Conference-BLOB</span><span class="sxs-lookup"><span data-stu-id="9fde9-114">ms-TAPI-Conference-Blob</span></span>                                                                                      |
| <span data-ttu-id="9fde9-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="9fde9-115">Ldap-Display-Name</span></span> | <span data-ttu-id="9fde9-116">Мстапи — Конференцеблоб</span><span class="sxs-lookup"><span data-stu-id="9fde9-116">msTAPI-ConferenceBlob</span></span>                                                                                        |
| <span data-ttu-id="9fde9-117">Размер</span><span class="sxs-lookup"><span data-stu-id="9fde9-117">Size</span></span>              | <span data-ttu-id="9fde9-118">Может иметь произвольную длину.</span><span class="sxs-lookup"><span data-stu-id="9fde9-118">Can be of arbitrary length.</span></span>                                                                                  |
| <span data-ttu-id="9fde9-119">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="9fde9-119">Update Privilege</span></span>  | <span data-ttu-id="9fde9-120">Специальные привилегии не требуются.</span><span class="sxs-lookup"><span data-stu-id="9fde9-120">No special privileges required.</span></span>                                                                              |
| <span data-ttu-id="9fde9-121">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="9fde9-121">Update Frequency</span></span>  | <span data-ttu-id="9fde9-122">Может измениться на усмотрение владельца конференции TAPI, когда необходимо изменить некоторые данные о Конференции.</span><span class="sxs-lookup"><span data-stu-id="9fde9-122">Can change at the discretion of a TAPI conference owner when some data about the conference needs to change.</span></span> |
| <span data-ttu-id="9fde9-123">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="9fde9-123">Attribute-Id</span></span>      | <span data-ttu-id="9fde9-124">1.2.840.113556.1.4.1700</span><span class="sxs-lookup"><span data-stu-id="9fde9-124">1.2.840.113556.1.4.1700</span></span>                                                                                      |
| <span data-ttu-id="9fde9-125">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="9fde9-125">System-Id-Guid</span></span>    | <span data-ttu-id="9fde9-126">4cc4601e-7201-4141-abc8-3e529ae88863</span><span class="sxs-lookup"><span data-stu-id="9fde9-126">4cc4601e-7201-4141-abc8-3e529ae88863</span></span>                                                                         |
| <span data-ttu-id="9fde9-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fde9-127">Syntax</span></span>            | [<span data-ttu-id="9fde9-128">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="9fde9-128">**Object(Replica-Link)**</span></span>](s-object-replica-link.md)                                                        |



## <a name="implementations"></a><span data-ttu-id="9fde9-129">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="9fde9-129">Implementations</span></span>

-   [<span data-ttu-id="9fde9-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="9fde9-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="9fde9-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="9fde9-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="9fde9-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="9fde9-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="9fde9-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="9fde9-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="9fde9-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="9fde9-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="9fde9-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9fde9-135">Windows Server 2003</span></span>



| <span data-ttu-id="9fde9-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fde9-136">Entry</span></span> | <span data-ttu-id="9fde9-137">Значение</span><span class="sxs-lookup"><span data-stu-id="9fde9-137">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fde9-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fde9-138">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fde9-139">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fde9-140">System-Only</span></span>            | <span data-ttu-id="9fde9-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-141">False</span></span>                                                             |
| <span data-ttu-id="9fde9-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fde9-142">Is-Single-Valued</span></span>       | <span data-ttu-id="9fde9-143">True</span><span class="sxs-lookup"><span data-stu-id="9fde9-143">True</span></span>                                                              |
| <span data-ttu-id="9fde9-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fde9-144">Is Indexed</span></span>             | <span data-ttu-id="9fde9-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-145">False</span></span>                                                             |
| <span data-ttu-id="9fde9-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fde9-146">In Global Catalog</span></span>      | <span data-ttu-id="9fde9-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-147">False</span></span>                                                             |
| <span data-ttu-id="9fde9-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fde9-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fde9-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fde9-149">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fde9-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fde9-150">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fde9-151">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-152">Search-Flags</span></span>           | <span data-ttu-id="9fde9-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fde9-153">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fde9-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-154">System-Flags</span></span>           | <span data-ttu-id="9fde9-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fde9-155">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fde9-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fde9-156">Classes used in</span></span>        | [<span data-ttu-id="9fde9-157">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fde9-157">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="9fde9-158">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="9fde9-158">Windows Server 2003 R2</span></span>



| <span data-ttu-id="9fde9-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fde9-159">Entry</span></span> | <span data-ttu-id="9fde9-160">Значение</span><span class="sxs-lookup"><span data-stu-id="9fde9-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fde9-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fde9-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fde9-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fde9-163">System-Only</span></span>            | <span data-ttu-id="9fde9-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-164">False</span></span>                                                             |
| <span data-ttu-id="9fde9-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fde9-165">Is-Single-Valued</span></span>       | <span data-ttu-id="9fde9-166">True</span><span class="sxs-lookup"><span data-stu-id="9fde9-166">True</span></span>                                                              |
| <span data-ttu-id="9fde9-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fde9-167">Is Indexed</span></span>             | <span data-ttu-id="9fde9-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-168">False</span></span>                                                             |
| <span data-ttu-id="9fde9-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fde9-169">In Global Catalog</span></span>      | <span data-ttu-id="9fde9-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-170">False</span></span>                                                             |
| <span data-ttu-id="9fde9-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fde9-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fde9-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fde9-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fde9-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fde9-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fde9-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-175">Search-Flags</span></span>           | <span data-ttu-id="9fde9-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fde9-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fde9-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-177">System-Flags</span></span>           | <span data-ttu-id="9fde9-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fde9-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fde9-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fde9-179">Classes used in</span></span>        | [<span data-ttu-id="9fde9-180">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fde9-180">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="9fde9-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fde9-181">Windows Server 2008</span></span>



| <span data-ttu-id="9fde9-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fde9-182">Entry</span></span> | <span data-ttu-id="9fde9-183">Значение</span><span class="sxs-lookup"><span data-stu-id="9fde9-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fde9-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fde9-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fde9-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fde9-186">System-Only</span></span>            | <span data-ttu-id="9fde9-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-187">False</span></span>                                                             |
| <span data-ttu-id="9fde9-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fde9-188">Is-Single-Valued</span></span>       | <span data-ttu-id="9fde9-189">True</span><span class="sxs-lookup"><span data-stu-id="9fde9-189">True</span></span>                                                              |
| <span data-ttu-id="9fde9-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fde9-190">Is Indexed</span></span>             | <span data-ttu-id="9fde9-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-191">False</span></span>                                                             |
| <span data-ttu-id="9fde9-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fde9-192">In Global Catalog</span></span>      | <span data-ttu-id="9fde9-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-193">False</span></span>                                                             |
| <span data-ttu-id="9fde9-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fde9-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fde9-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fde9-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fde9-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fde9-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fde9-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-198">Search-Flags</span></span>           | <span data-ttu-id="9fde9-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fde9-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fde9-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-200">System-Flags</span></span>           | <span data-ttu-id="9fde9-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fde9-201">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fde9-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fde9-202">Classes used in</span></span>        | [<span data-ttu-id="9fde9-203">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fde9-203">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="9fde9-204">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9fde9-204">Windows Server 2008 R2</span></span>



| <span data-ttu-id="9fde9-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fde9-205">Entry</span></span> | <span data-ttu-id="9fde9-206">Значение</span><span class="sxs-lookup"><span data-stu-id="9fde9-206">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fde9-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fde9-207">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fde9-208">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fde9-209">System-Only</span></span>            | <span data-ttu-id="9fde9-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-210">False</span></span>                                                             |
| <span data-ttu-id="9fde9-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fde9-211">Is-Single-Valued</span></span>       | <span data-ttu-id="9fde9-212">True</span><span class="sxs-lookup"><span data-stu-id="9fde9-212">True</span></span>                                                              |
| <span data-ttu-id="9fde9-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fde9-213">Is Indexed</span></span>             | <span data-ttu-id="9fde9-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-214">False</span></span>                                                             |
| <span data-ttu-id="9fde9-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fde9-215">In Global Catalog</span></span>      | <span data-ttu-id="9fde9-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-216">False</span></span>                                                             |
| <span data-ttu-id="9fde9-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fde9-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fde9-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fde9-218">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fde9-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fde9-219">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fde9-220">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-221">Search-Flags</span></span>           | <span data-ttu-id="9fde9-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fde9-222">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fde9-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-223">System-Flags</span></span>           | <span data-ttu-id="9fde9-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fde9-224">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fde9-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fde9-225">Classes used in</span></span>        | [<span data-ttu-id="9fde9-226">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fde9-226">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="9fde9-227">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9fde9-227">Windows Server 2012</span></span>



| <span data-ttu-id="9fde9-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="9fde9-228">Entry</span></span> | <span data-ttu-id="9fde9-229">Значение</span><span class="sxs-lookup"><span data-stu-id="9fde9-229">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9fde9-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="9fde9-230">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="9fde9-231">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="9fde9-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="9fde9-232">System-Only</span></span>            | <span data-ttu-id="9fde9-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-233">False</span></span>                                                             |
| <span data-ttu-id="9fde9-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="9fde9-234">Is-Single-Valued</span></span>       | <span data-ttu-id="9fde9-235">True</span><span class="sxs-lookup"><span data-stu-id="9fde9-235">True</span></span>                                                              |
| <span data-ttu-id="9fde9-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="9fde9-236">Is Indexed</span></span>             | <span data-ttu-id="9fde9-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-237">False</span></span>                                                             |
| <span data-ttu-id="9fde9-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="9fde9-238">In Global Catalog</span></span>      | <span data-ttu-id="9fde9-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="9fde9-239">False</span></span>                                                             |
| <span data-ttu-id="9fde9-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="9fde9-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="9fde9-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="9fde9-241">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="9fde9-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="9fde9-242">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="9fde9-243">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="9fde9-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-244">Search-Flags</span></span>           | <span data-ttu-id="9fde9-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9fde9-245">0x00000000</span></span>                                                        |
| <span data-ttu-id="9fde9-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="9fde9-246">System-Flags</span></span>           | <span data-ttu-id="9fde9-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="9fde9-247">0x00000010</span></span>                                                        |
| <span data-ttu-id="9fde9-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="9fde9-248">Classes used in</span></span>        | [<span data-ttu-id="9fde9-249">**MS-TAPI-RT-Конференция**</span><span class="sxs-lookup"><span data-stu-id="9fde9-249">**ms-TAPI-Rt-Conference**</span></span>](c-mstapi-rtconference.md)<br/> |



 

 





