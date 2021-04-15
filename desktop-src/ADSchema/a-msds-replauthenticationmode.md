---
title: Атрибут ms-DS-REPL-Authentication-Mode
description: Атрибут ms-DS-REPL-Authentication-Mode используется для указания метода проверки подлинности, используемого для проверки подлинности партнеров репликации.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута в режиме проверки подлинности MS-DS-REPL
- msDS-схема Active Directory для атрибутов
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494019"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a><span data-ttu-id="8a1d7-105">Атрибут ms-DS-REPL-Authentication-Mode</span><span class="sxs-lookup"><span data-stu-id="8a1d7-105">ms-DS-Repl-Authentication-Mode attribute</span></span>

<span data-ttu-id="8a1d7-106">Атрибут **MS-DS-REPL-Authentication-Mode** используется для указания метода проверки подлинности, используемого для проверки подлинности партнеров репликации.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-106">The **ms-DS-Repl-Authentication-Mode** attribute is used to specify which authentication method is used to authenticate replication partners.</span></span> <span data-ttu-id="8a1d7-107">Этот атрибут применяется к разделу конфигурации экземпляра ADAM.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-107">This attribute applies to the configuration partition of an ADAM instance.</span></span>

<span data-ttu-id="8a1d7-108">Для этого атрибута возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-108">The following values are the possible values for this attribute.</span></span>

| <span data-ttu-id="8a1d7-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8a1d7-109">Value</span></span>        | <span data-ttu-id="8a1d7-110">Метод проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8a1d7-110">Authentication method</span></span>                          | <span data-ttu-id="8a1d7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8a1d7-111">Description</span></span>                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1d7-112">0</span><span class="sxs-lookup"><span data-stu-id="8a1d7-112">0</span></span><br/> | <span data-ttu-id="8a1d7-113">Согласование (сквозная проверка)</span><span class="sxs-lookup"><span data-stu-id="8a1d7-113">Negotiated pass-through</span></span><br/>             | <span data-ttu-id="8a1d7-114">Все экземпляры ADAM в наборе конфигурации используют идентичные имя учетной записи и пароль в качестве учетной записи службы ADAM.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-114">All ADAM instances in the configuration set use an identical account name and password as the ADAM service account.</span></span><br/>                                                 |
| <span data-ttu-id="8a1d7-115">1</span><span class="sxs-lookup"><span data-stu-id="8a1d7-115">1</span></span><br/> | <span data-ttu-id="8a1d7-116">На стадии изучения</span><span class="sxs-lookup"><span data-stu-id="8a1d7-116">Negotiated</span></span><br/>                          | <span data-ttu-id="8a1d7-117">Сначала выполняется попытка проверки подлинности Kerberos (с использованием имен SPN).</span><span class="sxs-lookup"><span data-stu-id="8a1d7-117">Kerberos authentication (using SPNs) is attempted first.</span></span> <span data-ttu-id="8a1d7-118">В случае сбоя Kerberos выполняется попытка проверки подлинности NTLM.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-118">If Kerberos fails, NTLM authentication is attempted.</span></span> <span data-ttu-id="8a1d7-119">В случае сбоя NTLM экземпляры ADAM не будут реплицироваться.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-119">If NTLM fails, the ADAM instances will not replicate.</span></span><br/> |
| <span data-ttu-id="8a1d7-120">2</span><span class="sxs-lookup"><span data-stu-id="8a1d7-120">2</span></span><br/> | <span data-ttu-id="8a1d7-121">Взаимная проверка подлинности Kerberos</span><span class="sxs-lookup"><span data-stu-id="8a1d7-121">Mutual authentication with Kerberos</span></span><br/> | <span data-ttu-id="8a1d7-122">Необходима проверка подлинности Kerberos с использованием имен участников безопасности службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="8a1d7-122">Kerberos authentication, using service principal names (SPNs), is required.</span></span> <span data-ttu-id="8a1d7-123">Если проверка подлинности Kerberos завершается сбоем, экземпляры ADAM не реплицируются.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-123">If Kerberos authentication fails, the ADAM instances will not replicate.</span></span><br/>                |



 

<span data-ttu-id="8a1d7-124">В следующей таблице содержатся программные идентификаторы для значений этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="8a1d7-124">The following table contains the programmatic identifiers for the values of this attribute.</span></span>

