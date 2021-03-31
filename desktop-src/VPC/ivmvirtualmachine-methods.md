---
title: Методы Ивмвиртуалмачине
description: Интерфейс Ивмвиртуалмачине предоставляет следующие методы.
ms.assetid: 7C80371E-22CC-41BC-A1E5-B550DAD5B8D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc83c4403e070d2d4c144a1028451e39ed12016
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792643"
---
# <a name="ivmvirtualmachine-methods"></a><span data-ttu-id="05dfd-103">Методы Ивмвиртуалмачине</span><span class="sxs-lookup"><span data-stu-id="05dfd-103">IVMVirtualMachine Methods</span></span>

<span data-ttu-id="05dfd-104">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05dfd-104">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05dfd-105">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05dfd-105">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05dfd-106">Интерфейс [**ивмвиртуалмачине**](ivmvirtualmachine.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="05dfd-106">The [**IVMVirtualMachine**](ivmvirtualmachine.md) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="05dfd-107">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="05dfd-107">In this section</span></span>

-   [<span data-ttu-id="05dfd-108">**Метод Адддвдромдриве**</span><span class="sxs-lookup"><span data-stu-id="05dfd-108">**AddDVDROMDrive Method**</span></span>](ivmvirtualmachine-adddvdromdrive.md)
-   [<span data-ttu-id="05dfd-109">**Метод AddHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="05dfd-109">**AddHardDiskConnection Method**</span></span>](ivmvirtualmachine-addharddiskconnection.md)
-   [<span data-ttu-id="05dfd-110">**Метод Адднетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="05dfd-110">**AddNetworkAdapter Method**</span></span>](ivmvirtualmachine-addnetworkadapter.md)
-   [<span data-ttu-id="05dfd-111">**Метод Аттачусбдевице**</span><span class="sxs-lookup"><span data-stu-id="05dfd-111">**AttachUSBDevice Method**</span></span>](ivmvirtualmachine-attachusbdevice.md)
-   [<span data-ttu-id="05dfd-112">**Метод Детачусбдевице**</span><span class="sxs-lookup"><span data-stu-id="05dfd-112">**DetachUSBDevice Method**</span></span>](ivmvirtualmachine-detachusbdevice.md)
-   [<span data-ttu-id="05dfd-113">**Метод Дискардсаведстате**</span><span class="sxs-lookup"><span data-stu-id="05dfd-113">**DiscardSavedState Method**</span></span>](ivmvirtualmachine-discardsavedstate.md)
-   [<span data-ttu-id="05dfd-114">**Метод Дискардундодискс**</span><span class="sxs-lookup"><span data-stu-id="05dfd-114">**DiscardUndoDisks Method**</span></span>](ivmvirtualmachine-discardundodisks.md)
-   [<span data-ttu-id="05dfd-115">**Метод Жетактиватионвалуе**</span><span class="sxs-lookup"><span data-stu-id="05dfd-115">**GetActivationValue Method**</span></span>](ivmvirtualmachine-getactivationvalue.md)
-   [<span data-ttu-id="05dfd-116">**Метод Жетконфигуратионвалуе**</span><span class="sxs-lookup"><span data-stu-id="05dfd-116">**GetConfigurationValue Method**</span></span>](ivmvirtualmachine-getconfigurationvalue.md)
-   [<span data-ttu-id="05dfd-117">**Метод Мержеундодискс**</span><span class="sxs-lookup"><span data-stu-id="05dfd-117">**MergeUndoDisks Method**</span></span>](ivmvirtualmachine-mergeundodisks.md)
-   [<span data-ttu-id="05dfd-118">**Приостановить метод**</span><span class="sxs-lookup"><span data-stu-id="05dfd-118">**Pause Method**</span></span>](ivmvirtualmachine-pause.md)
-   [<span data-ttu-id="05dfd-119">**Метод Ремовеактиватионвалуе**</span><span class="sxs-lookup"><span data-stu-id="05dfd-119">**RemoveActivationValue Method**</span></span>](ivmvirtualmachine-removeactivationvalue.md)
-   [<span data-ttu-id="05dfd-120">**Метод Ремовеконфигуратионвалуе**</span><span class="sxs-lookup"><span data-stu-id="05dfd-120">**RemoveConfigurationValue Method**</span></span>](ivmvirtualmachine-removeconfigurationvalue.md)
-   [<span data-ttu-id="05dfd-121">**Метод Ремоведвдромдриве**</span><span class="sxs-lookup"><span data-stu-id="05dfd-121">**RemoveDVDROMDrive Method**</span></span>](ivmvirtualmachine-removedvdromdrive.md)
-   [<span data-ttu-id="05dfd-122">**Метод Ремовехарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="05dfd-122">**RemoveHardDiskConnection Method**</span></span>](ivmvirtualmachine-removeharddiskconnection.md)
-   [<span data-ttu-id="05dfd-123">**Метод Ремовенетворкадаптер**</span><span class="sxs-lookup"><span data-stu-id="05dfd-123">**RemoveNetworkAdapter Method**</span></span>](ivmvirtualmachine-removenetworkadapter.md)
-   [<span data-ttu-id="05dfd-124">**Метод Reset**</span><span class="sxs-lookup"><span data-stu-id="05dfd-124">**Reset Method**</span></span>](ivmvirtualmachine-reset.md)
-   [<span data-ttu-id="05dfd-125">**Метод Resume**</span><span class="sxs-lookup"><span data-stu-id="05dfd-125">**Resume Method**</span></span>](ivmvirtualmachine-resume.md)
-   [<span data-ttu-id="05dfd-126">**Метод Save**</span><span class="sxs-lookup"><span data-stu-id="05dfd-126">**Save Method**</span></span>](ivmvirtualmachine-save.md)
-   [<span data-ttu-id="05dfd-127">**Метод Сетактиватионвалуе**</span><span class="sxs-lookup"><span data-stu-id="05dfd-127">**SetActivationValue Method**</span></span>](ivmvirtualmachine-setactivationvalue.md)
-   [<span data-ttu-id="05dfd-128">**Метод Сетконфигуратионвалуе**</span><span class="sxs-lookup"><span data-stu-id="05dfd-128">**SetConfigurationValue Method**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
-   [<span data-ttu-id="05dfd-129">**Метод Старткоммуникатиончаннел**</span><span class="sxs-lookup"><span data-stu-id="05dfd-129">**StartCommunicationChannel Method**</span></span>](ivmvirtualmachine-startcommunicationchannel.md)
-   [<span data-ttu-id="05dfd-130">**Метод запуска**</span><span class="sxs-lookup"><span data-stu-id="05dfd-130">**Startup Method**</span></span>](ivmvirtualmachine-startup.md)
-   [<span data-ttu-id="05dfd-131">**Метод Startup2**</span><span class="sxs-lookup"><span data-stu-id="05dfd-131">**Startup2 Method**</span></span>](ivmvirtualmachine-startup2.md)
-   [<span data-ttu-id="05dfd-132">**Метод Турнофф**</span><span class="sxs-lookup"><span data-stu-id="05dfd-132">**TurnOff Method**</span></span>](ivmvirtualmachine-turnoff.md)

 

 