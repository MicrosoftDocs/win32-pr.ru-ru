---
title: Класс MDM_Policy_Result01_Update02
description: '\_Класс политики MDM \_ Result01 \_ Update02 представляет доступные политики обновления.'
ms.assetid: 06604da6-5298-4273-a030-529491c2823c
keywords:
- Класс MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02 класс, описание
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02.InstanceID
- MDM_Policy_Result01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0be844bb4ef8fc20e7ab5bbc8b7709cdfde4034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988231"
---
# <a name="mdm_policy_result01_update02-class"></a><span data-ttu-id="ed3b7-105">\_Класс политики MDM \_ Result01 \_ Update02</span><span class="sxs-lookup"><span data-stu-id="ed3b7-105">MDM\_Policy\_Result01\_Update02 class</span></span>

<span data-ttu-id="ed3b7-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="ed3b7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ed3b7-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="ed3b7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ed3b7-108">Класс **\_ политики MDM \_ Result01 \_ Update02** представляет доступные политики обновления.</span><span class="sxs-lookup"><span data-stu-id="ed3b7-108">The **MDM\_Policy\_Result01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="ed3b7-109">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ed3b7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3b7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed3b7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Update02
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

## <a name="members"></a><span data-ttu-id="ed3b7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="ed3b7-111">Members</span></span>

<span data-ttu-id="ed3b7-112">Класс **\_ политики MDM \_ Result01 \_ Update02** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ed3b7-112">The **MDM\_Policy\_Result01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="ed3b7-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed3b7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed3b7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed3b7-114">Properties</span></span>

<span data-ttu-id="ed3b7-115">Класс **\_ политики MDM \_ Result01 \_ Update02** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ed3b7-115">The **MDM\_Policy\_Result01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ed3b7-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="ed3b7-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-117">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="ed3b7-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-120">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="ed3b7-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-123">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-125">алловаутаупдате</span><span class="sxs-lookup"><span data-stu-id="ed3b7-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-126">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="ed3b7-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="ed3b7-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-132">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="ed3b7-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-135">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="ed3b7-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-138">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ed3b7-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-141">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="ed3b7-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-144">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="ed3b7-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-147">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="ed3b7-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-150">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-151">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-152">деферфеатуреупдатеспериодиндайс</span><span class="sxs-lookup"><span data-stu-id="ed3b7-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-155">деферкуалитюпдатеспериодиндайс</span><span class="sxs-lookup"><span data-stu-id="ed3b7-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-156">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="ed3b7-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-159">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="ed3b7-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-162">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="ed3b7-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-165">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="ed3b7-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-168">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="ed3b7-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-171">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-172">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="ed3b7-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-174">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="ed3b7-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-177">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-179">ексклудевудриверсинкуалитюпдате</span><span class="sxs-lookup"><span data-stu-id="ed3b7-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-180">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="ed3b7-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-183">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-185">игноремоаппдовнлоадлимит</span><span class="sxs-lookup"><span data-stu-id="ed3b7-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-186">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-188">игноремаупдатедовнлоадлимит</span><span class="sxs-lookup"><span data-stu-id="ed3b7-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-189">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed3b7-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3b7-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-194">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed3b7-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed3b7-195">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="ed3b7-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="ed3b7-196">Для этого класса строка имеет значение "Update".</span><span class="sxs-lookup"><span data-stu-id="ed3b7-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="ed3b7-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="ed3b7-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-198">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ed3b7-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed3b7-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-203">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed3b7-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed3b7-204">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="ed3b7-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="ed3b7-205">Для этого класса строка имеет значение "./вендор/мсфт/Полици/ресулт"</span><span class="sxs-lookup"><span data-stu-id="ed3b7-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="ed3b7-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="ed3b7-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-207">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-208">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="ed3b7-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-210">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="ed3b7-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="ed3b7-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-216">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-217">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="ed3b7-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="ed3b7-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-222">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="ed3b7-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-225">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="ed3b7-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-228">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-229">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="ed3b7-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-231">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-232">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="ed3b7-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-234">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-235">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="ed3b7-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-237">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="ed3b7-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-240">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-241">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="ed3b7-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-243">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="ed3b7-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-246">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="ed3b7-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-249">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-250">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="ed3b7-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-252">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="ed3b7-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-255">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="ed3b7-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-258">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-259">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="ed3b7-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-261">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-263">упдатесервицеурл</span><span class="sxs-lookup"><span data-stu-id="ed3b7-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-264">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ed3b7-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="ed3b7-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed3b7-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed3b7-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed3b7-268">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ed3b7-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed3b7-269">Требования</span><span class="sxs-lookup"><span data-stu-id="ed3b7-269">Requirements</span></span>



| <span data-ttu-id="ed3b7-270">Требование</span><span class="sxs-lookup"><span data-stu-id="ed3b7-270">Requirement</span></span> | <span data-ttu-id="ed3b7-271">Значение</span><span class="sxs-lookup"><span data-stu-id="ed3b7-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3b7-272">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed3b7-272">Minimum supported client</span></span><br/> | <span data-ttu-id="ed3b7-273">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="ed3b7-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed3b7-274">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed3b7-274">Minimum supported server</span></span><br/> | <span data-ttu-id="ed3b7-275">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ed3b7-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ed3b7-276">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ed3b7-276">Namespace</span></span><br/>                | <span data-ttu-id="ed3b7-277">Корневой \\ CIMv2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="ed3b7-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="ed3b7-278">MOF</span><span class="sxs-lookup"><span data-stu-id="ed3b7-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed3b7-279"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed3b7-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed3b7-280">DLL</span><span class="sxs-lookup"><span data-stu-id="ed3b7-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed3b7-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed3b7-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed3b7-282">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed3b7-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3b7-283">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="ed3b7-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

