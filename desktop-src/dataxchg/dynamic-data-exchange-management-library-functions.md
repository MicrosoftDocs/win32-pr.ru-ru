---
title: Функции ДДЕМЛ
description: . | Функции ДДЕМЛ
ms.assetid: daaa18e6-2948-4058-9943-e5212c835d54
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc466c21d28822ca5c3c2849bd88523efb5ebc00
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273514"
---
# <a name="ddeml-functions"></a><span data-ttu-id="82c05-104">Функции ДДЕМЛ</span><span class="sxs-lookup"><span data-stu-id="82c05-104">DDEML Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="82c05-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="82c05-105">In this section</span></span>

-   [<span data-ttu-id="82c05-106">**ддеабандонтрансактион**</span><span class="sxs-lookup"><span data-stu-id="82c05-106">**DdeAbandonTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction)
-   [<span data-ttu-id="82c05-107">**ддеакцессдата**</span><span class="sxs-lookup"><span data-stu-id="82c05-107">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
-   [<span data-ttu-id="82c05-108">**ддеадддата**</span><span class="sxs-lookup"><span data-stu-id="82c05-108">**DdeAddData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata)
-   [<span data-ttu-id="82c05-109">*ддекаллбакк*</span><span class="sxs-lookup"><span data-stu-id="82c05-109">*DdeCallback*</span></span>](/windows/win32/api/ddeml/nc-ddeml-pfncallback)
-   [<span data-ttu-id="82c05-110">**ддеклиенттрансактион**</span><span class="sxs-lookup"><span data-stu-id="82c05-110">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
-   [<span data-ttu-id="82c05-111">**ддекмпстрингхандлес**</span><span class="sxs-lookup"><span data-stu-id="82c05-111">**DdeCmpStringHandles**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles)
-   [<span data-ttu-id="82c05-112">**ддеконнект**</span><span class="sxs-lookup"><span data-stu-id="82c05-112">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
-   [<span data-ttu-id="82c05-113">**ддеконнектлист**</span><span class="sxs-lookup"><span data-stu-id="82c05-113">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
-   [<span data-ttu-id="82c05-114">**ддекреатедатахандле**</span><span class="sxs-lookup"><span data-stu-id="82c05-114">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
-   [<span data-ttu-id="82c05-115">**ддекреатестрингхандле**</span><span class="sxs-lookup"><span data-stu-id="82c05-115">**DdeCreateStringHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea)
-   [<span data-ttu-id="82c05-116">**ддедисконнект**</span><span class="sxs-lookup"><span data-stu-id="82c05-116">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
-   [<span data-ttu-id="82c05-117">**ддедисконнектлист**</span><span class="sxs-lookup"><span data-stu-id="82c05-117">**DdeDisconnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnectlist)
-   [<span data-ttu-id="82c05-118">**ддинаблекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="82c05-118">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
-   [<span data-ttu-id="82c05-119">**ддефридатахандле**</span><span class="sxs-lookup"><span data-stu-id="82c05-119">**DdeFreeDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle)
-   [<span data-ttu-id="82c05-120">**ддефристрингхандле**</span><span class="sxs-lookup"><span data-stu-id="82c05-120">**DdeFreeStringHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle)
-   [<span data-ttu-id="82c05-121">**ддежетдата**</span><span class="sxs-lookup"><span data-stu-id="82c05-121">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
-   [<span data-ttu-id="82c05-122">**ддежетластеррор**</span><span class="sxs-lookup"><span data-stu-id="82c05-122">**DdeGetLastError**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror)
-   [<span data-ttu-id="82c05-123">**ддеимперсонатеклиент**</span><span class="sxs-lookup"><span data-stu-id="82c05-123">**DdeImpersonateClient**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient)
-   [<span data-ttu-id="82c05-124">**ддеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="82c05-124">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
-   [<span data-ttu-id="82c05-125">**ддекипстрингхандле**</span><span class="sxs-lookup"><span data-stu-id="82c05-125">**DdeKeepStringHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle)
-   [<span data-ttu-id="82c05-126">**дденамесервице**</span><span class="sxs-lookup"><span data-stu-id="82c05-126">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
-   [<span data-ttu-id="82c05-127">**ддепостадвисе**</span><span class="sxs-lookup"><span data-stu-id="82c05-127">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
-   [<span data-ttu-id="82c05-128">**ддекуериконвинфо**</span><span class="sxs-lookup"><span data-stu-id="82c05-128">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
-   [<span data-ttu-id="82c05-129">**ддекуеринекстсервер**</span><span class="sxs-lookup"><span data-stu-id="82c05-129">**DdeQueryNextServer**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequerynextserver)
-   [<span data-ttu-id="82c05-130">**ддекуеристринг**</span><span class="sxs-lookup"><span data-stu-id="82c05-130">**DdeQueryString**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa)
-   [<span data-ttu-id="82c05-131">**ддереконнект**</span><span class="sxs-lookup"><span data-stu-id="82c05-131">**DdeReconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddereconnect)
-   [<span data-ttu-id="82c05-132">**ддесетусерхандле**</span><span class="sxs-lookup"><span data-stu-id="82c05-132">**DdeSetUserHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle)
-   [<span data-ttu-id="82c05-133">**ддеунакцессдата**</span><span class="sxs-lookup"><span data-stu-id="82c05-133">**DdeUnaccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata)
-   [<span data-ttu-id="82c05-134">**ддеунинитиализе**</span><span class="sxs-lookup"><span data-stu-id="82c05-134">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)

 

 
