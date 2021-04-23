---
title: Метод Query. Аддкондитион
description: Метод Аддкондитион добавляет условие в объект запроса с помощью логики и.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- Аддкондитион метод Windows Media Player
- метод Аддкондитион Windows Media Player, класс запроса
- Класс запроса проигрыватель Windows Media Player, метод Аддкондитион
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704184"
---
# <a name="queryaddcondition-method"></a><span data-ttu-id="f195d-106">Метод Query. Аддкондитион</span><span class="sxs-lookup"><span data-stu-id="f195d-106">Query.addCondition method</span></span>

<span data-ttu-id="f195d-107">Метод **аддкондитион** добавляет условие в объект **запроса** с помощью логики и.</span><span class="sxs-lookup"><span data-stu-id="f195d-107">The **addCondition** method adds a condition to the **Query** object using AND logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f195d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f195d-108">Syntax</span></span>


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="f195d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f195d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f195d-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f195d-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f195d-111">**Строка** , содержащая имя атрибута.</span><span class="sxs-lookup"><span data-stu-id="f195d-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="f195d-112">*оператор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f195d-112">*operator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f195d-113">**Строка** , содержащая оператор.</span><span class="sxs-lookup"><span data-stu-id="f195d-113">**String** containing the operator.</span></span> <span data-ttu-id="f195d-114">Поддерживаемые значения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="f195d-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="f195d-115">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f195d-115">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f195d-116">**Строка** , содержащая значение атрибута.</span><span class="sxs-lookup"><span data-stu-id="f195d-116">**String** containing the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f195d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f195d-117">Return value</span></span>

<span data-ttu-id="f195d-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f195d-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f195d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f195d-119">Remarks</span></span>

