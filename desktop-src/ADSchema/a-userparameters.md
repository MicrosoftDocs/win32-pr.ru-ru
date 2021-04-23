---
title: Атрибут User-Parameters
description: Параметры пользователя.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута User-Parameters
- Схема AD атрибута Усерпараметерс
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7c1d593f0a655dea4fa3ddb25753de712ab83cd
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536119"
---
# <a name="user-parameters-attribute"></a><span data-ttu-id="317e6-105">Атрибут User-Parameters</span><span class="sxs-lookup"><span data-stu-id="317e6-105">User-Parameters attribute</span></span>

<span data-ttu-id="317e6-106">Параметры пользователя.</span><span class="sxs-lookup"><span data-stu-id="317e6-106">Parameters of the user.</span></span> <span data-ttu-id="317e6-107">Указывает на строку в Юникоде, которая задается не для использования приложениями.</span><span class="sxs-lookup"><span data-stu-id="317e6-107">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="317e6-108">Эта строка может быть пустой строкой или содержать любое число символов перед завершающим нулевым символом.</span><span class="sxs-lookup"><span data-stu-id="317e6-108">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="317e6-109">Продукты Майкрософт используют этот элемент для хранения пользовательских данных, относящихся к отдельной программе.</span><span class="sxs-lookup"><span data-stu-id="317e6-109">Microsoft products use this member to store user data specific to the individual program.</span></span>



| <span data-ttu-id="317e6-110">Ввод</span><span class="sxs-lookup"><span data-stu-id="317e6-110">Entry</span></span> | <span data-ttu-id="317e6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="317e6-111">Value</span></span> |
|-------------------|---------------------------------------------|
| <span data-ttu-id="317e6-112">CN</span><span class="sxs-lookup"><span data-stu-id="317e6-112">CN</span></span>                | <span data-ttu-id="317e6-113">User-Parameters</span><span class="sxs-lookup"><span data-stu-id="317e6-113">User-Parameters</span></span>                             |
| <span data-ttu-id="317e6-114">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="317e6-114">Ldap-Display-Name</span></span> | <span data-ttu-id="317e6-115">усерпараметерс</span><span class="sxs-lookup"><span data-stu-id="317e6-115">userParameters</span></span>                              |
| <span data-ttu-id="317e6-116">Размер</span><span class="sxs-lookup"><span data-stu-id="317e6-116">Size</span></span>              | \-                                          |
| <span data-ttu-id="317e6-117">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="317e6-117">Update Privilege</span></span>  | <span data-ttu-id="317e6-118">Изменено приложениями.</span><span class="sxs-lookup"><span data-stu-id="317e6-118">Modified by applications.</span></span>                   |
| <span data-ttu-id="317e6-119">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="317e6-119">Update Frequency</span></span>  | \-                                          |
| <span data-ttu-id="317e6-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="317e6-120">Attribute-Id</span></span>      | <span data-ttu-id="317e6-121">1.2.840.113556.1.4.138</span><span class="sxs-lookup"><span data-stu-id="317e6-121">1.2.840.113556.1.4.138</span></span>                      |
| <span data-ttu-id="317e6-122">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="317e6-122">System-Id-Guid</span></span>    | <span data-ttu-id="317e6-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="317e6-123">bf967a6d-0de6-11d0-a285-00aa003049e2</span></span>        |
| <span data-ttu-id="317e6-124">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="317e6-124">Syntax</span></span>            | [<span data-ttu-id="317e6-125">**String(Юникод)**</span><span class="sxs-lookup"><span data-stu-id="317e6-125">**String(Unicode)**</span></span>](s-string-unicode.md) |



## <a name="implementations"></a><span data-ttu-id="317e6-126">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="317e6-126">Implementations</span></span>

