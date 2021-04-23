---
title: Структура DRM_LICENSE_STATE_DATA (Вмдрмсдк. h)
description: '\_ \_ \_ Структура данных о состоянии лицензии DRM содержит сведения об ограничениях лицензии для права доступа DRM.'
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- Формат DRM_LICENSE_STATE_DATA структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708390"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a><span data-ttu-id="da16c-105">Структура DRM_LICENSE_STATE_DATA (Вмдрмсдк. h)</span><span class="sxs-lookup"><span data-stu-id="da16c-105">DRM_LICENSE_STATE_DATA structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="da16c-106">Структура **\_ данных о \_ состоянии \_ лицензии DRM** содержит сведения об ограничениях лицензии для права доступа DRM.</span><span class="sxs-lookup"><span data-stu-id="da16c-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains information about the license restrictions for a DRM right.</span></span>

## <a name="syntax"></a><span data-ttu-id="da16c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da16c-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="da16c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="da16c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="da16c-109">**двстреамид**</span><span class="sxs-lookup"><span data-stu-id="da16c-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="da16c-110">Номер потока, к которому применяется лицензия.</span><span class="sxs-lookup"><span data-stu-id="da16c-110">Stream number to which the license applies.</span></span> <span data-ttu-id="da16c-111">Значение должно быть равно 0, что означает, что лицензия применяется ко всем потокам в файле.</span><span class="sxs-lookup"><span data-stu-id="da16c-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="da16c-112">**двкатегори**</span><span class="sxs-lookup"><span data-stu-id="da16c-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="da16c-113">Категория отображаемой строки.</span><span class="sxs-lookup"><span data-stu-id="da16c-113">Category of string to be displayed.</span></span> <span data-ttu-id="da16c-114">Возможные значения и их значение см. в разделе [**\_ \_ \_ Категория состояния лицензии DRM**](drmdrm-license-state-category.md) .</span><span class="sxs-lookup"><span data-stu-id="da16c-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drmdrm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="da16c-115">**двнумкаунтс**</span><span class="sxs-lookup"><span data-stu-id="da16c-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="da16c-116">Количество элементов, предоставляемых в **двкаунт**.</span><span class="sxs-lookup"><span data-stu-id="da16c-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="da16c-117">Обычно это значение равно 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="da16c-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="da16c-118">**Двкаунт \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="da16c-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="da16c-119">Массив из 0 или 1 или более значений **DWORD** , представляющих количество выполнений действия, указанного в **двкатегори** .</span><span class="sxs-lookup"><span data-stu-id="da16c-119">An array of 0 or 1 or more **DWORD** values that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="da16c-120">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="da16c-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da16c-121">**двнумдатес**</span><span class="sxs-lookup"><span data-stu-id="da16c-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="da16c-122">Количество элементов, представленных в **DateTime**.</span><span class="sxs-lookup"><span data-stu-id="da16c-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="da16c-123">Обычно используется не более двух дат, например с лицензией, которая действительна с одной даты до другой даты.</span><span class="sxs-lookup"><span data-stu-id="da16c-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="da16c-124">**DateTime \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="da16c-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="da16c-125">Массив из одной или нескольких структур **fileTime** , представляющих одну или несколько дат в лицензии.</span><span class="sxs-lookup"><span data-stu-id="da16c-125">An array of one or more **FILETIME** structures representing one or more dates in the license.</span></span> <span data-ttu-id="da16c-126">Значение определенной даты зависит от значения **двкатегори**.</span><span class="sxs-lookup"><span data-stu-id="da16c-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="da16c-127">**дввагуе**</span><span class="sxs-lookup"><span data-stu-id="da16c-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="da16c-128">Ноль или более следующих флагов объединены с побитовой **или**:</span><span class="sxs-lookup"><span data-stu-id="da16c-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="da16c-129">Flag</span><span class="sxs-lookup"><span data-stu-id="da16c-129">Flag</span></span>                                    | <span data-ttu-id="da16c-130">Описание</span><span class="sxs-lookup"><span data-stu-id="da16c-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da16c-131">\_ \_ \_ неясные данные \_ состояния лицензии DRM</span><span class="sxs-lookup"><span data-stu-id="da16c-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="da16c-132">Если задано, могут существовать дополнительные лицензии, применимые к содержимому.</span><span class="sxs-lookup"><span data-stu-id="da16c-132">If set, there may be more licenses that apply to the content.</span></span> <span data-ttu-id="da16c-133">Единственный способ узнать об отдельных лицензиях, применимых к данному ИДЕНТИФИКАТОРу ключа, — это перечислить лицензии.</span><span class="sxs-lookup"><span data-stu-id="da16c-133">The only way to be certain about the individual licenses that apply to a given key ID is to enumerate the licenses.</span></span> <span data-ttu-id="da16c-134">Для этого вызовите [**ивмдрмлиценсеманажемент:: креателиценсинумератион**](iwmdrmlicensemanagement-createlicenseenumeration.md), передав идентификатор ключа в качестве параметра бстркид.</span><span class="sxs-lookup"><span data-stu-id="da16c-134">To do this, call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing the key ID as the bstrKID parameter.</span></span> <span data-ttu-id="da16c-135">Затем используйте полученный интерфейс Ивмдрмлиценсе для проверки лицензий.</span><span class="sxs-lookup"><span data-stu-id="da16c-135">Then use the retrieved IWMDRMLicense interface to examine the licenses.</span></span> |
| <span data-ttu-id="da16c-136">\_ \_ \_ \_ имеется ОПЛ данных о состоянии лицензии DRM \_</span><span class="sxs-lookup"><span data-stu-id="da16c-136">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="da16c-137">Если этот параметр задан, лицензия включает уровни защиты выходных данных (Оплс), которые должны быть извлечены и проверены в отношении назначения выходных данных приложения.</span><span class="sxs-lookup"><span data-stu-id="da16c-137">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="da16c-138">\_данные о \_ состоянии лицензии DRM \_ \_ имеются в SAP \_</span><span class="sxs-lookup"><span data-stu-id="da16c-138">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="da16c-139">Если задано, содержимое должно доставляться с использованием пути Secure Audio (SAP).</span><span class="sxs-lookup"><span data-stu-id="da16c-139">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da16c-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da16c-140">Remarks</span></span>

