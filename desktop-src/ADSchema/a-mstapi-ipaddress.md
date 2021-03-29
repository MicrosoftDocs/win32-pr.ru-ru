---
title: атрибут MS-TAPI-IP-Address
description: IP-адреса клиентского компьютера TAPI, в который вошел пользователь. Этот атрибут можно использовать в качестве универсального атрибута для хранения IP-адресов компьютеров.
ms.assetid: 4ea850ad-d54a-4b5f-a37d-68817432d874
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TAPI-IP-Address
- Схема AD атрибута Мстапи-IpAddress
topic_type:
- apiref
api_name:
- ms-TAPI-Ip-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078afde8200468df7e996e096deeef4bfd1b7ec0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989670"
---
# <a name="ms-tapi-ip-address-attribute"></a><span data-ttu-id="a5bd3-106">атрибут MS-TAPI-IP-Address</span><span class="sxs-lookup"><span data-stu-id="a5bd3-106">ms-TAPI-Ip-Address attribute</span></span>

<span data-ttu-id="a5bd3-107">IP-адреса клиентского компьютера TAPI, в который вошел пользователь.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-107">IP addresses of a TAPI client computer that a user is logged into.</span></span> <span data-ttu-id="a5bd3-108">Этот атрибут можно использовать в качестве универсального атрибута для хранения IP-адресов компьютеров.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-108">This attribute can be used as a generic attribute to hold computer IP addresses.</span></span>



| <span data-ttu-id="a5bd3-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5bd3-109">Entry</span></span> | <span data-ttu-id="a5bd3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a5bd3-110">Value</span></span> |
|-------------------|------------------------------------------------------------|
| <span data-ttu-id="a5bd3-111">CN</span><span class="sxs-lookup"><span data-stu-id="a5bd3-111">CN</span></span>                | <span data-ttu-id="a5bd3-112">MS-TAPI-IP-Address</span><span class="sxs-lookup"><span data-stu-id="a5bd3-112">ms-TAPI-Ip-Address</span></span>                                         |
| <span data-ttu-id="a5bd3-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="a5bd3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="a5bd3-114">Мстапи-IpAddress</span><span class="sxs-lookup"><span data-stu-id="a5bd3-114">msTAPI-IpAddress</span></span>                                           |
| <span data-ttu-id="a5bd3-115">Размер</span><span class="sxs-lookup"><span data-stu-id="a5bd3-115">Size</span></span>              | <span data-ttu-id="a5bd3-116">Каждый IP-адрес хранится в виде строки в нотации. B. C. D.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-116">Each IP address is stored as a string in A.B.C.D notation.</span></span> |
| <span data-ttu-id="a5bd3-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="a5bd3-117">Update Privilege</span></span>  | <span data-ttu-id="a5bd3-118">Специальные привилегии не требуются.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-118">No special privileges required.</span></span>                            |
| <span data-ttu-id="a5bd3-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="a5bd3-119">Update Frequency</span></span>  | <span data-ttu-id="a5bd3-120">Обычно очень низкий.</span><span class="sxs-lookup"><span data-stu-id="a5bd3-120">Typically very low.</span></span>                                        |
| <span data-ttu-id="a5bd3-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a5bd3-121">Attribute-Id</span></span>      | <span data-ttu-id="a5bd3-122">1.2.840.113556.1.4.1701</span><span class="sxs-lookup"><span data-stu-id="a5bd3-122">1.2.840.113556.1.4.1701</span></span>                                    |
| <span data-ttu-id="a5bd3-123">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="a5bd3-123">System-Id-Guid</span></span>    | <span data-ttu-id="a5bd3-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span><span class="sxs-lookup"><span data-stu-id="a5bd3-124">efd7d7f7-178e-4767-87fa-f8a16b840544</span></span>                       |
| <span data-ttu-id="a5bd3-125">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5bd3-125">Syntax</span></span>            | [<span data-ttu-id="a5bd3-126">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-126">**String(Unicode)**</span></span>](s-string-unicode.md)                |