-   [<span data-ttu-id="317e6-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="317e6-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="317e6-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="317e6-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="317e6-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="317e6-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="317e6-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="317e6-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="317e6-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="317e6-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="317e6-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="317e6-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="317e6-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="317e6-133">Windows 2000 Server</span></span>



| <span data-ttu-id="317e6-134">Ввод</span><span class="sxs-lookup"><span data-stu-id="317e6-134">Entry</span></span> | <span data-ttu-id="317e6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="317e6-135">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="317e6-136">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="317e6-136">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-137">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="317e6-137">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-138">System-Only</span><span class="sxs-lookup"><span data-stu-id="317e6-138">System-Only</span></span>            | <span data-ttu-id="317e6-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-139">False</span></span>                             |
| <span data-ttu-id="317e6-140">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="317e6-140">Is-Single-Valued</span></span>       | <span data-ttu-id="317e6-141">True</span><span class="sxs-lookup"><span data-stu-id="317e6-141">True</span></span>                              |
| <span data-ttu-id="317e6-142">Индексируется</span><span class="sxs-lookup"><span data-stu-id="317e6-142">Is Indexed</span></span>             | <span data-ttu-id="317e6-143">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-143">False</span></span>                             |
| <span data-ttu-id="317e6-144">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="317e6-144">In Global Catalog</span></span>      | <span data-ttu-id="317e6-145">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-145">False</span></span>                             |
| <span data-ttu-id="317e6-146">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="317e6-146">NT-Security-Descriptor</span></span> | <span data-ttu-id="317e6-147">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="317e6-147">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="317e6-148">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="317e6-148">Range-Lower</span></span>            | <span data-ttu-id="317e6-149">0</span><span class="sxs-lookup"><span data-stu-id="317e6-149">0</span></span>                                 |
| <span data-ttu-id="317e6-150">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="317e6-150">Range-Upper</span></span>            | <span data-ttu-id="317e6-151">32767</span><span class="sxs-lookup"><span data-stu-id="317e6-151">32767</span></span>                             |
| <span data-ttu-id="317e6-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-152">Search-Flags</span></span>           | <span data-ttu-id="317e6-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="317e6-153">0x00000000</span></span>                        |
| <span data-ttu-id="317e6-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-154">System-Flags</span></span>           | <span data-ttu-id="317e6-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="317e6-155">0x00000010</span></span>                        |
| <span data-ttu-id="317e6-156">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="317e6-156">Classes used in</span></span>        | [<span data-ttu-id="317e6-157">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="317e6-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="317e6-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="317e6-158">Windows Server 2003</span></span>



| <span data-ttu-id="317e6-159">Ввод</span><span class="sxs-lookup"><span data-stu-id="317e6-159">Entry</span></span> | <span data-ttu-id="317e6-160">Значение</span><span class="sxs-lookup"><span data-stu-id="317e6-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="317e6-161">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="317e6-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="317e6-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="317e6-163">System-Only</span></span>            | <span data-ttu-id="317e6-164">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-164">False</span></span>                             |
| <span data-ttu-id="317e6-165">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="317e6-165">Is-Single-Valued</span></span>       | <span data-ttu-id="317e6-166">True</span><span class="sxs-lookup"><span data-stu-id="317e6-166">True</span></span>                              |
| <span data-ttu-id="317e6-167">Индексируется</span><span class="sxs-lookup"><span data-stu-id="317e6-167">Is Indexed</span></span>             | <span data-ttu-id="317e6-168">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-168">False</span></span>                             |
| <span data-ttu-id="317e6-169">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="317e6-169">In Global Catalog</span></span>      | <span data-ttu-id="317e6-170">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-170">False</span></span>                             |
| <span data-ttu-id="317e6-171">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="317e6-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="317e6-172">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="317e6-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="317e6-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="317e6-173">Range-Lower</span></span>            | <span data-ttu-id="317e6-174">0</span><span class="sxs-lookup"><span data-stu-id="317e6-174">0</span></span>                                 |
| <span data-ttu-id="317e6-175">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="317e6-175">Range-Upper</span></span>            | <span data-ttu-id="317e6-176">32767</span><span class="sxs-lookup"><span data-stu-id="317e6-176">32767</span></span>                             |
| <span data-ttu-id="317e6-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-177">Search-Flags</span></span>           | <span data-ttu-id="317e6-178">0x00000000</span><span class="sxs-lookup"><span data-stu-id="317e6-178">0x00000000</span></span>                        |
| <span data-ttu-id="317e6-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-179">System-Flags</span></span>           | <span data-ttu-id="317e6-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="317e6-180">0x00000010</span></span>                        |
| <span data-ttu-id="317e6-181">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="317e6-181">Classes used in</span></span>        | [<span data-ttu-id="317e6-182">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="317e6-182">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="317e6-183">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="317e6-183">Windows Server 2003 R2</span></span>



| <span data-ttu-id="317e6-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="317e6-184">Entry</span></span> | <span data-ttu-id="317e6-185">Значение</span><span class="sxs-lookup"><span data-stu-id="317e6-185">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="317e6-186">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="317e6-186">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-187">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="317e6-187">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-188">System-Only</span><span class="sxs-lookup"><span data-stu-id="317e6-188">System-Only</span></span>            | <span data-ttu-id="317e6-189">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-189">False</span></span>                             |
| <span data-ttu-id="317e6-190">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="317e6-190">Is-Single-Valued</span></span>       | <span data-ttu-id="317e6-191">True</span><span class="sxs-lookup"><span data-stu-id="317e6-191">True</span></span>                              |
| <span data-ttu-id="317e6-192">Индексируется</span><span class="sxs-lookup"><span data-stu-id="317e6-192">Is Indexed</span></span>             | <span data-ttu-id="317e6-193">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-193">False</span></span>                             |
| <span data-ttu-id="317e6-194">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="317e6-194">In Global Catalog</span></span>      | <span data-ttu-id="317e6-195">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-195">False</span></span>                             |
| <span data-ttu-id="317e6-196">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="317e6-196">NT-Security-Descriptor</span></span> | <span data-ttu-id="317e6-197">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="317e6-197">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="317e6-198">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="317e6-198">Range-Lower</span></span>            | <span data-ttu-id="317e6-199">0</span><span class="sxs-lookup"><span data-stu-id="317e6-199">0</span></span>                                 |
| <span data-ttu-id="317e6-200">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="317e6-200">Range-Upper</span></span>            | <span data-ttu-id="317e6-201">32767</span><span class="sxs-lookup"><span data-stu-id="317e6-201">32767</span></span>                             |
| <span data-ttu-id="317e6-202">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-202">Search-Flags</span></span>           | <span data-ttu-id="317e6-203">0x00000000</span><span class="sxs-lookup"><span data-stu-id="317e6-203">0x00000000</span></span>                        |
| <span data-ttu-id="317e6-204">System-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-204">System-Flags</span></span>           | <span data-ttu-id="317e6-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="317e6-205">0x00000010</span></span>                        |
| <span data-ttu-id="317e6-206">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="317e6-206">Classes used in</span></span>        | [<span data-ttu-id="317e6-207">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="317e6-207">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="317e6-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="317e6-208">Windows Server 2008</span></span>



| <span data-ttu-id="317e6-209">Ввод</span><span class="sxs-lookup"><span data-stu-id="317e6-209">Entry</span></span> | <span data-ttu-id="317e6-210">Значение</span><span class="sxs-lookup"><span data-stu-id="317e6-210">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="317e6-211">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="317e6-211">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-212">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="317e6-212">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-213">System-Only</span><span class="sxs-lookup"><span data-stu-id="317e6-213">System-Only</span></span>            | <span data-ttu-id="317e6-214">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-214">False</span></span>                             |
| <span data-ttu-id="317e6-215">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="317e6-215">Is-Single-Valued</span></span>       | <span data-ttu-id="317e6-216">True</span><span class="sxs-lookup"><span data-stu-id="317e6-216">True</span></span>                              |
| <span data-ttu-id="317e6-217">Индексируется</span><span class="sxs-lookup"><span data-stu-id="317e6-217">Is Indexed</span></span>             | <span data-ttu-id="317e6-218">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-218">False</span></span>                             |
| <span data-ttu-id="317e6-219">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="317e6-219">In Global Catalog</span></span>      | <span data-ttu-id="317e6-220">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-220">False</span></span>                             |
| <span data-ttu-id="317e6-221">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="317e6-221">NT-Security-Descriptor</span></span> | <span data-ttu-id="317e6-222">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="317e6-222">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="317e6-223">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="317e6-223">Range-Lower</span></span>            | <span data-ttu-id="317e6-224">0</span><span class="sxs-lookup"><span data-stu-id="317e6-224">0</span></span>                                 |
| <span data-ttu-id="317e6-225">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="317e6-225">Range-Upper</span></span>            | <span data-ttu-id="317e6-226">32767</span><span class="sxs-lookup"><span data-stu-id="317e6-226">32767</span></span>                             |
| <span data-ttu-id="317e6-227">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-227">Search-Flags</span></span>           | <span data-ttu-id="317e6-228">0x00000000</span><span class="sxs-lookup"><span data-stu-id="317e6-228">0x00000000</span></span>                        |
| <span data-ttu-id="317e6-229">System-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-229">System-Flags</span></span>           | <span data-ttu-id="317e6-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="317e6-230">0x00000010</span></span>                        |
| <span data-ttu-id="317e6-231">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="317e6-231">Classes used in</span></span>        | [<span data-ttu-id="317e6-232">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="317e6-232">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="317e6-233">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="317e6-233">Windows Server 2008 R2</span></span>



| <span data-ttu-id="317e6-234">Ввод</span><span class="sxs-lookup"><span data-stu-id="317e6-234">Entry</span></span> | <span data-ttu-id="317e6-235">Значение</span><span class="sxs-lookup"><span data-stu-id="317e6-235">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="317e6-236">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="317e6-236">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-237">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="317e6-237">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-238">System-Only</span><span class="sxs-lookup"><span data-stu-id="317e6-238">System-Only</span></span>            | <span data-ttu-id="317e6-239">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-239">False</span></span>                             |
| <span data-ttu-id="317e6-240">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="317e6-240">Is-Single-Valued</span></span>       | <span data-ttu-id="317e6-241">True</span><span class="sxs-lookup"><span data-stu-id="317e6-241">True</span></span>                              |
| <span data-ttu-id="317e6-242">Индексируется</span><span class="sxs-lookup"><span data-stu-id="317e6-242">Is Indexed</span></span>             | <span data-ttu-id="317e6-243">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-243">False</span></span>                             |
| <span data-ttu-id="317e6-244">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="317e6-244">In Global Catalog</span></span>      | <span data-ttu-id="317e6-245">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-245">False</span></span>                             |
| <span data-ttu-id="317e6-246">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="317e6-246">NT-Security-Descriptor</span></span> | <span data-ttu-id="317e6-247">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="317e6-247">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="317e6-248">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="317e6-248">Range-Lower</span></span>            | <span data-ttu-id="317e6-249">0</span><span class="sxs-lookup"><span data-stu-id="317e6-249">0</span></span>                                 |
| <span data-ttu-id="317e6-250">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="317e6-250">Range-Upper</span></span>            | <span data-ttu-id="317e6-251">32767</span><span class="sxs-lookup"><span data-stu-id="317e6-251">32767</span></span>                             |
| <span data-ttu-id="317e6-252">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-252">Search-Flags</span></span>           | <span data-ttu-id="317e6-253">0x00000000</span><span class="sxs-lookup"><span data-stu-id="317e6-253">0x00000000</span></span>                        |
| <span data-ttu-id="317e6-254">System-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-254">System-Flags</span></span>           | <span data-ttu-id="317e6-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="317e6-255">0x00000010</span></span>                        |
| <span data-ttu-id="317e6-256">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="317e6-256">Classes used in</span></span>        | [<span data-ttu-id="317e6-257">**Нажат**</span><span class="sxs-lookup"><span data-stu-id="317e6-257">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="317e6-258">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="317e6-258">Windows Server 2012</span></span>



| <span data-ttu-id="317e6-259">Ввод</span><span class="sxs-lookup"><span data-stu-id="317e6-259">Entry</span></span> | <span data-ttu-id="317e6-260">Значение</span><span class="sxs-lookup"><span data-stu-id="317e6-260">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="317e6-261">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="317e6-261">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-262">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="317e6-262">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="317e6-263">System-Only</span><span class="sxs-lookup"><span data-stu-id="317e6-263">System-Only</span></span>            | <span data-ttu-id="317e6-264">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-264">False</span></span>                             |
| <span data-ttu-id="317e6-265">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="317e6-265">Is-Single-Valued</span></span>       | <span data-ttu-id="317e6-266">True</span><span class="sxs-lookup"><span data-stu-id="317e6-266">True</span></span>                              |
| <span data-ttu-id="317e6-267">Индексируется</span><span class="sxs-lookup"><span data-stu-id="317e6-267">Is Indexed</span></span>             | <span data-ttu-id="317e6-268">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-268">False</span></span>                             |
| <span data-ttu-id="317e6-269">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="317e6-269">In Global Catalog</span></span>      | <span data-ttu-id="317e6-270">Неверно</span><span class="sxs-lookup"><span data-stu-id="317e6-270">False</span></span>                             |
| <span data-ttu-id="317e6-271">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="317e6-271">NT-Security-Descriptor</span></span> | <span data-ttu-id="317e6-272">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="317e6-272">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="317e6-273">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="317e6-273">Range-Lower</span></span>            | <span data-ttu-id="317e6-274">0</span><span class="sxs-lookup"><span data-stu-id="317e6-274">0</span></span>                                 |
| <span data-ttu-id="317e6-275">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="317e6-275">Range-Upper</span></span>            | <span data-ttu-id="317e6-276">32767</span><span class="sxs-lookup"><span data-stu-id="317e6-276">32767</span></span>                             |
| <span data-ttu-id="317e6-277">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-277">Search-Flags</span></span>           | <span data-ttu-id="317e6-278">0x00000000</span><span class="sxs-lookup"><span data-stu-id="317e6-278">0x00000000</span></span>                        |
| <span data-ttu-id="317e6-279">System-Flags</span><span class="sxs-lookup"><span data-stu-id="317e6-279">System-Flags</span></span>           | <span data-ttu-id="317e6-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="317e6-280">0x00000010</span></span>                        |
| <span data-ttu-id="317e6-281">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="317e6-281">Classes used in</span></span>        | [<span data-ttu-id="317e6-282">**Пользователь**</span><span class="sxs-lookup"><span data-stu-id="317e6-282">**User**</span></span>](c-user.md)<br/> |



 

 





