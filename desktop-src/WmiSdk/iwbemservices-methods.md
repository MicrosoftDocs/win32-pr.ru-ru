---
description: Интерфейс IWbemServices предоставляет следующие методы.
ms.assetid: B4A2048E-6C2F-43E0-97BD-E6D37D8E4657
ms.tgt_platform: multiple
title: Методы IWbemServices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a960ec223d16bd9258ba2d9d56518d88beab50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702365"
---
# <a name="iwbemservices-methods"></a><span data-ttu-id="80e30-103">Методы IWbemServices</span><span class="sxs-lookup"><span data-stu-id="80e30-103">IWbemServices Methods</span></span>

<span data-ttu-id="80e30-104">Интерфейс [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="80e30-104">The [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="80e30-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="80e30-105">In this section</span></span>

-   [<span data-ttu-id="80e30-106">**Метод Канцеласинккалл**</span><span class="sxs-lookup"><span data-stu-id="80e30-106">**CancelAsyncCall method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall)
-   [<span data-ttu-id="80e30-107">**Метод Креатеклассенум**</span><span class="sxs-lookup"><span data-stu-id="80e30-107">**CreateClassEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)
-   [<span data-ttu-id="80e30-108">**Метод Креатеклассенумасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-108">**CreateClassEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [<span data-ttu-id="80e30-109">**Метод CreateInstanceEnum**</span><span class="sxs-lookup"><span data-stu-id="80e30-109">**CreateInstanceEnum method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)
-   [<span data-ttu-id="80e30-110">**Метод Креатеинстанцеенумасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-110">**CreateInstanceEnumAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [<span data-ttu-id="80e30-111">**Метод Делетекласс**</span><span class="sxs-lookup"><span data-stu-id="80e30-111">**DeleteClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass)
-   [<span data-ttu-id="80e30-112">**Метод Делетеклассасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-112">**DeleteClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)
-   [<span data-ttu-id="80e30-113">**Метод DeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="80e30-113">**DeleteInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance)
-   [<span data-ttu-id="80e30-114">**Метод Делетеинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-114">**DeleteInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [<span data-ttu-id="80e30-115">**Метод ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="80e30-115">**ExecMethod method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
-   [<span data-ttu-id="80e30-116">**Метод Ексекмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-116">**ExecMethodAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
-   [<span data-ttu-id="80e30-117">**Метод Ексекнотификатионкуери**</span><span class="sxs-lookup"><span data-stu-id="80e30-117">**ExecNotificationQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)
-   [<span data-ttu-id="80e30-118">**Метод ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="80e30-118">**ExecNotificationQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [<span data-ttu-id="80e30-119">**Метод ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="80e30-119">**ExecQuery method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   [<span data-ttu-id="80e30-120">**Метод Ексеккуерясинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-120">**ExecQueryAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)
-   [<span data-ttu-id="80e30-121">**Метод GetObject**</span><span class="sxs-lookup"><span data-stu-id="80e30-121">**GetObject method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)
-   [<span data-ttu-id="80e30-122">**Метод Жетобжектасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-122">**GetObjectAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)
-   [<span data-ttu-id="80e30-123">**Метод OpenNamespace**</span><span class="sxs-lookup"><span data-stu-id="80e30-123">**OpenNamespace method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace)
-   [<span data-ttu-id="80e30-124">**Метод Путкласс**</span><span class="sxs-lookup"><span data-stu-id="80e30-124">**PutClass method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
-   [<span data-ttu-id="80e30-125">**Метод Путклассасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-125">**PutClassAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)
-   [<span data-ttu-id="80e30-126">**Метод PutInstance**</span><span class="sxs-lookup"><span data-stu-id="80e30-126">**PutInstance method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)
-   [<span data-ttu-id="80e30-127">**Метод Путинстанцеасинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-127">**PutInstanceAsync method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)
-   [<span data-ttu-id="80e30-128">**Метод Куерйобжектсинк**</span><span class="sxs-lookup"><span data-stu-id="80e30-128">**QueryObjectSink method**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-queryobjectsink)

 

 



