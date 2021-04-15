---
title: Метод Ивмдрмлиценсекуери Куеряктионалловед (Вмдрмсдк. h)
description: Метод Куеряктионалловед выполняет запрос в локальном хранилище лицензий для получения состояния лицензии для одного или нескольких действий DRM, которые применяются к указанному ИДЕНТИФИКАТОРу ключа.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Формат Windows Media, Куеряктионалловед метод
- Куеряктионалловед метод Windows Media Format, интерфейс Ивмдрмлиценсекуери
- Интерфейс Ивмдрмлиценсекуери Windows Media Format, метод Куеряктионалловед
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675758"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a><span data-ttu-id="f9522-106">Метод Ивмдрмлиценсекуери:: Куеряктионалловед</span><span class="sxs-lookup"><span data-stu-id="f9522-106">IWMDRMLicenseQuery::QueryActionAllowed method</span></span>

<span data-ttu-id="f9522-107">Метод **куеряктионалловед** выполняет запрос в локальном хранилище лицензий для получения состояния лицензии для одного или нескольких действий DRM, которые применяются к УКАЗАНному идентификатору ключа.</span><span class="sxs-lookup"><span data-stu-id="f9522-107">The **QueryActionAllowed** method performs a query on the local license store to retrieve the license status for one or more DRM actions that apply to a specified Key ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9522-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9522-108">Syntax</span></span>


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="f9522-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9522-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9522-110">*бстркид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9522-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9522-111">Идентификатор ключа, для которого запрашиваются запросы.</span><span class="sxs-lookup"><span data-stu-id="f9522-111">Key ID for which to query.</span></span> <span data-ttu-id="f9522-112">Будут оцениваться только лицензии, применимые к этому ИДЕНТИФИКАТОРу ключа.</span><span class="sxs-lookup"><span data-stu-id="f9522-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="f9522-113">*бстрминрекиндивверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9522-113">*bstrMinReqIndivVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9522-114">Минимальная версия системы безопасности, указанная в заголовке ASF файла.</span><span class="sxs-lookup"><span data-stu-id="f9522-114">The minimum security version specified in the header of the ASF file.</span></span> <span data-ttu-id="f9522-115">Это необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f9522-115">This parameter is optional.</span></span> <span data-ttu-id="f9522-116">Передайте **значение NULL** , чтобы выполнить запрос без этой информации.</span><span class="sxs-lookup"><span data-stu-id="f9522-116">Pass **NULL** to perform the query without this information.</span></span>

</dd> <dt>

<span data-ttu-id="f9522-117">*кактионстокуери* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9522-117">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9522-118">Число действий, для которых запрашиваются запросы.</span><span class="sxs-lookup"><span data-stu-id="f9522-118">The number of actions for which to query.</span></span> <span data-ttu-id="f9522-119">Это значение должно быть равно количеству элементов в массивах, переданных для параметров *ргбстрактионстокуери* и *ргдвкуериресулт* .</span><span class="sxs-lookup"><span data-stu-id="f9522-119">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgdwQueryResult* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="f9522-120">*\[ ргбстрактионстокуери \]* \[в\]</span><span class="sxs-lookup"><span data-stu-id="f9522-120">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9522-121">Массив из одного или нескольких прав, для которых запрашиваются запросы.</span><span class="sxs-lookup"><span data-stu-id="f9522-121">Array of one or more rights for which to query.</span></span> <span data-ttu-id="f9522-122">Этот массив должен содержать столько элементов, сколько указано параметром *кактионстокуери*.</span><span class="sxs-lookup"><span data-stu-id="f9522-122">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="f9522-123">Каждому элементу должно быть присвоено одно из следующих констант:</span><span class="sxs-lookup"><span data-stu-id="f9522-123">Each element must be set to one of the following constants:</span></span>



| <span data-ttu-id="f9522-124">Константа</span><span class="sxs-lookup"><span data-stu-id="f9522-124">Constant</span></span>                                         | <span data-ttu-id="f9522-125">Описание</span><span class="sxs-lookup"><span data-stu-id="f9522-125">Description</span></span>                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f9522-126">g \_ всзвмдрм \_ актионалловед, \_ Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="f9522-126">g\_wszWMDRM\_ActionAllowed\_Playback</span></span>             | <span data-ttu-id="f9522-127">Включите, чтобы запросить право на воспроизведение содержимого.</span><span class="sxs-lookup"><span data-stu-id="f9522-127">Include to query for the right to play the content.</span></span>                              |
| <span data-ttu-id="f9522-128">g \_ всзвмдрм \_ актионалловед \_ Copy</span><span class="sxs-lookup"><span data-stu-id="f9522-128">g\_wszWMDRM\_ActionAllowed\_Copy</span></span>                 | <span data-ttu-id="f9522-129">Включить для запроса право копировать содержимое на внешние устройства или носитель.</span><span class="sxs-lookup"><span data-stu-id="f9522-129">Include to query for the right to copy the content to external devices or media.</span></span> |
| <span data-ttu-id="f9522-130">g \_ всзвмдрм \_ актионалловед \_ плайлистбурн</span><span class="sxs-lookup"><span data-stu-id="f9522-130">g\_wszWMDRM\_ActionAllowed\_PlaylistBurn</span></span>         | <span data-ttu-id="f9522-131">Включить для запроса право копировать содержимое на компакт-диск в составе списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f9522-131">Include to query for the right to copy the content to CD as part of a playlist.</span></span>  |
| <span data-ttu-id="f9522-132">g \_ всзвмдрм \_ актионалловед \_ креатесумбнаилимаже</span><span class="sxs-lookup"><span data-stu-id="f9522-132">g\_wszWMDRM\_ActionAllowed\_CreateThumbnailImage</span></span> | <span data-ttu-id="f9522-133">Включить, чтобы запросить право на создание эскиза из содержимого.</span><span class="sxs-lookup"><span data-stu-id="f9522-133">Include to query for the right to create a thumbnail image from the content.</span></span>     |
| <span data-ttu-id="f9522-134">g \_ всзвмдрм \_ актионалловед \_ копитокд</span><span class="sxs-lookup"><span data-stu-id="f9522-134">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>             | <span data-ttu-id="f9522-135">Включить, чтобы запросить право на копирование содержимого на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="f9522-135">Include to query for the right to copy the content to CD.</span></span>                        |



 

