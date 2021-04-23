---
description: Описание обновления операционной системы на устройстве.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Перечисление Упдатеассессментстатус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662540"
---
# <a name="updateassessmentstatus-enumeration"></a><span data-ttu-id="1b145-103">Перечисление Упдатеассессментстатус</span><span class="sxs-lookup"><span data-stu-id="1b145-103">UpdateAssessmentStatus enumeration</span></span>

<span data-ttu-id="1b145-104">Описание обновления операционной системы на устройстве.</span><span class="sxs-lookup"><span data-stu-id="1b145-104">Describes how up-to-date the OS on a device is.</span></span> <span data-ttu-id="1b145-105">**Упдатеассессментстатус** используется структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) и [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) в членах **ассессментфоркуррент**, **ассессментфоруптодате** и **securityStatus** .</span><span class="sxs-lookup"><span data-stu-id="1b145-105">**UpdateAssessmentStatus** is used by the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, in the **assessmentForCurrent**, **assessmentForUpToDate**, and **securityStatus** members.</span></span> <span data-ttu-id="1b145-106">Возвращается ровно одна константа.</span><span class="sxs-lookup"><span data-stu-id="1b145-106">Exactly one constant is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b145-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b145-107">Syntax</span></span>


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a><span data-ttu-id="1b145-108">Константы</span><span class="sxs-lookup"><span data-stu-id="1b145-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1b145-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**Упдатеассессментстатус \_ Последняя версия**</span><span class="sxs-lookup"><span data-stu-id="1b145-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span> **UpdateAssessmentStatus\_Latest**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-110">Этот результат в **ассессментфоркуррент** означает, что устройство находится в последней версии обновления компонентов и качества, доступном для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="1b145-110">This result within **assessmentForCurrent** implies that the device is on the latest feature update and quality update available for that device.</span></span> <span data-ttu-id="1b145-111">В **ассессментфоруптодате** этот результат означает, что устройство находится в последнем обновлении для выпуска Windows, на котором он работает.</span><span class="sxs-lookup"><span data-stu-id="1b145-111">Within **assessmentForUpToDate**, this result implies that the device is on the latest quality update for the release of Windows it is running.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**Упдатеассессментстатус \_ Нотлатестсофтрестриктион**</span><span class="sxs-lookup"><span data-stu-id="1b145-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestSoftRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-113">Последнее обновление компонента не было установлено из-за необратимого ограничения.</span><span class="sxs-lookup"><span data-stu-id="1b145-113">The latest feature update has not been installed due to a soft restriction.</span></span> <span data-ttu-id="1b145-114">Если в обновление было включено мягкое ограничение, обновление не будет установлено автоматически. пользователь должен самостоятельно инициировать скачивание в рамках обновления.</span><span class="sxs-lookup"><span data-stu-id="1b145-114">When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX.</span></span> <span data-ttu-id="1b145-115">Это состояние применяется только к **ассессментфоркуррент**.</span><span class="sxs-lookup"><span data-stu-id="1b145-115">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**Упдатеассессментстатус \_ Нотлатессардрестриктион**</span><span class="sxs-lookup"><span data-stu-id="1b145-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestHardRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-117">Последнее обновление компонента не было установлено в связи с жестким ограничением.</span><span class="sxs-lookup"><span data-stu-id="1b145-117">The latest feature update has not been installed due to a hard restriction.</span></span> <span data-ttu-id="1b145-118">Если в обновление было размещено жесткое ограничение, обновление не применяется к устройству.</span><span class="sxs-lookup"><span data-stu-id="1b145-118">When a hard restriction has been placed on an update, the update is not applicable to the device.</span></span> <span data-ttu-id="1b145-119">Это состояние применяется только к **ассессментфоркуррент**.</span><span class="sxs-lookup"><span data-stu-id="1b145-119">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**Упдатеассессментстатус \_ Нотлатестендофсуппорт**</span><span class="sxs-lookup"><span data-stu-id="1b145-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span> **UpdateAssessmentStatus\_NotLatestEndOfSupport**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-121">Устройство не находится в последнем обновлении, так как обновление компонентов устройства больше не поддерживается корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="1b145-121">The device is not on the latest update because the device's feature update is no longer supported by Microsoft.</span></span> <span data-ttu-id="1b145-122">Когда корпорация Майкрософт прекращает поддержку выпуска компонентов, это состояние будет возвращено как для **ассессментфоркуррент** , так и для **ассессментфоруптодате**.</span><span class="sxs-lookup"><span data-stu-id="1b145-122">When Microsoft stops supporting a feature release, this status will be returned for both **assessmentForCurrent** and **assessmentForUpToDate**.</span></span>

