---
title: Класс MDM_Policy_Config01_Defender02
description: Политика MDM \_ \_ Config01 \_ Defender02class представляет политики, связанные с защитником Windows.
ms.assetid: 6d9d4edd-fcb6-45ea-bc5d-1bffb9cf8740
keywords:
- Класс MDM_Policy_Config01_Defender02
- MDM_Policy_Config01_Defender02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Defender02
- MDM_Policy_Config01_Defender02.InstanceID
- MDM_Policy_Config01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b184008fc0ce7fc44dcb7106ceec3abc0e91450d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489909"
---
# <a name="mdm_policy_config01_defender02-class"></a><span data-ttu-id="8628e-105">\_Класс политики MDM \_ Config01 \_ Defender02</span><span class="sxs-lookup"><span data-stu-id="8628e-105">MDM\_Policy\_Config01\_Defender02 class</span></span>

<span data-ttu-id="8628e-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="8628e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8628e-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="8628e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8628e-108">Класс **\_ политики MDM \_ Config01 \_ Defender02** представляет политики, связанные с защитником Windows.</span><span class="sxs-lookup"><span data-stu-id="8628e-108">The **MDM\_Policy\_Config01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="8628e-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="8628e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8628e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8628e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScanParameter;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
};
```

## <a name="members"></a><span data-ttu-id="8628e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="8628e-111">Members</span></span>

<span data-ttu-id="8628e-112">Класс **\_ политики MDM \_ Config01 \_ Defender02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8628e-112">The **MDM\_Policy\_Config01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="8628e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8628e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8628e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="8628e-114">Properties</span></span>

<span data-ttu-id="8628e-115">Класс **\_ политики MDM \_ Config01 \_ Defender02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8628e-115">The **MDM\_Policy\_Config01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8628e-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="8628e-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="8628e-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="8628e-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="8628e-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="8628e-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="8628e-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="8628e-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="8628e-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="8628e-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="8628e-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="8628e-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="8628e-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="8628e-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-155">аттакксурфацередуктиононлексклусионс</span><span class="sxs-lookup"><span data-stu-id="8628e-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-158">аттакксурфацередуктионрулес</span><span class="sxs-lookup"><span data-stu-id="8628e-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="8628e-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-164">клаудблокклевел</span><span class="sxs-lookup"><span data-stu-id="8628e-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-167">клаудекстендедтимеаут</span><span class="sxs-lookup"><span data-stu-id="8628e-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-168">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-170">контролледфолдеракцессалловедаппликатионс</span><span class="sxs-lookup"><span data-stu-id="8628e-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-173">контролледфолдеракцесспротектедфолдерс</span><span class="sxs-lookup"><span data-stu-id="8628e-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="8628e-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-177">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-179">енаблеконтролледфолдеракцесс</span><span class="sxs-lookup"><span data-stu-id="8628e-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-180">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-182">енабленетворкпротектион</span><span class="sxs-lookup"><span data-stu-id="8628e-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-183">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="8628e-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="8628e-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="8628e-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8628e-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8628e-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8628e-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8628e-197">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8628e-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8628e-198">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="8628e-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="8628e-199">Для этого класса строка имеет значение "защитник".</span><span class="sxs-lookup"><span data-stu-id="8628e-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="8628e-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8628e-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8628e-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8628e-203">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8628e-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8628e-204">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="8628e-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="8628e-205">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="8628e-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="8628e-206">пуапротектион</span><span class="sxs-lookup"><span data-stu-id="8628e-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-207">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="8628e-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-210">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="8628e-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-213">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="8628e-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-216">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="8628e-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-219">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="8628e-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-222">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="8628e-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-225">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="8628e-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-228">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="8628e-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8628e-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="8628e-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8628e-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8628e-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8628e-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8628e-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8628e-233">Требования</span><span class="sxs-lookup"><span data-stu-id="8628e-233">Requirements</span></span>



| <span data-ttu-id="8628e-234">Требование</span><span class="sxs-lookup"><span data-stu-id="8628e-234">Requirement</span></span> | <span data-ttu-id="8628e-235">Значение</span><span class="sxs-lookup"><span data-stu-id="8628e-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8628e-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8628e-236">Minimum supported client</span></span><br/> | <span data-ttu-id="8628e-237">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8628e-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8628e-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8628e-238">Minimum supported server</span></span><br/> | <span data-ttu-id="8628e-239">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8628e-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8628e-240">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8628e-240">Namespace</span></span><br/>                | <span data-ttu-id="8628e-241">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="8628e-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8628e-242">MOF</span><span class="sxs-lookup"><span data-stu-id="8628e-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8628e-243"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8628e-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8628e-244">DLL</span><span class="sxs-lookup"><span data-stu-id="8628e-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8628e-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8628e-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8628e-246">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8628e-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8628e-247">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="8628e-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

