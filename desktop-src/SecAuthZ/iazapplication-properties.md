---
description: Интерфейс Иазаппликатион предоставляет следующие свойства.
ms.assetid: 36282F91-6C14-4943-967B-046DD0FD94DC
title: Свойства Иазаппликатион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4086acb6e6ceba0821af7cc117d8598bee731d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664150"
---
# <a name="iazapplication-properties"></a><span data-ttu-id="606b1-103">Свойства Иазаппликатион</span><span class="sxs-lookup"><span data-stu-id="606b1-103">IAzApplication Properties</span></span>

<span data-ttu-id="606b1-104">Интерфейс [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="606b1-104">The [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="606b1-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="606b1-105">In this section</span></span>

-   [<span data-ttu-id="606b1-106">**ApplicationData, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-106">**ApplicationData Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_applicationdata)
-   [<span data-ttu-id="606b1-107">**Аппликатионграупс, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-107">**ApplicationGroups Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_applicationgroups)
-   [<span data-ttu-id="606b1-108">**Апплисторесакл, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-108">**ApplyStoreSacl Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_applystoresacl)
-   [<span data-ttu-id="606b1-109">**Аусзинтерфацеклсид, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-109">**AuthzInterfaceClsid Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_authzinterfaceclsid)
-   [<span data-ttu-id="606b1-110">**Делегатедполициусерс, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-110">**DelegatedPolicyUsers Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_delegatedpolicyusers)
-   [<span data-ttu-id="606b1-111">**Делегатедполициусерснаме, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-111">**DelegatedPolicyUsersName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_delegatedpolicyusersname)
-   [<span data-ttu-id="606b1-112">**Свойство Description**</span><span class="sxs-lookup"><span data-stu-id="606b1-112">**Description Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_description)
-   [<span data-ttu-id="606b1-113">**Женератеаудитс, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-113">**GenerateAudits Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_generateaudits)
-   [<span data-ttu-id="606b1-114">**Свойство Name**</span><span class="sxs-lookup"><span data-stu-id="606b1-114">**Name Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_name)
-   [<span data-ttu-id="606b1-115">**Свойство Operations**</span><span class="sxs-lookup"><span data-stu-id="606b1-115">**Operations Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_operations)
-   [<span data-ttu-id="606b1-116">**Полициадминистраторс, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-116">**PolicyAdministrators Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_policyadministrators)
-   [<span data-ttu-id="606b1-117">**Полициадминистраторснаме, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-117">**PolicyAdministratorsName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_policyadministratorsname)
-   [<span data-ttu-id="606b1-118">**Полициреадерс, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-118">**PolicyReaders Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_policyreaders)
-   [<span data-ttu-id="606b1-119">**Полициреадерснаме, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-119">**PolicyReadersName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_policyreadersname)
-   [<span data-ttu-id="606b1-120">**Roles, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-120">**Roles Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_roles)
-   [<span data-ttu-id="606b1-121">**Свойство областей**</span><span class="sxs-lookup"><span data-stu-id="606b1-121">**Scopes Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_scopes)
-   [<span data-ttu-id="606b1-122">**Tasks, свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-122">**Tasks Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_tasks)
-   [<span data-ttu-id="606b1-123">**Свойство Version**</span><span class="sxs-lookup"><span data-stu-id="606b1-123">**Version Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_version)
-   [<span data-ttu-id="606b1-124">**Доступное для записи свойство**</span><span class="sxs-lookup"><span data-stu-id="606b1-124">**Writable Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-get_writable)

 

 



