---
title: Ивмпкуери Аддкондитион, метод
description: Метод Аддкондитион добавляет условие в составной запрос с помощью логики и.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- Аддкондитион метод Windows Media Player
- Аддкондитион метод проигрывателя Windows Media Player, интерфейс Ивмпкуери
- Интерфейс Ивмпкуери Windows Media Player, метод Аддкондитион
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718032"
---
# <a name="iwmpqueryaddcondition-method"></a><span data-ttu-id="af985-106">Метод Ивмпкуери:: Аддкондитион</span><span class="sxs-lookup"><span data-stu-id="af985-106">IWMPQuery::addCondition method</span></span>

<span data-ttu-id="af985-107">Метод **аддкондитион** добавляет условие в составной запрос с помощью логики **и** .</span><span class="sxs-lookup"><span data-stu-id="af985-107">The **addCondition** method adds a condition to the compound query using **AND** logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="af985-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af985-108">Syntax</span></span>


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a><span data-ttu-id="af985-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="af985-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af985-110">*бстраттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af985-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af985-111">**Строка System. String** , которая представляет собой имя атрибута, добавляемого в запрос.</span><span class="sxs-lookup"><span data-stu-id="af985-111">A **System.String** that is the name of the attribute to be added to the query.</span></span>

</dd> <dt>

<span data-ttu-id="af985-112">*бстроператор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af985-112">*bstrOperator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af985-113">**Строка System. String** , которая является оператором.</span><span class="sxs-lookup"><span data-stu-id="af985-113">A **System.String** that is the operator.</span></span> <span data-ttu-id="af985-114">Поддерживаемые значения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="af985-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="af985-115">*бстрвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af985-115">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af985-116">**Строка System. String** , которая является значением атрибута.</span><span class="sxs-lookup"><span data-stu-id="af985-116">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af985-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af985-117">Return value</span></span>

<span data-ttu-id="af985-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="af985-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af985-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af985-119">Remarks</span></span>

