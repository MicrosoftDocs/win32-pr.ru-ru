---
title: Ивмпплайлистколлектион Невплайлист, метод
description: Метод Невплайлист возвращает интерфейс Ивмпплайлист для нового пустого списка воспроизведения в библиотеке.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- Невплайлист метод Windows Media Player
- Невплайлист метод проигрывателя Windows Media Player, интерфейс Ивмпплайлистколлектион
- Интерфейс Ивмпплайлистколлектион Windows Media Player, метод Невплайлист
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704125"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a><span data-ttu-id="5beb9-106">Метод Ивмпплайлистколлектион:: Невплайлист</span><span class="sxs-lookup"><span data-stu-id="5beb9-106">IWMPPlaylistCollection::newPlaylist method</span></span>

<span data-ttu-id="5beb9-107">Метод **невплайлист** возвращает интерфейс **ивмпплайлист** для нового пустого списка воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="5beb9-107">The **newPlaylist** method returns an **IWMPPlaylist** interface for a new, empty playlist in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="5beb9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5beb9-108">Syntax</span></span>


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a><span data-ttu-id="5beb9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5beb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5beb9-110">*bstrName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5beb9-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb9-111">**Строка System. String** , которая является именем нового списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5beb9-111">A **System.String** that is the name of the new playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5beb9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5beb9-112">Return value</span></span>

<span data-ttu-id="5beb9-113">Интерфейс **вмплиб. ивмпплайлист** для нового списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="5beb9-113">A **WMPLib.IWMPPlaylist** interface for the new playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="5beb9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5beb9-114">Remarks</span></span>

<span data-ttu-id="5beb9-115">Этот метод создает пустой список воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="5beb9-115">This method creates an empty playlist in the library.</span></span> <span data-ttu-id="5beb9-116">Чтобы заполнить список воспроизведения с помощью элементов мультимедиа, используйте **ивмпплайлист. аппендитем** или **ивмпплайлист. insertItem**.</span><span class="sxs-lookup"><span data-stu-id="5beb9-116">To fill the playlist with media items, use **IWMPPlaylist.appendItem** or **IWMPPlaylist.insertItem**.</span></span>

<span data-ttu-id="5beb9-117">В библиотеке разрешено несколько списков воспроизведения с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="5beb9-117">Multiple playlists having the same name are permitted in the library.</span></span> <span data-ttu-id="5beb9-118">Чтобы избежать создания дубликата имени списка воспроизведения с помощью этого метода, используйте метод **жетбинаме** и **ивмпплайлистаррай. Count** , чтобы узнать, существует ли уже список воспроизведения с определенным именем.</span><span class="sxs-lookup"><span data-stu-id="5beb9-118">To avoid creating a duplicate playlist name with this method, use the **getByName** method and **IWMPPlaylistArray.count** to discover whether a playlist with a particular name already exists.</span></span>

<span data-ttu-id="5beb9-119">Начальные и конечные пробелы не допускаются в именах списков воспроизведения и автоматически удаляются из значения, указанного для параметра *bstrName* .</span><span class="sxs-lookup"><span data-stu-id="5beb9-119">Leading and trailing spaces are not permitted in playlist names, and are automatically removed from the value specified for the *bstrName* parameter.</span></span>

<span data-ttu-id="5beb9-120">Перед вызовом этого метода необходимо иметь полный доступ к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="5beb9-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="5beb9-121">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5beb9-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5beb9-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="5beb9-122">Examples</span></span>

<span data-ttu-id="5beb9-123">В следующем примере создается пустой список воспроизведения с именем «Срилист», который добавляется в коллекцию списков воспроизведения и возвращается в него интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5beb9-123">The following example creates a new empty playlist called "ThreeList", adds it to the playlist collection, and returns an interface to it.</span></span> <span data-ttu-id="5beb9-124">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="5beb9-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a><span data-ttu-id="5beb9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="5beb9-125">Requirements</span></span>



| <span data-ttu-id="5beb9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="5beb9-126">Requirement</span></span> | <span data-ttu-id="5beb9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="5beb9-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5beb9-128">Версия</span><span class="sxs-lookup"><span data-stu-id="5beb9-128">Version</span></span><br/>   | <span data-ttu-id="5beb9-129">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5beb9-129">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="5beb9-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5beb9-130">Namespace</span></span><br/> | <span data-ttu-id="5beb9-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="5beb9-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="5beb9-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="5beb9-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="5beb9-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="5beb9-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5beb9-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5beb9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5beb9-135">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5beb9-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5beb9-136">**Ивмпплайлист. Аппендитем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5beb9-136">**IWMPPlaylist.appendItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5beb9-137">**Ивмпплайлист. insertItem (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5beb9-137">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5beb9-138">**Ивмпплайлистаррай. Count (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5beb9-138">**IWMPPlaylistArray.count (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5beb9-139">**Интерфейс Ивмпплайлистколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5beb9-139">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="5beb9-140">**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="5beb9-140">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