## <a name="implementations"></a><span data-ttu-id="a5bd3-127">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="a5bd3-127">Implementations</span></span>

-   [<span data-ttu-id="a5bd3-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a5bd3-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a5bd3-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a5bd3-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a5bd3-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="a5bd3-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a5bd3-133">Windows Server 2003</span></span>



| <span data-ttu-id="a5bd3-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5bd3-134">Entry</span></span> | <span data-ttu-id="a5bd3-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a5bd3-135">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a5bd3-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5bd3-136">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5bd3-137">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5bd3-138">System-Only</span></span>            | <span data-ttu-id="a5bd3-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-139">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5bd3-140">Is-Single-Valued</span></span>       | <span data-ttu-id="a5bd3-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-141">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5bd3-142">Is Indexed</span></span>             | <span data-ttu-id="a5bd3-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-143">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5bd3-144">In Global Catalog</span></span>      | <span data-ttu-id="a5bd3-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-145">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5bd3-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5bd3-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5bd3-147">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a5bd3-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5bd3-148">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-149">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5bd3-149">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-150">Search-Flags</span></span>           | <span data-ttu-id="a5bd3-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5bd3-151">0x00000000</span></span>                                                |
| <span data-ttu-id="a5bd3-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-152">System-Flags</span></span>           | <span data-ttu-id="a5bd3-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5bd3-153">0x00000010</span></span>                                                |
| <span data-ttu-id="a5bd3-154">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5bd3-154">Classes used in</span></span>        | [<span data-ttu-id="a5bd3-155">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-155">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a5bd3-156">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a5bd3-156">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a5bd3-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5bd3-157">Entry</span></span> | <span data-ttu-id="a5bd3-158">Значение</span><span class="sxs-lookup"><span data-stu-id="a5bd3-158">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a5bd3-159">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5bd3-159">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5bd3-160">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5bd3-161">System-Only</span></span>            | <span data-ttu-id="a5bd3-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-162">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5bd3-163">Is-Single-Valued</span></span>       | <span data-ttu-id="a5bd3-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-164">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5bd3-165">Is Indexed</span></span>             | <span data-ttu-id="a5bd3-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-166">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5bd3-167">In Global Catalog</span></span>      | <span data-ttu-id="a5bd3-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-168">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5bd3-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5bd3-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5bd3-170">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a5bd3-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5bd3-171">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-172">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5bd3-172">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-173">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-173">Search-Flags</span></span>           | <span data-ttu-id="a5bd3-174">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5bd3-174">0x00000000</span></span>                                                |
| <span data-ttu-id="a5bd3-175">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-175">System-Flags</span></span>           | <span data-ttu-id="a5bd3-176">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5bd3-176">0x00000010</span></span>                                                |
| <span data-ttu-id="a5bd3-177">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5bd3-177">Classes used in</span></span>        | [<span data-ttu-id="a5bd3-178">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-178">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a5bd3-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5bd3-179">Windows Server 2008</span></span>



| <span data-ttu-id="a5bd3-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5bd3-180">Entry</span></span> | <span data-ttu-id="a5bd3-181">Значение</span><span class="sxs-lookup"><span data-stu-id="a5bd3-181">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a5bd3-182">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5bd3-182">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-183">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5bd3-183">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-184">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5bd3-184">System-Only</span></span>            | <span data-ttu-id="a5bd3-185">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-185">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-186">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5bd3-186">Is-Single-Valued</span></span>       | <span data-ttu-id="a5bd3-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-187">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-188">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5bd3-188">Is Indexed</span></span>             | <span data-ttu-id="a5bd3-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-189">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-190">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5bd3-190">In Global Catalog</span></span>      | <span data-ttu-id="a5bd3-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-191">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-192">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5bd3-192">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5bd3-193">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5bd3-193">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a5bd3-194">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5bd3-194">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-195">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5bd3-195">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-196">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-196">Search-Flags</span></span>           | <span data-ttu-id="a5bd3-197">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5bd3-197">0x00000000</span></span>                                                |
| <span data-ttu-id="a5bd3-198">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-198">System-Flags</span></span>           | <span data-ttu-id="a5bd3-199">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5bd3-199">0x00000010</span></span>                                                |
| <span data-ttu-id="a5bd3-200">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5bd3-200">Classes used in</span></span>        | [<span data-ttu-id="a5bd3-201">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-201">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a5bd3-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5bd3-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a5bd3-203">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5bd3-203">Entry</span></span> | <span data-ttu-id="a5bd3-204">Значение</span><span class="sxs-lookup"><span data-stu-id="a5bd3-204">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a5bd3-205">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5bd3-205">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5bd3-206">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5bd3-207">System-Only</span></span>            | <span data-ttu-id="a5bd3-208">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-208">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-209">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5bd3-209">Is-Single-Valued</span></span>       | <span data-ttu-id="a5bd3-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-210">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-211">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5bd3-211">Is Indexed</span></span>             | <span data-ttu-id="a5bd3-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-212">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-213">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5bd3-213">In Global Catalog</span></span>      | <span data-ttu-id="a5bd3-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-214">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-215">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5bd3-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5bd3-216">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5bd3-216">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a5bd3-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5bd3-217">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5bd3-218">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-219">Search-Flags</span></span>           | <span data-ttu-id="a5bd3-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5bd3-220">0x00000000</span></span>                                                |
| <span data-ttu-id="a5bd3-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-221">System-Flags</span></span>           | <span data-ttu-id="a5bd3-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5bd3-222">0x00000010</span></span>                                                |
| <span data-ttu-id="a5bd3-223">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5bd3-223">Classes used in</span></span>        | [<span data-ttu-id="a5bd3-224">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-224">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a5bd3-225">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a5bd3-225">Windows Server 2012</span></span>



| <span data-ttu-id="a5bd3-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="a5bd3-226">Entry</span></span> | <span data-ttu-id="a5bd3-227">Значение</span><span class="sxs-lookup"><span data-stu-id="a5bd3-227">Value</span></span> |
|------------------------|-----------------------------------------------------------|
| <span data-ttu-id="a5bd3-228">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="a5bd3-228">Link-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-229">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a5bd3-229">MAPI-Id</span></span>                | \-                                                        |
| <span data-ttu-id="a5bd3-230">System-Only</span><span class="sxs-lookup"><span data-stu-id="a5bd3-230">System-Only</span></span>            | <span data-ttu-id="a5bd3-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-231">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-232">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="a5bd3-232">Is-Single-Valued</span></span>       | <span data-ttu-id="a5bd3-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-233">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-234">Индексируется</span><span class="sxs-lookup"><span data-stu-id="a5bd3-234">Is Indexed</span></span>             | <span data-ttu-id="a5bd3-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-235">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-236">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="a5bd3-236">In Global Catalog</span></span>      | <span data-ttu-id="a5bd3-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5bd3-237">False</span></span>                                                     |
| <span data-ttu-id="a5bd3-238">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="a5bd3-238">NT-Security-Descriptor</span></span> | <span data-ttu-id="a5bd3-239">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="a5bd3-239">O:BAG:BAD:S:</span></span>                                              |
| <span data-ttu-id="a5bd3-240">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a5bd3-240">Range-Lower</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-241">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a5bd3-241">Range-Upper</span></span>            | \-                                                        |
| <span data-ttu-id="a5bd3-242">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-242">Search-Flags</span></span>           | <span data-ttu-id="a5bd3-243">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a5bd3-243">0x00000000</span></span>                                                |
| <span data-ttu-id="a5bd3-244">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a5bd3-244">System-Flags</span></span>           | <span data-ttu-id="a5bd3-245">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a5bd3-245">0x00000010</span></span>                                                |
| <span data-ttu-id="a5bd3-246">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="a5bd3-246">Classes used in</span></span>        | [<span data-ttu-id="a5bd3-247">**MS-TAPI-RT-Person**</span><span class="sxs-lookup"><span data-stu-id="a5bd3-247">**ms-TAPI-Rt-Person**</span></span>](c-mstapi-rtperson.md)<br/> |



 

 





