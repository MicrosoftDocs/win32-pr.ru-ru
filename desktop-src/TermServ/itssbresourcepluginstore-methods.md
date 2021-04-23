---
title: Методы Итссбресаурцеплугинсторе
description: Интерфейс Итссбресаурцеплугинсторе предоставляет следующие методы.
ms.assetid: D3D59244-E319-47C8-A931-72679C11AC40
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c56d403bc681152a5076d6c219790b452bd749d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888643"
---
# <a name="itssbresourcepluginstore-methods"></a><span data-ttu-id="254b7-103">Методы Итссбресаурцеплугинсторе</span><span class="sxs-lookup"><span data-stu-id="254b7-103">ITsSbResourcePluginStore Methods</span></span>

<span data-ttu-id="254b7-104">Интерфейс [**итссбресаурцеплугинсторе**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="254b7-104">The [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="254b7-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="254b7-105">In this section</span></span>

-   [<span data-ttu-id="254b7-106">**Метод Аккуиретаржетлокк**</span><span class="sxs-lookup"><span data-stu-id="254b7-106">**AcquireTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)
-   [<span data-ttu-id="254b7-107">**Метод Адденвиронменттосторе**</span><span class="sxs-lookup"><span data-stu-id="254b7-107">**AddEnvironmentToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)
-   [<span data-ttu-id="254b7-108">**Метод Аддсессионтосторе**</span><span class="sxs-lookup"><span data-stu-id="254b7-108">**AddSessionToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)
-   [<span data-ttu-id="254b7-109">**Метод Аддтаржеттосторе**</span><span class="sxs-lookup"><span data-stu-id="254b7-109">**AddTargetToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)
-   [<span data-ttu-id="254b7-110">**Метод Делететаржет**</span><span class="sxs-lookup"><span data-stu-id="254b7-110">**DeleteTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)
-   [<span data-ttu-id="254b7-111">**Метод Енумератинвиронментс**</span><span class="sxs-lookup"><span data-stu-id="254b7-111">**EnumerateEnvironments method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)
-   [<span data-ttu-id="254b7-112">**Метод Енумератефармс**</span><span class="sxs-lookup"><span data-stu-id="254b7-112">**EnumerateFarms method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)
-   [<span data-ttu-id="254b7-113">**Метод Енумератесессионс**</span><span class="sxs-lookup"><span data-stu-id="254b7-113">**EnumerateSessions method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)
-   [<span data-ttu-id="254b7-114">**Метод Енумератетаржетс**</span><span class="sxs-lookup"><span data-stu-id="254b7-114">**EnumerateTargets method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)
-   [<span data-ttu-id="254b7-115">**Метод Жетфармпроперти**</span><span class="sxs-lookup"><span data-stu-id="254b7-115">**GetFarmProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)
-   [<span data-ttu-id="254b7-116">**Метод Жетсерверстате**</span><span class="sxs-lookup"><span data-stu-id="254b7-116">**GetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getserverstate)
-   [<span data-ttu-id="254b7-117">**Метод Куеренвиронмент**</span><span class="sxs-lookup"><span data-stu-id="254b7-117">**QueryEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)
-   [<span data-ttu-id="254b7-118">**Метод Куерисессионбисессионид**</span><span class="sxs-lookup"><span data-stu-id="254b7-118">**QuerySessionBySessionId method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)
-   [<span data-ttu-id="254b7-119">**Метод Куеритаржет**</span><span class="sxs-lookup"><span data-stu-id="254b7-119">**QueryTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)
-   [<span data-ttu-id="254b7-120">**Метод Релеасетаржетлокк**</span><span class="sxs-lookup"><span data-stu-id="254b7-120">**ReleaseTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)
-   [<span data-ttu-id="254b7-121">**Метод Ремовинвиронментфромсторе**</span><span class="sxs-lookup"><span data-stu-id="254b7-121">**RemoveEnvironmentFromStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)
-   [<span data-ttu-id="254b7-122">**Метод Савинвиронмент**</span><span class="sxs-lookup"><span data-stu-id="254b7-122">**SaveEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)
-   [<span data-ttu-id="254b7-123">**Метод Савесессион**</span><span class="sxs-lookup"><span data-stu-id="254b7-123">**SaveSession method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)
-   [<span data-ttu-id="254b7-124">**Метод Саветаржет**</span><span class="sxs-lookup"><span data-stu-id="254b7-124">**SaveTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)
-   [<span data-ttu-id="254b7-125">**Метод Сетенвиронментпроперти**</span><span class="sxs-lookup"><span data-stu-id="254b7-125">**SetEnvironmentProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)
-   [<span data-ttu-id="254b7-126">**Метод Сетенвиронментпропертивисверсиончекк**</span><span class="sxs-lookup"><span data-stu-id="254b7-126">**SetEnvironmentPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck)
-   [<span data-ttu-id="254b7-127">**Метод Сетсервердраинмоде**</span><span class="sxs-lookup"><span data-stu-id="254b7-127">**SetServerDrainMode method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverdrainmode)
-   [<span data-ttu-id="254b7-128">**Метод Сетсерверваитингтостарт**</span><span class="sxs-lookup"><span data-stu-id="254b7-128">**SetServerWaitingToStart method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverwaitingtostart)
-   [<span data-ttu-id="254b7-129">**Метод Сетсессионстате**</span><span class="sxs-lookup"><span data-stu-id="254b7-129">**SetSessionState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)
-   [<span data-ttu-id="254b7-130">**Метод Сеттаржетпроперти**</span><span class="sxs-lookup"><span data-stu-id="254b7-130">**SetTargetProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)
-   [<span data-ttu-id="254b7-131">**Метод Сеттаржетпропертивисверсиончекк**</span><span class="sxs-lookup"><span data-stu-id="254b7-131">**SetTargetPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)
-   [<span data-ttu-id="254b7-132">**Метод Сеттаржетстате**</span><span class="sxs-lookup"><span data-stu-id="254b7-132">**SetTargetState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)
-   [<span data-ttu-id="254b7-133">**Метод Тестандсетсерверстате**</span><span class="sxs-lookup"><span data-stu-id="254b7-133">**TestAndSetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-testandsetserverstate)

 

 




