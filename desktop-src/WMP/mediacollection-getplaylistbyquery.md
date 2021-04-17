---
title: Медиаколлектион. Жетплайлистбикуери, метод
description: Метод Жетплайлистбикуери извлекает объект списка воспроизведения, содержащий объекты мультимедиа, соответствующие условиям запроса.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- Жетплайлистбикуери метод Windows Media Player
- Жетплайлистбикуери метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетплайлистбикуери
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685413"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a><span data-ttu-id="16793-106">Медиаколлектион. Жетплайлистбикуери, метод</span><span class="sxs-lookup"><span data-stu-id="16793-106">MediaCollection.getPlaylistByQuery method</span></span>

<span data-ttu-id="16793-107">Метод **жетплайлистбикуери** извлекает объект **списка воспроизведения** , содержащий объекты **мультимедиа** , соответствующие условиям запроса.</span><span class="sxs-lookup"><span data-stu-id="16793-107">The **getPlaylistByQuery** method retrieves a **Playlist** object containing **Media** objects that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="16793-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16793-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="16793-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="16793-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16793-110">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16793-110">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16793-111">Объект **запроса** , который определяет условия, используемые для создания списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="16793-111">**Query** object that defines the conditions used to create the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="16793-112">*mediaType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16793-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16793-113">**Строка** , содержащая тип носителя.</span><span class="sxs-lookup"><span data-stu-id="16793-113">**String** containing the media type.</span></span> <span data-ttu-id="16793-114">Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".</span><span class="sxs-lookup"><span data-stu-id="16793-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="16793-115">*sortAttribute* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16793-115">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16793-116">**Строка** , содержащая имя атрибута, используемого для сортировки.</span><span class="sxs-lookup"><span data-stu-id="16793-116">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="16793-117">Пустая строка ("") означает, что сортировка не применяется.</span><span class="sxs-lookup"><span data-stu-id="16793-117">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="16793-118">*сортасцендинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="16793-118">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16793-119">**Логическое** значение, true, указывающее, что список воспроизведения должен быть отсортирован в возрастающем порядке.</span><span class="sxs-lookup"><span data-stu-id="16793-119">**Boolean**, true indicating that the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16793-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16793-120">Return value</span></span>

<span data-ttu-id="16793-121">Этот метод возвращает объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="16793-121">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16793-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16793-122">Remarks</span></span>

<span data-ttu-id="16793-123">В составных запросах, использующих **запрос** , регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="16793-123">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="16793-124">Если составной запрос, заданный параметром *запроса* , содержит условие, построенное на атрибуте **mediaType** , это условие игнорируется.</span><span class="sxs-lookup"><span data-stu-id="16793-124">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="16793-125">Значение параметра *mediaType* всегда используется.</span><span class="sxs-lookup"><span data-stu-id="16793-125">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="16793-126">Например, если составной запрос содержит условие «MediaType равно Audio», а параметру *mediaType* — «Video», то итоговый список будет содержать только элементы видео.</span><span class="sxs-lookup"><span data-stu-id="16793-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="16793-127">Требования</span><span class="sxs-lookup"><span data-stu-id="16793-127">Requirements</span></span>



| <span data-ttu-id="16793-128">Требование</span><span class="sxs-lookup"><span data-stu-id="16793-128">Requirement</span></span> | <span data-ttu-id="16793-129">Значение</span><span class="sxs-lookup"><span data-stu-id="16793-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16793-130">Версия</span><span class="sxs-lookup"><span data-stu-id="16793-130">Version</span></span><br/> | <span data-ttu-id="16793-131">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="16793-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="16793-132">DLL</span><span class="sxs-lookup"><span data-stu-id="16793-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="16793-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16793-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16793-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16793-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16793-135">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="16793-135">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="16793-136">**Атрибут MediaType**</span><span class="sxs-lookup"><span data-stu-id="16793-136">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="16793-137">**Объект запроса**</span><span class="sxs-lookup"><span data-stu-id="16793-137">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





