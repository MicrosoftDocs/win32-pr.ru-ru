---
title: Медиаколлектион. Жетстрингколлектионбикуери, метод
description: Метод Жетстрингколлектионбикуери извлекает объект StringCollection, содержащий все строки, соответствующие условиям запроса.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- Жетстрингколлектионбикуери метод Windows Media Player
- Жетстрингколлектионбикуери метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетстрингколлектионбикуери
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685412"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a><span data-ttu-id="da758-106">Медиаколлектион. Жетстрингколлектионбикуери, метод</span><span class="sxs-lookup"><span data-stu-id="da758-106">MediaCollection.getStringCollectionByQuery method</span></span>

<span data-ttu-id="da758-107">Метод **жетстрингколлектионбикуери** извлекает объект **StringCollection** , содержащий все строки, соответствующие условиям запроса.</span><span class="sxs-lookup"><span data-stu-id="da758-107">The **getStringCollectionByQuery** method retrieves a **StringCollection** object containing all strings that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="da758-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da758-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="da758-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="da758-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da758-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da758-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da758-111">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="da758-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="da758-112">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da758-112">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da758-113">Объект **запроса** .</span><span class="sxs-lookup"><span data-stu-id="da758-113">**Query** object.</span></span>

</dd> <dt>

<span data-ttu-id="da758-114">*mediaType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da758-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da758-115">**Строка** , содержащая тип носителя.</span><span class="sxs-lookup"><span data-stu-id="da758-115">**String** containing the media type.</span></span> <span data-ttu-id="da758-116">Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".</span><span class="sxs-lookup"><span data-stu-id="da758-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="da758-117">*sortAttribute* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da758-117">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da758-118">**Строка** , содержащая имя атрибута, используемого для сортировки.</span><span class="sxs-lookup"><span data-stu-id="da758-118">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="da758-119">Пустая строка ("") означает, что сортировка не применяется.</span><span class="sxs-lookup"><span data-stu-id="da758-119">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="da758-120">*сортасцендинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da758-120">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da758-121">**Логическое** значение, true, указывающее, что **StringCollection** должен быть отсортирован в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="da758-121">**Boolean**, true indicating that the **StringCollection** must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da758-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da758-122">Return value</span></span>

<span data-ttu-id="da758-123">Этот метод возвращает объект **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="da758-123">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="da758-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da758-124">Remarks</span></span>

<span data-ttu-id="da758-125">В составных запросах, использующих **запрос** , регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="da758-125">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="da758-126">Если составной запрос, заданный параметром *запроса* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется.</span><span class="sxs-lookup"><span data-stu-id="da758-126">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="da758-127">Значение параметра *mediaType* всегда используется.</span><span class="sxs-lookup"><span data-stu-id="da758-127">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="da758-128">Например, если составной запрос содержит условие «MediaType равно Audio», а параметру *mediaType* — «Video», то итоговый список будет содержать только элементы видео.</span><span class="sxs-lookup"><span data-stu-id="da758-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="da758-129">Требования</span><span class="sxs-lookup"><span data-stu-id="da758-129">Requirements</span></span>



| <span data-ttu-id="da758-130">Требование</span><span class="sxs-lookup"><span data-stu-id="da758-130">Requirement</span></span> | <span data-ttu-id="da758-131">Значение</span><span class="sxs-lookup"><span data-stu-id="da758-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da758-132">Версия</span><span class="sxs-lookup"><span data-stu-id="da758-132">Version</span></span><br/> | <span data-ttu-id="da758-133">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="da758-133">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="da758-134">DLL</span><span class="sxs-lookup"><span data-stu-id="da758-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="da758-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da758-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da758-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da758-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da758-137">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="da758-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="da758-138">**Атрибут MediaType**</span><span class="sxs-lookup"><span data-stu-id="da758-138">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="da758-139">**Объект запроса**</span><span class="sxs-lookup"><span data-stu-id="da758-139">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





