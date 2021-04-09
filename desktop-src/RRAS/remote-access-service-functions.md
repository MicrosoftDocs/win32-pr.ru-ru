---
title: Функции службы удаленного доступа
description: Используйте следующие функции для реализации функциональности службы удаленного доступа.
ms.assetid: 5883a77a-6af8-47a8-bb28-6ef60a5aa2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d272403c8cd485f5e9d3d1de0c7fe5ac1cac9442
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134366"
---
# <a name="remote-access-service-functions"></a><span data-ttu-id="9dac5-103">Функции службы удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="9dac5-103">Remote Access Service Functions</span></span>

<span data-ttu-id="9dac5-104">Используйте следующие функции для реализации функциональности службы удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="9dac5-104">Use the following functions to implement RAS functionality.</span></span>

<span data-ttu-id="9dac5-105">**кмфри**</span><span class="sxs-lookup"><span data-stu-id="9dac5-105">**CmFree**</span></span>

<span data-ttu-id="9dac5-106">**кммаллок**</span><span class="sxs-lookup"><span data-stu-id="9dac5-106">**CmMalloc**</span></span>

[<span data-ttu-id="9dac5-107">**орасадфунк**</span><span class="sxs-lookup"><span data-stu-id="9dac5-107">**ORASADFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-orasadfunc)

[<span data-ttu-id="9dac5-108">**расадфунк**</span><span class="sxs-lookup"><span data-stu-id="9dac5-108">**RASADFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasadfunca)

