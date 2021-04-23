---
title: MS-DS-User-не-атрибут срока действия-пароля
description: Указывает, истечет ли срок действия пароля для учетной записи, на которую ссылается этот атрибут.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Active-DS-User-не-схема AD атрибута срока действия пароля
- Схема AD атрибута msDS-Усердонтекспирепассворд
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138623"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a><span data-ttu-id="500e3-105">MS-DS-User-не-атрибут срока действия-пароля</span><span class="sxs-lookup"><span data-stu-id="500e3-105">ms-DS-User-Dont-Expire-Password attribute</span></span>

<span data-ttu-id="500e3-106">Указывает, истечет ли срок действия пароля для учетной записи, на которую ссылается этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="500e3-106">Indicates whether the password for the account this attribute references will expire.</span></span> <span data-ttu-id="500e3-107">Значение true, если срок действия пароля не истечет; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="500e3-107">True if the password will not expire; otherwise, False.</span></span>



| <span data-ttu-id="500e3-108">Ввод</span><span class="sxs-lookup"><span data-stu-id="500e3-108">Entry</span></span> | <span data-ttu-id="500e3-109">Значение</span><span class="sxs-lookup"><span data-stu-id="500e3-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="500e3-110">CN</span><span class="sxs-lookup"><span data-stu-id="500e3-110">CN</span></span>                | <span data-ttu-id="500e3-111">MS-DS-User-не-Expires — пароль</span><span class="sxs-lookup"><span data-stu-id="500e3-111">ms-DS-User-Dont-Expire-Password</span></span>      |
| <span data-ttu-id="500e3-112">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="500e3-112">Ldap-Display-Name</span></span> | <span data-ttu-id="500e3-113">msDS-Усердонтекспирепассворд</span><span class="sxs-lookup"><span data-stu-id="500e3-113">msDS-UserDontExpirePassword</span></span>          |
| <span data-ttu-id="500e3-114">Размер</span><span class="sxs-lookup"><span data-stu-id="500e3-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="500e3-115">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="500e3-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="500e3-116">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="500e3-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="500e3-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="500e3-117">Attribute-Id</span></span>      | <span data-ttu-id="500e3-118">1.2.840.113556.1.4.1855</span><span class="sxs-lookup"><span data-stu-id="500e3-118">1.2.840.113556.1.4.1855</span></span>              |
| <span data-ttu-id="500e3-119">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="500e3-119">System-Id-Guid</span></span>    | <span data-ttu-id="500e3-120">8788193a-2925-43d9-a221-bb7fff397675</span><span class="sxs-lookup"><span data-stu-id="500e3-120">8788193a-2925-43d9-a221-bb7fff397675</span></span> |
| <span data-ttu-id="500e3-121">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="500e3-121">Syntax</span></span>            | [<span data-ttu-id="500e3-122">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="500e3-122">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="500e3-123">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="500e3-123">Implementations</span></span>

-   [<span data-ttu-id="500e3-124">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="500e3-124">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="500e3-125">ADAM</span><span class="sxs-lookup"><span data-stu-id="500e3-125">ADAM</span></span>



| <span data-ttu-id="500e3-126">Ввод</span><span class="sxs-lookup"><span data-stu-id="500e3-126">Entry</span></span> | <span data-ttu-id="500e3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="500e3-127">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="500e3-128">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="500e3-128">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="500e3-129">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="500e3-129">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="500e3-130">System-Only</span><span class="sxs-lookup"><span data-stu-id="500e3-130">System-Only</span></span>            | <span data-ttu-id="500e3-131">Неверно</span><span class="sxs-lookup"><span data-stu-id="500e3-131">False</span></span>                                                             |
| <span data-ttu-id="500e3-132">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="500e3-132">Is-Single-Valued</span></span>       | <span data-ttu-id="500e3-133">True</span><span class="sxs-lookup"><span data-stu-id="500e3-133">True</span></span>                                                              |
| <span data-ttu-id="500e3-134">Индексируется</span><span class="sxs-lookup"><span data-stu-id="500e3-134">Is Indexed</span></span>             | <span data-ttu-id="500e3-135">Неверно</span><span class="sxs-lookup"><span data-stu-id="500e3-135">False</span></span>                                                             |
| <span data-ttu-id="500e3-136">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="500e3-136">In Global Catalog</span></span>      | <span data-ttu-id="500e3-137">Неверно</span><span class="sxs-lookup"><span data-stu-id="500e3-137">False</span></span>                                                             |
| <span data-ttu-id="500e3-138">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="500e3-138">NT-Security-Descriptor</span></span> | <span data-ttu-id="500e3-139">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="500e3-139">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="500e3-140">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="500e3-140">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="500e3-141">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="500e3-141">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="500e3-142">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="500e3-142">Search-Flags</span></span>           | <span data-ttu-id="500e3-143">0x00000000</span><span class="sxs-lookup"><span data-stu-id="500e3-143">0x00000000</span></span>                                                        |
| <span data-ttu-id="500e3-144">System-Flags</span><span class="sxs-lookup"><span data-stu-id="500e3-144">System-Flags</span></span>           | <span data-ttu-id="500e3-145">0x00000010</span><span class="sxs-lookup"><span data-stu-id="500e3-145">0x00000010</span></span>                                                        |
| <span data-ttu-id="500e3-146">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="500e3-146">Classes used in</span></span>        | [<span data-ttu-id="500e3-147">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="500e3-147">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="500e3-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="500e3-148">Remarks</span></span>

<span data-ttu-id="500e3-149">В ADAM этот атрибут заменяет флаг [**ADS \_ УФ \_ не \_ Expires \_ PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) атрибута [**userAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="500e3-149">In ADAM, this attribute replaces the [**ADS\_UF\_DONT\_EXPIRE\_PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

