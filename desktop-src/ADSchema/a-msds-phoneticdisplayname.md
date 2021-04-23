---
title: Атрибут ms-DS-фонетического отображаемого имени
description: Фонетическое отображаемое имя объекта. В случае отсутствия фонетического отображаемого имени используется существующее отображаемое имя.
ms.assetid: d1dd7d20-c280-4533-9da9-a7b6ff224970
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-фонетического отображаемого имени
- Схема AD атрибута msDS-Фонетикдисплайнаме
topic_type:
- apiref
api_name:
- ms-DS-Phonetic-Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87be99b0937199b4467e12418761f21f1dbc4983
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989819"
---
# <a name="ms-ds-phonetic-display-name-attribute"></a><span data-ttu-id="cd282-106">Атрибут ms-DS-фонетического отображаемого имени</span><span class="sxs-lookup"><span data-stu-id="cd282-106">ms-DS-Phonetic-Display-Name attribute</span></span>

<span data-ttu-id="cd282-107">Фонетическое отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="cd282-107">The phonetic display name of an object.</span></span> <span data-ttu-id="cd282-108">В случае отсутствия фонетического отображаемого имени используется существующее отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="cd282-108">In the absence of a phonetic display name, the existing display name is used.</span></span>



| <span data-ttu-id="cd282-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd282-109">Entry</span></span> | <span data-ttu-id="cd282-110">Значение</span><span class="sxs-lookup"><span data-stu-id="cd282-110">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="cd282-111">CN</span><span class="sxs-lookup"><span data-stu-id="cd282-111">CN</span></span>                | <span data-ttu-id="cd282-112">MS-DS-фонетическо-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cd282-112">ms-DS-Phonetic-Display-Name</span></span>                 |
| <span data-ttu-id="cd282-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="cd282-113">Ldap-Display-Name</span></span> | <span data-ttu-id="cd282-114">msDS-PhoneticDisplayName</span><span class="sxs-lookup"><span data-stu-id="cd282-114">msDS-PhoneticDisplayName</span></span>                    |
| <span data-ttu-id="cd282-115">Размер</span><span class="sxs-lookup"><span data-stu-id="cd282-115">Size</span></span>              | \-                                          |
| <span data-ttu-id="cd282-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="cd282-116">Update Privilege</span></span>  | \-                                          |
| <span data-ttu-id="cd282-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="cd282-117">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="cd282-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="cd282-118">Attribute-Id</span></span>      | <span data-ttu-id="cd282-119">1.2.840.113556.1.4.1946</span><span class="sxs-lookup"><span data-stu-id="cd282-119">1.2.840.113556.1.4.1946</span></span>                     |
| <span data-ttu-id="cd282-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="cd282-120">System-Id-Guid</span></span>    | <span data-ttu-id="cd282-121">e21a94e4-2d66-4ce5-b30d-0ef87a776ff0</span><span class="sxs-lookup"><span data-stu-id="cd282-121">e21a94e4-2d66-4ce5-b30d-0ef87a776ff0</span></span>        |
| <span data-ttu-id="cd282-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd282-122">Syntax</span></span>            | [<span data-ttu-id="cd282-123">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="cd282-123">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="cd282-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="cd282-124">Implementations</span></span>

-   [<span data-ttu-id="cd282-125">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="cd282-125">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="cd282-126">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="cd282-126">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="cd282-127">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="cd282-127">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2008"></a><span data-ttu-id="cd282-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd282-128">Windows Server 2008</span></span>



| <span data-ttu-id="cd282-129">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd282-129">Entry</span></span> | <span data-ttu-id="cd282-130">Значение</span><span class="sxs-lookup"><span data-stu-id="cd282-130">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd282-131">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd282-131">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="cd282-132">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd282-132">MAPI-Id</span></span>                | <span data-ttu-id="cd282-133">0x8C92</span><span class="sxs-lookup"><span data-stu-id="cd282-133">0x8C92</span></span>                                                                                                                  |
| <span data-ttu-id="cd282-134">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd282-134">System-Only</span></span>            | <span data-ttu-id="cd282-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd282-135">False</span></span>                                                                                                                   |
| <span data-ttu-id="cd282-136">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd282-136">Is-Single-Valued</span></span>       | <span data-ttu-id="cd282-137">True</span><span class="sxs-lookup"><span data-stu-id="cd282-137">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-138">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd282-138">Is Indexed</span></span>             | <span data-ttu-id="cd282-139">True</span><span class="sxs-lookup"><span data-stu-id="cd282-139">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-140">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd282-140">In Global Catalog</span></span>      | <span data-ttu-id="cd282-141">True</span><span class="sxs-lookup"><span data-stu-id="cd282-141">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-142">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd282-142">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd282-143">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd282-143">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="cd282-144">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd282-144">Range-Lower</span></span>            | <span data-ttu-id="cd282-145">0</span><span class="sxs-lookup"><span data-stu-id="cd282-145">0</span></span>                                                                                                                       |
| <span data-ttu-id="cd282-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd282-146">Range-Upper</span></span>            | <span data-ttu-id="cd282-147">256</span><span class="sxs-lookup"><span data-stu-id="cd282-147">256</span></span>                                                                                                                     |
| <span data-ttu-id="cd282-148">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd282-148">Search-Flags</span></span>           | <span data-ttu-id="cd282-149">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cd282-149">0x00000005</span></span>                                                                                                              |
| <span data-ttu-id="cd282-150">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd282-150">System-Flags</span></span>           | <span data-ttu-id="cd282-151">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd282-151">0x00000010</span></span>                                                                                                              |
| <span data-ttu-id="cd282-152">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd282-152">Classes used in</span></span>        | [<span data-ttu-id="cd282-153">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="cd282-153">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="cd282-154">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cd282-154">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="cd282-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd282-155">Windows Server 2008 R2</span></span>



| <span data-ttu-id="cd282-156">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd282-156">Entry</span></span> | <span data-ttu-id="cd282-157">Значение</span><span class="sxs-lookup"><span data-stu-id="cd282-157">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd282-158">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd282-158">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="cd282-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd282-159">MAPI-Id</span></span>                | <span data-ttu-id="cd282-160">0x8C92</span><span class="sxs-lookup"><span data-stu-id="cd282-160">0x8C92</span></span>                                                                                                                  |
| <span data-ttu-id="cd282-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd282-161">System-Only</span></span>            | <span data-ttu-id="cd282-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd282-162">False</span></span>                                                                                                                   |
| <span data-ttu-id="cd282-163">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd282-163">Is-Single-Valued</span></span>       | <span data-ttu-id="cd282-164">True</span><span class="sxs-lookup"><span data-stu-id="cd282-164">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-165">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd282-165">Is Indexed</span></span>             | <span data-ttu-id="cd282-166">True</span><span class="sxs-lookup"><span data-stu-id="cd282-166">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-167">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd282-167">In Global Catalog</span></span>      | <span data-ttu-id="cd282-168">True</span><span class="sxs-lookup"><span data-stu-id="cd282-168">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-169">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd282-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd282-170">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd282-170">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="cd282-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd282-171">Range-Lower</span></span>            | <span data-ttu-id="cd282-172">0</span><span class="sxs-lookup"><span data-stu-id="cd282-172">0</span></span>                                                                                                                       |
| <span data-ttu-id="cd282-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd282-173">Range-Upper</span></span>            | <span data-ttu-id="cd282-174">256</span><span class="sxs-lookup"><span data-stu-id="cd282-174">256</span></span>                                                                                                                     |
| <span data-ttu-id="cd282-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd282-175">Search-Flags</span></span>           | <span data-ttu-id="cd282-176">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cd282-176">0x00000005</span></span>                                                                                                              |
| <span data-ttu-id="cd282-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd282-177">System-Flags</span></span>           | <span data-ttu-id="cd282-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd282-178">0x00000010</span></span>                                                                                                              |
| <span data-ttu-id="cd282-179">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd282-179">Classes used in</span></span>        | [<span data-ttu-id="cd282-180">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="cd282-180">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="cd282-181">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cd282-181">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="cd282-182">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd282-182">Windows Server 2012</span></span>



| <span data-ttu-id="cd282-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="cd282-183">Entry</span></span> | <span data-ttu-id="cd282-184">Значение</span><span class="sxs-lookup"><span data-stu-id="cd282-184">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd282-185">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="cd282-185">Link-Id</span></span>                | \-                                                                                                                      |
| <span data-ttu-id="cd282-186">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="cd282-186">MAPI-Id</span></span>                | <span data-ttu-id="cd282-187">0x8C92</span><span class="sxs-lookup"><span data-stu-id="cd282-187">0x8C92</span></span>                                                                                                                  |
| <span data-ttu-id="cd282-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="cd282-188">System-Only</span></span>            | <span data-ttu-id="cd282-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="cd282-189">False</span></span>                                                                                                                   |
| <span data-ttu-id="cd282-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="cd282-190">Is-Single-Valued</span></span>       | <span data-ttu-id="cd282-191">True</span><span class="sxs-lookup"><span data-stu-id="cd282-191">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="cd282-192">Is Indexed</span></span>             | <span data-ttu-id="cd282-193">True</span><span class="sxs-lookup"><span data-stu-id="cd282-193">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="cd282-194">In Global Catalog</span></span>      | <span data-ttu-id="cd282-195">True</span><span class="sxs-lookup"><span data-stu-id="cd282-195">True</span></span>                                                                                                                    |
| <span data-ttu-id="cd282-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="cd282-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="cd282-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="cd282-197">O:BAG:BAD:S:</span></span>                                                                                                            |
| <span data-ttu-id="cd282-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="cd282-198">Range-Lower</span></span>            | <span data-ttu-id="cd282-199">0</span><span class="sxs-lookup"><span data-stu-id="cd282-199">0</span></span>                                                                                                                       |
| <span data-ttu-id="cd282-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="cd282-200">Range-Upper</span></span>            | <span data-ttu-id="cd282-201">256</span><span class="sxs-lookup"><span data-stu-id="cd282-201">256</span></span>                                                                                                                     |
| <span data-ttu-id="cd282-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="cd282-202">Search-Flags</span></span>           | <span data-ttu-id="cd282-203">0x00000005</span><span class="sxs-lookup"><span data-stu-id="cd282-203">0x00000005</span></span>                                                                                                              |
| <span data-ttu-id="cd282-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="cd282-204">System-Flags</span></span>           | <span data-ttu-id="cd282-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="cd282-205">0x00000010</span></span>                                                                                                              |
| <span data-ttu-id="cd282-206">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="cd282-206">Classes used in</span></span>        | [<span data-ttu-id="cd282-207">**Получатель почты**</span><span class="sxs-lookup"><span data-stu-id="cd282-207">**Mail-Recipient**</span></span>](c-mailrecipient.md)<br/> [<span data-ttu-id="cd282-208">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="cd282-208">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





