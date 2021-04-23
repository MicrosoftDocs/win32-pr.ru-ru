---
title: Структура DRM_LICENSE_STATE_DATA (Дрмекстерналс. h)
description: '\_ \_ Структура данных о состоянии лицензии DRM \_ содержит сведения о лицензиях для указанного права на использование DRM.'
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- Формат DRM_LICENSE_STATE_DATA структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701067"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a><span data-ttu-id="a719a-105">Структура DRM_LICENSE_STATE_DATA (Дрмекстерналс. h)</span><span class="sxs-lookup"><span data-stu-id="a719a-105">DRM_LICENSE_STATE_DATA structure (Drmexternals.h)</span></span>

<span data-ttu-id="a719a-106">Структура **\_ данных о \_ состоянии \_ лицензии DRM** содержит сведения о [*лицензиях*](wmformat-glossary.md) для указанного права на использование [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="a719a-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains [*license*](wmformat-glossary.md) information about a specified [*DRM*](wmformat-glossary.md) right.</span></span>

## <a name="syntax"></a><span data-ttu-id="a719a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a719a-107">Syntax</span></span>


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a><span data-ttu-id="a719a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a719a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a719a-109">**двстреамид**</span><span class="sxs-lookup"><span data-stu-id="a719a-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="a719a-110">Номер потока, к которому применяется лицензия.</span><span class="sxs-lookup"><span data-stu-id="a719a-110">Stream number to which the license applies.</span></span> <span data-ttu-id="a719a-111">Значение должно быть равно 0, что означает, что лицензия применяется ко всем потокам в файле.</span><span class="sxs-lookup"><span data-stu-id="a719a-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="a719a-112">**двкатегори**</span><span class="sxs-lookup"><span data-stu-id="a719a-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="a719a-113">Категория отображаемой строки.</span><span class="sxs-lookup"><span data-stu-id="a719a-113">Category of string to be displayed.</span></span> <span data-ttu-id="a719a-114">Возможные значения и их значение см. в разделе [**\_ \_ \_ Категория состояния лицензии DRM**](drm-license-state-category.md) .</span><span class="sxs-lookup"><span data-stu-id="a719a-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="a719a-115">**двнумкаунтс**</span><span class="sxs-lookup"><span data-stu-id="a719a-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="a719a-116">Количество элементов, предоставляемых в **двкаунт**.</span><span class="sxs-lookup"><span data-stu-id="a719a-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="a719a-117">Обычно это значение равно 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="a719a-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="a719a-118">**Двкаунт \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="a719a-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="a719a-119">Массив из 0 или 1 или более **DWORD**, который представляет количество выполнений действия, указанного в **двкатегори** .</span><span class="sxs-lookup"><span data-stu-id="a719a-119">An array of 0 or 1 or more **DWORD** s that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="a719a-120">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="a719a-120">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a719a-121">**двнумдатес**</span><span class="sxs-lookup"><span data-stu-id="a719a-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="a719a-122">Количество элементов, представленных в **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="a719a-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="a719a-123">Обычно используется не более двух дат, например с лицензией, которая действительна с одной даты до другой даты.</span><span class="sxs-lookup"><span data-stu-id="a719a-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="a719a-124">**DateTime \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="a719a-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="a719a-125">Массив из одной или нескольких структур FILETIME, представляющих одну или несколько дат в лицензии.</span><span class="sxs-lookup"><span data-stu-id="a719a-125">An array of one or more FILETIME structures representing one or more dates in the license.</span></span> <span data-ttu-id="a719a-126">Значение определенной даты зависит от значения **двкатегори**.</span><span class="sxs-lookup"><span data-stu-id="a719a-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="a719a-127">**дввагуе**</span><span class="sxs-lookup"><span data-stu-id="a719a-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="a719a-128">Ноль или более следующих флагов объединены с побитовой **или**:</span><span class="sxs-lookup"><span data-stu-id="a719a-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="a719a-129">Flag</span><span class="sxs-lookup"><span data-stu-id="a719a-129">Flag</span></span>                                    | <span data-ttu-id="a719a-130">Описание</span><span class="sxs-lookup"><span data-stu-id="a719a-130">Description</span></span>                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a719a-131">\_ \_ \_ неясные данные \_ состояния лицензии DRM</span><span class="sxs-lookup"><span data-stu-id="a719a-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="a719a-132">Если задано, могут существовать дополнительные лицензии, применимые к содержимому.</span><span class="sxs-lookup"><span data-stu-id="a719a-132">If set, there may be more licenses that apply to the content.</span></span>                                                                                         |
| <span data-ttu-id="a719a-133">\_ \_ \_ \_ имеется ОПЛ данных о состоянии лицензии DRM \_</span><span class="sxs-lookup"><span data-stu-id="a719a-133">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="a719a-134">Если этот параметр задан, лицензия включает уровни защиты выходных данных (Оплс), которые должны быть извлечены и проверены в отношении назначения выходных данных приложения.</span><span class="sxs-lookup"><span data-stu-id="a719a-134">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span> |
| <span data-ttu-id="a719a-135">\_данные о \_ состоянии лицензии DRM \_ \_ имеются в SAP \_</span><span class="sxs-lookup"><span data-stu-id="a719a-135">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="a719a-136">Если задано, содержимое должно доставляться с использованием пути Secure Audio (SAP).</span><span class="sxs-lookup"><span data-stu-id="a719a-136">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a719a-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a719a-137">Remarks</span></span>

<span data-ttu-id="a719a-138">Эта структура возвращается (в структуре [**\_ \_ \_ данных состояния лицензии WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) ) из вызова [**ивмдрмреадер:: жетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) при указании одного из свойств состояния лицензии DRM.</span><span class="sxs-lookup"><span data-stu-id="a719a-138">This structure is returned (encapsulated in a [**WM\_LICENSE\_STATE\_DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) structure) from a call to [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) when you specify one of the DRM license state properties.</span></span> <span data-ttu-id="a719a-139">К этим свойствам относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="a719a-139">These properties are:</span></span>

-   [<span data-ttu-id="a719a-140">**\_Воспроизведение ЛИЦЕНСЕСТАТЕ \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a719a-140">**DRM\_LicenseState\_Playback**</span></span>](drm-licensestate-playback.md)
-   [<span data-ttu-id="a719a-141">**\_Лиценсестате \_ копитокд DRM**</span><span class="sxs-lookup"><span data-stu-id="a719a-141">**DRM\_LicenseState\_CopyToCD**</span></span>](drm-licensestate-copytocd.md)
-   [<span data-ttu-id="a719a-142">**\_Лиценсестате \_ копитосдмидевице DRM**</span><span class="sxs-lookup"><span data-stu-id="a719a-142">**DRM\_LicenseState\_CopyToSDMIDevice**</span></span>](drm-licensestate-copytosdmidevice.md)
-   [<span data-ttu-id="a719a-143">**\_Лиценсестате \_ копитононсдмидевице DRM**</span><span class="sxs-lookup"><span data-stu-id="a719a-143">**DRM\_LicenseState\_CopyToNonSDMIDevice**</span></span>](drm-licensestate-copytononsdmidevice.md)
-   [<span data-ttu-id="a719a-144">**\_Лиценсестате \_ коллаборативеплай DRM**</span><span class="sxs-lookup"><span data-stu-id="a719a-144">**DRM\_LicenseState\_CollaborativePlay**</span></span>](drm-licensestate-collaborativeplay.md)
-   [<span data-ttu-id="a719a-145">**\_Лиценсестате \_ Copy DRM**</span><span class="sxs-lookup"><span data-stu-id="a719a-145">**DRM\_LicenseState\_Copy**</span></span>](drm-licensestate-copy.md)
-   [<span data-ttu-id="a719a-146">**\_Лиценсестате \_ плайлистбурн DRM**</span><span class="sxs-lookup"><span data-stu-id="a719a-146">**DRM\_LicenseState\_PlaylistBurn**</span></span>](drm-licensestate-playlistburn.md)

<span data-ttu-id="a719a-147">Если **двкатегори** — **\_ \_ число состояний лицензии WM DRM \_ \_ \_ от \_ до,** то массив **DateTime** обычно содержит две даты: "от" и "до".</span><span class="sxs-lookup"><span data-stu-id="a719a-147">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL,** then the **datetime** array will typically contain two dates, a "from" date and an "until" date.</span></span> <span data-ttu-id="a719a-148">Для создания более сложных лицензий можно также указать две пары дат.</span><span class="sxs-lookup"><span data-stu-id="a719a-148">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="a719a-149">Элементы массива **двкаунт** соответствуют датам или диапазонам дат, указанным в массиве **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="a719a-149">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="a719a-150">Если **двкатегори** является **\_ \_ \_ числом состояний лицензии WM DRM \_ \_ с \_ until** и **DateTime** содержит одну пару дат, **двкаунт** будет содержать один элемент.</span><span class="sxs-lookup"><span data-stu-id="a719a-150">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="a719a-151">Если **DateTime** содержит две пары даты (четыре элемента), **двкаунт** должен содержать два элемента: по одному для каждой пары дат.</span><span class="sxs-lookup"><span data-stu-id="a719a-151">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="a719a-152">В некоторых случаях для одного файла могут быть выпущены несколько лицензий.</span><span class="sxs-lookup"><span data-stu-id="a719a-152">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="a719a-153">Например, они могли получить лицензию, которая позволила пять раз воспроизвести до конца месяца, а затем получить вторую лицензию для неограниченных прав.</span><span class="sxs-lookup"><span data-stu-id="a719a-153">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="a719a-154">В этом случае флаг неявной \_ информации о состоянии лицензии DRM \_ \_ \_ задается в **дввагуе** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ), а компонент DRM использует алгоритм для определения наиболее вероятного набора прав, которые были применены.</span><span class="sxs-lookup"><span data-stu-id="a719a-154">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="a719a-155">По истечении срока действия одной лицензии компонент DRM проверяет остальные лицензии и так далее до истечения срока действия всех лицензий.</span><span class="sxs-lookup"><span data-stu-id="a719a-155">When one license expires, the DRM component will examine the remaining license(s), and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="a719a-156">Требования</span><span class="sxs-lookup"><span data-stu-id="a719a-156">Requirements</span></span>



| <span data-ttu-id="a719a-157">Требование</span><span class="sxs-lookup"><span data-stu-id="a719a-157">Requirement</span></span> | <span data-ttu-id="a719a-158">Значение</span><span class="sxs-lookup"><span data-stu-id="a719a-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a719a-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a719a-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a719a-160">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a719a-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a719a-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a719a-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a719a-162">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a719a-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a719a-163">Версия</span><span class="sxs-lookup"><span data-stu-id="a719a-163">Version</span></span><br/>                  | <span data-ttu-id="a719a-164">Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK</span><span class="sxs-lookup"><span data-stu-id="a719a-164">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="a719a-165">Header</span><span class="sxs-lookup"><span data-stu-id="a719a-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="a719a-166"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="a719a-166"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a719a-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a719a-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a719a-168">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="a719a-168">**Structures**</span></span>](structures.md)
</dt> </dl>

 