> [!Note]  
> <span data-ttu-id="1b145-123">Когда возвращается **упдатеассессментстатус \_ Нотлатестендофсуппорт** , **упдатеимпактлевел** оценки всегда имеет значение **\_ High упдатеимпактлевел**.</span><span class="sxs-lookup"><span data-stu-id="1b145-123">When **UpdateAssessmentStatus\_NotLatestEndOfSupport** is returned, the assessment's **UpdateImpactLevel** is always **UpdateImpactLevel\_High**.</span></span>

 

</dd> <dt>

<span data-ttu-id="1b145-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**Упдатеассессментстатус \_ НотлатестсервиЦингтраин**</span><span class="sxs-lookup"><span data-stu-id="1b145-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span> **UpdateAssessmentStatus\_NotLatestServicingTrain**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-125">Устройство не находится в новейшем обновлении компонентов, так как обслуживание устройства обработает ограничение на обновление до последнего обновления компонента.</span><span class="sxs-lookup"><span data-stu-id="1b145-125">The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update.</span></span> <span data-ttu-id="1b145-126">Например, если устройство находится на Current Branch for Business (CBB) и для Current Branch (CB) выпущено новое обновление, будет возвращено следующее.</span><span class="sxs-lookup"><span data-stu-id="1b145-126">For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned.</span></span> <span data-ttu-id="1b145-127">Это состояние применяется только к **ассессментфоркуррент**.</span><span class="sxs-lookup"><span data-stu-id="1b145-127">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**Упдатеассессментстатус \_ Нотлатестдеферредфеатуре**</span><span class="sxs-lookup"><span data-stu-id="1b145-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestDeferredFeature**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-129">Последнее обновление компонента не было установлено из-за политики отсрочки для обновления бизнес-компонентов на устройстве Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="1b145-129">The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy.</span></span> <span data-ttu-id="1b145-130">При определении **дайсаутофдате** учитываются политики отсрочки. **дайсаутофдате** не начнет увеличиваться до тех пор, пока не истечет период отсрочки.</span><span class="sxs-lookup"><span data-stu-id="1b145-130">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span> <span data-ttu-id="1b145-131">Это состояние применяется только к **ассессментфоркуррент**.</span><span class="sxs-lookup"><span data-stu-id="1b145-131">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**Упдатеассессментстатус \_ Нотлатестдеферредкуалити**</span><span class="sxs-lookup"><span data-stu-id="1b145-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestDeferredQuality**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-133">Это устройство не включено в Последнее обновление, так как для политики отсрочки обновления качества бизнеса на устройстве Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="1b145-133">The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.</span></span> <span data-ttu-id="1b145-134">При определении **дайсаутофдате** учитываются политики отсрочки. **дайсаутофдате** не начнет увеличиваться до тех пор, пока не истечет период отсрочки.</span><span class="sxs-lookup"><span data-stu-id="1b145-134">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**Упдатеассессментстатус \_ Нотлатестпауседфеатуре**</span><span class="sxs-lookup"><span data-stu-id="1b145-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestPausedFeature**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-136">Устройство не находится на последнем обновлении компонентов из-за приостановки обновления компонентов.</span><span class="sxs-lookup"><span data-stu-id="1b145-136">The device is not on the latest feature update due to the device having paused Feature Updates.</span></span> <span data-ttu-id="1b145-137">Является ли устройство приостановленным, не учитывается при вычислении **дайсаутофдате**.</span><span class="sxs-lookup"><span data-stu-id="1b145-137">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="1b145-138">Это состояние применяется только к **ассессментфоркуррент**.</span><span class="sxs-lookup"><span data-stu-id="1b145-138">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**Упдатеассессментстатус \_ Нотлатестпауседкуалити**</span><span class="sxs-lookup"><span data-stu-id="1b145-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestPausedQuality**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-140">Устройство не находится в последнем обновлении, так как оно приостановило обновление качества.</span><span class="sxs-lookup"><span data-stu-id="1b145-140">The device is not on the latest quality update due to the device having paused Quality Updates.</span></span> <span data-ttu-id="1b145-141">Является ли устройство приостановленным, не учитывается при вычислении **дайсаутофдате**.</span><span class="sxs-lookup"><span data-stu-id="1b145-141">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="1b145-142">**дайсаутофдате** не определяет, приостанавливается ли устройство к его вычислению.</span><span class="sxs-lookup"><span data-stu-id="1b145-142">**daysOutOfDate** does not factor whether a device is paused into its calculation.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**Упдатеассессментстатус \_ Нотлатестманажед**</span><span class="sxs-lookup"><span data-stu-id="1b145-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span> **UpdateAssessmentStatus\_NotLatestManaged**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-144">Устройство не находится в последнем обновлении, так как утверждение обновлений не выполняется с помощью Центр обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="1b145-144">The device is not on the latest update because the approval of updates is not done through Windows Update.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**Упдатеассессментстатус \_ Нотлатестункновн**</span><span class="sxs-lookup"><span data-stu-id="1b145-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span> **UpdateAssessmentStatus\_NotLatestUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-146">Устройство не находится в последнем обновлении из-за причины, которая не может быть определена оценкой.</span><span class="sxs-lookup"><span data-stu-id="1b145-146">The device is not on the latest update due to a reason that cannot be determined by the assessment.</span></span>

