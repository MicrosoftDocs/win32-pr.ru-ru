---
title: Атрибут ms-DS-Allowed-to-акту-On-My-Identity
description: Этот атрибут используется для проверки доступа, чтобы определить, имеет ли запрашивающий разрешение на действия от имени других удостоверений для служб, выполняющихся в качестве этой учетной записи.
ms.assetid: 38203665-4505-461b-b6ab-b634725ac2fa
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута Identity в службе MS-DS-Allowed-to-"
- Схема AD атрибута msDS-AllowedToActOnBehalfOfOtherIdentity
topic_type:
- apiref
api_name:
- ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45dacd532b1d8a55b3656dc1d65fc1ebd940476c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103893858"
---
# <a name="ms-ds-allowed-to-act-on-behalf-of-other-identity-attribute"></a><span data-ttu-id="ae678-105">Атрибут ms-DS-Allowed-to-акту-On-My-Identity</span><span class="sxs-lookup"><span data-stu-id="ae678-105">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity attribute</span></span>

<span data-ttu-id="ae678-106">Этот атрибут используется для проверки доступа, чтобы определить, имеет ли запрашивающий разрешение на действия от имени других удостоверений для служб, выполняющихся в качестве этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="ae678-106">This attribute is used for access checks to determine if a requestor has permission to act on the behalf of other identities to services running as this account.</span></span>



| <span data-ttu-id="ae678-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae678-107">Entry</span></span> | <span data-ttu-id="ae678-108">Значение</span><span class="sxs-lookup"><span data-stu-id="ae678-108">Value</span></span> |
|-------------------|-----------------------------------------------------|
| <span data-ttu-id="ae678-109">CN</span><span class="sxs-lookup"><span data-stu-id="ae678-109">CN</span></span>                | <span data-ttu-id="ae678-110">MS-DS-Allowed-to-"Active-on-чужое удостоверение"</span><span class="sxs-lookup"><span data-stu-id="ae678-110">ms-DS-Allowed-To-Act-On-Behalf-Of-Other-Identity</span></span>    |
| <span data-ttu-id="ae678-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="ae678-111">Ldap-Display-Name</span></span> | <span data-ttu-id="ae678-112">msDS-AllowedToActOnBehalfOfOtherIdentity</span><span class="sxs-lookup"><span data-stu-id="ae678-112">msDS-AllowedToActOnBehalfOfOtherIdentity</span></span>            |
| <span data-ttu-id="ae678-113">Размер</span><span class="sxs-lookup"><span data-stu-id="ae678-113">Size</span></span>              | \-                                                  |
| <span data-ttu-id="ae678-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="ae678-114">Update Privilege</span></span>  | \-                                                  |
| <span data-ttu-id="ae678-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="ae678-115">Update Frequency</span></span>  | \-                                                  |
| <span data-ttu-id="ae678-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="ae678-116">Attribute-Id</span></span>      | <span data-ttu-id="ae678-117">1.2.840.113556.1.4.2182</span><span class="sxs-lookup"><span data-stu-id="ae678-117">1.2.840.113556.1.4.2182</span></span>                             |
| <span data-ttu-id="ae678-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="ae678-118">System-Id-Guid</span></span>    | <span data-ttu-id="ae678-119">3f78c3e5-f79a-46bd-a0b8-9d18116ddc79</span><span class="sxs-lookup"><span data-stu-id="ae678-119">3f78c3e5-f79a-46bd-a0b8-9d18116ddc79</span></span>                |
| <span data-ttu-id="ae678-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae678-120">Syntax</span></span>            | [<span data-ttu-id="ae678-121">**String(NT-Sec-Desc)**</span><span class="sxs-lookup"><span data-stu-id="ae678-121">**String(NT-Sec-Desc)**</span></span>](s-string-nt-sec-desc.md) |



## <a name="implementations"></a><span data-ttu-id="ae678-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="ae678-122">Implementations</span></span>

-   [<span data-ttu-id="ae678-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="ae678-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="ae678-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae678-124">Windows Server 2012</span></span>



| <span data-ttu-id="ae678-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="ae678-125">Entry</span></span> | <span data-ttu-id="ae678-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ae678-126">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="ae678-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="ae678-127">Link-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ae678-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="ae678-128">MAPI-Id</span></span>                | \-                                                                 |
| <span data-ttu-id="ae678-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="ae678-129">System-Only</span></span>            | <span data-ttu-id="ae678-130">True</span><span class="sxs-lookup"><span data-stu-id="ae678-130">True</span></span>                                                               |
| <span data-ttu-id="ae678-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="ae678-131">Is-Single-Valued</span></span>       | <span data-ttu-id="ae678-132">True</span><span class="sxs-lookup"><span data-stu-id="ae678-132">True</span></span>                                                               |
| <span data-ttu-id="ae678-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="ae678-133">Is Indexed</span></span>             | <span data-ttu-id="ae678-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae678-134">False</span></span>                                                              |
| <span data-ttu-id="ae678-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="ae678-135">In Global Catalog</span></span>      | <span data-ttu-id="ae678-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="ae678-136">False</span></span>                                                              |
| <span data-ttu-id="ae678-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="ae678-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="ae678-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="ae678-138">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="ae678-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="ae678-139">Range-Lower</span></span>            | <span data-ttu-id="ae678-140">0</span><span class="sxs-lookup"><span data-stu-id="ae678-140">0</span></span>                                                                  |
| <span data-ttu-id="ae678-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="ae678-141">Range-Upper</span></span>            | <span data-ttu-id="ae678-142">132096</span><span class="sxs-lookup"><span data-stu-id="ae678-142">132096</span></span>                                                             |
| <span data-ttu-id="ae678-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="ae678-143">Search-Flags</span></span>           | <span data-ttu-id="ae678-144">0x00000000</span><span class="sxs-lookup"><span data-stu-id="ae678-144">0x00000000</span></span>                                                         |
| <span data-ttu-id="ae678-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="ae678-145">System-Flags</span></span>           | <span data-ttu-id="ae678-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ae678-146">0x00000010</span></span>                                                         |
| <span data-ttu-id="ae678-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="ae678-147">Classes used in</span></span>        | [<span data-ttu-id="ae678-148">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="ae678-148">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





