---
title: Сопоставление пользовательского интерфейса объекта "компьютер"
description: В следующих таблицах перечислены элементы страниц свойств объекта «компьютер» в оснастке «Active Directory пользователи и компьютеры».
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789612"
---
# <a name="computer-object-user-interface-mapping"></a><span data-ttu-id="277b9-103">Сопоставление пользовательского интерфейса объекта "компьютер"</span><span class="sxs-lookup"><span data-stu-id="277b9-103">Computer Object User Interface Mapping</span></span>

<span data-ttu-id="277b9-104">В следующих таблицах перечислены элементы страниц свойств объекта «компьютер» в оснастке «Active Directory пользователи и компьютеры».</span><span class="sxs-lookup"><span data-stu-id="277b9-104">The following tables list elements of the Computer object property sheets in the Active Directory Users and Computers snap-in.</span></span>

## <a name="general-property-sheet"></a><span data-ttu-id="277b9-105">Страница свойств "Общие"</span><span class="sxs-lookup"><span data-stu-id="277b9-105">General Property Sheet</span></span>

<span data-ttu-id="277b9-106">В следующей таблице перечислены метки пользовательского интерфейса на странице свойств **Общие** .</span><span class="sxs-lookup"><span data-stu-id="277b9-106">The following table lists the UI labels of the **General** property sheet.</span></span>



| <span data-ttu-id="277b9-107">Метка пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="277b9-107">UI label</span></span>                         | <span data-ttu-id="277b9-108">Атрибут домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="277b9-108">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="277b9-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="277b9-109">Comments</span></span>                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="277b9-110">Имя компьютера (пред-Windows 2000)</span><span class="sxs-lookup"><span data-stu-id="277b9-110">Computer Name (pre-Windows 2000)</span></span> | <span data-ttu-id="277b9-111">sAMAccountName</span><span class="sxs-lookup"><span data-stu-id="277b9-111">sAMAccountName</span></span>                             |                                                  |
| <span data-ttu-id="277b9-112">DNS-имя</span><span class="sxs-lookup"><span data-stu-id="277b9-112">DNS Name</span></span>                         | <span data-ttu-id="277b9-113">dNSHostName</span><span class="sxs-lookup"><span data-stu-id="277b9-113">dNSHostName</span></span>                                |                                                  |
| <span data-ttu-id="277b9-114">Роль</span><span class="sxs-lookup"><span data-stu-id="277b9-114">Role</span></span>                             | <span data-ttu-id="277b9-115">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="277b9-115">userAccountControl</span></span>                         | <span data-ttu-id="277b9-116">Переключает бит битовой маски userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="277b9-116">Toggles a bit in the userAccountControl bitmask.</span></span> |
| <span data-ttu-id="277b9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="277b9-117">Description</span></span>                      | <span data-ttu-id="277b9-118">description</span><span class="sxs-lookup"><span data-stu-id="277b9-118">description</span></span>                                |                                                  |
| <span data-ttu-id="277b9-119">Доверять компьютеру делегирование</span><span class="sxs-lookup"><span data-stu-id="277b9-119">Trust Computer for delegation</span></span>    | <span data-ttu-id="277b9-120">userAccountControl</span><span class="sxs-lookup"><span data-stu-id="277b9-120">userAccountControl</span></span>                         | <span data-ttu-id="277b9-121">Переключает бит битовой маски userAccountControl.</span><span class="sxs-lookup"><span data-stu-id="277b9-121">Toggles a bit in the userAccountControl bitmask.</span></span> |



 

## <a name="location-property-sheet"></a><span data-ttu-id="277b9-122">Страница свойств "расположение"</span><span class="sxs-lookup"><span data-stu-id="277b9-122">Location Property Sheet</span></span>

<span data-ttu-id="277b9-123">В следующей таблице перечислены метки пользовательского интерфейса на странице свойств **Расположение** .</span><span class="sxs-lookup"><span data-stu-id="277b9-123">The following table lists the UI labels of the **Location** property sheet.</span></span>



