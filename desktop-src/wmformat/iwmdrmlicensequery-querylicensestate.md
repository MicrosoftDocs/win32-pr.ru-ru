---
title: Метод Ивмдрмлиценсекуери Куерилиценсестате (Вмдрмсдк. h)
description: Метод Куерилиценсестате запрашивает в локальном хранилище лицензий сведения о лицензиях, которые применяются к ИДЕНТИФИКАТОРу ключа для одного или нескольких конкретных прав.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Формат Windows Media, Куерилиценсестате метод
- Куерилиценсестате метод Windows Media Format, интерфейс Ивмдрмлиценсекуери
- Интерфейс Ивмдрмлиценсекуери Windows Media Format, метод Куерилиценсестате
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694674"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a><span data-ttu-id="46ca7-106">Метод Ивмдрмлиценсекуери:: Куерилиценсестате</span><span class="sxs-lookup"><span data-stu-id="46ca7-106">IWMDRMLicenseQuery::QueryLicenseState method</span></span>

<span data-ttu-id="46ca7-107">Метод **куерилиценсестате** запрашивает в локальном хранилище лицензий сведения о лицензиях, которые применяются к идентификатору ключа для одного или нескольких конкретных прав.</span><span class="sxs-lookup"><span data-stu-id="46ca7-107">The **QueryLicenseState** method queries the local license store for license information that applies to a Key ID for one or more specific rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ca7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46ca7-108">Syntax</span></span>


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a><span data-ttu-id="46ca7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="46ca7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ca7-110">*бстркид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46ca7-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ca7-111">Идентификатор ключа, для которого запрашиваются запросы.</span><span class="sxs-lookup"><span data-stu-id="46ca7-111">Key ID for which to query.</span></span> <span data-ttu-id="46ca7-112">Будут оцениваться только лицензии, применимые к этому ИДЕНТИФИКАТОРу ключа.</span><span class="sxs-lookup"><span data-stu-id="46ca7-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="46ca7-113">*кактионстокуери* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="46ca7-113">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ca7-114">Число действий, для которых запрашиваются запросы.</span><span class="sxs-lookup"><span data-stu-id="46ca7-114">The number of actions for which to query.</span></span> <span data-ttu-id="46ca7-115">Это значение должно быть равно количеству элементов в массивах, переданных для параметров *ргбстрактионстокуери* и *ргресултстатедата* .</span><span class="sxs-lookup"><span data-stu-id="46ca7-115">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgResultStateData* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="46ca7-116">*\[ ргбстрактионстокуери \]* \[в\]</span><span class="sxs-lookup"><span data-stu-id="46ca7-116">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ca7-117">Массив из одного или нескольких прав, для которых запрашиваются запросы.</span><span class="sxs-lookup"><span data-stu-id="46ca7-117">Array of one or more rights for which to query.</span></span> <span data-ttu-id="46ca7-118">Этот массив должен содержать столько элементов, сколько указано параметром *кактионстокуери*.</span><span class="sxs-lookup"><span data-stu-id="46ca7-118">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="46ca7-119">Каждому элементу должно быть присвоено одно из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="46ca7-119">Each element must be set to one of the following constants.</span></span>