</dd> <dt>

<span data-ttu-id="f9522-136">*\[ ргдвкуериресулт \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="f9522-136">*rgdwQueryResult\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9522-137">Массив из одной или нескольких переменных типа DWORD, получающих результаты запроса для прав, указанных в *ргбстрактионстокуери*.</span><span class="sxs-lookup"><span data-stu-id="f9522-137">Array of one or more DWORD variables that receive the results of the query for the rights specified by *rgbstrActionsToQuery*.</span></span> <span data-ttu-id="f9522-138">Если действие разрешено, соответствующий элемент устанавливается в нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="f9522-138">If an action is allowed, the corresponding element is set to zero.</span></span> <span data-ttu-id="f9522-139">Если действие не разрешено, для элемента задается одно или несколько значений перечисления " [**\_ \_ \_ \_ результаты запроса", разрешенного для действия DRM**](drm-action-allowed-query-results.md) , в сочетании с использованием побитовой операции или.</span><span class="sxs-lookup"><span data-stu-id="f9522-139">If an action is not allowed, the element is set to one or more values of the [**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**](drm-action-allowed-query-results.md) enumeration combined by using the bitwise OR operation.</span></span> <span data-ttu-id="f9522-140">Этот массив должен содержать столько элементов, сколько указано параметром *кактионстокуери*.</span><span class="sxs-lookup"><span data-stu-id="f9522-140">This array must contain as many elements as specified by *cActionsToQuery*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9522-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9522-141">Return value</span></span>

<span data-ttu-id="f9522-142">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f9522-142">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f9522-143">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f9522-143">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f9522-144">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f9522-144">Return code</span></span>                                                                          | <span data-ttu-id="f9522-145">Описание</span><span class="sxs-lookup"><span data-stu-id="f9522-145">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f9522-146"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f9522-146"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f9522-147">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f9522-147">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9522-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9522-148">Remarks</span></span>

<span data-ttu-id="f9522-149">При запросе прав на воспроизведение и копирование вы получите более точные результаты, сначала задав параметры среды.</span><span class="sxs-lookup"><span data-stu-id="f9522-149">When querying for play and copy rights, you will get more accurate results by first setting environmental parameters.</span></span> <span data-ttu-id="f9522-150">Чтобы задать параметры среды, используйте метод [**сетактионалловедкуерипарамс**](iwmdrmlicensequery-setactionallowedqueryparams.md) .</span><span class="sxs-lookup"><span data-stu-id="f9522-150">Use the [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) method to set the environmental parameters.</span></span> <span data-ttu-id="f9522-151">На результаты запросов для право на запись не влияют параметры окружающей среды. можно безопасно использовать значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9522-151">The results of queries for the burn right are unaffected by the environmental parameters; you can safely use the defaults.</span></span>

<span data-ttu-id="f9522-152">Результаты, возвращаемые методом **куеряктионалловед** , объединяются от нуля или более лицензий в локальном хранилище лицензий.</span><span class="sxs-lookup"><span data-stu-id="f9522-152">The results returned by the **QueryActionAllowed** method are aggregated from zero or more licenses in the local license store.</span></span> <span data-ttu-id="f9522-153">Метод не может искать все лицензии, которые применяются к ИДЕНТИФИКАТОРу ключа, если он встречает включенный результат.</span><span class="sxs-lookup"><span data-stu-id="f9522-153">The method may not search all of the licenses that apply to the Key ID if it encounters an enabled result.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9522-154">Требования</span><span class="sxs-lookup"><span data-stu-id="f9522-154">Requirements</span></span>



| <span data-ttu-id="f9522-155">Требование</span><span class="sxs-lookup"><span data-stu-id="f9522-155">Requirement</span></span> | <span data-ttu-id="f9522-156">Значение</span><span class="sxs-lookup"><span data-stu-id="f9522-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9522-157">Header</span><span class="sxs-lookup"><span data-stu-id="f9522-157">Header</span></span><br/>  | <dl> <span data-ttu-id="f9522-158"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9522-158"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9522-159">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f9522-159">Library</span></span><br/> | <dl> <span data-ttu-id="f9522-160"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9522-160"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9522-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9522-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9522-162">**Интерфейс Ивмдрмлиценсекуери**</span><span class="sxs-lookup"><span data-stu-id="f9522-162">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="f9522-163">**Запрос сведений о простых правах**</span><span class="sxs-lookup"><span data-stu-id="f9522-163">**Querying for Simple Rights Information**</span></span>](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





