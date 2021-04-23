---
description: Класс Квбемпровидерглуе предоставляет следующие методы.
ms.assetid: E09290AF-1C2E-458A-811E-5357D470D3DF
ms.tgt_platform: multiple
title: Методы Квбемпровидерглуе
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea54ffdeaa6b74cda3b830ea65fdc17f8ffa129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998669"
---
# <a name="cwbemproviderglue-methods"></a><span data-ttu-id="9b03e-103">Методы Квбемпровидерглуе</span><span class="sxs-lookup"><span data-stu-id="9b03e-103">CWbemProviderGlue Methods</span></span>

<span data-ttu-id="9b03e-104">\[Класс [**квбемпровидерглуе**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) является частью платформы поставщика WMI, которая теперь считается окончательным состоянием, и дальнейшая разработка, улучшения и обновления не будут доступны для проблем, связанных с безопасностью, затрагивающих эти библиотеки.</span><span class="sxs-lookup"><span data-stu-id="9b03e-104">\[The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="9b03e-105">[API MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) следует использовать для всех новых разработок.\]</span><span class="sxs-lookup"><span data-stu-id="9b03e-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="9b03e-106">Класс [**квбемпровидерглуе**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9b03e-106">The [**CWbemProviderGlue**](/windows/desktop/api/WbemGlue/nl-wbemglue-cwbemproviderglue) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b03e-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="9b03e-107">In this section</span></span>

-   <span data-ttu-id="9b03e-108">[**Метод Фрамеворклогиндлл**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="9b03e-108">[**FrameworkLoginDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="9b03e-109">[**Метод Фрамеворклогоффдлл**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span><span class="sxs-lookup"><span data-stu-id="9b03e-109">[**FrameworkLogoffDLL method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong))</span></span>
-   <span data-ttu-id="9b03e-110">[**Метод Жеталлдеривединстанцес**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="9b03e-110">[**GetAllDerivedInstances method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstances(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="9b03e-111">**Метод Жеталлдеривединстанцесасинч**</span><span class="sxs-lookup"><span data-stu-id="9b03e-111">**GetAllDerivedInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallderivedinstancesasynch)
-   [<span data-ttu-id="9b03e-112">**Метод Жеталлинстанцес**</span><span class="sxs-lookup"><span data-stu-id="9b03e-112">**GetAllInstances method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstances)
-   [<span data-ttu-id="9b03e-113">**Метод Жеталлинстанцесасинч**</span><span class="sxs-lookup"><span data-stu-id="9b03e-113">**GetAllInstancesAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getallinstancesasynch)
-   <span data-ttu-id="9b03e-114">[**Методы Жетемптинстанце**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="9b03e-114">[**GetEmptyInstance methods**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))</span></span>
-   <span data-ttu-id="9b03e-115">[**Метод Жетинстанцебипас**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="9b03e-115">[**GetInstanceByPath method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancebypath(lpcwstr_cinstance_methodcontext))</span></span>
-   [<span data-ttu-id="9b03e-116">**Метод Жетинстанцекэйсбипас**</span><span class="sxs-lookup"><span data-stu-id="9b03e-116">**GetInstanceKeysByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancekeysbypath)
-   [<span data-ttu-id="9b03e-117">**Метод Жетинстанцепропертиесбипас**</span><span class="sxs-lookup"><span data-stu-id="9b03e-117">**GetInstancePropertiesByPath method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancepropertiesbypath)
-   <span data-ttu-id="9b03e-118">[**Метод Жетинстанцесбикуери**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="9b03e-118">[**GetInstancesByQuery method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyquery(lpcwstr_trefpointercollection_cinstance__methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="9b03e-119">**Метод Жетинстанцесбикуерясинч**</span><span class="sxs-lookup"><span data-stu-id="9b03e-119">**GetInstancesByQueryAsynch method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getinstancesbyqueryasynch)
-   <span data-ttu-id="9b03e-120">[**Метод Жетнамеспацеконнектион**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span><span class="sxs-lookup"><span data-stu-id="9b03e-120">[**GetNameSpaceConnection method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-getnamespaceconnection(lpcwstr_methodcontext))</span></span>
-   <span data-ttu-id="9b03e-121">[**Метод Исдериведфром**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="9b03e-121">[**IsDerivedFrom method**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-isderivedfrom(lpcwstr_lpcwstr_methodcontext_lpcwstr))</span></span>
-   [<span data-ttu-id="9b03e-122">**Метод Сетстатусобжект**</span><span class="sxs-lookup"><span data-stu-id="9b03e-122">**SetStatusObject method**</span></span>](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-setstatusobject)

 

 
