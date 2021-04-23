---
title: атрибут MS-TPM-SRK-Pub-Thumbprint
description: Этот атрибут содержит отпечаток Сркпуб, соответствующий определенному доверенному платформенному модулю. Это помогает индексировать устройства доверенного платформенного модуля в каталоге.
ms.assetid: 64cb0341-ae49-4992-87d7-6863719fa13f
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-TPM-SRK-Pub-Thumbprint
- Схема AD атрибута Мстпм-Сркпубсумбпринт
topic_type:
- apiref
api_name:
- ms-TPM-Srk-Pub-Thumbprint
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2ab2daec38d509e670771eef61824278bee4c4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536209"
---
# <a name="ms-tpm-srk-pub-thumbprint-attribute"></a><span data-ttu-id="609f6-106">атрибут MS-TPM-SRK-Pub-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="609f6-106">ms-TPM-Srk-Pub-Thumbprint attribute</span></span>

<span data-ttu-id="609f6-107">Этот атрибут содержит отпечаток Сркпуб, соответствующий определенному доверенному платформенному модулю.</span><span class="sxs-lookup"><span data-stu-id="609f6-107">This attribute contains the thumbprint of the SrkPub corresponding to a particular TPM.</span></span> <span data-ttu-id="609f6-108">Это помогает индексировать устройства доверенного платформенного модуля в каталоге.</span><span class="sxs-lookup"><span data-stu-id="609f6-108">This helps to index the TPM devices in the directory.</span></span>



| <span data-ttu-id="609f6-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="609f6-109">Entry</span></span> | <span data-ttu-id="609f6-110">Значение</span><span class="sxs-lookup"><span data-stu-id="609f6-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="609f6-111">CN</span><span class="sxs-lookup"><span data-stu-id="609f6-111">CN</span></span>                | <span data-ttu-id="609f6-112">MS-TPM-SRK-Pub-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="609f6-112">ms-TPM-Srk-Pub-Thumbprint</span></span>                             |
| <span data-ttu-id="609f6-113">LDAP-отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="609f6-113">Ldap-Display-Name</span></span> | <span data-ttu-id="609f6-114">Мстпм — Сркпубсумбпринт</span><span class="sxs-lookup"><span data-stu-id="609f6-114">msTPM-SrkPubThumbprint</span></span>                                |
| <span data-ttu-id="609f6-115">Размер</span><span class="sxs-lookup"><span data-stu-id="609f6-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="609f6-116">Привилегия обновления</span><span class="sxs-lookup"><span data-stu-id="609f6-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="609f6-117">Частота обновления</span><span class="sxs-lookup"><span data-stu-id="609f6-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="609f6-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="609f6-118">Attribute-Id</span></span>      | <span data-ttu-id="609f6-119">1.2.840.113556.1.4.2107</span><span class="sxs-lookup"><span data-stu-id="609f6-119">1.2.840.113556.1.4.2107</span></span>                               |
| <span data-ttu-id="609f6-120">System-ID — GUID</span><span class="sxs-lookup"><span data-stu-id="609f6-120">System-Id-Guid</span></span>    | <span data-ttu-id="609f6-121">19d706eb-4d76-44a2-85d6-1c342be3be37</span><span class="sxs-lookup"><span data-stu-id="609f6-121">19d706eb-4d76-44a2-85d6-1c342be3be37</span></span>                  |
| <span data-ttu-id="609f6-122">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="609f6-122">Syntax</span></span>            | [<span data-ttu-id="609f6-123">**Object(ссылка_на_реплику)**</span><span class="sxs-lookup"><span data-stu-id="609f6-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="609f6-124">Варианты реализации решения</span><span class="sxs-lookup"><span data-stu-id="609f6-124">Implementations</span></span>

-   [<span data-ttu-id="609f6-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="609f6-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="609f6-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="609f6-126">Windows Server 2012</span></span>



| <span data-ttu-id="609f6-127">Ввод</span><span class="sxs-lookup"><span data-stu-id="609f6-127">Entry</span></span> | <span data-ttu-id="609f6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="609f6-128">Value</span></span> |
|------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="609f6-129">Идентификатор ссылки</span><span class="sxs-lookup"><span data-stu-id="609f6-129">Link-Id</span></span>                | \-                                                                        |
| <span data-ttu-id="609f6-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="609f6-130">MAPI-Id</span></span>                | \-                                                                        |
| <span data-ttu-id="609f6-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="609f6-131">System-Only</span></span>            | <span data-ttu-id="609f6-132">Неверно</span><span class="sxs-lookup"><span data-stu-id="609f6-132">False</span></span>                                                                     |
| <span data-ttu-id="609f6-133">Является однозначным</span><span class="sxs-lookup"><span data-stu-id="609f6-133">Is-Single-Valued</span></span>       | <span data-ttu-id="609f6-134">True</span><span class="sxs-lookup"><span data-stu-id="609f6-134">True</span></span>                                                                      |
| <span data-ttu-id="609f6-135">Индексируется</span><span class="sxs-lookup"><span data-stu-id="609f6-135">Is Indexed</span></span>             | <span data-ttu-id="609f6-136">True</span><span class="sxs-lookup"><span data-stu-id="609f6-136">True</span></span>                                                                      |
| <span data-ttu-id="609f6-137">В глобальном каталоге</span><span class="sxs-lookup"><span data-stu-id="609f6-137">In Global Catalog</span></span>      | <span data-ttu-id="609f6-138">Неверно</span><span class="sxs-lookup"><span data-stu-id="609f6-138">False</span></span>                                                                     |
| <span data-ttu-id="609f6-139">NT-Security-дескриптор</span><span class="sxs-lookup"><span data-stu-id="609f6-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="609f6-140">О:БАГ: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="609f6-140">O:BAG:BAD:S:</span></span>                                                              |
| <span data-ttu-id="609f6-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="609f6-141">Range-Lower</span></span>            | \-                                                                        |
| <span data-ttu-id="609f6-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="609f6-142">Range-Upper</span></span>            | \-                                                                        |
| <span data-ttu-id="609f6-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="609f6-143">Search-Flags</span></span>           | <span data-ttu-id="609f6-144">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="609f6-144">0x0000000B</span></span>                                                                |
| <span data-ttu-id="609f6-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="609f6-145">System-Flags</span></span>           | <span data-ttu-id="609f6-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="609f6-146">0x00000010</span></span>                                                                |
| <span data-ttu-id="609f6-147">Классы, используемые в</span><span class="sxs-lookup"><span data-stu-id="609f6-147">Classes used in</span></span>        | [<span data-ttu-id="609f6-148">**MS-TPM-Information — объект**</span><span class="sxs-lookup"><span data-stu-id="609f6-148">**ms-TPM-Information-Object**</span></span>](c-mstpm-informationobject.md)<br/> |



 

 





