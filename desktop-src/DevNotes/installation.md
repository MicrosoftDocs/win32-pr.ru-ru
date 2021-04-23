---
description: Установка
ms.assetid: 02A7866F-0F72-4437-A882-EEE9C2E28EC7
title: Установка (заметки для разработчиков)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ddb476b6688bbbbef27eab571e3219071656a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896214"
---
# <a name="installation-developer-notes"></a><span data-ttu-id="2a1d5-103">Установка (заметки для разработчиков)</span><span class="sxs-lookup"><span data-stu-id="2a1d5-103">Installation (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2a1d5-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="2a1d5-104">In this section</span></span>

-   [<span data-ttu-id="2a1d5-105">**Соустановка**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-105">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
-   [<span data-ttu-id="2a1d5-106">**икфгинсталлинеткомпонентс**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-106">**IcfgInstallInetComponents**</span></span>](icfginstallinetcomponents.md)
-   [<span data-ttu-id="2a1d5-107">**икфгнидинеткомпонентс**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-107">**IcfgNeedInetComponents**</span></span>](icfgneedinetcomponents.md)
-   [<span data-ttu-id="2a1d5-108">**инсталлкаталог**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-108">**InstallCatalog**</span></span>](installcatalog.md)
-   [<span data-ttu-id="2a1d5-109">**инсталлкомпонентв**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-109">**InstallComponentW**</span></span>](installcomponentw.md)
-   [<span data-ttu-id="2a1d5-110">**инсталлперфдлл**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-110">**InstallPerfDll**</span></span>](/windows/desktop/api/LoadPerf/nf-loadperf-installperfdlla)
-   [<span data-ttu-id="2a1d5-111">**лоадлибраришим**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-111">**LoadLibraryShim**</span></span>](loadlibraryshim.md)
-   [<span data-ttu-id="2a1d5-112">**оЦинитиализе**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-112">**OcInitialize**</span></span>](ocinitialize.md)
-   [<span data-ttu-id="2a1d5-113">**октерминате**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-113">**OcTerminate**</span></span>](octerminate.md)
-   [<span data-ttu-id="2a1d5-114">**псетупжетфилетитле**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-114">**pSetupGetFileTitle**</span></span>](psetupgetfiletitle.md)
-   [<span data-ttu-id="2a1d5-115">**псетупжетглобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-115">**pSetupGetGlobalFlags**</span></span>](psetupgetglobalflags.md)
-   [<span data-ttu-id="2a1d5-116">**псетупинсталлкаталог**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-116">**pSetupInstallCatalog**</span></span>](psetupinstallcatalog.md)
-   [<span data-ttu-id="2a1d5-117">**псетуписусерадмин**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-117">**pSetupIsUserAdmin**</span></span>](psetupisuseradmin.md)
-   [<span data-ttu-id="2a1d5-118">**псетупсетглобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-118">**pSetupSetGlobalFlags**</span></span>](psetupsetglobalflags.md)
-   [<span data-ttu-id="2a1d5-119">**псетупстрингтабледестрой**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-119">**pSetupStringTableDestroy**</span></span>](psetupstringtabledestroy.md)
-   [<span data-ttu-id="2a1d5-120">**псетупстрингтаблеаддстринжекс**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-120">**pSetupStringTableAddStringEx**</span></span>](psetupstringtableaddstringex.md)
-   [<span data-ttu-id="2a1d5-121">**псетупстрингтаблеинитиализикс**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-121">**pSetupStringTableInitializeEx**</span></span>](psetupstringtableinitializeex.md)
-   [<span data-ttu-id="2a1d5-122">**псетупстрингтаблеинитиализе**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-122">**pSetupStringTableInitialize**</span></span>](psetupstringtableinitialize.md)
-   [<span data-ttu-id="2a1d5-123">**псетупверификаталогфиле**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-123">**pSetupVerifyCatalogFile**</span></span>](psetupverifycatalogfile.md)
-   [<span data-ttu-id="2a1d5-124">**перезагрузить \_ конфигурацию**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-124">**reload\_config**</span></span>](reload-config.md)
-   [<span data-ttu-id="2a1d5-125">**сксслукупклргуид**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-125">**SxsLookupClrGuid**</span></span>](sxslookupclrguid.md)
-   [<span data-ttu-id="2a1d5-126">**унинсталлкомпонент**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-126">**UninstallComponent**</span></span>](uninstallcomponent.md)
-   [<span data-ttu-id="2a1d5-127">**верификаталогфиле**</span><span class="sxs-lookup"><span data-stu-id="2a1d5-127">**VerifyCatalogFile**</span></span>](verifycatalogfile.md)

 

 
