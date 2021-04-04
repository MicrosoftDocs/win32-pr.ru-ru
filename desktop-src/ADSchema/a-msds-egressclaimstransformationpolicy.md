---
title: MS-DS-исходящие-Claims-преобразование-атрибут политики
description: Это ссылка на объект политики преобразования утверждений для исходящих утверждений (утверждений, походящих из этого леса) в доверенный домен.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- MS-DS-исходящие-Claims-преобразование-схема AD атрибута политики
- Схема AD атрибута msDS-Егрессклаимстрансформатионполици
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3978944b6ae85fcc5fd33682abec7dd3fff0057
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989703"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a><span data-ttu-id="8910b-105">MS-DS-исходящие-Claims-преобразование-атрибут политики</span><span class="sxs-lookup"><span data-stu-id="8910b-105">ms-DS-Egress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="8910b-106">Это ссылка на объект политики преобразования утверждений для исходящих утверждений (утверждений, походящих из этого леса) в доверенный домен.</span><span class="sxs-lookup"><span data-stu-id="8910b-106">This is a link to a Claims Transformation Policy Object for the egress claims (claims leaving this forest) to the Trusted Domain.</span></span> <span data-ttu-id="8910b-107">Это применимо только к входящему или двунаправленному доверию между лесами.</span><span class="sxs-lookup"><span data-stu-id="8910b-107">This is applicable only for an incoming or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="8910b-108">Если эта ссылка отсутствует, все утверждения разрешены для исходящего трафика "как есть".</span><span class="sxs-lookup"><span data-stu-id="8910b-108">When this link is not present, all claims are allowed to egress as-is.</span></span>



| <span data-ttu-id="8910b-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="8910b-109">Entry</span></span> | <span data-ttu-id="8910b-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8910b-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="8910b-111">CN</span><span class="sxs-lookup"><span data-stu-id="8910b-111">CN</span></span>                | <span data-ttu-id="8910b-112">MS-DS-исходящий трафик — утверждения-преобразование — политика</span><span class="sxs-lookup"><span data-stu-id="8910b-112">ms-DS-Egress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="8910b-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="8910b-113">Ldap-Display-Name</span></span> | <span data-ttu-id="8910b-114">msDS-Егрессклаимстрансформатионполици</span><span class="sxs-lookup"><span data-stu-id="8910b-114">msDS-EgressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="8910b-115">Размер</span><span class="sxs-lookup"><span data-stu-id="8910b-115">Size</span></span>              | \-                                        |
| <span data-ttu-id="8910b-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="8910b-116">Update Privilege</span></span>  | \-                                        |
| <span data-ttu-id="8910b-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="8910b-117">Update Frequency</span></span>  | \-                                        |
| <span data-ttu-id="8910b-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="8910b-118">Attribute-Id</span></span>      | <span data-ttu-id="8910b-119">1.2.840.113556.1.4.2192</span><span class="sxs-lookup"><span data-stu-id="8910b-119">1.2.840.113556.1.4.2192</span></span>                   |
| <span data-ttu-id="8910b-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="8910b-120">System-Id-Guid</span></span>    | <span data-ttu-id="8910b-121">c137427e-9a73-b040-9190-1b095bb43288</span><span class="sxs-lookup"><span data-stu-id="8910b-121">c137427e-9a73-b040-9190-1b095bb43288</span></span>      |
| <span data-ttu-id="8910b-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8910b-122">Syntax</span></span>            | [<span data-ttu-id="8910b-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="8910b-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)   |



## <a name="implementations"></a><span data-ttu-id="8910b-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="8910b-124">Implementations</span></span>

-   [<span data-ttu-id="8910b-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="8910b-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="8910b-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8910b-126">Windows Server 2012</span></span>



| <span data-ttu-id="8910b-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="8910b-127">Entry</span></span> | <span data-ttu-id="8910b-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8910b-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="8910b-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="8910b-129">Link-Id</span></span>                | <span data-ttu-id="8910b-130">2192</span><span class="sxs-lookup"><span data-stu-id="8910b-130">2192</span></span>                                                 |
| <span data-ttu-id="8910b-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="8910b-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="8910b-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="8910b-132">System-Only</span></span>            | <span data-ttu-id="8910b-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="8910b-133">False</span></span>                                                |
| <span data-ttu-id="8910b-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="8910b-134">Is-Single-Valued</span></span>       | <span data-ttu-id="8910b-135">True</span><span class="sxs-lookup"><span data-stu-id="8910b-135">True</span></span>                                                 |
| <span data-ttu-id="8910b-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="8910b-136">Is Indexed</span></span>             | <span data-ttu-id="8910b-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="8910b-137">False</span></span>                                                |
| <span data-ttu-id="8910b-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="8910b-138">In Global Catalog</span></span>      | <span data-ttu-id="8910b-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="8910b-139">False</span></span>                                                |
| <span data-ttu-id="8910b-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="8910b-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="8910b-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="8910b-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="8910b-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="8910b-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="8910b-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="8910b-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="8910b-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="8910b-144">Search-Flags</span></span>           | <span data-ttu-id="8910b-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="8910b-145">0x00000000</span></span>                                           |
| <span data-ttu-id="8910b-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="8910b-146">System-Flags</span></span>           | <span data-ttu-id="8910b-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="8910b-147">0x00000010</span></span>                                           |
| <span data-ttu-id="8910b-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="8910b-148">Classes used in</span></span>        | [<span data-ttu-id="8910b-149">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="8910b-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





