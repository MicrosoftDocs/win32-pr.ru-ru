---
description: Класс provider предоставляет следующие методы.
ms.assetid: AD0BCAC7-6B5C-4BAF-9641-37D315D3E7B1
ms.tgt_platform: multiple
title: Методы поставщика
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb4d8f5d012b5209519670562a7f735a34e6f84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703188"
---
# <a name="provider-methods"></a><span data-ttu-id="ebffc-103">Методы поставщика</span><span class="sxs-lookup"><span data-stu-id="ebffc-103">Provider Methods</span></span>

<span data-ttu-id="ebffc-104">\[Класс [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="ebffc-104">\[The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="ebffc-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="ebffc-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="ebffc-106">Класс [**provider**](/windows/desktop/api/Provider/nl-provider-provider) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ebffc-106">The [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ebffc-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="ebffc-107">In this section</span></span>

-   [<span data-ttu-id="ebffc-108">**Метод Commit**</span><span class="sxs-lookup"><span data-stu-id="ebffc-108">**Commit method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-commit)
-   [<span data-ttu-id="ebffc-109">**Метод Креатеневинстанце**</span><span class="sxs-lookup"><span data-stu-id="ebffc-109">**CreateNewInstance method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-createnewinstance)
-   <span data-ttu-id="ebffc-110">[**Метод DeleteInstance**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="ebffc-110">[**DeleteInstance method**](/windows/desktop/api/Provider/nf-provider-provider-deleteinstance(parsedobjectpath_long_methodcontext))</span></span>
-   [<span data-ttu-id="ebffc-111">**Метод Енумератеинстанцес**</span><span class="sxs-lookup"><span data-stu-id="ebffc-111">**EnumerateInstances method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-enumerateinstances)
-   <span data-ttu-id="ebffc-112">[**Метод ExecMethod**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="ebffc-112">[**ExecMethod method**](/windows/desktop/api/Provider/nf-provider-provider-execmethod(parsedobjectpath_bstr_long_cinstance_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="ebffc-113">**Метод ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="ebffc-113">**ExecQuery method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-execquery)
-   [<span data-ttu-id="ebffc-114">**Метод Flush**</span><span class="sxs-lookup"><span data-stu-id="ebffc-114">**Flush method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-flush)
-   [<span data-ttu-id="ebffc-115">**Метод Жетлокалкомпутернаме**</span><span class="sxs-lookup"><span data-stu-id="ebffc-115">**GetLocalComputerName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalcomputername)
-   [<span data-ttu-id="ebffc-116">**Метод Жетлокалинстанцепас**</span><span class="sxs-lookup"><span data-stu-id="ebffc-116">**GetLocalInstancePath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getlocalinstancepath)
-   [<span data-ttu-id="ebffc-117">**Метод. Namespace**</span><span class="sxs-lookup"><span data-stu-id="ebffc-117">**GetNamespace method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getnamespace)
-   <span data-ttu-id="ebffc-118">[**Метод GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span><span class="sxs-lookup"><span data-stu-id="ebffc-118">[**GetObject method**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_))</span></span>
-   [<span data-ttu-id="ebffc-119">**Метод Жетпровидернаме**</span><span class="sxs-lookup"><span data-stu-id="ebffc-119">**GetProviderName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-getprovidername)
-   [<span data-ttu-id="ebffc-120">**Метод Макелокалпас**</span><span class="sxs-lookup"><span data-stu-id="ebffc-120">**MakeLocalPath method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-makelocalpath)
-   [<span data-ttu-id="ebffc-121">**Метод поставщика**</span><span class="sxs-lookup"><span data-stu-id="ebffc-121">**Provider method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-provider)
-   <span data-ttu-id="ebffc-122">[**Метод PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span><span class="sxs-lookup"><span data-stu-id="ebffc-122">[**PutInstance method**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long))</span></span>
-   [<span data-ttu-id="ebffc-123">**Метод Сеткреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="ebffc-123">**SetCreationClassName method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-setcreationclassname)
-   [<span data-ttu-id="ebffc-124">**Метод Валидатеделетионфлагс**</span><span class="sxs-lookup"><span data-stu-id="ebffc-124">**ValidateDeletionFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatedeletionflags)
-   [<span data-ttu-id="ebffc-125">**Метод Валидатинумератионфлагс**</span><span class="sxs-lookup"><span data-stu-id="ebffc-125">**ValidateEnumerationFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateenumerationflags)
-   [<span data-ttu-id="ebffc-126">**Метод Валидатефлагс**</span><span class="sxs-lookup"><span data-stu-id="ebffc-126">**ValidateFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateflags)
-   [<span data-ttu-id="ebffc-127">**Метод Валидатежетобжфлагс**</span><span class="sxs-lookup"><span data-stu-id="ebffc-127">**ValidateGetObjFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validategetobjflags)
-   [<span data-ttu-id="ebffc-128">**Метод Валидатемесодфлагс**</span><span class="sxs-lookup"><span data-stu-id="ebffc-128">**ValidateMethodFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatemethodflags)
-   [<span data-ttu-id="ebffc-129">**Метод Валидатепутинстанцефлагс**</span><span class="sxs-lookup"><span data-stu-id="ebffc-129">**ValidatePutInstanceFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validateputinstanceflags)
-   [<span data-ttu-id="ebffc-130">**Метод Валидатекуерифлагс**</span><span class="sxs-lookup"><span data-stu-id="ebffc-130">**ValidateQueryFlags method**</span></span>](/windows/desktop/api/Provider/nf-provider-provider-validatequeryflags)

 

 
