---
title: Атрибут ms-DS-User-Password-Expires
description: Указывает, истек ли срок действия пароля для учетной записи, на которую ссылается этот атрибут.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута с истекшим сроком действия MS-DS-User-Password
- Схема AD атрибута msDS-Усерпассвордекспиред
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d99143c470e58d1b1cb5e0cbd7e5302618ff0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262266"
---
# <a name="ms-ds-user-password-expired-attribute"></a><span data-ttu-id="07be5-105">Атрибут ms-DS-User-Password-Expires</span><span class="sxs-lookup"><span data-stu-id="07be5-105">ms-DS-User-Password-Expired attribute</span></span>

<span data-ttu-id="07be5-106">Указывает, истек ли срок действия пароля для учетной записи, на которую ссылается этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="07be5-106">Indicates whether the password for the account that this attribute references has expired.</span></span> <span data-ttu-id="07be5-107">Значение true, если срок действия пароля истек; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="07be5-107">True if the password has expired; otherwise, False.</span></span>



| <span data-ttu-id="07be5-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="07be5-108">Entry</span></span> | <span data-ttu-id="07be5-109">Значение</span><span class="sxs-lookup"><span data-stu-id="07be5-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="07be5-110">CN</span><span class="sxs-lookup"><span data-stu-id="07be5-110">CN</span></span>                | <span data-ttu-id="07be5-111">MS-DS-User-Password-срок действия истек</span><span class="sxs-lookup"><span data-stu-id="07be5-111">ms-DS-User-Password-Expired</span></span>          |
| <span data-ttu-id="07be5-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="07be5-112">Ldap-Display-Name</span></span> | <span data-ttu-id="07be5-113">msDS-Усерпассвордекспиред</span><span class="sxs-lookup"><span data-stu-id="07be5-113">msDS-UserPasswordExpired</span></span>             |
| <span data-ttu-id="07be5-114">Размер</span><span class="sxs-lookup"><span data-stu-id="07be5-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="07be5-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="07be5-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="07be5-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="07be5-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="07be5-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="07be5-117">Attribute-Id</span></span>      | <span data-ttu-id="07be5-118">1.2.840.113556.1.4.1858</span><span class="sxs-lookup"><span data-stu-id="07be5-118">1.2.840.113556.1.4.1858</span></span>              |
| <span data-ttu-id="07be5-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="07be5-119">System-Id-Guid</span></span>    | <span data-ttu-id="07be5-120">565c7ab5-e13e-47f6-abb5-de741806f125</span><span class="sxs-lookup"><span data-stu-id="07be5-120">565c7ab5-e13e-47f6-abb5-de741806f125</span></span> |
| <span data-ttu-id="07be5-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07be5-121">Syntax</span></span>            | [<span data-ttu-id="07be5-122">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="07be5-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="07be5-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="07be5-123">Implementations</span></span>

-   [<span data-ttu-id="07be5-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="07be5-124">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="07be5-125">ADAM</span><span class="sxs-lookup"><span data-stu-id="07be5-125">ADAM</span></span>



| <span data-ttu-id="07be5-126">Ввод</span><span class="sxs-lookup"><span data-stu-id="07be5-126">Entry</span></span> | <span data-ttu-id="07be5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="07be5-127">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="07be5-128">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="07be5-128">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="07be5-129">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="07be5-129">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="07be5-130">System-Only</span><span class="sxs-lookup"><span data-stu-id="07be5-130">System-Only</span></span>            | <span data-ttu-id="07be5-131">Неверно</span><span class="sxs-lookup"><span data-stu-id="07be5-131">False</span></span>                                                             |
| <span data-ttu-id="07be5-132">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="07be5-132">Is-Single-Valued</span></span>       | <span data-ttu-id="07be5-133">True</span><span class="sxs-lookup"><span data-stu-id="07be5-133">True</span></span>                                                              |
| <span data-ttu-id="07be5-134">Индексируется</span><span class="sxs-lookup"><span data-stu-id="07be5-134">Is Indexed</span></span>             | <span data-ttu-id="07be5-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="07be5-135">False</span></span>                                                             |
| <span data-ttu-id="07be5-136">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="07be5-136">In Global Catalog</span></span>      | <span data-ttu-id="07be5-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="07be5-137">False</span></span>                                                             |
| <span data-ttu-id="07be5-138">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="07be5-138">NT-Security-Descriptor</span></span> | <span data-ttu-id="07be5-139">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="07be5-139">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="07be5-140">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="07be5-140">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="07be5-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="07be5-141">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="07be5-142">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="07be5-142">Search-Flags</span></span>           | <span data-ttu-id="07be5-143">0x00000000</span><span class="sxs-lookup"><span data-stu-id="07be5-143">0x00000000</span></span>                                                        |
| <span data-ttu-id="07be5-144">System-Flags</span><span class="sxs-lookup"><span data-stu-id="07be5-144">System-Flags</span></span>           | <span data-ttu-id="07be5-145">0x00000014</span><span class="sxs-lookup"><span data-stu-id="07be5-145">0x00000014</span></span>                                                        |
| <span data-ttu-id="07be5-146">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="07be5-146">Classes used in</span></span>        | [<span data-ttu-id="07be5-147">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="07be5-147">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="07be5-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07be5-148">Remarks</span></span>

<span data-ttu-id="07be5-149">В ADAM этот атрибут заменяет флаг " [**ADS" \_ УФ " \_ \_ срок действия пароля истек**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " атрибута [**userAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="07be5-149">In ADAM, this attribute replaces the [**ADS\_UF\_PASSWORD\_EXPIRED**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

