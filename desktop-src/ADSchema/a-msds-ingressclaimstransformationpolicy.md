---
title: MS-DS-входящие-Claims-преобразование-атрибут политики
description: Это ссылка на объект политики преобразования утверждений для входящих утверждений (утверждений, поступающих в этот лес) из доверенного домена.
ms.assetid: 67f87782-85ed-41bb-a60d-f6c11fcda80e
ms.tgt_platform: multiple
keywords:
- MS-DS-входящий-Claims-преобразование-схема AD атрибута политики
- Схема AD атрибута msDS-Ингрессклаимстрансформатионполици
topic_type:
- apiref
api_name:
- ms-DS-Ingress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50e3c187a4cb3b2a465257b408a1f5603c756ba
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536038"
---
# <a name="ms-ds-ingress-claims-transformation-policy-attribute"></a><span data-ttu-id="22dd3-105">MS-DS-входящие-Claims-преобразование-атрибут политики</span><span class="sxs-lookup"><span data-stu-id="22dd3-105">ms-DS-Ingress-Claims-Transformation-Policy attribute</span></span>

<span data-ttu-id="22dd3-106">Это ссылка на объект политики преобразования утверждений для входящих утверждений (утверждений, поступающих в этот лес) из доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="22dd3-106">This is a link to a Claims Transformation Policy Object for the ingress claims (claims entering this forest) from the Trusted Domain.</span></span> <span data-ttu-id="22dd3-107">Это применимо только к исходящему или двунаправленному доверию между лесами.</span><span class="sxs-lookup"><span data-stu-id="22dd3-107">This is applicable only for an outgoing or bidirectional Cross-Forest Trust.</span></span> <span data-ttu-id="22dd3-108">Если эта ссылка отсутствует, все входящие утверждения будут удалены.</span><span class="sxs-lookup"><span data-stu-id="22dd3-108">If this link is absent, all the ingress claims are dropped.</span></span>



| <span data-ttu-id="22dd3-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="22dd3-109">Entry</span></span> | <span data-ttu-id="22dd3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="22dd3-110">Value</span></span> |
|-------------------|--------------------------------------------|
| <span data-ttu-id="22dd3-111">CN</span><span class="sxs-lookup"><span data-stu-id="22dd3-111">CN</span></span>                | <span data-ttu-id="22dd3-112">MS-DS-входящие-Claims-преобразование — политика</span><span class="sxs-lookup"><span data-stu-id="22dd3-112">ms-DS-Ingress-Claims-Transformation-Policy</span></span> |
| <span data-ttu-id="22dd3-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="22dd3-113">Ldap-Display-Name</span></span> | <span data-ttu-id="22dd3-114">msDS-Ингрессклаимстрансформатионполици</span><span class="sxs-lookup"><span data-stu-id="22dd3-114">msDS-IngressClaimsTransformationPolicy</span></span>     |
| <span data-ttu-id="22dd3-115">Размер</span><span class="sxs-lookup"><span data-stu-id="22dd3-115">Size</span></span>              | \-                                         |
| <span data-ttu-id="22dd3-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="22dd3-116">Update Privilege</span></span>  | \-                                         |
| <span data-ttu-id="22dd3-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="22dd3-117">Update Frequency</span></span>  | \-                                         |
| <span data-ttu-id="22dd3-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="22dd3-118">Attribute-Id</span></span>      | <span data-ttu-id="22dd3-119">1.2.840.113556.1.4.2191</span><span class="sxs-lookup"><span data-stu-id="22dd3-119">1.2.840.113556.1.4.2191</span></span>                    |
| <span data-ttu-id="22dd3-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="22dd3-120">System-Id-Guid</span></span>    | <span data-ttu-id="22dd3-121">86284c08-0c6e-1540-8b15-75147d23d20d</span><span class="sxs-lookup"><span data-stu-id="22dd3-121">86284c08-0c6e-1540-8b15-75147d23d20d</span></span>       |
| <span data-ttu-id="22dd3-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22dd3-122">Syntax</span></span>            | [<span data-ttu-id="22dd3-123">**Object(DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="22dd3-123">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)    |



## <a name="implementations"></a><span data-ttu-id="22dd3-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="22dd3-124">Implementations</span></span>

-   [<span data-ttu-id="22dd3-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="22dd3-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="22dd3-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="22dd3-126">Windows Server 2012</span></span>



| <span data-ttu-id="22dd3-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="22dd3-127">Entry</span></span> | <span data-ttu-id="22dd3-128">Значение</span><span class="sxs-lookup"><span data-stu-id="22dd3-128">Value</span></span> |
|------------------------|------------------------------------------------------|
| <span data-ttu-id="22dd3-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="22dd3-129">Link-Id</span></span>                | <span data-ttu-id="22dd3-130">2190</span><span class="sxs-lookup"><span data-stu-id="22dd3-130">2190</span></span>                                                 |
| <span data-ttu-id="22dd3-131">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="22dd3-131">MAPI-Id</span></span>                | \-                                                   |
| <span data-ttu-id="22dd3-132">System-Only</span><span class="sxs-lookup"><span data-stu-id="22dd3-132">System-Only</span></span>            | <span data-ttu-id="22dd3-133">Неверно</span><span class="sxs-lookup"><span data-stu-id="22dd3-133">False</span></span>                                                |
| <span data-ttu-id="22dd3-134">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="22dd3-134">Is-Single-Valued</span></span>       | <span data-ttu-id="22dd3-135">True</span><span class="sxs-lookup"><span data-stu-id="22dd3-135">True</span></span>                                                 |
| <span data-ttu-id="22dd3-136">Индексируется</span><span class="sxs-lookup"><span data-stu-id="22dd3-136">Is Indexed</span></span>             | <span data-ttu-id="22dd3-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="22dd3-137">False</span></span>                                                |
| <span data-ttu-id="22dd3-138">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="22dd3-138">In Global Catalog</span></span>      | <span data-ttu-id="22dd3-139">Неверно</span><span class="sxs-lookup"><span data-stu-id="22dd3-139">False</span></span>                                                |
| <span data-ttu-id="22dd3-140">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="22dd3-140">NT-Security-Descriptor</span></span> | <span data-ttu-id="22dd3-141">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="22dd3-141">O:BAG:BAD:S:</span></span>                                         |
| <span data-ttu-id="22dd3-142">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="22dd3-142">Range-Lower</span></span>            | \-                                                   |
| <span data-ttu-id="22dd3-143">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="22dd3-143">Range-Upper</span></span>            | \-                                                   |
| <span data-ttu-id="22dd3-144">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="22dd3-144">Search-Flags</span></span>           | <span data-ttu-id="22dd3-145">0x00000000</span><span class="sxs-lookup"><span data-stu-id="22dd3-145">0x00000000</span></span>                                           |
| <span data-ttu-id="22dd3-146">System-Flags</span><span class="sxs-lookup"><span data-stu-id="22dd3-146">System-Flags</span></span>           | <span data-ttu-id="22dd3-147">0x00000010</span><span class="sxs-lookup"><span data-stu-id="22dd3-147">0x00000010</span></span>                                           |
| <span data-ttu-id="22dd3-148">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="22dd3-148">Classes used in</span></span>        | [<span data-ttu-id="22dd3-149">**Доверенный домен**</span><span class="sxs-lookup"><span data-stu-id="22dd3-149">**Trusted-Domain**</span></span>](c-trusteddomain.md)<br/> |



 

 





