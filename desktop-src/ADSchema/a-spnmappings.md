---
title: Атрибут SPN-Mappings
description: Этот атрибут с несколькими значениями содержит список имен субъектов-служб (SPN) для отображения эквивалентности типов SPN.
ms.assetid: 6d37618d-426d-4e7b-8475-c912adb595ee
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута SPN-Mappings
- Схема AD атрибута Спнмаппингс
topic_type:
- apiref
api_name:
- SPN-Mappings
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3ccb07e068a22d0a85928832890f0b66ebda016
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536137"
---
# <a name="spn-mappings-attribute"></a><span data-ttu-id="5c7ad-105">Атрибут SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="5c7ad-105">SPN-Mappings attribute</span></span>

<span data-ttu-id="5c7ad-106">Этот атрибут с несколькими значениями содержит список имен субъектов-служб (SPN) для отображения эквивалентности типов SPN.</span><span class="sxs-lookup"><span data-stu-id="5c7ad-106">This multiple-valued attribute contains a list of service principal names (SPN) to show the equivalence of SPN types.</span></span> <span data-ttu-id="5c7ad-107">Имя субъекта-службы является именем, которое клиент использует для уникальной идентификации экземпляра службы.</span><span class="sxs-lookup"><span data-stu-id="5c7ad-107">The SPN is the name a client uses to uniquely identify an instance of a service.</span></span> <span data-ttu-id="5c7ad-108">Если на компьютерах в лесу установлено несколько экземпляров службы, то каждый экземпляр должен иметь свое имя участника-службы.</span><span class="sxs-lookup"><span data-stu-id="5c7ad-108">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="5c7ad-109">Каждый экземпляр службы может иметь несколько имен участников-служб при наличии нескольких имен, которые могут использоваться клиентами для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5c7ad-109">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="5c7ad-110">Например, "LDAP/..." Имена участников-служб можно сопоставить, чтобы они были эквивалентны "Host/...". Участника.</span><span class="sxs-lookup"><span data-stu-id="5c7ad-110">For example, "ldap/..." SPNs could be mapped so that they are equivalent to "host/..." SPNs.</span></span>



| <span data-ttu-id="5c7ad-111">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c7ad-111">Entry</span></span> | <span data-ttu-id="5c7ad-112">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7ad-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7ad-113">CN</span><span class="sxs-lookup"><span data-stu-id="5c7ad-113">CN</span></span>                | <span data-ttu-id="5c7ad-114">SPN-Mappings</span><span class="sxs-lookup"><span data-stu-id="5c7ad-114">SPN-Mappings</span></span>                                                                                                       |
| <span data-ttu-id="5c7ad-115">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="5c7ad-115">Ldap-Display-Name</span></span> | <span data-ttu-id="5c7ad-116">спнмаппингс</span><span class="sxs-lookup"><span data-stu-id="5c7ad-116">sPNMappings</span></span>                                                                                                        |
| <span data-ttu-id="5c7ad-117">Размер</span><span class="sxs-lookup"><span data-stu-id="5c7ad-117">Size</span></span>              | \-                                                                                                                 |
| <span data-ttu-id="5c7ad-118">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="5c7ad-118">Update Privilege</span></span>  | <span data-ttu-id="5c7ad-119">Это значение задается во время установки продукта.</span><span class="sxs-lookup"><span data-stu-id="5c7ad-119">This value is set during the product installation.</span></span> <span data-ttu-id="5c7ad-120">Он может быть изменен системным администратором позже.</span><span class="sxs-lookup"><span data-stu-id="5c7ad-120">It can be modified by the system administrator at a later time.</span></span> |
| <span data-ttu-id="5c7ad-121">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="5c7ad-121">Update Frequency</span></span>  | \-                                                                                                                 |
| <span data-ttu-id="5c7ad-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="5c7ad-122">Attribute-Id</span></span>      | <span data-ttu-id="5c7ad-123">1.2.840.113556.1.4.1347</span><span class="sxs-lookup"><span data-stu-id="5c7ad-123">1.2.840.113556.1.4.1347</span></span>                                                                                            |
| <span data-ttu-id="5c7ad-124">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="5c7ad-124">System-Id-Guid</span></span>    | <span data-ttu-id="5c7ad-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span><span class="sxs-lookup"><span data-stu-id="5c7ad-125">2ab0e76c-7041-11d2-9905-0000f87a57d4</span></span>                                                                               |
| <span data-ttu-id="5c7ad-126">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c7ad-126">Syntax</span></span>            | [<span data-ttu-id="5c7ad-127">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                                        |



## <a name="implementations"></a><span data-ttu-id="5c7ad-128">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="5c7ad-128">Implementations</span></span>

