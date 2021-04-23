---
description: Интерфейс Иазаппликатион предоставляет следующие методы.
ms.assetid: C969D653-9FEE-45B6-8DB1-4D778C836E9D
title: Методы Иазаппликатион
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fc8ffd17addcd2b8da01b4999a7c88f78dab8b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265926"
---
# <a name="iazapplication-methods"></a><span data-ttu-id="34d25-103">Методы Иазаппликатион</span><span class="sxs-lookup"><span data-stu-id="34d25-103">IAzApplication Methods</span></span>

<span data-ttu-id="34d25-104">Интерфейс [**иазаппликатион**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="34d25-104">The [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34d25-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="34d25-105">In this section</span></span>

-   [<span data-ttu-id="34d25-106">**Метод Аддделегатедполициусер**</span><span class="sxs-lookup"><span data-stu-id="34d25-106">**AddDelegatedPolicyUser Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyuser)
-   [<span data-ttu-id="34d25-107">**Метод Аддделегатедполициусернаме**</span><span class="sxs-lookup"><span data-stu-id="34d25-107">**AddDelegatedPolicyUserName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-adddelegatedpolicyusername)
-   [<span data-ttu-id="34d25-108">**Метод Аддполициадминистратор**</span><span class="sxs-lookup"><span data-stu-id="34d25-108">**AddPolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-addpolicyadministrator)
-   [<span data-ttu-id="34d25-109">**Метод Аддполициадминистраторнаме**</span><span class="sxs-lookup"><span data-stu-id="34d25-109">**AddPolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-addpolicyadministratorname)
-   [<span data-ttu-id="34d25-110">**Метод Аддполициреадер**</span><span class="sxs-lookup"><span data-stu-id="34d25-110">**AddPolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-addpolicyreader)
-   [<span data-ttu-id="34d25-111">**Метод Аддполициреадернаме**</span><span class="sxs-lookup"><span data-stu-id="34d25-111">**AddPolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-addpolicyreadername)
-   [<span data-ttu-id="34d25-112">**Метод Аддпропертитем**</span><span class="sxs-lookup"><span data-stu-id="34d25-112">**AddPropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-addpropertyitem)
-   [<span data-ttu-id="34d25-113">**Метод Креатеаппликатионграуп**</span><span class="sxs-lookup"><span data-stu-id="34d25-113">**CreateApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-createapplicationgroup)
-   [<span data-ttu-id="34d25-114">**Метод CreateOperation**</span><span class="sxs-lookup"><span data-stu-id="34d25-114">**CreateOperation Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-createoperation)
-   [<span data-ttu-id="34d25-115">**Метод CreateRole**</span><span class="sxs-lookup"><span data-stu-id="34d25-115">**CreateRole Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-createrole)
-   [<span data-ttu-id="34d25-116">**Метод Креатескопе**</span><span class="sxs-lookup"><span data-stu-id="34d25-116">**CreateScope Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-createscope)
-   [<span data-ttu-id="34d25-117">**Метод CreateTask**</span><span class="sxs-lookup"><span data-stu-id="34d25-117">**CreateTask Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-createtask)
-   [<span data-ttu-id="34d25-118">**Метод Делетеаппликатионграуп**</span><span class="sxs-lookup"><span data-stu-id="34d25-118">**DeleteApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deleteapplicationgroup)
-   [<span data-ttu-id="34d25-119">**Метод Делетеделегатедполициусер**</span><span class="sxs-lookup"><span data-stu-id="34d25-119">**DeleteDelegatedPolicyUser Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletedelegatedpolicyuser)
-   [<span data-ttu-id="34d25-120">**Метод Делетеделегатедполициусернаме**</span><span class="sxs-lookup"><span data-stu-id="34d25-120">**DeleteDelegatedPolicyUserName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletedelegatedpolicyusername)
-   [<span data-ttu-id="34d25-121">**Метод Делетеоператион**</span><span class="sxs-lookup"><span data-stu-id="34d25-121">**DeleteOperation Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deleteoperation)
-   [<span data-ttu-id="34d25-122">**Метод Делетеполициадминистратор**</span><span class="sxs-lookup"><span data-stu-id="34d25-122">**DeletePolicyAdministrator Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletepolicyadministrator)
-   [<span data-ttu-id="34d25-123">**Метод Делетеполициадминистраторнаме**</span><span class="sxs-lookup"><span data-stu-id="34d25-123">**DeletePolicyAdministratorName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletepolicyadministratorname)
-   [<span data-ttu-id="34d25-124">**Метод Делетеполициреадер**</span><span class="sxs-lookup"><span data-stu-id="34d25-124">**DeletePolicyReader Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletepolicyreader)
-   [<span data-ttu-id="34d25-125">**Метод Делетеполициреадернаме**</span><span class="sxs-lookup"><span data-stu-id="34d25-125">**DeletePolicyReaderName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletepolicyreadername)
-   [<span data-ttu-id="34d25-126">**Метод Делетепропертитем**</span><span class="sxs-lookup"><span data-stu-id="34d25-126">**DeletePropertyItem Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletepropertyitem)
-   [<span data-ttu-id="34d25-127">**Метод Делетероле**</span><span class="sxs-lookup"><span data-stu-id="34d25-127">**DeleteRole Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deleterole)
-   [<span data-ttu-id="34d25-128">**Метод Делетескопе**</span><span class="sxs-lookup"><span data-stu-id="34d25-128">**DeleteScope Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletescope)
-   [<span data-ttu-id="34d25-129">**Метод Делететаск**</span><span class="sxs-lookup"><span data-stu-id="34d25-129">**DeleteTask Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-deletetask)
-   [<span data-ttu-id="34d25-130">**Метод Property**</span><span class="sxs-lookup"><span data-stu-id="34d25-130">**GetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-getproperty)
-   [<span data-ttu-id="34d25-131">**Метод Инитиализеклиентконтекстфромнаме**</span><span class="sxs-lookup"><span data-stu-id="34d25-131">**InitializeClientContextFromName Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromname)
-   [<span data-ttu-id="34d25-132">**Метод Инитиализеклиентконтекстфромстрингсид**</span><span class="sxs-lookup"><span data-stu-id="34d25-132">**InitializeClientContextFromStringSid Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromstringsid)
-   [<span data-ttu-id="34d25-133">**Метод Инитиализеклиентконтекстфромтокен**</span><span class="sxs-lookup"><span data-stu-id="34d25-133">**InitializeClientContextFromToken Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-initializeclientcontextfromtoken)
-   [<span data-ttu-id="34d25-134">**Метод Опенаппликатионграуп**</span><span class="sxs-lookup"><span data-stu-id="34d25-134">**OpenApplicationGroup Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-openapplicationgroup)
-   [<span data-ttu-id="34d25-135">**Метод Опеноператион**</span><span class="sxs-lookup"><span data-stu-id="34d25-135">**OpenOperation Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-openoperation)
-   [<span data-ttu-id="34d25-136">**Метод Опенроле**</span><span class="sxs-lookup"><span data-stu-id="34d25-136">**OpenRole Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-openrole)
-   [<span data-ttu-id="34d25-137">**Метод OpenScope**</span><span class="sxs-lookup"><span data-stu-id="34d25-137">**OpenScope Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-openscope)
-   [<span data-ttu-id="34d25-138">**Метод Опентаск**</span><span class="sxs-lookup"><span data-stu-id="34d25-138">**OpenTask Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-opentask)
-   [<span data-ttu-id="34d25-139">**Метод SetProperty**</span><span class="sxs-lookup"><span data-stu-id="34d25-139">**SetProperty Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-setproperty)
-   [<span data-ttu-id="34d25-140">**Метод Submit**</span><span class="sxs-lookup"><span data-stu-id="34d25-140">**Submit Method**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazapplication-submit)

 

 



