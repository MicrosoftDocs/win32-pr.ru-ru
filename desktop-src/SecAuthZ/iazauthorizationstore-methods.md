---
description: Интерфейс Иазаусоризатионсторе предоставляет следующие методы.
ms.assetid: ECBCD34B-4AF0-4FED-8E1D-BFD544390804
title: Методы Иазаусоризатионсторе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c8d71185e9e52d46d1a51e2f2966334a72ad0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664145"
---
# <a name="iazauthorizationstore-methods"></a><span data-ttu-id="efa0d-103">Методы Иазаусоризатионсторе</span><span class="sxs-lookup"><span data-stu-id="efa0d-103">IAzAuthorizationStore Methods</span></span>

<span data-ttu-id="efa0d-104">Интерфейс [**иазаусоризатионсторе**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="efa0d-104">The [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="efa0d-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="efa0d-105">In this section</span></span>

-   [<span data-ttu-id="efa0d-106">**Метод Аддделегатедполициусер**</span><span class="sxs-lookup"><span data-stu-id="efa0d-106">**AddDelegatedPolicyUser Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyuser)
-   [<span data-ttu-id="efa0d-107">**Метод Аддделегатедполициусернаме**</span><span class="sxs-lookup"><span data-stu-id="efa0d-107">**AddDelegatedPolicyUserName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-adddelegatedpolicyusername)
-   [<span data-ttu-id="efa0d-108">**Метод Аддполициадминистратор**</span><span class="sxs-lookup"><span data-stu-id="efa0d-108">**AddPolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyadministrator)
-   [<span data-ttu-id="efa0d-109">**Метод Аддполициадминистраторнаме**</span><span class="sxs-lookup"><span data-stu-id="efa0d-109">**AddPolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyadministratorname)
-   [<span data-ttu-id="efa0d-110">**Метод Аддполициреадер**</span><span class="sxs-lookup"><span data-stu-id="efa0d-110">**AddPolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyreader)
-   [<span data-ttu-id="efa0d-111">**Метод Аддполициреадернаме**</span><span class="sxs-lookup"><span data-stu-id="efa0d-111">**AddPolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpolicyreadername)
-   [<span data-ttu-id="efa0d-112">**Метод Аддпропертитем**</span><span class="sxs-lookup"><span data-stu-id="efa0d-112">**AddPropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-addpropertyitem)
-   [<span data-ttu-id="efa0d-113">**Метод Клосеаппликатион**</span><span class="sxs-lookup"><span data-stu-id="efa0d-113">**CloseApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-closeapplication)
-   [<span data-ttu-id="efa0d-114">**Метод CreateApplication**</span><span class="sxs-lookup"><span data-stu-id="efa0d-114">**CreateApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-createapplication)
-   [<span data-ttu-id="efa0d-115">**Метод Креатеаппликатионграуп**</span><span class="sxs-lookup"><span data-stu-id="efa0d-115">**CreateApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-createapplicationgroup)
-   [<span data-ttu-id="efa0d-116">**Метод Delete**</span><span class="sxs-lookup"><span data-stu-id="efa0d-116">**Delete Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-delete)
-   [<span data-ttu-id="efa0d-117">**Метод DeleteApplication**</span><span class="sxs-lookup"><span data-stu-id="efa0d-117">**DeleteApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deleteapplication)
-   [<span data-ttu-id="efa0d-118">**Метод Делетеаппликатионграуп**</span><span class="sxs-lookup"><span data-stu-id="efa0d-118">**DeleteApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deleteapplicationgroup)
-   [<span data-ttu-id="efa0d-119">**Метод Делетеделегатедполициусер**</span><span class="sxs-lookup"><span data-stu-id="efa0d-119">**DeleteDelegatedPolicyUser Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletedelegatedpolicyuser)
-   [<span data-ttu-id="efa0d-120">**Метод Делетеделегатедполициусернаме**</span><span class="sxs-lookup"><span data-stu-id="efa0d-120">**DeleteDelegatedPolicyUserName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletedelegatedpolicyusername)
-   [<span data-ttu-id="efa0d-121">**Метод Делетеполициадминистратор**</span><span class="sxs-lookup"><span data-stu-id="efa0d-121">**DeletePolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyadministrator)
-   [<span data-ttu-id="efa0d-122">**Метод Делетеполициадминистраторнаме**</span><span class="sxs-lookup"><span data-stu-id="efa0d-122">**DeletePolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyadministratorname)
-   [<span data-ttu-id="efa0d-123">**Метод Делетеполициреадер**</span><span class="sxs-lookup"><span data-stu-id="efa0d-123">**DeletePolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyreader)
-   [<span data-ttu-id="efa0d-124">**Метод Делетеполициреадернаме**</span><span class="sxs-lookup"><span data-stu-id="efa0d-124">**DeletePolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepolicyreadername)
-   [<span data-ttu-id="efa0d-125">**Метод Делетепропертитем**</span><span class="sxs-lookup"><span data-stu-id="efa0d-125">**DeletePropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-deletepropertyitem)
-   [<span data-ttu-id="efa0d-126">**Метод Property**</span><span class="sxs-lookup"><span data-stu-id="efa0d-126">**GetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-getproperty)
-   [<span data-ttu-id="efa0d-127">**Метод Initialize**</span><span class="sxs-lookup"><span data-stu-id="efa0d-127">**Initialize Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-initialize)
-   [<span data-ttu-id="efa0d-128">**Метод Опенаппликатион**</span><span class="sxs-lookup"><span data-stu-id="efa0d-128">**OpenApplication Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-openapplication)
-   [<span data-ttu-id="efa0d-129">**Метод Опенаппликатионграуп**</span><span class="sxs-lookup"><span data-stu-id="efa0d-129">**OpenApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-openapplicationgroup)
-   [<span data-ttu-id="efa0d-130">**Метод SetProperty**</span><span class="sxs-lookup"><span data-stu-id="efa0d-130">**SetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-setproperty)
-   [<span data-ttu-id="efa0d-131">**Метод Submit**</span><span class="sxs-lookup"><span data-stu-id="efa0d-131">**Submit Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-submit)
-   [<span data-ttu-id="efa0d-132">**Метод Упдатекаче**</span><span class="sxs-lookup"><span data-stu-id="efa0d-132">**UpdateCache Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-updatecache)

 

 



