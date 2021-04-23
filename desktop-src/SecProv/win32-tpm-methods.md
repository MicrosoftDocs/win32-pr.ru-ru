---
description: '\_Класс TPM Win32 предоставляет следующие методы.'
ms.assetid: 6027D9A7-524F-478D-8227-97B9DE6AC8ED
title: Методы Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6e3c5a49bc60d9d18fa27f3e0edfbd275973be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897038"
---
# <a name="win32_tpm-methods"></a><span data-ttu-id="a843d-103">\_Методы TPM Win32</span><span class="sxs-lookup"><span data-stu-id="a843d-103">Win32\_Tpm Methods</span></span>

<span data-ttu-id="a843d-104">Класс [**\_ TPM Win32**](win32-tpm.md) предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a843d-104">The [**Win32\_Tpm**](win32-tpm.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a843d-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="a843d-105">In this section</span></span>

-   [<span data-ttu-id="a843d-106">**Метод Аддблоккедкомманд**</span><span class="sxs-lookup"><span data-stu-id="a843d-106">**AddBlockedCommand Method**</span></span>](addblockedcommand-win32-tpm.md)
-   [<span data-ttu-id="a843d-107">**Метод Чанжеовнераус**</span><span class="sxs-lookup"><span data-stu-id="a843d-107">**ChangeOwnerAuth Method**</span></span>](changeownerauth-win32-tpm.md)
-   [<span data-ttu-id="a843d-108">**Метод Clear**</span><span class="sxs-lookup"><span data-stu-id="a843d-108">**Clear Method**</span></span>](clear-win32-tpm.md)
-   [<span data-ttu-id="a843d-109">**Метод Конверттувнераус**</span><span class="sxs-lookup"><span data-stu-id="a843d-109">**ConvertToOwnerAuth Method**</span></span>](converttoownerauth-win32-tpm.md)
-   [<span data-ttu-id="a843d-110">**Метод Креатиндорсементкэйпаир**</span><span class="sxs-lookup"><span data-stu-id="a843d-110">**CreateEndorsementKeyPair Method**</span></span>](createendorsementkeypair-win32-tpm.md)
-   [<span data-ttu-id="a843d-111">**Disable, метод**</span><span class="sxs-lookup"><span data-stu-id="a843d-111">**Disable Method**</span></span>](disable-win32-tpm.md)
-   [<span data-ttu-id="a843d-112">**Метод Дисаблеаутопровисионинг**</span><span class="sxs-lookup"><span data-stu-id="a843d-112">**DisableAutoProvisioning method**</span></span>](win32-tpm-disableautoprovisioning.md)
-   [<span data-ttu-id="a843d-113">**Enable, метод**</span><span class="sxs-lookup"><span data-stu-id="a843d-113">**Enable Method**</span></span>](enable-win32-tpm.md)
-   [<span data-ttu-id="a843d-114">**Метод Енаблеаутопровисионинг**</span><span class="sxs-lookup"><span data-stu-id="a843d-114">**EnableAutoProvisioning method**</span></span>](win32-tpm-enableautoprovisioning.md)
-   [<span data-ttu-id="a843d-115">**Метод Жетовнераус**</span><span class="sxs-lookup"><span data-stu-id="a843d-115">**GetOwnerAuth method**</span></span>](win32-tpm-getownerauth.md)
-   [<span data-ttu-id="a843d-116">**Метод Жетфисикалпресенцеконфирматионстатус**</span><span class="sxs-lookup"><span data-stu-id="a843d-116">**GetPhysicalPresenceConfirmationStatus method**</span></span>](win32-tpm-getphysicalpresenceconfirmationstatus.md)
-   [<span data-ttu-id="a843d-117">**Метод Жетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="a843d-117">**GetPhysicalPresenceRequest Method**</span></span>](getphysicalpresencerequest-win32-tpm.md)
-   [<span data-ttu-id="a843d-118">**Метод Жетфисикалпресенцереспонсе**</span><span class="sxs-lookup"><span data-stu-id="a843d-118">**GetPhysicalPresenceResponse Method**</span></span>](getphysicalpresenceresponse-win32-tpm.md)
-   [<span data-ttu-id="a843d-119">**Метод Жетфисикалпресенцетранситион**</span><span class="sxs-lookup"><span data-stu-id="a843d-119">**GetPhysicalPresenceTransition Method**</span></span>](getphysicalpresencetransition-win32-tpm.md)
-   [<span data-ttu-id="a843d-120">**Метод Жетсркадсумбпринт**</span><span class="sxs-lookup"><span data-stu-id="a843d-120">**GetSrkADThumbprint method**</span></span>](win32-tpm-getsrkadthumbprint.md)
-   [<span data-ttu-id="a843d-121">**Метод Жетсркпубликкэймодулус**</span><span class="sxs-lookup"><span data-stu-id="a843d-121">**GetSrkPublicKeyModulus method**</span></span>](win32-tpm-getsrkpublickeymodulus.md)
-   [<span data-ttu-id="a843d-122">**Метод Импортовнераус**</span><span class="sxs-lookup"><span data-stu-id="a843d-122">**ImportOwnerAuth method**</span></span>](win32-tpm-importownerauth.md)
-   [<span data-ttu-id="a843d-123">**Метод, активированный**</span><span class="sxs-lookup"><span data-stu-id="a843d-123">**IsActivated Method**</span></span>](isactivated-win32-tpm.md)
-   [<span data-ttu-id="a843d-124">**Метод Исаутопровисионинженаблед**</span><span class="sxs-lookup"><span data-stu-id="a843d-124">**IsAutoProvisioningEnabled method**</span></span>](win32-tpm-isautoprovisioningenabled.md)
-   [<span data-ttu-id="a843d-125">**Метод Искоммандблоккед**</span><span class="sxs-lookup"><span data-stu-id="a843d-125">**IsCommandBlocked Method**</span></span>](iscommandblocked-win32-tpm.md)
-   [<span data-ttu-id="a843d-126">**Метод Искоммандпресент**</span><span class="sxs-lookup"><span data-stu-id="a843d-126">**IsCommandPresent Method**</span></span>](iscommandpresent-win32-tpm.md)
-   [<span data-ttu-id="a843d-127">**Включенный метод**</span><span class="sxs-lookup"><span data-stu-id="a843d-127">**IsEnabled Method**</span></span>](isenabled-win32-tpm.md)
-   [<span data-ttu-id="a843d-128">**Метод Исендорсементкэйпаирпресент**</span><span class="sxs-lookup"><span data-stu-id="a843d-128">**IsEndorsementKeyPairPresent Method**</span></span>](isendorsementkeypairpresent-win32-tpm.md)
-   [<span data-ttu-id="a843d-129">**Метод владеет**</span><span class="sxs-lookup"><span data-stu-id="a843d-129">**IsOwned Method**</span></span>](isowned-win32-tpm.md)
-   [<span data-ttu-id="a843d-130">**Метод Исовнерклеардисаблед**</span><span class="sxs-lookup"><span data-stu-id="a843d-130">**IsOwnerClearDisabled Method**</span></span>](isownercleardisabled-win32-tpm.md)
-   [<span data-ttu-id="a843d-131">**Метод Исовнершипалловед**</span><span class="sxs-lookup"><span data-stu-id="a843d-131">**IsOwnershipAllowed Method**</span></span>](isownershipallowed-win32-tpm.md)
-   [<span data-ttu-id="a843d-132">**Метод Исфисикалклеардисаблед**</span><span class="sxs-lookup"><span data-stu-id="a843d-132">**IsPhysicalClearDisabled Method**</span></span>](isphysicalcleardisabled-win32-tpm.md)
-   [<span data-ttu-id="a843d-133">**Метод Исфисикалпресенцехардваринаблед**</span><span class="sxs-lookup"><span data-stu-id="a843d-133">**IsPhysicalPresenceHardwareEnabled Method**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md)
-   [<span data-ttu-id="a843d-134">**Метод Read**</span><span class="sxs-lookup"><span data-stu-id="a843d-134">**IsReady method**</span></span>](win32-tpm-isready.md)
-   [<span data-ttu-id="a843d-135">**Метод Исреадинформатион**</span><span class="sxs-lookup"><span data-stu-id="a843d-135">**IsReadyInformation method**</span></span>](win32-tpm-isreadyinformation.md)
-   [<span data-ttu-id="a843d-136">**Метод Иссркаускомпатибле**</span><span class="sxs-lookup"><span data-stu-id="a843d-136">**IsSrkAuthCompatible Method**</span></span>](issrkauthcompatible-win32-tpm.md)
-   [<span data-ttu-id="a843d-137">**Метод инициализации**</span><span class="sxs-lookup"><span data-stu-id="a843d-137">**Provision method**</span></span>](win32-tpm-provision.md)
-   [<span data-ttu-id="a843d-138">**Метод Ремовеблоккедкомманд**</span><span class="sxs-lookup"><span data-stu-id="a843d-138">**RemoveBlockedCommand Method**</span></span>](removeblockedcommand-win32-tpm.md)
-   [<span data-ttu-id="a843d-139">**Метод Ресетауслоккаут**</span><span class="sxs-lookup"><span data-stu-id="a843d-139">**ResetAuthLockOut Method**</span></span>](resetauthlockout-win32-tpm.md)
-   [<span data-ttu-id="a843d-140">**Метод Ресетсркаус**</span><span class="sxs-lookup"><span data-stu-id="a843d-140">**ResetSrkAuth Method**</span></span>](resetsrkauth-win32-tpm.md)
-   [<span data-ttu-id="a843d-141">**Метод SelfTest**</span><span class="sxs-lookup"><span data-stu-id="a843d-141">**SelfTest Method**</span></span>](selftest-win32-tpm.md)
-   [<span data-ttu-id="a843d-142">**Метод Сетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="a843d-142">**SetPhysicalPresenceRequest Method**</span></span>](setphysicalpresencerequest-win32-tpm.md)
-   [<span data-ttu-id="a843d-143">**Метод Такеовнершип**</span><span class="sxs-lookup"><span data-stu-id="a843d-143">**TakeOwnership Method**</span></span>](takeownership-win32-tpm.md)

 

 



