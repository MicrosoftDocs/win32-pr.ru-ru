---
title: MS-DS-User-Account-Control-вычисленный атрибут
description: msDS-User-Account-Control — вычисление выполняется примерно так же, как userAccountControl, но значение атрибута может содержать дополнительные несохраненные биты.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- MS-DS-User-Account-Control-схема AD для атрибута
- msDS-User-Account-Control-схема AD для атрибута
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b5e9b047dd44d637b56cae8ded9e0991c46025
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655162"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a><span data-ttu-id="33df7-105">MS-DS-User-Account-Control-вычисленный атрибут</span><span class="sxs-lookup"><span data-stu-id="33df7-105">ms-DS-User-Account-Control-Computed attribute</span></span>

<span data-ttu-id="33df7-106">**msDS-User-Account-Control — вычисление** выполняется примерно так же, как [**userAccountControl**](a-useraccountcontrol.md), но значение атрибута может содержать дополнительные несохраненные биты.</span><span class="sxs-lookup"><span data-stu-id="33df7-106">**msDS-User-Account-Control-Computed** is much like [**userAccountControl**](a-useraccountcontrol.md), but the attribute's value can contain additional bits that are not persisted.</span></span> <span data-ttu-id="33df7-107">К вычисленным битам относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="33df7-107">The computed bits include the following.</span></span>



| <span data-ttu-id="33df7-108">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-108">Value</span></span>                | <span data-ttu-id="33df7-109">Имя (определено в iAds. h)</span><span class="sxs-lookup"><span data-stu-id="33df7-109">Name (defined in Iads.h)</span></span>                     |
|----------------------|----------------------------------------------|
| <span data-ttu-id="33df7-110">0x0010</span><span class="sxs-lookup"><span data-stu-id="33df7-110">0x0010</span></span><br/>    | <span data-ttu-id="33df7-111">**\_Блокировка УФ**</span><span class="sxs-lookup"><span data-stu-id="33df7-111">**UF\_LOCKOUT**</span></span><br/>                   |
| <span data-ttu-id="33df7-112">0x800000</span><span class="sxs-lookup"><span data-stu-id="33df7-112">0x800000</span></span><br/>  | <span data-ttu-id="33df7-113">**\_ \_ срок действия пароля УФ истек**</span><span class="sxs-lookup"><span data-stu-id="33df7-113">**UF\_PASSWORD\_EXPIRED**</span></span><br/>         |
| <span data-ttu-id="33df7-114">0x4000000</span><span class="sxs-lookup"><span data-stu-id="33df7-114">0x4000000</span></span><br/> | <span data-ttu-id="33df7-115">**\_ \_ учетная запись частичных СЕКРЕТов УФ \_**</span><span class="sxs-lookup"><span data-stu-id="33df7-115">**UF\_PARTIAL\_SECRETS\_ACCOUNT**</span></span><br/> |
| <span data-ttu-id="33df7-116">0x8000000</span><span class="sxs-lookup"><span data-stu-id="33df7-116">0x8000000</span></span><br/> | <span data-ttu-id="33df7-117">**УФ \_ использовать \_ \_ ключи AES**</span><span class="sxs-lookup"><span data-stu-id="33df7-117">**UF\_USE\_AES\_KEYS**</span></span><br/>            |



 

