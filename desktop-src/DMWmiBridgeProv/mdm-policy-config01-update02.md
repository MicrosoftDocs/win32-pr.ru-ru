---
title: Класс MDM_Policy_Config01_Update02
description: '\_Класс политики MDM \_ Config01 \_ Update02 представляет доступные политики обновления.'
ms.assetid: 7324912c-7ac5-42fd-baee-f7e2d81de023
keywords:
- Класс MDM_Policy_Config01_Update02
- MDM_Policy_Config01_Update02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Update02
- MDM_Policy_Config01_Update02.InstanceID
- MDM_Policy_Config01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3044fc527fd23d49fac383dc25778d3a978b2788
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490809"
---
# <a name="mdm_policy_config01_update02-class"></a><span data-ttu-id="9d52a-105">\_Класс политики MDM \_ Config01 \_ Update02</span><span class="sxs-lookup"><span data-stu-id="9d52a-105">MDM\_Policy\_Config01\_Update02 class</span></span>

<span data-ttu-id="9d52a-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="9d52a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9d52a-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="9d52a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9d52a-108">Класс **\_ политики MDM \_ Config01 \_ Update02** представляет доступные политики обновления.</span><span class="sxs-lookup"><span data-stu-id="9d52a-108">The **MDM\_Policy\_Config01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="9d52a-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9d52a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d52a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d52a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a><span data-ttu-id="9d52a-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9d52a-111">Members</span></span>

<span data-ttu-id="9d52a-112">Класс **\_ политики MDM \_ Config01 \_ Update02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9d52a-112">The **MDM\_Policy\_Config01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="9d52a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d52a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d52a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9d52a-114">Properties</span></span>

<span data-ttu-id="9d52a-115">Класс **\_ политики MDM \_ Config01 \_ Update02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9d52a-115">The **MDM\_Policy\_Config01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9d52a-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="9d52a-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="9d52a-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="9d52a-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-125">алловаутаупдате</span><span class="sxs-lookup"><span data-stu-id="9d52a-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="9d52a-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="9d52a-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="9d52a-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="9d52a-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="9d52a-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="9d52a-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="9d52a-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="9d52a-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-152">деферфеатуреупдатеспериодиндайс</span><span class="sxs-lookup"><span data-stu-id="9d52a-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-155">деферкуалитюпдатеспериодиндайс</span><span class="sxs-lookup"><span data-stu-id="9d52a-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="9d52a-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="9d52a-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="9d52a-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="9d52a-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-168">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="9d52a-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="9d52a-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-174">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="9d52a-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-177">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-179">ексклудевудриверсинкуалитюпдате</span><span class="sxs-lookup"><span data-stu-id="9d52a-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-180">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="9d52a-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-183">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-185">игноремоаппдовнлоадлимит</span><span class="sxs-lookup"><span data-stu-id="9d52a-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-186">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-188">игноремаупдатедовнлоадлимит</span><span class="sxs-lookup"><span data-stu-id="9d52a-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-189">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d52a-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d52a-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d52a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d52a-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-194">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d52a-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d52a-195">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="9d52a-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="9d52a-196">Для этого класса строка имеет значение "Update".</span><span class="sxs-lookup"><span data-stu-id="9d52a-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="9d52a-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="9d52a-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-198">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d52a-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9d52a-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d52a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9d52a-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-203">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9d52a-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9d52a-204">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="9d52a-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="9d52a-205">Для этого класса строка имеет значение "./вендор/мсфт/Полици/конфиг"</span><span class="sxs-lookup"><span data-stu-id="9d52a-205">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="9d52a-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="9d52a-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-207">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="9d52a-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-210">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="9d52a-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d52a-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="9d52a-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-216">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="9d52a-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d52a-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="9d52a-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-222">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="9d52a-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-225">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="9d52a-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-228">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="9d52a-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-231">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="9d52a-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-234">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="9d52a-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-237">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="9d52a-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-240">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-241">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="9d52a-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-243">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="9d52a-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-246">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="9d52a-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-249">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="9d52a-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-252">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="9d52a-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-255">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="9d52a-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-258">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-259">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="9d52a-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-261">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="9d52a-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-263">упдатесервицеурл</span><span class="sxs-lookup"><span data-stu-id="9d52a-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d52a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9d52a-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="9d52a-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d52a-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9d52a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d52a-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="9d52a-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d52a-269">Требования</span><span class="sxs-lookup"><span data-stu-id="9d52a-269">Requirements</span></span>



| <span data-ttu-id="9d52a-270">Требование</span><span class="sxs-lookup"><span data-stu-id="9d52a-270">Requirement</span></span> | <span data-ttu-id="9d52a-271">Значение</span><span class="sxs-lookup"><span data-stu-id="9d52a-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d52a-272">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d52a-272">Minimum supported client</span></span><br/> | <span data-ttu-id="9d52a-273">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9d52a-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d52a-274">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d52a-274">Minimum supported server</span></span><br/> | <span data-ttu-id="9d52a-275">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9d52a-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9d52a-276">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d52a-276">Namespace</span></span><br/>                | <span data-ttu-id="9d52a-277">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="9d52a-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="9d52a-278">MOF</span><span class="sxs-lookup"><span data-stu-id="9d52a-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d52a-279"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d52a-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d52a-280">DLL</span><span class="sxs-lookup"><span data-stu-id="9d52a-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d52a-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d52a-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d52a-282">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d52a-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d52a-283">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="9d52a-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