| <span data-ttu-id="46ca7-120">Константа</span><span class="sxs-lookup"><span data-stu-id="46ca7-120">Constant</span></span>                                        | <span data-ttu-id="46ca7-121">Описание</span><span class="sxs-lookup"><span data-stu-id="46ca7-121">Description</span></span>                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ca7-122">g \_ всзвмдрм \_ лиценсестате \_ BACKUP</span><span class="sxs-lookup"><span data-stu-id="46ca7-122">g\_wszWMDRM\_LicenseState\_Backup</span></span>               | <span data-ttu-id="46ca7-123">Включите, чтобы запросить сведения о правильном резервном копировании и восстановлении лицензии.</span><span class="sxs-lookup"><span data-stu-id="46ca7-123">Include to query for the details about the right to back up and restore the license.</span></span>                                                               |
| <span data-ttu-id="46ca7-124">g \_ всзвмдрм \_ лиценсестате \_ коллаборативеплай</span><span class="sxs-lookup"><span data-stu-id="46ca7-124">g\_wszWMDRM\_LicenseState\_CollaborativePlay</span></span>    | <span data-ttu-id="46ca7-125">Включите, чтобы запросить сведения о правильном доступе к содержимому с группой пользователей в рамках сценария совместного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="46ca7-125">Include to query for the details about the right to share the content with a group of users as part of a collaborative playback scenario.</span></span>          |
| <span data-ttu-id="46ca7-126">g \_ всзвмдрм \_ лиценсестате \_ Copy</span><span class="sxs-lookup"><span data-stu-id="46ca7-126">g\_wszWMDRM\_LicenseState\_Copy</span></span>                 | <span data-ttu-id="46ca7-127">Включить в запрос, чтобы получить сведения о правильном копировании содержимого на внешние устройства или носитель.</span><span class="sxs-lookup"><span data-stu-id="46ca7-127">Include to query for the details about the right to copy the content to external devices or media.</span></span>                                                 |
| <span data-ttu-id="46ca7-128">g \_ всзвмдрм \_ лиценсестате \_ копитокд</span><span class="sxs-lookup"><span data-stu-id="46ca7-128">g\_wszWMDRM\_LicenseState\_CopyToCD</span></span>             | <span data-ttu-id="46ca7-129">Включить в запрос, чтобы получить сведения о правильном копировании содержимого на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="46ca7-129">Include to query for the details about the right to copy the content to CD.</span></span>                                                                        |
| <span data-ttu-id="46ca7-130">g \_ всзвмдрм \_ лиценсестате \_ копитононсдмидевице</span><span class="sxs-lookup"><span data-stu-id="46ca7-130">g\_wszWMDRM\_LicenseState\_CopyToNonSDMIDevice</span></span>  | <span data-ttu-id="46ca7-131">Включить в запрос, чтобы получить сведения о правильном копировании содержимого на устройство, которое не поддерживает инициативу по защите цифровых мультимедийных данных (SDMI).</span><span class="sxs-lookup"><span data-stu-id="46ca7-131">Include to query for the details about the right to copy the content to a device that does not support the secure digital media initiative (SDMI).</span></span> |
| <span data-ttu-id="46ca7-132">g \_ всзвмдрм \_ лиценсестате \_ копитосдмидевице</span><span class="sxs-lookup"><span data-stu-id="46ca7-132">g\_wszWMDRM\_LicenseState\_CopyToSDMIDevice</span></span>     | <span data-ttu-id="46ca7-133">Включите, чтобы запросить сведения о правильном копировании содержимого на устройство, которое поддерживает SDMI.</span><span class="sxs-lookup"><span data-stu-id="46ca7-133">Include to query for the details about the right to copy the content to a device that supports the SDMI.</span></span>                                           |
| <span data-ttu-id="46ca7-134">g \_ всзвмдрм \_ лиценсестате \_ креатесумбнаилимаже</span><span class="sxs-lookup"><span data-stu-id="46ca7-134">g\_wszWMDRM\_LicenseState\_CreateThumbnailImage</span></span> | <span data-ttu-id="46ca7-135">Включить в запрос для получения подробных сведений о правильном создании эскиза из содержимого.</span><span class="sxs-lookup"><span data-stu-id="46ca7-135">Include to query for the details about the right to create a thumbnail image from the content.</span></span>                                                     |
| <span data-ttu-id="46ca7-136">g \_ всзвмдрм \_ лиценсестате, \_ Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="46ca7-136">g\_wszWMDRM\_LicenseState\_Playback</span></span>             | <span data-ttu-id="46ca7-137">Включить в запрос для получения подробных сведений о правом воспроизведения содержимого.</span><span class="sxs-lookup"><span data-stu-id="46ca7-137">Include to query for the details about the right to play the content.</span></span>                                                                              |
| <span data-ttu-id="46ca7-138">g \_ всзвмдрм \_ лиценсестате \_ плайлистбурн</span><span class="sxs-lookup"><span data-stu-id="46ca7-138">g\_wszWMDRM\_LicenseState\_PlaylistBurn</span></span>         | <span data-ttu-id="46ca7-139">Включить в запрос, чтобы получить сведения о правильном копировании содержимого на компакт-диск в составе списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="46ca7-139">Include to query for the details about the right to copy the content to CD as part of a playlist.</span></span>                                                  |



 

</dd> <dt>

<span data-ttu-id="46ca7-140">*\[ ргресултстатедата \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="46ca7-140">*rgResultStateData\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46ca7-141">Массив из одной или нескольких [**структур \_ \_ \_ данных состояния лицензии DRM**](drmdrm-license-state-data.md) , которые получают сведения о состоянии лицензии, которые относятся к правому в соответствующем элементе параметра *ргбстрактионстокуери* .</span><span class="sxs-lookup"><span data-stu-id="46ca7-141">Array of one or more [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structures that receive the license state information that applies to the right in the corresponding element of the *rgbstrActionsToQuery* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ca7-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46ca7-142">Return value</span></span>

<span data-ttu-id="46ca7-143">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="46ca7-143">The method returns an **HRESULT**.</span></span> <span data-ttu-id="46ca7-144">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="46ca7-144">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="46ca7-145">Код возврата</span><span class="sxs-lookup"><span data-stu-id="46ca7-145">Return code</span></span>                                                                          | <span data-ttu-id="46ca7-146">Описание</span><span class="sxs-lookup"><span data-stu-id="46ca7-146">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="46ca7-147"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="46ca7-147"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="46ca7-148">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="46ca7-148">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="46ca7-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46ca7-149">Remarks</span></span>

<span data-ttu-id="46ca7-150">Будет выполнен поиск и оценка всех лицензий, применимых к указанному ИДЕНТИФИКАТОРу ключа.</span><span class="sxs-lookup"><span data-stu-id="46ca7-150">All licenses that apply to the specified Key ID will be searched and evaluated.</span></span> <span data-ttu-id="46ca7-151">Результаты суммируются, поэтому каждая структура **\_ \_ \_ данных состояния лицензии DRM** может содержать данные из нескольких лицензий.</span><span class="sxs-lookup"><span data-stu-id="46ca7-151">The results are aggregated, so each **DRM\_LICENSE\_STATE\_DATA** structure may contain information from multiple licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ca7-152">Требования</span><span class="sxs-lookup"><span data-stu-id="46ca7-152">Requirements</span></span>



| <span data-ttu-id="46ca7-153">Требование</span><span class="sxs-lookup"><span data-stu-id="46ca7-153">Requirement</span></span> | <span data-ttu-id="46ca7-154">Значение</span><span class="sxs-lookup"><span data-stu-id="46ca7-154">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46ca7-155">Header</span><span class="sxs-lookup"><span data-stu-id="46ca7-155">Header</span></span><br/>  | <dl> <span data-ttu-id="46ca7-156"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="46ca7-156"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="46ca7-157">Библиотека</span><span class="sxs-lookup"><span data-stu-id="46ca7-157">Library</span></span><br/> | <dl> <span data-ttu-id="46ca7-158"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46ca7-158"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ca7-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46ca7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ca7-160">**Интерфейс Ивмдрмлиценсекуери**</span><span class="sxs-lookup"><span data-stu-id="46ca7-160">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> </dl>

 

 