<span data-ttu-id="af985-120">Условия, содержащиеся в составном запросе, организованы в группы условий.</span><span class="sxs-lookup"><span data-stu-id="af985-120">Conditions contained in a compound query are organized into condition groups.</span></span> <span data-ttu-id="af985-121">Несколько условий в группе условий всегда объединяются с помощью логики **и** .</span><span class="sxs-lookup"><span data-stu-id="af985-121">Multiple conditions within a condition group are always concatenated by using **AND** logic.</span></span> <span data-ttu-id="af985-122">Группы условий всегда объединяются друг с другом с помощью логики **или** .</span><span class="sxs-lookup"><span data-stu-id="af985-122">Condition groups are always concatenated to each other by using **OR** logic.</span></span> <span data-ttu-id="af985-123">Чтобы запустить новую группу условий, вызовите метод [ивмпкуери. бегиннекстграуп](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="af985-123">To start a new condition group, call [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span></span>

<span data-ttu-id="af985-124">В составных запросах, использующих **ивмпкуери** , регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="af985-124">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="af985-125">Список значений для параметра *бстраттрибуте* можно найти в [алфавитном справочнике по атрибутам](alphabetical-attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="af985-125">A list of values for the *bstrAttribute* parameter can be found in [Alphabetical Attribute Reference](alphabetical-attribute-reference.md).</span></span>

<span data-ttu-id="af985-126">В следующей таблице перечислены поддерживаемые значения для *бстроператор*.</span><span class="sxs-lookup"><span data-stu-id="af985-126">The following table lists the supported values for *bstrOperator*.</span></span>



| <span data-ttu-id="af985-127">Строка</span><span class="sxs-lookup"><span data-stu-id="af985-127">String</span></span>              | <span data-ttu-id="af985-128">Применяется к</span><span class="sxs-lookup"><span data-stu-id="af985-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="af985-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="af985-129">BeginsWith</span></span>          | <span data-ttu-id="af985-130">Строки</span><span class="sxs-lookup"><span data-stu-id="af985-130">Strings</span></span>        |
| <span data-ttu-id="af985-131">Содержит</span><span class="sxs-lookup"><span data-stu-id="af985-131">Contains</span></span>            | <span data-ttu-id="af985-132">Строки</span><span class="sxs-lookup"><span data-stu-id="af985-132">Strings</span></span>        |
| <span data-ttu-id="af985-133">Равно</span><span class="sxs-lookup"><span data-stu-id="af985-133">Equals</span></span>              | <span data-ttu-id="af985-134">Все типы</span><span class="sxs-lookup"><span data-stu-id="af985-134">All types</span></span>      |
| <span data-ttu-id="af985-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="af985-135">GreaterThan</span></span>         | <span data-ttu-id="af985-136">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="af985-136">Numbers, Dates</span></span> |
| <span data-ttu-id="af985-137">GreaterThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="af985-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="af985-138">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="af985-138">Numbers, Dates</span></span> |
| <span data-ttu-id="af985-139">LessThan;</span><span class="sxs-lookup"><span data-stu-id="af985-139">LessThan</span></span>            | <span data-ttu-id="af985-140">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="af985-140">Numbers, Dates</span></span> |
| <span data-ttu-id="af985-141">LessThanOrEquals</span><span class="sxs-lookup"><span data-stu-id="af985-141">LessThanOrEquals</span></span>    | <span data-ttu-id="af985-142">Числа, даты</span><span class="sxs-lookup"><span data-stu-id="af985-142">Numbers, Dates</span></span> |
| <span data-ttu-id="af985-143">нотбегинсвис</span><span class="sxs-lookup"><span data-stu-id="af985-143">NotBeginsWith</span></span>       | <span data-ttu-id="af985-144">Строки</span><span class="sxs-lookup"><span data-stu-id="af985-144">Strings</span></span>        |
| <span data-ttu-id="af985-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="af985-145">NotContains</span></span>         | <span data-ttu-id="af985-146">Строки</span><span class="sxs-lookup"><span data-stu-id="af985-146">Strings</span></span>        |
| <span data-ttu-id="af985-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="af985-147">NotEquals</span></span>           | <span data-ttu-id="af985-148">Все типы</span><span class="sxs-lookup"><span data-stu-id="af985-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="af985-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="af985-149">Examples</span></span>

<span data-ttu-id="af985-150">Следующий пример создает запрос, добавляет к нему два условия и использует этот запрос для извлечения результатов запроса в виде коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="af985-150">The following example creates a query, adds two conditions to it, and uses that query to extract the results of the query as a string collection.</span></span> <span data-ttu-id="af985-151">Затем результаты отображаются в окне списка.</span><span class="sxs-lookup"><span data-stu-id="af985-151">The results are then displayed in a list box.</span></span> <span data-ttu-id="af985-152">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="af985-152">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="af985-153">Требования</span><span class="sxs-lookup"><span data-stu-id="af985-153">Requirements</span></span>



| <span data-ttu-id="af985-154">Требование</span><span class="sxs-lookup"><span data-stu-id="af985-154">Requirement</span></span> | <span data-ttu-id="af985-155">Значение</span><span class="sxs-lookup"><span data-stu-id="af985-155">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af985-156">Версия</span><span class="sxs-lookup"><span data-stu-id="af985-156">Version</span></span><br/>   | <span data-ttu-id="af985-157">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="af985-157">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="af985-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="af985-158">Namespace</span></span><br/> | <span data-ttu-id="af985-159">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="af985-159">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="af985-160">Сборка</span><span class="sxs-lookup"><span data-stu-id="af985-160">Assembly</span></span><br/>  | <dl> <span data-ttu-id="af985-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="af985-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af985-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af985-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af985-163">**Алфавитный справочник по атрибутам**</span><span class="sxs-lookup"><span data-stu-id="af985-163">**Alphabetical Attribute Reference**</span></span>](alphabetical-attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="af985-164">**IWMPMediaCollection2. createQuery (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="af985-164">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af985-165">**IWMPMediaCollection2. Жетплайлистбикуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="af985-165">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af985-166">**IWMPMediaCollection2. Жетстрингколлектионбикуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="af985-166">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="af985-167">**Интерфейс Ивмпкуери**</span><span class="sxs-lookup"><span data-stu-id="af985-167">**IWMPQuery Interface**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