[<span data-ttu-id="9dac5-109">**расклеарконнектионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-109">**RasClearConnectionStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasclearconnectionstatistics)

[<span data-ttu-id="9dac5-110">**расклеарлинкстатистикс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-110">**RasClearLinkStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasclearlinkstatistics)

[<span data-ttu-id="9dac5-111">**расконнектионнотификатион**</span><span class="sxs-lookup"><span data-stu-id="9dac5-111">**RasConnectionNotification**</span></span>](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa)

[<span data-ttu-id="9dac5-112">**раскреатефонебукентри**</span><span class="sxs-lookup"><span data-stu-id="9dac5-112">**RasCreatePhonebookEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya)

[<span data-ttu-id="9dac5-113">**раскустомделетинтринотифи**</span><span class="sxs-lookup"><span data-stu-id="9dac5-113">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

[<span data-ttu-id="9dac5-114">**раскустомдиал**</span><span class="sxs-lookup"><span data-stu-id="9dac5-114">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)

[<span data-ttu-id="9dac5-115">**раскустомдиалдлг**</span><span class="sxs-lookup"><span data-stu-id="9dac5-115">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)

[<span data-ttu-id="9dac5-116">**раскустоментридлг**</span><span class="sxs-lookup"><span data-stu-id="9dac5-116">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)

[<span data-ttu-id="9dac5-117">**раскустомхангуп**</span><span class="sxs-lookup"><span data-stu-id="9dac5-117">**RasCustomHangUp**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)

[<span data-ttu-id="9dac5-118">**расделетинтри**</span><span class="sxs-lookup"><span data-stu-id="9dac5-118">**RasDeleteEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya)

[<span data-ttu-id="9dac5-119">**расделетесубентри**</span><span class="sxs-lookup"><span data-stu-id="9dac5-119">**RasDeleteSubEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdeletesubentrya)

[<span data-ttu-id="9dac5-120">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="9dac5-120">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)

[<span data-ttu-id="9dac5-121">**расдиалдлг**</span><span class="sxs-lookup"><span data-stu-id="9dac5-121">**RasDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)

[<span data-ttu-id="9dac5-122">**расдиалфунк**</span><span class="sxs-lookup"><span data-stu-id="9dac5-122">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)

[<span data-ttu-id="9dac5-123">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="9dac5-123">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)

[<span data-ttu-id="9dac5-124">**RasDialFunc2**</span><span class="sxs-lookup"><span data-stu-id="9dac5-124">**RasDialFunc2**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc2)

[<span data-ttu-id="9dac5-125">**раседитфонебукентри**</span><span class="sxs-lookup"><span data-stu-id="9dac5-125">**RasEditPhonebookEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya)

[<span data-ttu-id="9dac5-126">**расентридлг**</span><span class="sxs-lookup"><span data-stu-id="9dac5-126">**RasEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)

[<span data-ttu-id="9dac5-127">**расенумаутодиаладдрессес**</span><span class="sxs-lookup"><span data-stu-id="9dac5-127">**RasEnumAutodialAddresses**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa)

[<span data-ttu-id="9dac5-128">**расенумконнектионс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-128">**RasEnumConnections**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa)

[<span data-ttu-id="9dac5-129">**расенумдевицес**</span><span class="sxs-lookup"><span data-stu-id="9dac5-129">**RasEnumDevices**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa)

[<span data-ttu-id="9dac5-130">**расенументриес**</span><span class="sxs-lookup"><span data-stu-id="9dac5-130">**RasEnumEntries**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumentriesa)

[<span data-ttu-id="9dac5-131">**расфриеапусеридентити**</span><span class="sxs-lookup"><span data-stu-id="9dac5-131">**RasFreeEapUserIdentity**</span></span>](/windows/desktop/api/Ras/nf-ras-rasfreeeapuseridentitya)

[<span data-ttu-id="9dac5-132">**расжетаутодиаладдресс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-132">**RasGetAutodialAddress**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa)

[<span data-ttu-id="9dac5-133">**расжетаутодиаленабле**</span><span class="sxs-lookup"><span data-stu-id="9dac5-133">**RasGetAutodialEnable**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea)

[<span data-ttu-id="9dac5-134">**расжетаутодиалпарам**</span><span class="sxs-lookup"><span data-stu-id="9dac5-134">**RasGetAutodialParam**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama)

[<span data-ttu-id="9dac5-135">**расжетконнектионстатистикс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-135">**RasGetConnectionStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetconnectionstatistics)

[<span data-ttu-id="9dac5-136">**расжетконнектстатус**</span><span class="sxs-lookup"><span data-stu-id="9dac5-136">**RasGetConnectStatus**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)

[<span data-ttu-id="9dac5-137">**расжеткаунтринфо**</span><span class="sxs-lookup"><span data-stu-id="9dac5-137">**RasGetCountryInfo**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa)

[<span data-ttu-id="9dac5-138">**расжеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-138">**RasGetCredentials**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa)

[<span data-ttu-id="9dac5-139">**расжеткустомаусдата**</span><span class="sxs-lookup"><span data-stu-id="9dac5-139">**RasGetCustomAuthData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcustomauthdataa)

[<span data-ttu-id="9dac5-140">**расжетеапусердата**</span><span class="sxs-lookup"><span data-stu-id="9dac5-140">**RasGetEapUserData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeteapuserdataa)

[<span data-ttu-id="9dac5-141">**расжетеапусеридентити**</span><span class="sxs-lookup"><span data-stu-id="9dac5-141">**RasGetEapUserIdentity**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeteapuseridentitya)

[<span data-ttu-id="9dac5-142">**расжетентридиалпарамс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-142">**RasGetEntryDialParams**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa)

[<span data-ttu-id="9dac5-143">**расжетентрипропертиес**</span><span class="sxs-lookup"><span data-stu-id="9dac5-143">**RasGetEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa)

[<span data-ttu-id="9dac5-144">**расжетеррорстринг**</span><span class="sxs-lookup"><span data-stu-id="9dac5-144">**RasGetErrorString**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)

[<span data-ttu-id="9dac5-145">**расжетлинкстатистикс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-145">**RasGetLinkStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetlinkstatistics)

[<span data-ttu-id="9dac5-146">**расжетнапстатус**</span><span class="sxs-lookup"><span data-stu-id="9dac5-146">**RasGetNapStatus**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetnapstatus)

<span data-ttu-id="9dac5-147">[**расжетпрожектионинфо**](/previous-versions/windows/embedded/ms897107(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9dac5-147">[**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10))</span></span>

[<span data-ttu-id="9dac5-148">**расжетпрожектионинфоекс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-148">**RasGetProjectionInfoEx**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetprojectioninfoex)

<span data-ttu-id="9dac5-149">[**расжеткуарантинеконнектионид**](/previous-versions/windows/desktop/legacy/aa377552(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9dac5-149">[**RasGetQuarantineConnectionId**](/previous-versions/windows/desktop/legacy/aa377552(v=vs.85))</span></span>

[<span data-ttu-id="9dac5-150">**расжетсубентрихандле**</span><span class="sxs-lookup"><span data-stu-id="9dac5-150">**RasGetSubEntryHandle**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea)

[<span data-ttu-id="9dac5-151">**расжетсубентрипропертиес**</span><span class="sxs-lookup"><span data-stu-id="9dac5-151">**RasGetSubEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa)

[<span data-ttu-id="9dac5-152">**рашангуп**</span><span class="sxs-lookup"><span data-stu-id="9dac5-152">**RasHangUp**</span></span>](/windows/desktop/api/Ras/nf-ras-rashangupa)

[<span data-ttu-id="9dac5-153">**расинвокиапуи**</span><span class="sxs-lookup"><span data-stu-id="9dac5-153">**RasInvokeEapUI**</span></span>](/windows/desktop/api/Ras/nf-ras-rasinvokeeapui)

<span data-ttu-id="9dac5-154">[**расмонитордлг**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9dac5-154">[**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85))</span></span>

[<span data-ttu-id="9dac5-155">**распбдлгфунк**</span><span class="sxs-lookup"><span data-stu-id="9dac5-155">**RasPBDlgFunc**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca)

[<span data-ttu-id="9dac5-156">**расфонебукдлг**</span><span class="sxs-lookup"><span data-stu-id="9dac5-156">**RasPhonebookDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga)

[<span data-ttu-id="9dac5-157">**расренаминтри**</span><span class="sxs-lookup"><span data-stu-id="9dac5-157">**RasRenameEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasrenameentrya)

[<span data-ttu-id="9dac5-158">**рассетаутодиаладдресс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-158">**RasSetAutodialAddress**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa)

[<span data-ttu-id="9dac5-159">**рассетаутодиаленабле**</span><span class="sxs-lookup"><span data-stu-id="9dac5-159">**RasSetAutodialEnable**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea)

[<span data-ttu-id="9dac5-160">**рассетаутодиалпарам**</span><span class="sxs-lookup"><span data-stu-id="9dac5-160">**RasSetAutodialParam**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialparama)

[<span data-ttu-id="9dac5-161">**рассеткоммсеттингс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-161">**RasSetCommSettings**</span></span>](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings)

[<span data-ttu-id="9dac5-162">**рассеткредентиалс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-162">**RasSetCredentials**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa)

[<span data-ttu-id="9dac5-163">**рассеткустомаусдата**</span><span class="sxs-lookup"><span data-stu-id="9dac5-163">**RasSetCustomAuthData**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetcustomauthdataa)

[<span data-ttu-id="9dac5-164">**рассетеапусердата**</span><span class="sxs-lookup"><span data-stu-id="9dac5-164">**RasSetEapUserData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasseteapuserdataa)

[<span data-ttu-id="9dac5-165">**рассетентридиалпарамс**</span><span class="sxs-lookup"><span data-stu-id="9dac5-165">**RasSetEntryDialParams**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa)

[<span data-ttu-id="9dac5-166">**рассетентрипропертиес**</span><span class="sxs-lookup"><span data-stu-id="9dac5-166">**RasSetEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa)

[<span data-ttu-id="9dac5-167">**рассетсубентрипропертиес**</span><span class="sxs-lookup"><span data-stu-id="9dac5-167">**RasSetSubEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa)

[<span data-ttu-id="9dac5-168">**расупдатеконнектион**</span><span class="sxs-lookup"><span data-stu-id="9dac5-168">**RasUpdateConnection**</span></span>](/windows/desktop/api/Ras/nf-ras-rasupdateconnection)

[<span data-ttu-id="9dac5-169">**расвалидатинтринаме**</span><span class="sxs-lookup"><span data-stu-id="9dac5-169">**RasValidateEntryName**</span></span>](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea)

[<span data-ttu-id="9dac5-170">Функции DLL пользовательских скриптов для RAS</span><span class="sxs-lookup"><span data-stu-id="9dac5-170">RAS Custom Scripting DLL Functions</span></span>](ras-custom-scripting-dll-functions.md)

 

 