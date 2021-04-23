---
title: Install — атрибут уровня пользовательского интерфейса
description: Этот атрибут содержит сведения о типе (уровне) установки, используемом для пользовательского интерфейса.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- Install — схема AD атрибута уровня пользовательского интерфейса
- Схема AD атрибута Инсталлуилевел
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989525"
---
# <a name="install-ui-level-attribute"></a><span data-ttu-id="2be39-105">Install — атрибут уровня пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2be39-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="2be39-106">Этот атрибут содержит сведения о типе (уровне) установки, используемом для пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2be39-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="2be39-107">Возможны следующие уровни установки: 2 ИНСТАЛЛУИЛЕВЕЛ \_ None (автоматическая установка) 3 инсталлуилевел \_ Basic (простая установка с обработкой ошибок) 4 инсталлуилевел \_ сокращенный (разработанный пользовательский интерфейс, диалоговые окна мастера подавляются) 5 инсталлуилевел \_ Full (пользовательский интерфейс с мастерами, ход выполнения, ошибки)</span><span class="sxs-lookup"><span data-stu-id="2be39-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="2be39-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="2be39-108">Entry</span></span> | <span data-ttu-id="2be39-109">Значение</span><span class="sxs-lookup"><span data-stu-id="2be39-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="2be39-110">CN</span><span class="sxs-lookup"><span data-stu-id="2be39-110">CN</span></span>                | <span data-ttu-id="2be39-111">Install — уровень пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2be39-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="2be39-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2be39-112">Ldap-Display-Name</span></span> | <span data-ttu-id="2be39-113">инсталлуилевел</span><span class="sxs-lookup"><span data-stu-id="2be39-113">installUiLevel</span></span>                       |
| <span data-ttu-id="2be39-114">Размер</span><span class="sxs-lookup"><span data-stu-id="2be39-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="2be39-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2be39-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="2be39-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2be39-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="2be39-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2be39-117">Attribute-Id</span></span>      | <span data-ttu-id="2be39-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="2be39-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="2be39-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2be39-119">System-Id-Guid</span></span>    | <span data-ttu-id="2be39-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="2be39-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="2be39-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2be39-121">Syntax</span></span>            | [<span data-ttu-id="2be39-122">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="2be39-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="2be39-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2be39-123">Implementations</span></span>

