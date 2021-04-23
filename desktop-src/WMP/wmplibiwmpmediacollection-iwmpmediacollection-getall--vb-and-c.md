---
title: Ивмпмедиаколлектион Жеталл, метод
description: Метод Жеталл возвращает интерфейс Ивмпплайлист, соответствующий списку воспроизведения, содержащему все элементы мультимедиа в библиотеке.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- Жеталл метод Windows Media Player
- Жеталл метод проигрывателя Windows Media Player, интерфейс Ивмпмедиаколлектион
- Интерфейс Ивмпмедиаколлектион Windows Media Player, метод Жеталл
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665101"
---
# <a name="iwmpmediacollectiongetall-method"></a><span data-ttu-id="a8fd4-106">Метод Ивмпмедиаколлектион:: Жеталл</span><span class="sxs-lookup"><span data-stu-id="a8fd4-106">IWMPMediaCollection::getAll method</span></span>

<span data-ttu-id="a8fd4-107">Метод **жеталл** возвращает интерфейс **ивмпплайлист** , соответствующий списку воспроизведения, содержащему все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-107">The **getAll** method returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8fd4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8fd4-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="a8fd4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8fd4-109">Parameters</span></span>

<span data-ttu-id="a8fd4-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8fd4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8fd4-111">Return value</span></span>

<span data-ttu-id="a8fd4-112">Интерфейс **вмплиб. ивмпплайлист** для списка воспроизведения, который содержит все запрошенные элементы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-112">The **WMPLib.IWMPPlaylist** interface for the playlist that contains all of the requested media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8fd4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8fd4-113">Remarks</span></span>

<span data-ttu-id="a8fd4-114">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a8fd4-115">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a8fd4-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a8fd4-116">Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение метода **жеталл** зависит от того, какой из этих двух способов вы используете.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-116">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getAll** method depends on which of those two ways you use.</span></span> <span data-ttu-id="a8fd4-117">При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)метод **жеталл** возвращает все элементы мультимедиа в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-117">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getAll** method returns all the media items in the library.</span></span> <span data-ttu-id="a8fd4-118">Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)метод **жеталл** возвращает только звуковые элементы в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-118">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getAll** method returns only the audio items in the library.</span></span>

## <a name="examples"></a><span data-ttu-id="a8fd4-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8fd4-119">Examples</span></span>

<span data-ttu-id="a8fd4-120">В следующем примере **жеталл** используется для воспроизведения элементов мультимедиа случайным образом из коллекции носителей.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-120">The following example uses **getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="a8fd4-121">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="a8fd4-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="a8fd4-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a8fd4-122">Requirements</span></span>



| <span data-ttu-id="a8fd4-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a8fd4-123">Requirement</span></span> | <span data-ttu-id="a8fd4-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a8fd4-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fd4-125">Версия</span><span class="sxs-lookup"><span data-stu-id="a8fd4-125">Version</span></span><br/>   | <span data-ttu-id="a8fd4-126">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a8fd4-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a8fd4-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a8fd4-127">Namespace</span></span><br/> | <span data-ttu-id="a8fd4-128">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a8fd4-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a8fd4-129">Сборка</span><span class="sxs-lookup"><span data-stu-id="a8fd4-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a8fd4-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a8fd4-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8fd4-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8fd4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fd4-132">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a8fd4-132">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8fd4-133">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a8fd4-133">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





