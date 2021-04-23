---
title: IWMPMediaCollection2 createQuery, метод
description: Метод createQuery возвращает интерфейс Ивмпкуери, представляющий новый запрос.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- createQuery метод Windows Media Player
- createQuery метод проигрывателя Windows Media Player, интерфейс IWMPMediaCollection2
- Интерфейс IWMPMediaCollection2 Windows Media Player, метод createQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699194"
---
# <a name="iwmpmediacollection2createquery-method"></a><span data-ttu-id="76646-106">Метод IWMPMediaCollection2:: createQuery</span><span class="sxs-lookup"><span data-stu-id="76646-106">IWMPMediaCollection2::createQuery method</span></span>

<span data-ttu-id="76646-107">`createQuery`Метод возвращает интерфейс **ивмпкуери** , представляющий новый запрос.</span><span class="sxs-lookup"><span data-stu-id="76646-107">The `createQuery` method returns an **IWMPQuery** interface that represents a new query.</span></span>

## <a name="syntax"></a><span data-ttu-id="76646-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76646-108">Syntax</span></span>


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a><span data-ttu-id="76646-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="76646-109">Parameters</span></span>

<span data-ttu-id="76646-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="76646-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="76646-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76646-111">Return value</span></span>

<span data-ttu-id="76646-112">Интерфейс **вмплиб. ивмпкуери** , представляющий новый пустой запрос.</span><span class="sxs-lookup"><span data-stu-id="76646-112">A **WMPLib.IWMPQuery** interface that represents a new, empty query.</span></span>

## <a name="remarks"></a><span data-ttu-id="76646-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76646-113">Remarks</span></span>

<span data-ttu-id="76646-114">Создание нового запроса — это первый шаг к созданию составного запроса.</span><span class="sxs-lookup"><span data-stu-id="76646-114">Creating a new query is the first step toward creating a compound query.</span></span>

## <a name="examples"></a><span data-ttu-id="76646-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="76646-115">Examples</span></span>

<span data-ttu-id="76646-116">В следующем примере используется `createQuery` для получения интерфейса **ивмпкуери** , который инициализируется значением NULL.</span><span class="sxs-lookup"><span data-stu-id="76646-116">The following example uses `createQuery` to get an **IWMPQuery** interface that is initialized to null.</span></span> <span data-ttu-id="76646-117">Так как для этого запроса не было добавлено никаких условий, при его использовании в качестве аргумента в методе **жетстрингколлектионбикуери** метод возвращает коллекцию строк, содержащую все элементы мультимедиа указанного типа мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="76646-117">Because this query has no conditions added to it, when it is used as an argument in the **getStringCollectionByQuery** method, the method will return a string collection that contains all of the media items of the specified media type.</span></span> <span data-ttu-id="76646-118">Затем Коллекция строк отображается в списке.</span><span class="sxs-lookup"><span data-stu-id="76646-118">The string collection is then displayed in a list box.</span></span>


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="76646-119">Требования</span><span class="sxs-lookup"><span data-stu-id="76646-119">Requirements</span></span>



| <span data-ttu-id="76646-120">Требование</span><span class="sxs-lookup"><span data-stu-id="76646-120">Requirement</span></span> | <span data-ttu-id="76646-121">Значение</span><span class="sxs-lookup"><span data-stu-id="76646-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76646-122">Версия</span><span class="sxs-lookup"><span data-stu-id="76646-122">Version</span></span><br/>   | <span data-ttu-id="76646-123">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="76646-123">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="76646-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="76646-124">Namespace</span></span><br/> | <span data-ttu-id="76646-125">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="76646-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="76646-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="76646-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="76646-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="76646-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76646-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76646-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76646-129">**Интерфейс IWMPMediaCollection2 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="76646-129">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76646-130">**Интерфейс Ивмпкуери (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="76646-130">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





