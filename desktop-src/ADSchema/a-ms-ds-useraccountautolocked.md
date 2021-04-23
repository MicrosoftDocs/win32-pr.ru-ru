---
title: MS-DS-User-Account-атрибут автоматической блокировки
description: Указывает, заблокирована ли учетная запись, на которую ссылается этот атрибут.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-User-Account-Auto-locked
- Схема AD атрибута ms-DS-Усераккаунтаутолоккед
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072112"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a><span data-ttu-id="4d85c-105">MS-DS-User-Account-атрибут автоматической блокировки</span><span class="sxs-lookup"><span data-stu-id="4d85c-105">ms-DS-User-Account-Auto-Locked attribute</span></span>

<span data-ttu-id="4d85c-106">Указывает, заблокирована ли учетная запись, на которую ссылается этот атрибут. Значение true, если учетная запись заблокирована; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="4d85c-106">Indicates whether the account that this attribute references has been locked out. True if the account is locked out; otherwise, False.</span></span>



| <span data-ttu-id="4d85c-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d85c-107">Entry</span></span> | <span data-ttu-id="4d85c-108">Значение</span><span class="sxs-lookup"><span data-stu-id="4d85c-108">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="4d85c-109">CN</span><span class="sxs-lookup"><span data-stu-id="4d85c-109">CN</span></span>                | <span data-ttu-id="4d85c-110">MS-DS-пользователь-учетная запись — автоматическая блокировка</span><span class="sxs-lookup"><span data-stu-id="4d85c-110">ms-DS-User-Account-Auto-Locked</span></span>       |
| <span data-ttu-id="4d85c-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4d85c-111">Ldap-Display-Name</span></span> | <span data-ttu-id="4d85c-112">MS-DS-Усераккаунтаутолоккед</span><span class="sxs-lookup"><span data-stu-id="4d85c-112">ms-DS-UserAccountAutoLocked</span></span>          |
| <span data-ttu-id="4d85c-113">Размер</span><span class="sxs-lookup"><span data-stu-id="4d85c-113">Size</span></span>              | \-                                   |
| <span data-ttu-id="4d85c-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="4d85c-114">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="4d85c-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="4d85c-115">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="4d85c-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="4d85c-116">Attribute-Id</span></span>      | <span data-ttu-id="4d85c-117">1.2.840.113556.1.4.1857</span><span class="sxs-lookup"><span data-stu-id="4d85c-117">1.2.840.113556.1.4.1857</span></span>              |
| <span data-ttu-id="4d85c-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="4d85c-118">System-Id-Guid</span></span>    | <span data-ttu-id="4d85c-119">f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d</span><span class="sxs-lookup"><span data-stu-id="4d85c-119">f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d</span></span> |
| <span data-ttu-id="4d85c-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d85c-120">Syntax</span></span>            | [<span data-ttu-id="4d85c-121">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="4d85c-121">**Boolean**</span></span>](s-boolean.md)         |



## <a name="implementations"></a><span data-ttu-id="4d85c-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="4d85c-122">Implementations</span></span>

-   [<span data-ttu-id="4d85c-123">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="4d85c-123">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="4d85c-124">ADAM</span><span class="sxs-lookup"><span data-stu-id="4d85c-124">ADAM</span></span>



| <span data-ttu-id="4d85c-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="4d85c-125">Entry</span></span> | <span data-ttu-id="4d85c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4d85c-126">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="4d85c-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="4d85c-127">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4d85c-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="4d85c-128">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="4d85c-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="4d85c-129">System-Only</span></span>            | <span data-ttu-id="4d85c-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d85c-130">False</span></span>                                                             |
| <span data-ttu-id="4d85c-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="4d85c-131">Is-Single-Valued</span></span>       | <span data-ttu-id="4d85c-132">True</span><span class="sxs-lookup"><span data-stu-id="4d85c-132">True</span></span>                                                              |
| <span data-ttu-id="4d85c-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="4d85c-133">Is Indexed</span></span>             | <span data-ttu-id="4d85c-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d85c-134">False</span></span>                                                             |
| <span data-ttu-id="4d85c-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="4d85c-135">In Global Catalog</span></span>      | <span data-ttu-id="4d85c-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="4d85c-136">False</span></span>                                                             |
| <span data-ttu-id="4d85c-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="4d85c-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="4d85c-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="4d85c-138">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="4d85c-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="4d85c-139">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="4d85c-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="4d85c-140">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="4d85c-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="4d85c-141">Search-Flags</span></span>           | <span data-ttu-id="4d85c-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4d85c-142">0x00000000</span></span>                                                        |
| <span data-ttu-id="4d85c-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="4d85c-143">System-Flags</span></span>           | <span data-ttu-id="4d85c-144">0x00000014</span><span class="sxs-lookup"><span data-stu-id="4d85c-144">0x00000014</span></span>                                                        |
| <span data-ttu-id="4d85c-145">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="4d85c-145">Classes used in</span></span>        | [<span data-ttu-id="4d85c-146">**Объект MS-DS-BIND-Object**</span><span class="sxs-lookup"><span data-stu-id="4d85c-146">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4d85c-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d85c-147">Remarks</span></span>

<span data-ttu-id="4d85c-148">В ADAM этот атрибут заменяет флаг [**ADS \_ УФ \_ блокировки**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) атрибута [**userAccountControl**](a-useraccountcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="4d85c-148">In ADAM, this attribute replaces the [**ADS\_UF\_LOCKOUT**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) flag of the [**userAccountControl**](a-useraccountcontrol.md) attribute.</span></span>

 