<span data-ttu-id="da16c-141">Эта структура извлекается путем вызова **ивмдрмлиценсекуери:: куерилиценсестате**.</span><span class="sxs-lookup"><span data-stu-id="da16c-141">This structure is retrieved by calling **IWMDRMLicenseQuery::QueryLicenseState**.</span></span>

<span data-ttu-id="da16c-142">Если **двкатегори** — **\_ \_ число состояний лицензии WM DRM \_ \_ \_ от \_ до**, то массив **DateTime** обычно содержит две даты: "от" и "до".</span><span class="sxs-lookup"><span data-stu-id="da16c-142">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**, then the **datetime** array will typically contain two dates: a "from" date and an "until" date.</span></span> <span data-ttu-id="da16c-143">Для создания более сложных лицензий можно также указать две пары дат.</span><span class="sxs-lookup"><span data-stu-id="da16c-143">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="da16c-144">Элементы массива **двкаунт** соответствуют датам или диапазонам дат, указанным в массиве **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="da16c-144">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="da16c-145">Если **двкатегори** является **\_ \_ \_ числом состояний лицензии WM DRM \_ \_ с \_ until** и **DateTime** содержит одну пару дат, **двкаунт** будет содержать один элемент.</span><span class="sxs-lookup"><span data-stu-id="da16c-145">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="da16c-146">Если **DateTime** содержит две пары даты (четыре элемента), **двкаунт** должен содержать два элемента: по одному для каждой пары дат.</span><span class="sxs-lookup"><span data-stu-id="da16c-146">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="da16c-147">В некоторых случаях для одного файла могут быть выпущены несколько лицензий.</span><span class="sxs-lookup"><span data-stu-id="da16c-147">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="da16c-148">Например, они могли получить лицензию, которая позволила пять раз воспроизвести до конца месяца, а затем получить вторую лицензию для неограниченных прав.</span><span class="sxs-lookup"><span data-stu-id="da16c-148">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="da16c-149">В этом случае флаг неявной \_ информации о состоянии лицензии DRM \_ \_ \_ задается в **дввагуе** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ), а компонент DRM использует алгоритм для определения наиболее вероятного набора прав, которые были применены.</span><span class="sxs-lookup"><span data-stu-id="da16c-149">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="da16c-150">По истечении срока действия одной лицензии компонент DRM проверяет остальные лицензии и так далее до истечения срока действия всех лицензий.</span><span class="sxs-lookup"><span data-stu-id="da16c-150">When one license expires, the DRM component will examine the remaining licenses, and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="da16c-151">Требования</span><span class="sxs-lookup"><span data-stu-id="da16c-151">Requirements</span></span>



| <span data-ttu-id="da16c-152">Требование</span><span class="sxs-lookup"><span data-stu-id="da16c-152">Requirement</span></span> | <span data-ttu-id="da16c-153">Значение</span><span class="sxs-lookup"><span data-stu-id="da16c-153">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da16c-154">Header</span><span class="sxs-lookup"><span data-stu-id="da16c-154">Header</span></span><br/> | <dl> <span data-ttu-id="da16c-155"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="da16c-155"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da16c-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da16c-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da16c-157">**Структуры**</span><span class="sxs-lookup"><span data-stu-id="da16c-157">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





