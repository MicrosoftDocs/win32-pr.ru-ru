---
title: Класс MDM_Policy_Result01_Defender02
description: Политика MDM \_ \_ Result01 \_ Defender02class представляет политики, связанные с защитником Windows.
ms.assetid: 82c8a7a2-8369-46c4-aa87-b44b742a274d
keywords:
- Класс MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02.InstanceID
- MDM_Policy_Result01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae898751a9f15af1c945efd3e6a473dfe07c7cd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489783"
---
# <a name="mdm_policy_result01_defender02-class"></a><span data-ttu-id="0c3a1-105">\_Класс политики MDM \_ Result01 \_ Defender02</span><span class="sxs-lookup"><span data-stu-id="0c3a1-105">MDM\_Policy\_Result01\_Defender02 class</span></span>

<span data-ttu-id="0c3a1-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0c3a1-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="0c3a1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0c3a1-108">Класс **\_ политики MDM \_ Result01 \_ Defender02** представляет политики, связанные с защитником Windows.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-108">The **MDM\_Policy\_Result01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="0c3a1-109">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3a1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c3a1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Defender02
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
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
  sint32 ScanParameter;
};
```

## <a name="members"></a><span data-ttu-id="0c3a1-111">Члены</span><span class="sxs-lookup"><span data-stu-id="0c3a1-111">Members</span></span>

<span data-ttu-id="0c3a1-112">Класс **\_ политики MDM \_ Result01 \_ Defender02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0c3a1-112">The **MDM\_Policy\_Result01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="0c3a1-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c3a1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c3a1-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c3a1-114">Properties</span></span>

<span data-ttu-id="0c3a1-115">Класс **\_ политики MDM \_ Result01 \_ Defender02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-115">The **MDM\_Policy\_Result01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0c3a1-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="0c3a1-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="0c3a1-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="0c3a1-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="0c3a1-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="0c3a1-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="0c3a1-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="0c3a1-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="0c3a1-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="0c3a1-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="0c3a1-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="0c3a1-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="0c3a1-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="0c3a1-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-155">аттакксурфацередуктиононлексклусионс</span><span class="sxs-lookup"><span data-stu-id="0c3a1-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-158">аттакксурфацередуктионрулес</span><span class="sxs-lookup"><span data-stu-id="0c3a1-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="0c3a1-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-164">клаудблокклевел</span><span class="sxs-lookup"><span data-stu-id="0c3a1-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-167">клаудекстендедтимеаут</span><span class="sxs-lookup"><span data-stu-id="0c3a1-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-168">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-170">контролледфолдеракцессалловедаппликатионс</span><span class="sxs-lookup"><span data-stu-id="0c3a1-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-171">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-173">контролледфолдеракцесспротектедфолдерс</span><span class="sxs-lookup"><span data-stu-id="0c3a1-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="0c3a1-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-177">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-179">енаблеконтролледфолдеракцесс</span><span class="sxs-lookup"><span data-stu-id="0c3a1-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-180">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-182">енабленетворкпротектион</span><span class="sxs-lookup"><span data-stu-id="0c3a1-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-183">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="0c3a1-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="0c3a1-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="0c3a1-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-193">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c3a1-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c3a1-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-197">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0c3a1-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0c3a1-198">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="0c3a1-199">Для этого класса строка имеет значение "защитник".</span><span class="sxs-lookup"><span data-stu-id="0c3a1-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="0c3a1-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c3a1-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-203">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0c3a1-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0c3a1-204">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="0c3a1-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="0c3a1-205">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="0c3a1-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="0c3a1-206">пуапротектион</span><span class="sxs-lookup"><span data-stu-id="0c3a1-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-207">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="0c3a1-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-210">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="0c3a1-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-213">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="0c3a1-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-216">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="0c3a1-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-219">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="0c3a1-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-222">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="0c3a1-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-225">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="0c3a1-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-228">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c3a1-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="0c3a1-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3a1-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0c3a1-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3a1-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0c3a1-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c3a1-233">Требования</span><span class="sxs-lookup"><span data-stu-id="0c3a1-233">Requirements</span></span>



| <span data-ttu-id="0c3a1-234">Требование</span><span class="sxs-lookup"><span data-stu-id="0c3a1-234">Requirement</span></span> | <span data-ttu-id="0c3a1-235">Значение</span><span class="sxs-lookup"><span data-stu-id="0c3a1-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3a1-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c3a1-236">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3a1-237">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0c3a1-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c3a1-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c3a1-238">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3a1-239">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c3a1-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0c3a1-240">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0c3a1-240">Namespace</span></span><br/>                | <span data-ttu-id="0c3a1-241">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="0c3a1-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="0c3a1-242">MOF</span><span class="sxs-lookup"><span data-stu-id="0c3a1-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c3a1-243"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c3a1-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c3a1-244">DLL</span><span class="sxs-lookup"><span data-stu-id="0c3a1-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c3a1-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c3a1-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c3a1-246">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c3a1-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c3a1-247">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="0c3a1-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