| <span data-ttu-id="8a1d7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8a1d7-125">Value</span></span>        | <span data-ttu-id="8a1d7-126">Идентификатор (из NTDSAPI. h)</span><span class="sxs-lookup"><span data-stu-id="8a1d7-126">Identifier (from Ntdsapi.h)</span></span>                                               |
|--------------|---------------------------------------------------------------------------|
| <span data-ttu-id="8a1d7-127">0</span><span class="sxs-lookup"><span data-stu-id="8a1d7-127">0</span></span><br/> | <span data-ttu-id="8a1d7-128">**\_ \_ режим проверки подлинности ADAM REPL \_ \_ — согласование \_ передачи \_**</span><span class="sxs-lookup"><span data-stu-id="8a1d7-128">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE\_PASS\_THROUGH**</span></span><br/> |
| <span data-ttu-id="8a1d7-129">1</span><span class="sxs-lookup"><span data-stu-id="8a1d7-129">1</span></span><br/> | <span data-ttu-id="8a1d7-130">**\_ \_ согласование режима проверки подлинности ADAM REPL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8a1d7-130">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE**</span></span><br/>                |
| <span data-ttu-id="8a1d7-131">2</span><span class="sxs-lookup"><span data-stu-id="8a1d7-131">2</span></span><br/> | <span data-ttu-id="8a1d7-132">**\_ \_ \_ \_ требуется взаимная проверка \_ подлинности режима ADAM REPL \_**</span><span class="sxs-lookup"><span data-stu-id="8a1d7-132">**ADAM\_REPL\_AUTHENTICATION\_MODE\_MUTUAL\_AUTH\_REQUIRED**</span></span><br/>   |



 



| <span data-ttu-id="8a1d7-133">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a1d7-133">Entry</span></span> | <span data-ttu-id="8a1d7-134">Значение</span><span class="sxs-lookup"><span data-stu-id="8a1d7-134">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="8a1d7-135">CN</span><span class="sxs-lookup"><span data-stu-id="8a1d7-135">CN</span></span>                | <span data-ttu-id="8a1d7-136">MS-DS-REPL-режим проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="8a1d7-136">ms-DS-Repl-Authentication-Mode</span></span>       |
| <span data-ttu-id="8a1d7-137">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8a1d7-137">Ldap-Display-Name</span></span> | <span data-ttu-id="8a1d7-138">msDS-ReplAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="8a1d7-138">msDS-ReplAuthenticationMode</span></span>          |
| <span data-ttu-id="8a1d7-139">Размер</span><span class="sxs-lookup"><span data-stu-id="8a1d7-139">Size</span></span>              | \-                                   |
| <span data-ttu-id="8a1d7-140">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8a1d7-140">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="8a1d7-141">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8a1d7-141">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="8a1d7-142">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8a1d7-142">Attribute-Id</span></span>      | <span data-ttu-id="8a1d7-143">1.2.840.113556.1.4.1861</span><span class="sxs-lookup"><span data-stu-id="8a1d7-143">1.2.840.113556.1.4.1861</span></span>              |
| <span data-ttu-id="8a1d7-144">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8a1d7-144">System-Id-Guid</span></span>    | <span data-ttu-id="8a1d7-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span><span class="sxs-lookup"><span data-stu-id="8a1d7-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span></span> |
| <span data-ttu-id="8a1d7-146">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a1d7-146">Syntax</span></span>            | [<span data-ttu-id="8a1d7-147">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="8a1d7-147">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="8a1d7-148">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8a1d7-148">Implementations</span></span>

-   [<span data-ttu-id="8a1d7-149">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="8a1d7-149">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="8a1d7-150">ADAM</span><span class="sxs-lookup"><span data-stu-id="8a1d7-150">ADAM</span></span>



| <span data-ttu-id="8a1d7-151">Ввод</span><span class="sxs-lookup"><span data-stu-id="8a1d7-151">Entry</span></span> | <span data-ttu-id="8a1d7-152">Значение</span><span class="sxs-lookup"><span data-stu-id="8a1d7-152">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="8a1d7-153">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8a1d7-153">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="8a1d7-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8a1d7-154">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="8a1d7-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="8a1d7-155">System-Only</span></span>            | <span data-ttu-id="8a1d7-156">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a1d7-156">False</span></span>                                               |
| <span data-ttu-id="8a1d7-157">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8a1d7-157">Is-Single-Valued</span></span>       | <span data-ttu-id="8a1d7-158">True</span><span class="sxs-lookup"><span data-stu-id="8a1d7-158">True</span></span>                                                |
| <span data-ttu-id="8a1d7-159">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8a1d7-159">Is Indexed</span></span>             | <span data-ttu-id="8a1d7-160">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a1d7-160">False</span></span>                                               |
| <span data-ttu-id="8a1d7-161">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8a1d7-161">In Global Catalog</span></span>      | <span data-ttu-id="8a1d7-162">Неверно</span><span class="sxs-lookup"><span data-stu-id="8a1d7-162">False</span></span>                                               |
| <span data-ttu-id="8a1d7-163">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8a1d7-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="8a1d7-164">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8a1d7-164">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="8a1d7-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8a1d7-165">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="8a1d7-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8a1d7-166">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="8a1d7-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1d7-167">Search-Flags</span></span>           | <span data-ttu-id="8a1d7-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8a1d7-168">0x00000000</span></span>                                          |
| <span data-ttu-id="8a1d7-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8a1d7-169">System-Flags</span></span>           | <span data-ttu-id="8a1d7-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8a1d7-170">0x00000010</span></span>                                          |
| <span data-ttu-id="8a1d7-171">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8a1d7-171">Classes used in</span></span>        | [<span data-ttu-id="8a1d7-172">**Конфигурация**</span><span class="sxs-lookup"><span data-stu-id="8a1d7-172">**Configuration**</span></span>](c-configuration.md)<br/> |



 

 