<span data-ttu-id="33df7-118">Полный список битов [**управления учетными записями пользователей**](a-useraccountcontrol.md) и, следовательно, определяемых пользователем контрольных данных **msDS-User-Control** , также можно найти на странице справочника по **контролю учетных записей** (сопоставляется через набор флагов [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ) или на страницах справочника по управлению сетями для структуры [**\_ сведений о пользователе \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .</span><span class="sxs-lookup"><span data-stu-id="33df7-118">The full list of bits that [**User-Account-Control**](a-useraccountcontrol.md) and therefore **msDS-User-Account-Control-Computed** can also contain can be found in the **User-Account-Control** reference page (mapped through the [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) flagset) or on the network management reference pages for the [**user\_info\_1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) structure.</span></span>



| <span data-ttu-id="33df7-119">Ввод</span><span class="sxs-lookup"><span data-stu-id="33df7-119">Entry</span></span> | <span data-ttu-id="33df7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-120">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="33df7-121">CN</span><span class="sxs-lookup"><span data-stu-id="33df7-121">CN</span></span>                | <span data-ttu-id="33df7-122">MS-DS-User-Account-Control — вычисленный</span><span class="sxs-lookup"><span data-stu-id="33df7-122">ms-DS-User-Account-Control-Computed</span></span>  |
| <span data-ttu-id="33df7-123">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="33df7-123">Ldap-Display-Name</span></span> | <span data-ttu-id="33df7-124">msDS-User-Account-Control — вычисление</span><span class="sxs-lookup"><span data-stu-id="33df7-124">msDS-User-Account-Control-Computed</span></span>   |
| <span data-ttu-id="33df7-125">Размер</span><span class="sxs-lookup"><span data-stu-id="33df7-125">Size</span></span>              | \-                                   |
| <span data-ttu-id="33df7-126">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="33df7-126">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="33df7-127">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="33df7-127">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="33df7-128">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="33df7-128">Attribute-Id</span></span>      | <span data-ttu-id="33df7-129">1.2.840.113556.1.4.1460</span><span class="sxs-lookup"><span data-stu-id="33df7-129">1.2.840.113556.1.4.1460</span></span>              |
| <span data-ttu-id="33df7-130">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="33df7-130">System-Id-Guid</span></span>    | <span data-ttu-id="33df7-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span><span class="sxs-lookup"><span data-stu-id="33df7-131">2cc4b836-b63f-4940-8d23-ea7acf06af56</span></span> |
| <span data-ttu-id="33df7-132">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33df7-132">Syntax</span></span>            | [<span data-ttu-id="33df7-133">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="33df7-133">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="33df7-134">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="33df7-134">Implementations</span></span>

-   [<span data-ttu-id="33df7-135">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="33df7-135">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="33df7-136">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="33df7-136">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="33df7-137">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="33df7-137">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="33df7-138">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="33df7-138">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="33df7-139">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="33df7-139">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="33df7-140">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="33df7-140">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="33df7-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="33df7-141">Windows Server 2003</span></span>



| <span data-ttu-id="33df7-142">Ввод</span><span class="sxs-lookup"><span data-stu-id="33df7-142">Entry</span></span> | <span data-ttu-id="33df7-143">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-143">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="33df7-144">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="33df7-144">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-145">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33df7-145">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-146">System-Only</span><span class="sxs-lookup"><span data-stu-id="33df7-146">System-Only</span></span>            | <span data-ttu-id="33df7-147">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-147">False</span></span>                             |
| <span data-ttu-id="33df7-148">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="33df7-148">Is-Single-Valued</span></span>       | <span data-ttu-id="33df7-149">True</span><span class="sxs-lookup"><span data-stu-id="33df7-149">True</span></span>                              |
| <span data-ttu-id="33df7-150">Индексируется</span><span class="sxs-lookup"><span data-stu-id="33df7-150">Is Indexed</span></span>             | <span data-ttu-id="33df7-151">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-151">False</span></span>                             |
| <span data-ttu-id="33df7-152">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="33df7-152">In Global Catalog</span></span>      | <span data-ttu-id="33df7-153">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-153">False</span></span>                             |
| <span data-ttu-id="33df7-154">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="33df7-154">NT-Security-Descriptor</span></span> | <span data-ttu-id="33df7-155">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="33df7-155">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="33df7-156">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33df7-156">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="33df7-157">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33df7-157">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="33df7-158">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-158">Search-Flags</span></span>           | <span data-ttu-id="33df7-159">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33df7-159">0x00000000</span></span>                        |
| <span data-ttu-id="33df7-160">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-160">System-Flags</span></span>           | <span data-ttu-id="33df7-161">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33df7-161">0x00000014</span></span>                        |
| <span data-ttu-id="33df7-162">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="33df7-162">Classes used in</span></span>        | [<span data-ttu-id="33df7-163">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="33df7-163">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="33df7-164">ADAM</span><span class="sxs-lookup"><span data-stu-id="33df7-164">ADAM</span></span>



| <span data-ttu-id="33df7-165">Ввод</span><span class="sxs-lookup"><span data-stu-id="33df7-165">Entry</span></span> | <span data-ttu-id="33df7-166">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-166">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="33df7-167">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="33df7-167">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="33df7-168">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33df7-168">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="33df7-169">System-Only</span><span class="sxs-lookup"><span data-stu-id="33df7-169">System-Only</span></span>            | <span data-ttu-id="33df7-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-170">False</span></span>                                                             |
| <span data-ttu-id="33df7-171">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="33df7-171">Is-Single-Valued</span></span>       | <span data-ttu-id="33df7-172">True</span><span class="sxs-lookup"><span data-stu-id="33df7-172">True</span></span>                                                              |
| <span data-ttu-id="33df7-173">Индексируется</span><span class="sxs-lookup"><span data-stu-id="33df7-173">Is Indexed</span></span>             | <span data-ttu-id="33df7-174">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-174">False</span></span>                                                             |
| <span data-ttu-id="33df7-175">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="33df7-175">In Global Catalog</span></span>      | <span data-ttu-id="33df7-176">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-176">False</span></span>                                                             |
| <span data-ttu-id="33df7-177">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="33df7-177">NT-Security-Descriptor</span></span> | <span data-ttu-id="33df7-178">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="33df7-178">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="33df7-179">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33df7-179">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="33df7-180">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33df7-180">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="33df7-181">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-181">Search-Flags</span></span>           | <span data-ttu-id="33df7-182">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33df7-182">0x00000000</span></span>                                                        |
| <span data-ttu-id="33df7-183">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-183">System-Flags</span></span>           | <span data-ttu-id="33df7-184">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33df7-184">0x00000014</span></span>                                                        |
| <span data-ttu-id="33df7-185">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="33df7-185">Classes used in</span></span>        | [<span data-ttu-id="33df7-186">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="33df7-186">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="33df7-187">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="33df7-187">Windows Server 2003 R2</span></span>



| <span data-ttu-id="33df7-188">Ввод</span><span class="sxs-lookup"><span data-stu-id="33df7-188">Entry</span></span> | <span data-ttu-id="33df7-189">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-189">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="33df7-190">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="33df7-190">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-191">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33df7-191">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="33df7-192">System-Only</span></span>            | <span data-ttu-id="33df7-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-193">False</span></span>                             |
| <span data-ttu-id="33df7-194">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="33df7-194">Is-Single-Valued</span></span>       | <span data-ttu-id="33df7-195">True</span><span class="sxs-lookup"><span data-stu-id="33df7-195">True</span></span>                              |
| <span data-ttu-id="33df7-196">Индексируется</span><span class="sxs-lookup"><span data-stu-id="33df7-196">Is Indexed</span></span>             | <span data-ttu-id="33df7-197">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-197">False</span></span>                             |
| <span data-ttu-id="33df7-198">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="33df7-198">In Global Catalog</span></span>      | <span data-ttu-id="33df7-199">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-199">False</span></span>                             |
| <span data-ttu-id="33df7-200">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="33df7-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="33df7-201">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="33df7-201">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="33df7-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33df7-202">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="33df7-203">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33df7-203">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="33df7-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-204">Search-Flags</span></span>           | <span data-ttu-id="33df7-205">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33df7-205">0x00000000</span></span>                        |
| <span data-ttu-id="33df7-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-206">System-Flags</span></span>           | <span data-ttu-id="33df7-207">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33df7-207">0x00000014</span></span>                        |
| <span data-ttu-id="33df7-208">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="33df7-208">Classes used in</span></span>        | [<span data-ttu-id="33df7-209">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="33df7-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="33df7-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33df7-210">Windows Server 2008</span></span>



| <span data-ttu-id="33df7-211">Ввод</span><span class="sxs-lookup"><span data-stu-id="33df7-211">Entry</span></span> | <span data-ttu-id="33df7-212">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="33df7-213">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="33df7-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33df7-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="33df7-215">System-Only</span></span>            | <span data-ttu-id="33df7-216">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-216">False</span></span>                             |
| <span data-ttu-id="33df7-217">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="33df7-217">Is-Single-Valued</span></span>       | <span data-ttu-id="33df7-218">True</span><span class="sxs-lookup"><span data-stu-id="33df7-218">True</span></span>                              |
| <span data-ttu-id="33df7-219">Индексируется</span><span class="sxs-lookup"><span data-stu-id="33df7-219">Is Indexed</span></span>             | <span data-ttu-id="33df7-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-220">False</span></span>                             |
| <span data-ttu-id="33df7-221">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="33df7-221">In Global Catalog</span></span>      | <span data-ttu-id="33df7-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-222">False</span></span>                             |
| <span data-ttu-id="33df7-223">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="33df7-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="33df7-224">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="33df7-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="33df7-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33df7-225">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="33df7-226">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33df7-226">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="33df7-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-227">Search-Flags</span></span>           | <span data-ttu-id="33df7-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33df7-228">0x00000000</span></span>                        |
| <span data-ttu-id="33df7-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-229">System-Flags</span></span>           | <span data-ttu-id="33df7-230">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33df7-230">0x00000014</span></span>                        |
| <span data-ttu-id="33df7-231">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="33df7-231">Classes used in</span></span>        | [<span data-ttu-id="33df7-232">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="33df7-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="33df7-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="33df7-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="33df7-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="33df7-234">Entry</span></span> | <span data-ttu-id="33df7-235">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="33df7-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="33df7-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33df7-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="33df7-238">System-Only</span></span>            | <span data-ttu-id="33df7-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-239">False</span></span>                             |
| <span data-ttu-id="33df7-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="33df7-240">Is-Single-Valued</span></span>       | <span data-ttu-id="33df7-241">True</span><span class="sxs-lookup"><span data-stu-id="33df7-241">True</span></span>                              |
| <span data-ttu-id="33df7-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="33df7-242">Is Indexed</span></span>             | <span data-ttu-id="33df7-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-243">False</span></span>                             |
| <span data-ttu-id="33df7-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="33df7-244">In Global Catalog</span></span>      | <span data-ttu-id="33df7-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-245">False</span></span>                             |
| <span data-ttu-id="33df7-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="33df7-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="33df7-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="33df7-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="33df7-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33df7-248">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="33df7-249">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33df7-249">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="33df7-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-250">Search-Flags</span></span>           | <span data-ttu-id="33df7-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33df7-251">0x00000000</span></span>                        |
| <span data-ttu-id="33df7-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-252">System-Flags</span></span>           | <span data-ttu-id="33df7-253">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33df7-253">0x00000014</span></span>                        |
| <span data-ttu-id="33df7-254">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="33df7-254">Classes used in</span></span>        | [<span data-ttu-id="33df7-255">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="33df7-255">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="33df7-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33df7-256">Windows Server 2012</span></span>



| <span data-ttu-id="33df7-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="33df7-257">Entry</span></span> | <span data-ttu-id="33df7-258">Значение</span><span class="sxs-lookup"><span data-stu-id="33df7-258">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="33df7-259">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="33df7-259">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="33df7-260">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="33df7-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="33df7-261">System-Only</span></span>            | <span data-ttu-id="33df7-262">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-262">False</span></span>                             |
| <span data-ttu-id="33df7-263">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="33df7-263">Is-Single-Valued</span></span>       | <span data-ttu-id="33df7-264">True</span><span class="sxs-lookup"><span data-stu-id="33df7-264">True</span></span>                              |
| <span data-ttu-id="33df7-265">Индексируется</span><span class="sxs-lookup"><span data-stu-id="33df7-265">Is Indexed</span></span>             | <span data-ttu-id="33df7-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-266">False</span></span>                             |
| <span data-ttu-id="33df7-267">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="33df7-267">In Global Catalog</span></span>      | <span data-ttu-id="33df7-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="33df7-268">False</span></span>                             |
| <span data-ttu-id="33df7-269">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="33df7-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="33df7-270">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="33df7-270">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="33df7-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="33df7-271">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="33df7-272">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="33df7-272">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="33df7-273">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-273">Search-Flags</span></span>           | <span data-ttu-id="33df7-274">0x00000000</span><span class="sxs-lookup"><span data-stu-id="33df7-274">0x00000000</span></span>                        |
| <span data-ttu-id="33df7-275">System-Flags</span><span class="sxs-lookup"><span data-stu-id="33df7-275">System-Flags</span></span>           | <span data-ttu-id="33df7-276">0x00000014</span><span class="sxs-lookup"><span data-stu-id="33df7-276">0x00000014</span></span>                        |
| <span data-ttu-id="33df7-277">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="33df7-277">Classes used in</span></span>        | [<span data-ttu-id="33df7-278">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="33df7-278">**User**</span></span>](c-user.md)<br/> |



 

