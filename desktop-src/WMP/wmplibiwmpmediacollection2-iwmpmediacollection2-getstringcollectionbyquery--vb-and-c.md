---
title: IWMPMediaCollection2 Жетстрингколлектионбикуери, метод
description: Метод Жетстрингколлектионбикуери возвращает интерфейс Ивмпстрингколлектион, который предоставляет доступ к набору всех строковых значений для указанного атрибута, соответствующих условиям запроса.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- Жетстрингколлектионбикуери метод Windows Media Player
- Жетстрингколлектионбикуери метод проигрывателя Windows Media Player, интерфейс IWMPMediaCollection2
- Интерфейс IWMPMediaCollection2 Windows Media Player, метод Жетстрингколлектионбикуери
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704530"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a><span data-ttu-id="83d5e-106">Метод IWMPMediaCollection2:: Жетстрингколлектионбикуери</span><span class="sxs-lookup"><span data-stu-id="83d5e-106">IWMPMediaCollection2::getStringCollectionByQuery method</span></span>

<span data-ttu-id="83d5e-107">`getStringCollectionByQuery`Метод возвращает интерфейс **ивмпстрингколлектион** , который предоставляет доступ к набору всех строковых значений для указанного атрибута, соответствующих условиям запроса.</span><span class="sxs-lookup"><span data-stu-id="83d5e-107">The `getStringCollectionByQuery` method returns an **IWMPStringCollection** interface that provides access to the set of all string values for a specified attribute that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d5e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83d5e-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a><span data-ttu-id="83d5e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="83d5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83d5e-110">*бстраттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83d5e-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5e-111">**Строка System. String** , которая является именем атрибута.</span><span class="sxs-lookup"><span data-stu-id="83d5e-111">The **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="83d5e-112">*пкуери* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83d5e-112">*pQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5e-113">Интерфейс **вмплиб. ивмпкуери** , который представляет собой запрос, определяющий условия, используемые для получения коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="83d5e-113">The **WMPLib.IWMPQuery** interface that is the query that defines the conditions used to retrieve the string collection.</span></span>

</dd> <dt>

<span data-ttu-id="83d5e-114">*бстрмедиатипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83d5e-114">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5e-115">**Строка System. String** , которая является типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="83d5e-115">The **System.String** that is the media type.</span></span> <span data-ttu-id="83d5e-116">Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".</span><span class="sxs-lookup"><span data-stu-id="83d5e-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="83d5e-117">*бстрсортаттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83d5e-117">*bstrSortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5e-118">**Строка System. String** , которая является именем атрибута, используемого для сортировки.</span><span class="sxs-lookup"><span data-stu-id="83d5e-118">The **System.String** that is the attribute name used for sorting.</span></span> <span data-ttu-id="83d5e-119">Строка нулевой длины ("") означает, что сортировка не применяется.</span><span class="sxs-lookup"><span data-stu-id="83d5e-119">A zero-length string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="83d5e-120">*фсортасцендинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83d5e-120">*fSortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83d5e-121">Значение **System. Boolean** , указывающее, должен ли набор строковых значений быть отсортирован в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="83d5e-121">The **System.Boolean** value that indicates whether the set of string values must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83d5e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83d5e-122">Return value</span></span>

<span data-ttu-id="83d5e-123">Интерфейс **вмплиб. ивмпстрингколлектион** для полученного набора строковых значений.</span><span class="sxs-lookup"><span data-stu-id="83d5e-123">A **WMPLib.IWMPStringCollection** interface for the retrieved set of string values.</span></span>

## <a name="remarks"></a><span data-ttu-id="83d5e-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83d5e-124">Remarks</span></span>

<span data-ttu-id="83d5e-125">В составных запросах, использующих **ивмпкуери** , регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="83d5e-125">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="83d5e-126">Если составной запрос, заданный параметром *пкуери* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется.</span><span class="sxs-lookup"><span data-stu-id="83d5e-126">When the compound query specified by the *pQuery* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="83d5e-127">Значение параметра *бстрмедиатипе* всегда используется.</span><span class="sxs-lookup"><span data-stu-id="83d5e-127">The value for the *bstrMediaType* parameter is always used.</span></span> <span data-ttu-id="83d5e-128">Например, если составной запрос содержит условие «MediaType равно Audio», а значение параметра *бстрмедиатипе* — «Video», то итоговый список будет содержать только элементы видео.</span><span class="sxs-lookup"><span data-stu-id="83d5e-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *bstrMediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="83d5e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="83d5e-129">Requirements</span></span>



| <span data-ttu-id="83d5e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="83d5e-130">Requirement</span></span> | <span data-ttu-id="83d5e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="83d5e-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d5e-132">Версия</span><span class="sxs-lookup"><span data-stu-id="83d5e-132">Version</span></span><br/>   | <span data-ttu-id="83d5e-133">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="83d5e-133">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="83d5e-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="83d5e-134">Namespace</span></span><br/> | <span data-ttu-id="83d5e-135">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="83d5e-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="83d5e-136">Сборка</span><span class="sxs-lookup"><span data-stu-id="83d5e-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="83d5e-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="83d5e-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83d5e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83d5e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d5e-139">**Интерфейс IWMPMediaCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="83d5e-139">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="83d5e-140">**Интерфейс Ивмпкуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="83d5e-140">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="83d5e-141">**Интерфейс Ивмпстрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="83d5e-141">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="83d5e-142">**Атрибут MediaType**</span><span class="sxs-lookup"><span data-stu-id="83d5e-142">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> </dl>

 

 





