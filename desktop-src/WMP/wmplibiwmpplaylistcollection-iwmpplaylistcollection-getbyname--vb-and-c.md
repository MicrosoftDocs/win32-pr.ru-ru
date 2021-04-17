---
title: Ивмпплайлистколлектион Жетбинаме, метод
description: Метод Жетбинаме возвращает интерфейс Ивмпплайлистаррай, который предоставляет доступ к спискам воспроизведения с указанным именем, если таковые имеются.
ms.assetid: d41afab1-4103-4f59-a432-21a502499444
keywords:
- Жетбинаме метод Windows Media Player
- Жетбинаме метод проигрывателя Windows Media Player, интерфейс Ивмпплайлистколлектион
- Интерфейс Ивмпплайлистколлектион Windows Media Player, метод Жетбинаме
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e51f83b4db019286c04762a081e649fec282135e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708432"
---
# <a name="iwmpplaylistcollectiongetbyname-method"></a><span data-ttu-id="774e4-106">Метод Ивмпплайлистколлектион:: Жетбинаме</span><span class="sxs-lookup"><span data-stu-id="774e4-106">IWMPPlaylistCollection::getByName method</span></span>

<span data-ttu-id="774e4-107">Метод **жетбинаме** возвращает интерфейс **ивмпплайлистаррай** , который предоставляет доступ к спискам воспроизведения с указанным именем, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="774e4-107">The **getByName** method returns a **IWMPPlaylistArray** interface that provides access to playlists with the specified name, if any exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="774e4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="774e4-108">Syntax</span></span>


```CSharp
public IWMPPlaylistArray getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylistArray
Implements IWMPPlaylistCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="774e4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="774e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="774e4-110">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="774e4-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="774e4-111">**Строка System. String** , которая является именем списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="774e4-111">A **System.String** that is the name of the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="774e4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="774e4-112">Return value</span></span>

<span data-ttu-id="774e4-113">Интерфейс **вмплиб. ивмпплайлистаррай** для извлеченного массива списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="774e4-113">A **WMPLib.IWMPPlaylistArray** interface for the retrieved array of playlists.</span></span>

## <a name="remarks"></a><span data-ttu-id="774e4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="774e4-114">Remarks</span></span>

<span data-ttu-id="774e4-115">Используйте **ивмпплайлистаррай. Count** , чтобы определить, существует ли список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="774e4-115">Use **IWMPPlaylistArray.count** to determine whether a playlist exists.</span></span> <span data-ttu-id="774e4-116">Если значение **Count** равно нулю, массив пуст.</span><span class="sxs-lookup"><span data-stu-id="774e4-116">If **count** is zero, the array is empty.</span></span>

<span data-ttu-id="774e4-117">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="774e4-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="774e4-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="774e4-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="774e4-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="774e4-119">Examples</span></span>

<span data-ttu-id="774e4-120">В следующем примере используется **жетбинаме** для проверки коллекции списков воспроизведения с именем "Избранное--4 и 5 Star".</span><span class="sxs-lookup"><span data-stu-id="774e4-120">The following example uses **getByName** to check the playlist collection for a playlist named "Favorites -- 4 and 5 star rated".</span></span> <span data-ttu-id="774e4-121">Если список воспроизведения с таким именем существует, **жетбинаме** устанавливает его как текущий список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="774e4-121">If a playlist by that name exists, **getByName** sets it as the current playlist.</span></span> <span data-ttu-id="774e4-122">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="774e4-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the count of the playlists named "Favorites -- 4 and 5 star rated".
int checkit = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").count;

// Since duplicate playlist names are allowed, the count returned
// will be either zero (no playlist) or greater than zero (playlist exists).
if (checkit > 0)
{
    // Retrieve a playlist array containing "Favorites -- 4 and 5 star rated".
    // Assume that there is only one playlist with that name, and assign it to the 
    // current playlist.
    player.currentPlaylist = player.playlistCollection.getByName("Favorites -- 4 and 5 star rated").Item(0);
}
```


```VB

'  Get the count of the playlists named &quot;Favorites -- 4 and 5 star rated&quot;.
Dim checkit As Integer = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).count

&#39;  Since duplicate playlist names are allowed, the count returned
&#39;  will be either zero (no playlist) or greater than zero (playlist exists).
If (checkit > 0) Then

    &#39;  Retrieve a playlist array object containing &quot;Favorites -- 4 and 5 star rated&quot;.
    &#39;  Assume that there is only one playlist with that name, and assign it to the 
    &#39;  current playlist.
    player.currentPlaylist = player.playlistCollection.getByName(&quot;Favorites -- 4 and 5 star rated&quot;).Item(0)

End If
```





## <a name="requirements"></a><span data-ttu-id="774e4-123">Требования</span><span class="sxs-lookup"><span data-stu-id="774e4-123">Requirements</span></span>



| <span data-ttu-id="774e4-124">Требование</span><span class="sxs-lookup"><span data-stu-id="774e4-124">Requirement</span></span> | <span data-ttu-id="774e4-125">Значение</span><span class="sxs-lookup"><span data-stu-id="774e4-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="774e4-126">Версия</span><span class="sxs-lookup"><span data-stu-id="774e4-126">Version</span></span><br/>   | <span data-ttu-id="774e4-127">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="774e4-127">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="774e4-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="774e4-128">Namespace</span></span><br/> | <span data-ttu-id="774e4-129">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="774e4-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="774e4-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="774e4-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="774e4-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="774e4-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774e4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="774e4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774e4-133">**Интерфейс Ивмпплайлистаррай (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="774e4-133">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="774e4-134">**Ивмпплайлистаррай. Count (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="774e4-134">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="774e4-135">**Интерфейс Ивмпплайлистколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="774e4-135">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





