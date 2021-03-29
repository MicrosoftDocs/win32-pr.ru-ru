---
title: Управление контекстом поставщика
description: Управление контекстом поставщика
ms.assetid: A73A6171-C81B-48EF-A689-3219E0B6B7C3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7970cdd6f3a69760a74ba4f0419ecb5022a339
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790554"
---
# <a name="provider-context-management"></a><span data-ttu-id="10ca2-103">Управление контекстом поставщика</span><span class="sxs-lookup"><span data-stu-id="10ca2-103">Provider Context Management</span></span>

## <a name="in-this-section"></a><span data-ttu-id="10ca2-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="10ca2-104">In this section</span></span>

-   [<span data-ttu-id="10ca2-105">**\_ \_ \_ CALLBACK0 изменения контекста поставщика \_ фвпм**</span><span class="sxs-lookup"><span data-stu-id="10ca2-105">**FWPM\_PROVIDER\_CONTEXT\_CHANGE\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_provider_context_change_callback0)
-   [<span data-ttu-id="10ca2-106">**FwpmProviderContextAdd0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-106">**FwpmProviderContextAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)
-   [<span data-ttu-id="10ca2-107">**FwpmProviderContextAdd1**</span><span class="sxs-lookup"><span data-stu-id="10ca2-107">**FwpmProviderContextAdd1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd1)
-   [<span data-ttu-id="10ca2-108">**FwpmProviderContextAdd2**</span><span class="sxs-lookup"><span data-stu-id="10ca2-108">**FwpmProviderContextAdd2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [<span data-ttu-id="10ca2-109">**FwpmProviderContextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-109">**FwpmProviderContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextcreateenumhandle0)
-   [<span data-ttu-id="10ca2-110">**FwpmProviderContextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-110">**FwpmProviderContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebyid0)
-   [<span data-ttu-id="10ca2-111">**FwpmProviderContextDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-111">**FwpmProviderContextDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdeletebykey0)
-   [<span data-ttu-id="10ca2-112">**FwpmProviderContextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-112">**FwpmProviderContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextdestroyenumhandle0)
-   [<span data-ttu-id="10ca2-113">**FwpmProviderContextEnum0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-113">**FwpmProviderContextEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum0)
-   [<span data-ttu-id="10ca2-114">**FwpmProviderContextEnum1**</span><span class="sxs-lookup"><span data-stu-id="10ca2-114">**FwpmProviderContextEnum1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextenum1)
-   [<span data-ttu-id="10ca2-115">**FwpmProviderContextEnum2**</span><span class="sxs-lookup"><span data-stu-id="10ca2-115">**FwpmProviderContextEnum2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [<span data-ttu-id="10ca2-116">**FwpmProviderContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-116">**FwpmProviderContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid0)
-   [<span data-ttu-id="10ca2-117">**FwpmProviderContextGetById1**</span><span class="sxs-lookup"><span data-stu-id="10ca2-117">**FwpmProviderContextGetById1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid1)
-   [<span data-ttu-id="10ca2-118">**FwpmProviderContextGetById2**</span><span class="sxs-lookup"><span data-stu-id="10ca2-118">**FwpmProviderContextGetById2**</span></span>](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [<span data-ttu-id="10ca2-119">**FwpmProviderContextGetByKey0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-119">**FwpmProviderContextGetByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey0)
-   [<span data-ttu-id="10ca2-120">**FwpmProviderContextGetByKey1**</span><span class="sxs-lookup"><span data-stu-id="10ca2-120">**FwpmProviderContextGetByKey1**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey1)
-   [<span data-ttu-id="10ca2-121">**FwpmProviderContextGetByKey2**</span><span class="sxs-lookup"><span data-stu-id="10ca2-121">**FwpmProviderContextGetByKey2**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [<span data-ttu-id="10ca2-122">**FwpmProviderContextGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-122">**FwpmProviderContextGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetsecurityinfobykey0)
-   [<span data-ttu-id="10ca2-123">**FwpmProviderContextSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-123">**FwpmProviderContextSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsetsecurityinfobykey0)
-   [<span data-ttu-id="10ca2-124">**FwpmProviderContextSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-124">**FwpmProviderContextSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscribechanges0)
-   [<span data-ttu-id="10ca2-125">**FwpmProviderContextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-125">**FwpmProviderContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextsubscriptionsget0)
-   [<span data-ttu-id="10ca2-126">**FwpmProviderContextUnsubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="10ca2-126">**FwpmProviderContextUnsubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextunsubscribechanges0)

 

 