-   [<span data-ttu-id="5c7ad-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="5c7ad-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="5c7ad-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="5c7ad-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="5c7ad-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="5c7ad-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="5c7ad-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5c7ad-135">Windows 2000 Server</span></span>



| <span data-ttu-id="5c7ad-136">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c7ad-136">Entry</span></span> | <span data-ttu-id="5c7ad-137">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7ad-137">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5c7ad-138">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c7ad-138">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c7ad-139">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c7ad-140">System-Only</span></span>            | <span data-ttu-id="5c7ad-141">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-141">False</span></span>                                            |
| <span data-ttu-id="5c7ad-142">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c7ad-142">Is-Single-Valued</span></span>       | <span data-ttu-id="5c7ad-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-143">False</span></span>                                            |
| <span data-ttu-id="5c7ad-144">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c7ad-144">Is Indexed</span></span>             | <span data-ttu-id="5c7ad-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-145">False</span></span>                                            |
| <span data-ttu-id="5c7ad-146">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c7ad-146">In Global Catalog</span></span>      | <span data-ttu-id="5c7ad-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-147">False</span></span>                                            |
| <span data-ttu-id="5c7ad-148">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c7ad-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c7ad-149">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c7ad-149">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5c7ad-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c7ad-150">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c7ad-151">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-152">Search-Flags</span></span>           | <span data-ttu-id="5c7ad-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c7ad-153">0x00000000</span></span>                                       |
| <span data-ttu-id="5c7ad-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-154">System-Flags</span></span>           | <span data-ttu-id="5c7ad-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c7ad-155">0x00000010</span></span>                                       |
| <span data-ttu-id="5c7ad-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c7ad-156">Classes used in</span></span>        | [<span data-ttu-id="5c7ad-157">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-157">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="5c7ad-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5c7ad-158">Windows Server 2003</span></span>



| <span data-ttu-id="5c7ad-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c7ad-159">Entry</span></span> | <span data-ttu-id="5c7ad-160">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7ad-160">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5c7ad-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c7ad-161">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c7ad-162">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c7ad-163">System-Only</span></span>            | <span data-ttu-id="5c7ad-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-164">False</span></span>                                            |
| <span data-ttu-id="5c7ad-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c7ad-165">Is-Single-Valued</span></span>       | <span data-ttu-id="5c7ad-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-166">False</span></span>                                            |
| <span data-ttu-id="5c7ad-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c7ad-167">Is Indexed</span></span>             | <span data-ttu-id="5c7ad-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-168">False</span></span>                                            |
| <span data-ttu-id="5c7ad-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c7ad-169">In Global Catalog</span></span>      | <span data-ttu-id="5c7ad-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-170">False</span></span>                                            |
| <span data-ttu-id="5c7ad-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c7ad-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c7ad-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c7ad-172">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5c7ad-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c7ad-173">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c7ad-174">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-175">Search-Flags</span></span>           | <span data-ttu-id="5c7ad-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c7ad-176">0x00000000</span></span>                                       |
| <span data-ttu-id="5c7ad-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-177">System-Flags</span></span>           | <span data-ttu-id="5c7ad-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c7ad-178">0x00000010</span></span>                                       |
| <span data-ttu-id="5c7ad-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c7ad-179">Classes used in</span></span>        | [<span data-ttu-id="5c7ad-180">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-180">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="5c7ad-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="5c7ad-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="5c7ad-182">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c7ad-182">Entry</span></span> | <span data-ttu-id="5c7ad-183">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7ad-183">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5c7ad-184">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c7ad-184">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c7ad-185">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c7ad-186">System-Only</span></span>            | <span data-ttu-id="5c7ad-187">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-187">False</span></span>                                            |
| <span data-ttu-id="5c7ad-188">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c7ad-188">Is-Single-Valued</span></span>       | <span data-ttu-id="5c7ad-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-189">False</span></span>                                            |
| <span data-ttu-id="5c7ad-190">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c7ad-190">Is Indexed</span></span>             | <span data-ttu-id="5c7ad-191">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-191">False</span></span>                                            |
| <span data-ttu-id="5c7ad-192">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c7ad-192">In Global Catalog</span></span>      | <span data-ttu-id="5c7ad-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-193">False</span></span>                                            |
| <span data-ttu-id="5c7ad-194">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c7ad-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c7ad-195">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c7ad-195">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5c7ad-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c7ad-196">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c7ad-197">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-198">Search-Flags</span></span>           | <span data-ttu-id="5c7ad-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c7ad-199">0x00000000</span></span>                                       |
| <span data-ttu-id="5c7ad-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-200">System-Flags</span></span>           | <span data-ttu-id="5c7ad-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c7ad-201">0x00000010</span></span>                                       |
| <span data-ttu-id="5c7ad-202">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c7ad-202">Classes used in</span></span>        | [<span data-ttu-id="5c7ad-203">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-203">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="5c7ad-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c7ad-204">Windows Server 2008</span></span>



| <span data-ttu-id="5c7ad-205">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c7ad-205">Entry</span></span> | <span data-ttu-id="5c7ad-206">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7ad-206">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5c7ad-207">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c7ad-207">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c7ad-208">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c7ad-209">System-Only</span></span>            | <span data-ttu-id="5c7ad-210">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-210">False</span></span>                                            |
| <span data-ttu-id="5c7ad-211">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c7ad-211">Is-Single-Valued</span></span>       | <span data-ttu-id="5c7ad-212">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-212">False</span></span>                                            |
| <span data-ttu-id="5c7ad-213">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c7ad-213">Is Indexed</span></span>             | <span data-ttu-id="5c7ad-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-214">False</span></span>                                            |
| <span data-ttu-id="5c7ad-215">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c7ad-215">In Global Catalog</span></span>      | <span data-ttu-id="5c7ad-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-216">False</span></span>                                            |
| <span data-ttu-id="5c7ad-217">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c7ad-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c7ad-218">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c7ad-218">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5c7ad-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c7ad-219">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c7ad-220">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-221">Search-Flags</span></span>           | <span data-ttu-id="5c7ad-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c7ad-222">0x00000000</span></span>                                       |
| <span data-ttu-id="5c7ad-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-223">System-Flags</span></span>           | <span data-ttu-id="5c7ad-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c7ad-224">0x00000010</span></span>                                       |
| <span data-ttu-id="5c7ad-225">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c7ad-225">Classes used in</span></span>        | [<span data-ttu-id="5c7ad-226">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-226">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="5c7ad-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c7ad-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="5c7ad-228">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c7ad-228">Entry</span></span> | <span data-ttu-id="5c7ad-229">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7ad-229">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5c7ad-230">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c7ad-230">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c7ad-231">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c7ad-232">System-Only</span></span>            | <span data-ttu-id="5c7ad-233">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-233">False</span></span>                                            |
| <span data-ttu-id="5c7ad-234">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c7ad-234">Is-Single-Valued</span></span>       | <span data-ttu-id="5c7ad-235">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-235">False</span></span>                                            |
| <span data-ttu-id="5c7ad-236">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c7ad-236">Is Indexed</span></span>             | <span data-ttu-id="5c7ad-237">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-237">False</span></span>                                            |
| <span data-ttu-id="5c7ad-238">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c7ad-238">In Global Catalog</span></span>      | <span data-ttu-id="5c7ad-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-239">False</span></span>                                            |
| <span data-ttu-id="5c7ad-240">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c7ad-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c7ad-241">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c7ad-241">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5c7ad-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c7ad-242">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c7ad-243">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-244">Search-Flags</span></span>           | <span data-ttu-id="5c7ad-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c7ad-245">0x00000000</span></span>                                       |
| <span data-ttu-id="5c7ad-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-246">System-Flags</span></span>           | <span data-ttu-id="5c7ad-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c7ad-247">0x00000010</span></span>                                       |
| <span data-ttu-id="5c7ad-248">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c7ad-248">Classes used in</span></span>        | [<span data-ttu-id="5c7ad-249">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-249">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="5c7ad-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c7ad-250">Windows Server 2012</span></span>



| <span data-ttu-id="5c7ad-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="5c7ad-251">Entry</span></span> | <span data-ttu-id="5c7ad-252">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7ad-252">Value</span></span> |
|------------------------|--------------------------------------------------|
| <span data-ttu-id="5c7ad-253">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="5c7ad-253">Link-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="5c7ad-254">MAPI-Id</span></span>                | \-                                               |
| <span data-ttu-id="5c7ad-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="5c7ad-255">System-Only</span></span>            | <span data-ttu-id="5c7ad-256">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-256">False</span></span>                                            |
| <span data-ttu-id="5c7ad-257">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="5c7ad-257">Is-Single-Valued</span></span>       | <span data-ttu-id="5c7ad-258">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-258">False</span></span>                                            |
| <span data-ttu-id="5c7ad-259">Индексируется</span><span class="sxs-lookup"><span data-stu-id="5c7ad-259">Is Indexed</span></span>             | <span data-ttu-id="5c7ad-260">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-260">False</span></span>                                            |
| <span data-ttu-id="5c7ad-261">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="5c7ad-261">In Global Catalog</span></span>      | <span data-ttu-id="5c7ad-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="5c7ad-262">False</span></span>                                            |
| <span data-ttu-id="5c7ad-263">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="5c7ad-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="5c7ad-264">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="5c7ad-264">O:BAG:BAD:S:</span></span>                                     |
| <span data-ttu-id="5c7ad-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="5c7ad-265">Range-Lower</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="5c7ad-266">Range-Upper</span></span>            | \-                                               |
| <span data-ttu-id="5c7ad-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-267">Search-Flags</span></span>           | <span data-ttu-id="5c7ad-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="5c7ad-268">0x00000000</span></span>                                       |
| <span data-ttu-id="5c7ad-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="5c7ad-269">System-Flags</span></span>           | <span data-ttu-id="5c7ad-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c7ad-270">0x00000010</span></span>                                       |
| <span data-ttu-id="5c7ad-271">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="5c7ad-271">Classes used in</span></span>        | [<span data-ttu-id="5c7ad-272">**Служба NTDS**</span><span class="sxs-lookup"><span data-stu-id="5c7ad-272">**NTDS-Service**</span></span>](c-ntdsservice.md)<br/> |



 

 





