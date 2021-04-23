---
title: Атрибут ms-DS-Манажедпассворд
description: Этот сконструированный атрибут возвращает большой двоичный объект, содержащий предыдущий и текущий пароли, Тимеунтилепочекспирес и Тимеунтилнекстсчедуледупдате для группы MSA.
ms.assetid: bcabb20f-46f3-4c15-b71b-a8dfc43678bc
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-Манажедпассворд
- Схема AD атрибута msDS-Манажедпассворд
topic_type:
- apiref
api_name:
- ms-DS-ManagedPassword
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a440f1849e01ae4930b72441f75b17ce51a0566b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138654"
---
# <a name="ms-ds-managedpassword-attribute"></a><span data-ttu-id="2d1e6-105">Атрибут ms-DS-Манажедпассворд</span><span class="sxs-lookup"><span data-stu-id="2d1e6-105">ms-DS-ManagedPassword attribute</span></span>

<span data-ttu-id="2d1e6-106">Этот сконструированный атрибут возвращает большой двоичный объект, содержащий предыдущий и текущий пароли, Тимеунтилепочекспирес и Тимеунтилнекстсчедуледупдате для группы MSA.</span><span class="sxs-lookup"><span data-stu-id="2d1e6-106">This constructed attribute returns a blob that contains the clear-text previous and current password, TimeUntilEpochExpires, and TimeUntilNextScheduledUpdate for a group MSA.</span></span>



| <span data-ttu-id="2d1e6-107">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d1e6-107">Entry</span></span> | <span data-ttu-id="2d1e6-108">Значение</span><span class="sxs-lookup"><span data-stu-id="2d1e6-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2d1e6-109">CN</span><span class="sxs-lookup"><span data-stu-id="2d1e6-109">CN</span></span>                | <span data-ttu-id="2d1e6-110">MS-DS-Манажедпассворд</span><span class="sxs-lookup"><span data-stu-id="2d1e6-110">ms-DS-ManagedPassword</span></span>                                 |
| <span data-ttu-id="2d1e6-111">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="2d1e6-111">Ldap-Display-Name</span></span> | <span data-ttu-id="2d1e6-112">msDS-Манажедпассворд</span><span class="sxs-lookup"><span data-stu-id="2d1e6-112">msDS-ManagedPassword</span></span>                                  |
| <span data-ttu-id="2d1e6-113">Размер</span><span class="sxs-lookup"><span data-stu-id="2d1e6-113">Size</span></span>              | \-                                                    |
| <span data-ttu-id="2d1e6-114">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="2d1e6-114">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="2d1e6-115">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="2d1e6-115">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="2d1e6-116">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="2d1e6-116">Attribute-Id</span></span>      | <span data-ttu-id="2d1e6-117">1.2.840.113556.1.4.2196</span><span class="sxs-lookup"><span data-stu-id="2d1e6-117">1.2.840.113556.1.4.2196</span></span>                               |
| <span data-ttu-id="2d1e6-118">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="2d1e6-118">System-Id-Guid</span></span>    | <span data-ttu-id="2d1e6-119">e362ed86-b728-0842-b27d-2dea7a9df218</span><span class="sxs-lookup"><span data-stu-id="2d1e6-119">e362ed86-b728-0842-b27d-2dea7a9df218</span></span>                  |
| <span data-ttu-id="2d1e6-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d1e6-120">Syntax</span></span>            | [<span data-ttu-id="2d1e6-121">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="2d1e6-121">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="2d1e6-122">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="2d1e6-122">Implementations</span></span>

-   [<span data-ttu-id="2d1e6-123">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="2d1e6-123">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="2d1e6-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d1e6-124">Windows Server 2012</span></span>



| <span data-ttu-id="2d1e6-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="2d1e6-125">Entry</span></span> | <span data-ttu-id="2d1e6-126">Значение</span><span class="sxs-lookup"><span data-stu-id="2d1e6-126">Value</span></span> |
|------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d1e6-127">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="2d1e6-127">Link-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="2d1e6-128">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="2d1e6-128">MAPI-Id</span></span>                | \-                                                                                          |
| <span data-ttu-id="2d1e6-129">System-Only</span><span class="sxs-lookup"><span data-stu-id="2d1e6-129">System-Only</span></span>            | <span data-ttu-id="2d1e6-130">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d1e6-130">False</span></span>                                                                                       |
| <span data-ttu-id="2d1e6-131">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="2d1e6-131">Is-Single-Valued</span></span>       | <span data-ttu-id="2d1e6-132">True</span><span class="sxs-lookup"><span data-stu-id="2d1e6-132">True</span></span>                                                                                        |
| <span data-ttu-id="2d1e6-133">Индексируется</span><span class="sxs-lookup"><span data-stu-id="2d1e6-133">Is Indexed</span></span>             | <span data-ttu-id="2d1e6-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d1e6-134">False</span></span>                                                                                       |
| <span data-ttu-id="2d1e6-135">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="2d1e6-135">In Global Catalog</span></span>      | <span data-ttu-id="2d1e6-136">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d1e6-136">False</span></span>                                                                                       |
| <span data-ttu-id="2d1e6-137">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="2d1e6-137">NT-Security-Descriptor</span></span> | <span data-ttu-id="2d1e6-138">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="2d1e6-138">O:BAG:BAD:S:</span></span>                                                                                |
| <span data-ttu-id="2d1e6-139">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="2d1e6-139">Range-Lower</span></span>            | \-                                                                                          |
| <span data-ttu-id="2d1e6-140">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="2d1e6-140">Range-Upper</span></span>            | \-                                                                                          |
| <span data-ttu-id="2d1e6-141">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="2d1e6-141">Search-Flags</span></span>           | <span data-ttu-id="2d1e6-142">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2d1e6-142">0x00000000</span></span>                                                                                  |
| <span data-ttu-id="2d1e6-143">System-Flags</span><span class="sxs-lookup"><span data-stu-id="2d1e6-143">System-Flags</span></span>           | <span data-ttu-id="2d1e6-144">0x00000014</span><span class="sxs-lookup"><span data-stu-id="2d1e6-144">0x00000014</span></span>                                                                                  |
| <span data-ttu-id="2d1e6-145">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="2d1e6-145">Classes used in</span></span>        | [<span data-ttu-id="2d1e6-146">**MS-DS-Group-Managed-Service-учетная запись**</span><span class="sxs-lookup"><span data-stu-id="2d1e6-146">**ms-DS-Group-Managed-Service-Account**</span></span>](c-msds-groupmanagedserviceaccount.md)<br/> |



 

 