-   [<span data-ttu-id="2be39-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="2be39-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="2be39-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="2be39-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="2be39-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="2be39-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="2be39-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="2be39-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="2be39-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="2be39-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="2be39-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2be39-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="2be39-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2be39-130">Windows 2000 Server</span></span>



| <span data-ttu-id="2be39-131">Ввод</span><span class="sxs-lookup"><span data-stu-id="2be39-131">Entry</span></span> | <span data-ttu-id="2be39-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2be39-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2be39-133">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2be39-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be39-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be39-135">System-Only</span></span>            | <span data-ttu-id="2be39-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-136">False</span></span>                                                            |
| <span data-ttu-id="2be39-137">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2be39-137">Is-Single-Valued</span></span>       | <span data-ttu-id="2be39-138">True</span><span class="sxs-lookup"><span data-stu-id="2be39-138">True</span></span>                                                             |
| <span data-ttu-id="2be39-139">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2be39-139">Is Indexed</span></span>             | <span data-ttu-id="2be39-140">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-140">False</span></span>                                                            |
| <span data-ttu-id="2be39-141">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2be39-141">In Global Catalog</span></span>      | <span data-ttu-id="2be39-142">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-142">False</span></span>                                                            |
| <span data-ttu-id="2be39-143">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2be39-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be39-144">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2be39-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2be39-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be39-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be39-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-147">Search-Flags</span></span>           | <span data-ttu-id="2be39-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be39-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="2be39-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-149">System-Flags</span></span>           | <span data-ttu-id="2be39-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be39-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="2be39-151">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2be39-151">Classes used in</span></span>        | [<span data-ttu-id="2be39-152">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="2be39-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="2be39-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2be39-153">Windows Server 2003</span></span>



| <span data-ttu-id="2be39-154">Ввод</span><span class="sxs-lookup"><span data-stu-id="2be39-154">Entry</span></span> | <span data-ttu-id="2be39-155">Значение</span><span class="sxs-lookup"><span data-stu-id="2be39-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2be39-156">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2be39-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be39-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be39-158">System-Only</span></span>            | <span data-ttu-id="2be39-159">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-159">False</span></span>                                                            |
| <span data-ttu-id="2be39-160">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2be39-160">Is-Single-Valued</span></span>       | <span data-ttu-id="2be39-161">True</span><span class="sxs-lookup"><span data-stu-id="2be39-161">True</span></span>                                                             |
| <span data-ttu-id="2be39-162">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2be39-162">Is Indexed</span></span>             | <span data-ttu-id="2be39-163">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-163">False</span></span>                                                            |
| <span data-ttu-id="2be39-164">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2be39-164">In Global Catalog</span></span>      | <span data-ttu-id="2be39-165">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-165">False</span></span>                                                            |
| <span data-ttu-id="2be39-166">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2be39-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be39-167">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2be39-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2be39-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be39-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be39-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-170">Search-Flags</span></span>           | <span data-ttu-id="2be39-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be39-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="2be39-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-172">System-Flags</span></span>           | <span data-ttu-id="2be39-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be39-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="2be39-174">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2be39-174">Classes used in</span></span>        | [<span data-ttu-id="2be39-175">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="2be39-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="2be39-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="2be39-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="2be39-177">Ввод</span><span class="sxs-lookup"><span data-stu-id="2be39-177">Entry</span></span> | <span data-ttu-id="2be39-178">Значение</span><span class="sxs-lookup"><span data-stu-id="2be39-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2be39-179">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2be39-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be39-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be39-181">System-Only</span></span>            | <span data-ttu-id="2be39-182">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-182">False</span></span>                                                            |
| <span data-ttu-id="2be39-183">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2be39-183">Is-Single-Valued</span></span>       | <span data-ttu-id="2be39-184">True</span><span class="sxs-lookup"><span data-stu-id="2be39-184">True</span></span>                                                             |
| <span data-ttu-id="2be39-185">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2be39-185">Is Indexed</span></span>             | <span data-ttu-id="2be39-186">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-186">False</span></span>                                                            |
| <span data-ttu-id="2be39-187">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2be39-187">In Global Catalog</span></span>      | <span data-ttu-id="2be39-188">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-188">False</span></span>                                                            |
| <span data-ttu-id="2be39-189">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2be39-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be39-190">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2be39-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2be39-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be39-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be39-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-193">Search-Flags</span></span>           | <span data-ttu-id="2be39-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be39-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="2be39-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-195">System-Flags</span></span>           | <span data-ttu-id="2be39-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be39-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="2be39-197">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2be39-197">Classes used in</span></span>        | [<span data-ttu-id="2be39-198">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="2be39-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="2be39-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2be39-199">Windows Server 2008</span></span>



| <span data-ttu-id="2be39-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="2be39-200">Entry</span></span> | <span data-ttu-id="2be39-201">Значение</span><span class="sxs-lookup"><span data-stu-id="2be39-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2be39-202">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2be39-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be39-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be39-204">System-Only</span></span>            | <span data-ttu-id="2be39-205">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-205">False</span></span>                                                            |
| <span data-ttu-id="2be39-206">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2be39-206">Is-Single-Valued</span></span>       | <span data-ttu-id="2be39-207">True</span><span class="sxs-lookup"><span data-stu-id="2be39-207">True</span></span>                                                             |
| <span data-ttu-id="2be39-208">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2be39-208">Is Indexed</span></span>             | <span data-ttu-id="2be39-209">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-209">False</span></span>                                                            |
| <span data-ttu-id="2be39-210">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2be39-210">In Global Catalog</span></span>      | <span data-ttu-id="2be39-211">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-211">False</span></span>                                                            |
| <span data-ttu-id="2be39-212">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2be39-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be39-213">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2be39-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2be39-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be39-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be39-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-216">Search-Flags</span></span>           | <span data-ttu-id="2be39-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be39-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="2be39-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-218">System-Flags</span></span>           | <span data-ttu-id="2be39-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be39-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="2be39-220">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2be39-220">Classes used in</span></span>        | [<span data-ttu-id="2be39-221">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="2be39-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="2be39-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2be39-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="2be39-223">Ввод</span><span class="sxs-lookup"><span data-stu-id="2be39-223">Entry</span></span> | <span data-ttu-id="2be39-224">Значение</span><span class="sxs-lookup"><span data-stu-id="2be39-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2be39-225">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2be39-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be39-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be39-227">System-Only</span></span>            | <span data-ttu-id="2be39-228">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-228">False</span></span>                                                            |
| <span data-ttu-id="2be39-229">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2be39-229">Is-Single-Valued</span></span>       | <span data-ttu-id="2be39-230">True</span><span class="sxs-lookup"><span data-stu-id="2be39-230">True</span></span>                                                             |
| <span data-ttu-id="2be39-231">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2be39-231">Is Indexed</span></span>             | <span data-ttu-id="2be39-232">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-232">False</span></span>                                                            |
| <span data-ttu-id="2be39-233">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2be39-233">In Global Catalog</span></span>      | <span data-ttu-id="2be39-234">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-234">False</span></span>                                                            |
| <span data-ttu-id="2be39-235">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2be39-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be39-236">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2be39-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2be39-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be39-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be39-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-239">Search-Flags</span></span>           | <span data-ttu-id="2be39-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be39-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="2be39-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-241">System-Flags</span></span>           | <span data-ttu-id="2be39-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be39-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="2be39-243">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2be39-243">Classes used in</span></span>        | [<span data-ttu-id="2be39-244">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="2be39-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="2be39-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2be39-245">Windows Server 2012</span></span>



| <span data-ttu-id="2be39-246">Ввод</span><span class="sxs-lookup"><span data-stu-id="2be39-246">Entry</span></span> | <span data-ttu-id="2be39-247">Значение</span><span class="sxs-lookup"><span data-stu-id="2be39-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="2be39-248">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2be39-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2be39-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="2be39-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="2be39-250">System-Only</span></span>            | <span data-ttu-id="2be39-251">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-251">False</span></span>                                                            |
| <span data-ttu-id="2be39-252">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2be39-252">Is-Single-Valued</span></span>       | <span data-ttu-id="2be39-253">True</span><span class="sxs-lookup"><span data-stu-id="2be39-253">True</span></span>                                                             |
| <span data-ttu-id="2be39-254">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2be39-254">Is Indexed</span></span>             | <span data-ttu-id="2be39-255">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-255">False</span></span>                                                            |
| <span data-ttu-id="2be39-256">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2be39-256">In Global Catalog</span></span>      | <span data-ttu-id="2be39-257">Неверно</span><span class="sxs-lookup"><span data-stu-id="2be39-257">False</span></span>                                                            |
| <span data-ttu-id="2be39-258">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2be39-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="2be39-259">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2be39-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="2be39-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2be39-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2be39-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="2be39-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-262">Search-Flags</span></span>           | <span data-ttu-id="2be39-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2be39-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="2be39-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2be39-264">System-Flags</span></span>           | <span data-ttu-id="2be39-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2be39-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="2be39-266">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2be39-266">Classes used in</span></span>        | [<span data-ttu-id="2be39-267">**Регистрация пакета**</span><span class="sxs-lookup"><span data-stu-id="2be39-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