</dd> <dt>

<span data-ttu-id="1b145-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**Упдатеассессментстатус \_ Нотлатесттаржетедверсион**</span><span class="sxs-lookup"><span data-stu-id="1b145-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span> **UpdateAssessmentStatus\_NotLatestTargetedVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1b145-148">Устройство не находится в последнем обновлении компонентов из-за политики Центр обновления Windows на устройстве для целевой версии.</span><span class="sxs-lookup"><span data-stu-id="1b145-148">The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy.</span></span> <span data-ttu-id="1b145-149">Эта политика позволяет сохранить устройство в целевой версии выпуска.</span><span class="sxs-lookup"><span data-stu-id="1b145-149">This policy is keeping the device on the targeted feature release version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b145-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b145-150">Remarks</span></span>

<span data-ttu-id="1b145-151">Это перечисление чаще всего используется с структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) и [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , которые, в свою очередь, используются с методом [**жетосупдатеассессмент**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) для [**иваасассессор**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span><span class="sxs-lookup"><span data-stu-id="1b145-151">This enumeration is used most often with the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, which are in turn used with the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method for [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b145-152">Требования</span><span class="sxs-lookup"><span data-stu-id="1b145-152">Requirements</span></span>



| <span data-ttu-id="1b145-153">Требование</span><span class="sxs-lookup"><span data-stu-id="1b145-153">Requirement</span></span> | <span data-ttu-id="1b145-154">Значение</span><span class="sxs-lookup"><span data-stu-id="1b145-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b145-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1b145-155">Minimum supported client</span></span><br/> | <span data-ttu-id="1b145-156">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="1b145-156">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1b145-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1b145-157">Minimum supported server</span></span><br/> | <span data-ttu-id="1b145-158">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="1b145-158">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1b145-159">IDL</span><span class="sxs-lookup"><span data-stu-id="1b145-159">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b145-160"><dt>Ваасапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b145-160"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