| <span data-ttu-id="277b9-124">Метка пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="277b9-124">UI label</span></span> | <span data-ttu-id="277b9-125">Атрибут домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="277b9-125">Active Directory Domain Services attribute</span></span> |
|----------|--------------------------------------------|
| <span data-ttu-id="277b9-126">Расположение</span><span class="sxs-lookup"><span data-stu-id="277b9-126">Location</span></span> | <span data-ttu-id="277b9-127">location</span><span class="sxs-lookup"><span data-stu-id="277b9-127">location</span></span>                                   |



 

## <a name="member-of-property-sheet"></a><span data-ttu-id="277b9-128">Элемент вкладки свойств</span><span class="sxs-lookup"><span data-stu-id="277b9-128">Member Of Property Sheet</span></span>

<span data-ttu-id="277b9-129">В следующей таблице перечислены метки пользовательского интерфейса для **элемента** страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="277b9-129">The following table lists the UI labels of the **Member Of** property sheet.</span></span>



| <span data-ttu-id="277b9-130">Метка пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="277b9-130">UI label</span></span>          | <span data-ttu-id="277b9-131">Атрибут домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="277b9-131">Active Directory Domain Services attribute</span></span> | <span data-ttu-id="277b9-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="277b9-132">Comments</span></span>                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="277b9-133">Член групп</span><span class="sxs-lookup"><span data-stu-id="277b9-133">Member of</span></span>         | <span data-ttu-id="277b9-134">memberOf</span><span class="sxs-lookup"><span data-stu-id="277b9-134">memberOf</span></span>                                   | <span data-ttu-id="277b9-135">Включает все группы в списке пользовательского интерфейса, кроме первичной группы, представленной в AD с помощью атрибута [**примариграупид**](/windows/desktop/ADSchema/a-primarygroupid) .</span><span class="sxs-lookup"><span data-stu-id="277b9-135">Includes all of the groups in the UI list, except the primary group, which is represented in the AD through the [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) attribute.</span></span> |
| <span data-ttu-id="277b9-136">Задать основную группу</span><span class="sxs-lookup"><span data-stu-id="277b9-136">Set Primary Group</span></span> | <span data-ttu-id="277b9-137">примариграупид</span><span class="sxs-lookup"><span data-stu-id="277b9-137">primaryGroupID</span></span>                             | <span data-ttu-id="277b9-138">LDAP: связан с [**примариграуптокен**](/windows/desktop/ADSchema/a-primarygrouptoken) из основной группы.</span><span class="sxs-lookup"><span data-stu-id="277b9-138">LDAP: Tied to [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) of the primary group.</span></span>                                                                                  |



 

## <a name="operating-system-property-sheet"></a><span data-ttu-id="277b9-139">Страница свойств операционной системы</span><span class="sxs-lookup"><span data-stu-id="277b9-139">Operating System Property Sheet</span></span>

<span data-ttu-id="277b9-140">В следующей таблице перечислены метки пользовательского интерфейса на странице свойств **операционной системы** .</span><span class="sxs-lookup"><span data-stu-id="277b9-140">The following table lists the UI labels of the **Operating System** property sheet.</span></span>



| <span data-ttu-id="277b9-141">Метка пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="277b9-141">UI label</span></span>     | <span data-ttu-id="277b9-142">Атрибут домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="277b9-142">Active Directory Domain Services attribute</span></span> |
|--------------|--------------------------------------------|
| <span data-ttu-id="277b9-143">Имя</span><span class="sxs-lookup"><span data-stu-id="277b9-143">Name</span></span>         | <span data-ttu-id="277b9-144">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="277b9-144">operatingSystem</span></span>                            |
| <span data-ttu-id="277b9-145">Версия</span><span class="sxs-lookup"><span data-stu-id="277b9-145">Version</span></span>      | <span data-ttu-id="277b9-146">operatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="277b9-146">operatingSystemVersion</span></span>                     |
| <span data-ttu-id="277b9-147">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="277b9-147">Service Pack</span></span> | <span data-ttu-id="277b9-148">оператингсистемсервицепакк</span><span class="sxs-lookup"><span data-stu-id="277b9-148">operatingSystemServicePack</span></span>                 |



 

 

 