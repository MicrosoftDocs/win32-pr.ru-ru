---
title: Ивмпкуери Бегиннекстграуп, метод
description: Метод Бегиннекстграуп начинает новую группу условий. | Ивмпкуери Бегиннекстграуп, метод
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- Бегиннекстграуп метод Windows Media Player
- Бегиннекстграуп метод проигрывателя Windows Media Player, интерфейс Ивмпкуери
- Интерфейс Ивмпкуери Windows Media Player, метод Бегиннекстграуп
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718031"
---
# <a name="iwmpquerybeginnextgroup-method"></a><span data-ttu-id="50870-107">Метод Ивмпкуери:: Бегиннекстграуп</span><span class="sxs-lookup"><span data-stu-id="50870-107">IWMPQuery::beginNextGroup method</span></span>

<span data-ttu-id="50870-108">Метод **бегиннекстграуп** начинает новую группу условий.</span><span class="sxs-lookup"><span data-stu-id="50870-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="50870-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50870-109">Syntax</span></span>


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a><span data-ttu-id="50870-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="50870-110">Parameters</span></span>

<span data-ttu-id="50870-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="50870-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50870-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50870-112">Return value</span></span>

<span data-ttu-id="50870-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="50870-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50870-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50870-114">Remarks</span></span>

<span data-ttu-id="50870-115">Начало новой группы условий означает, что вы завершили текущую группу условий.</span><span class="sxs-lookup"><span data-stu-id="50870-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="50870-116">Новая группа условий всегда объединяется с предыдущей группой условий с помощью логики **или** .</span><span class="sxs-lookup"><span data-stu-id="50870-116">The new condition group is always concatenated to the previous condition group by using **OR** logic.</span></span>

## <a name="examples"></a><span data-ttu-id="50870-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="50870-117">Examples</span></span>

<span data-ttu-id="50870-118">В следующем примере создается сложный запрос с объединением двух групп, каждая из которых содержит условие.</span><span class="sxs-lookup"><span data-stu-id="50870-118">The following example creates a complex query by combing two groups that each contain a condition.</span></span> <span data-ttu-id="50870-119">Результаты запроса извлекаются в виде коллекции строк и отображаются в окне списка.</span><span class="sxs-lookup"><span data-stu-id="50870-119">The results of the query are extracted as a string collection and displayed in a list box.</span></span> <span data-ttu-id="50870-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="50870-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="50870-121">Требования</span><span class="sxs-lookup"><span data-stu-id="50870-121">Requirements</span></span>



| <span data-ttu-id="50870-122">Требование</span><span class="sxs-lookup"><span data-stu-id="50870-122">Requirement</span></span> | <span data-ttu-id="50870-123">Значение</span><span class="sxs-lookup"><span data-stu-id="50870-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50870-124">Версия</span><span class="sxs-lookup"><span data-stu-id="50870-124">Version</span></span><br/>   | <span data-ttu-id="50870-125">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="50870-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="50870-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="50870-126">Namespace</span></span><br/> | <span data-ttu-id="50870-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="50870-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="50870-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="50870-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="50870-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="50870-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50870-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50870-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50870-131">**IWMPMediaCollection2. createQuery (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="50870-131">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="50870-132">**IWMPMediaCollection2. Жетплайлистбикуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="50870-132">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="50870-133">**IWMPMediaCollection2. Жетстрингколлектионбикуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="50870-133">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="50870-134">**Интерфейс Ивмпкуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="50870-134">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





