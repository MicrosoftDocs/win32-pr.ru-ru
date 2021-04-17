---
description: Указывает на высокую, среднюю или низкую производительность устройства, на котором работает устаревшая ОС.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Перечисление Упдатеимпактлевел
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662539"
---
# <a name="updateimpactlevel-enumeration"></a><span data-ttu-id="8b49c-103">Перечисление Упдатеимпактлевел</span><span class="sxs-lookup"><span data-stu-id="8b49c-103">UpdateImpactLevel enumeration</span></span>

<span data-ttu-id="8b49c-104">Указывает на высокую, среднюю или низкую производительность устройства, на котором работает устаревшая ОС.</span><span class="sxs-lookup"><span data-stu-id="8b49c-104">Indicates a high, medium, or low impact of a device running an out-of-date OS.</span></span> <span data-ttu-id="8b49c-105">Это перечисление обычно используется структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , которые, в свою очередь, вложены в возвращенный [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) из [**жетосупдатеассессмент**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span><span class="sxs-lookup"><span data-stu-id="8b49c-105">This enumeration is generally used by [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures, which is in turn nested inside the returned [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) from [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b49c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b49c-106">Syntax</span></span>


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a><span data-ttu-id="8b49c-107">Константы</span><span class="sxs-lookup"><span data-stu-id="8b49c-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8b49c-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**Упдатеимпактлевел \_ Нет**</span><span class="sxs-lookup"><span data-stu-id="8b49c-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span> **UpdateImpactLevel\_None**</span></span>
</dt> <dd>

<span data-ttu-id="8b49c-109">На ваше устройство не влияет ожидаемое воздействие.</span><span class="sxs-lookup"><span data-stu-id="8b49c-109">There is no foreseeable impact to your device.</span></span> <span data-ttu-id="8b49c-110">Это может быть вызвано тем, что устройство является актуальным или не является актуальным, так как оно учитывает Центр обновления Windows для периодов отсрочки бизнеса или устарело, но еще не достигло порогового значения **дайсаутофдате** , чтобы достичь более высокого уровня влияния.</span><span class="sxs-lookup"><span data-stu-id="8b49c-110">This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the **daysOutOfDate** threshold to reach a higher impact level.</span></span>

</dd> <dt>

<span data-ttu-id="8b49c-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**Упдатеимпактлевел \_ низкий**</span><span class="sxs-lookup"><span data-stu-id="8b49c-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel\_Low**</span></span>
</dt> <dd>

<span data-ttu-id="8b49c-112">На устройстве не установлена последняя версия ОС, но имеется Последнее обновление.</span><span class="sxs-lookup"><span data-stu-id="8b49c-112">The device is not running the latest OS, but has a recent update.</span></span>

</dd> <dt>

<span data-ttu-id="8b49c-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**Упдатеимпактлевел \_ Средний уровень**</span><span class="sxs-lookup"><span data-stu-id="8b49c-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span> **UpdateImpactLevel\_Medium**</span></span>
</dt> <dd>

<span data-ttu-id="8b49c-114">Устройство работает под управлением последней ОС, но имеет умеренное Последнее обновление.</span><span class="sxs-lookup"><span data-stu-id="8b49c-114">The device is running the latest OS, but has a moderately recent update.</span></span>

</dd> <dt>

<span data-ttu-id="8b49c-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**Упдатеимпактлевел \_ высокий**</span><span class="sxs-lookup"><span data-stu-id="8b49c-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel\_High**</span></span>
</dt> <dd>

<span data-ttu-id="8b49c-116">Устройство устарело в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="8b49c-116">The device has been out-of-date for a long time.</span></span> <span data-ttu-id="8b49c-117">На этом устройстве могут быть уязвимости системы безопасности, и в них могут отсутствовать важные исправления, которые делают Windows более эффективной.</span><span class="sxs-lookup"><span data-stu-id="8b49c-117">This device may have security vulnerabilities and may be missing important fixes that make Windows run better.</span></span> <span data-ttu-id="8b49c-118">Если устройство работает под управлением версии Windows, которая больше не поддерживается, всегда возвращается **упдатеимпактлевел \_ High** .</span><span class="sxs-lookup"><span data-stu-id="8b49c-118">When a device is running a version of Windows that is no longer supported, **UpdateImpactLevel\_High** is always returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b49c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b49c-119">Remarks</span></span>

<span data-ttu-id="8b49c-120">При вызове [**жетосупдатеассессмент**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) возвращается структура [**осупдатеассессмент**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) .</span><span class="sxs-lookup"><span data-stu-id="8b49c-120">When [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) is called, an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structure is returned.</span></span> <span data-ttu-id="8b49c-121">В структуре есть **ассессментфоркуррент** и **ассессментфоруптодате**.</span><span class="sxs-lookup"><span data-stu-id="8b49c-121">Within the structure there is an **assessmentForCurrent** and **assessmentForUpToDate**.</span></span> <span data-ttu-id="8b49c-122">Оба из них являются структурами [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) .</span><span class="sxs-lookup"><span data-stu-id="8b49c-122">Both of these are [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures.</span></span> <span data-ttu-id="8b49c-123">Оба члена имеют перечисление **упдатеимпактлевел** , которое указывает на высокий, средний, низкий или не оказывает влияния на устройство с устаревшей ОС.</span><span class="sxs-lookup"><span data-stu-id="8b49c-123">Both members have an **UpdateImpactLevel** enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS.</span></span> <span data-ttu-id="8b49c-124">Эти уровни определяются значением **дайсаутофдате**.</span><span class="sxs-lookup"><span data-stu-id="8b49c-124">The These levels are determined by the value of **daysOutOfDate**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b49c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8b49c-125">Requirements</span></span>



| <span data-ttu-id="8b49c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8b49c-126">Requirement</span></span> | <span data-ttu-id="8b49c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8b49c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b49c-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b49c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8b49c-129">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="8b49c-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8b49c-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b49c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8b49c-131">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="8b49c-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8b49c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="8b49c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b49c-133"><dt>Ваасапи. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b49c-133"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