<span data-ttu-id="f195d-120">В составных запросах, использующих **запрос** , регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="f195d-120">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="f195d-121">Список значений для параметра *Attribute* можно найти в [алфавитном разделе Справочник по атрибутам](alphabetical-attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f195d-121">A list of values for the *attribute* parameter can be found in the [Alphabetical Attribute Reference](alphabetical-attribute-reference.md) section.</span></span>

<span data-ttu-id="f195d-122">Условия, содержащиеся в объекте **запроса** , организованы в группы условий.</span><span class="sxs-lookup"><span data-stu-id="f195d-122">Conditions contained in a **Query** object are organized into condition groups.</span></span> <span data-ttu-id="f195d-123">Несколько условий в группе условий всегда объединяются с помощью логики и.</span><span class="sxs-lookup"><span data-stu-id="f195d-123">Multiple conditions within a condition group are always concatenated using AND logic.</span></span> <span data-ttu-id="f195d-124">Группы условий всегда объединяются друг с другом с помощью логики или.</span><span class="sxs-lookup"><span data-stu-id="f195d-124">Condition groups are always concatenated to each other using OR logic.</span></span> <span data-ttu-id="f195d-125">Чтобы запустить новую группу условий, вызовите **Query. бегиннекстграуп**.</span><span class="sxs-lookup"><span data-stu-id="f195d-125">To start a new condition group, call **Query.beginNextGroup**.</span></span>

<span data-ttu-id="f195d-126">В следующей таблице перечислены поддерживаемые значения для *оператора*.</span><span class="sxs-lookup"><span data-stu-id="f195d-126">The following table lists the supported values for *operator*.</span></span>



| <span data-ttu-id="f195d-127">Оператор</span><span class="sxs-lookup"><span data-stu-id="f195d-127">Operator</span></span>            | <span data-ttu-id="f195d-128">Применяется к</span><span class="sxs-lookup"><span data-stu-id="f195d-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="f195d-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="f195d-129">BeginsWith</span></span>          | <span data-ttu-id="f195d-130">Строки</span><span class="sxs-lookup"><span data-stu-id="f195d-130">Strings</span></span>        |
| <span data-ttu-id="f195d-131">Содержит</span><span class="sxs-lookup"><span data-stu-id="f195d-131">Contains</span></span>            | <span data-ttu-id="f195d-132">Строки</span><span class="sxs-lookup"><span data-stu-id="f195d-132">Strings</span></span>        |
| <span data-ttu-id="f195d-133">Равно</span><span class="sxs-lookup"><span data-stu-id="f195d-133">Equals</span></span>              | <span data-ttu-id="f195d-134">Все типы</span><span class="sxs-lookup"><span data-stu-id="f195d-134">All types</span></span>      |
| <span data-ttu-id="f195d-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="f195d-135">GreaterThan</span></span>         | <span data-ttu-id="f195d-136">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="f195d-136">Numbers, Dates</span></span> |
| <span data-ttu-id="f195d-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="f195d-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="f195d-138">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="f195d-138">Numbers, Dates</span></span> |
| <span data-ttu-id="f195d-139">LessThan;</span><span class="sxs-lookup"><span data-stu-id="f195d-139">LessThan</span></span>            | <span data-ttu-id="f195d-140">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="f195d-140">Numbers, Dates</span></span> |
| <span data-ttu-id="f195d-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="f195d-141">LessThanOrEquals</span></span>    | <span data-ttu-id="f195d-142">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="f195d-142">Numbers, Dates</span></span> |
| <span data-ttu-id="f195d-143">нотбегинсвис</span><span class="sxs-lookup"><span data-stu-id="f195d-143">NotBeginsWith</span></span>       | <span data-ttu-id="f195d-144">Строки</span><span class="sxs-lookup"><span data-stu-id="f195d-144">Strings</span></span>        |
| <span data-ttu-id="f195d-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="f195d-145">NotContains</span></span>         | <span data-ttu-id="f195d-146">Строки</span><span class="sxs-lookup"><span data-stu-id="f195d-146">Strings</span></span>        |
| <span data-ttu-id="f195d-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="f195d-147">NotEquals</span></span>           | <span data-ttu-id="f195d-148">Все типы</span><span class="sxs-lookup"><span data-stu-id="f195d-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="f195d-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="f195d-149">Examples</span></span>

<span data-ttu-id="f195d-150">В следующем примере JScript для выполнения примера запроса используется **Query. аддкондитион** и **Query. бегиннекстграуп** .</span><span class="sxs-lookup"><span data-stu-id="f195d-150">The following JScript example uses **Query.addCondition** and **Query.beginNextGroup** to perform an example query.</span></span>


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a><span data-ttu-id="f195d-151">Требования</span><span class="sxs-lookup"><span data-stu-id="f195d-151">Requirements</span></span>



| <span data-ttu-id="f195d-152">Требование</span><span class="sxs-lookup"><span data-stu-id="f195d-152">Requirement</span></span> | <span data-ttu-id="f195d-153">Значение</span><span class="sxs-lookup"><span data-stu-id="f195d-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f195d-154">Версия</span><span class="sxs-lookup"><span data-stu-id="f195d-154">Version</span></span><br/> | <span data-ttu-id="f195d-155">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="f195d-155">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="f195d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f195d-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="f195d-157"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f195d-157"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f195d-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f195d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f195d-159">**Медиаколлектион. createQuery**</span><span class="sxs-lookup"><span data-stu-id="f195d-159">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="f195d-160">**Медиаколлектион. Жетплайлистбикуери**</span><span class="sxs-lookup"><span data-stu-id="f195d-160">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="f195d-161">**Медиаколлектион. Жетстрингколлектионбикуери**</span><span class="sxs-lookup"><span data-stu-id="f195d-161">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="f195d-162">**Объект запроса**</span><span class="sxs-lookup"><span data-stu-id="f195d-162">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="f195d-163">**Query. Бегиннекстграуп**</span><span class="sxs-lookup"><span data-stu-id="f195d-163">**Query.beginNextGroup**</span></span>](query-beginnextgroup.md)
</dt> </dl>

 

 





