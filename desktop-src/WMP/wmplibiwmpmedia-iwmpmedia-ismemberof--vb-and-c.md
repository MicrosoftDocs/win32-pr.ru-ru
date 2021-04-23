---
title: Ивмпмедиа isMemberOf, метод
description: Метод isMemberOf возвращает значение, указывающее, является ли указанный элемент мультимедиа членом указанного списка воспроизведения.
ms.assetid: 491e0dd5-38e5-47a5-9c94-f1d27d297f8d
keywords:
- isMemberOf метод Windows Media Player
- isMemberOf метод проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, метод isMemberOf
topic_type:
- apiref
api_name:
- IWMPMedia.isMemberOf
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f627e9b2f0e1c4b226dda13d280d521ad52df2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669244"
---
# <a name="iwmpmediaismemberof-method"></a><span data-ttu-id="d9d2a-106">Метод Ивмпмедиа:: isMemberOf</span><span class="sxs-lookup"><span data-stu-id="d9d2a-106">IWMPMedia::isMemberOf method</span></span>

<span data-ttu-id="d9d2a-107">Метод **isMemberOf** возвращает значение, указывающее, является ли указанный элемент мультимедиа членом указанного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-107">The **isMemberOf** method returns a value indicating whether the specified media item is a member of the specified playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9d2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9d2a-108">Syntax</span></span>


```CSharp
public System.Boolean isMemberOf(
  IWMPPlaylist pPlaylist
);
```


```VB

Public Function isMemberOf( _
  ByVal pPlaylist As IWMPPlaylist _
) As System.Boolean
Implements IWMPMedia.isMemberOf
```





## <a name="parameters"></a><span data-ttu-id="d9d2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9d2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9d2a-110">*пплайлист* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9d2a-110">*pPlaylist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9d2a-111">Интерфейс **вмплиб. ивмпплайлист** .</span><span class="sxs-lookup"><span data-stu-id="d9d2a-111">A **WMPLib.IWMPPlaylist** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9d2a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9d2a-112">Return value</span></span>

<span data-ttu-id="d9d2a-113">Значение **System. Boolean** , указывающее, является ли элемент мультимедиа членом списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-113">A **System.Boolean** value that indicates whether the media item is a member of the playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9d2a-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9d2a-114">Remarks</span></span>

<span data-ttu-id="d9d2a-115">Этот метод не может проверять списки воспроизведения, полученные через интерфейс **ивмпмедиаколлектион** .</span><span class="sxs-lookup"><span data-stu-id="d9d2a-115">This method cannot check playlists retrieved through the **IWMPMediaCollection** interface.</span></span> <span data-ttu-id="d9d2a-116">Чтобы проверить, является ли элемент мультимедиа членом определенного списка воспроизведения, извлеките коллекцию списков воспроизведения с помощью свойства **аксвиндовсмедиаплайер. плайлистколлектион** .</span><span class="sxs-lookup"><span data-stu-id="d9d2a-116">To test whether a media item is a member of a particular named playlist, retrieve the playlist collection with the **AxWindowsMediaPlayer.playlistCollection** property.</span></span> <span data-ttu-id="d9d2a-117">После получения коллекции Извлеките отдельный список воспроизведения, вызвав метод **ивмпплайлистколлектион. жетбинаме** .</span><span class="sxs-lookup"><span data-stu-id="d9d2a-117">Once you retrieve the collection, retrieve the individual playlist by calling the **IWMPPlaylistCollection.getByName** method.</span></span>

<span data-ttu-id="d9d2a-118">Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-118">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="d9d2a-119">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d9d2a-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d9d2a-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="d9d2a-120">Examples</span></span>

<span data-ttu-id="d9d2a-121">В следующем примере **isMemberOf** используется для проверки того, является ли текущий элемент мультимедиа членом списка воспроизведения с именем вся музыка.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-121">The following example uses **isMemberOf** to test whether the current media item is a member of the playlist named All Music.</span></span> <span data-ttu-id="d9d2a-122">Если это не так, текущий элемент мультимедиа добавляется к списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-122">If it is not, the current media item is appended to the playlist.</span></span> <span data-ttu-id="d9d2a-123">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the playlist named All Music.
WMPLib.IWMPPlaylist sPlaylist = player.playlistCollection.getByName("All Music").Item(0);

// Test whether the current media item is a member of the All Music playlist.
// If it is not a member, append the current media item to the playlist.
if (player.currentMedia.isMemberOf(sPlaylist) == false)
{
    sPlaylist.appendItem(player.currentMedia);
}
```


```VB

' Get an interface to the playlist named All Music.
Dim sPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Test whether the current media item is a member of the All Music playlist.
&#39; If it is not a member, then append the current media item to the playlist.
If (player.currentMedia.isMemberOf(sPlaylist) = False) Then

    sPlaylist.appendItem(player.currentMedia)

End If
```





## <a name="requirements"></a><span data-ttu-id="d9d2a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d9d2a-124">Requirements</span></span>



| <span data-ttu-id="d9d2a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d9d2a-125">Requirement</span></span> | <span data-ttu-id="d9d2a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d9d2a-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9d2a-127">Версия</span><span class="sxs-lookup"><span data-stu-id="d9d2a-127">Version</span></span><br/>   | <span data-ttu-id="d9d2a-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d9d2a-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d9d2a-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9d2a-129">Namespace</span></span><br/> | <span data-ttu-id="d9d2a-130">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="d9d2a-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d9d2a-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="d9d2a-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d9d2a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d9d2a-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9d2a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9d2a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9d2a-134">**Аксвиндовсмедиаплайер. Плайлистколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d9d2a-134">**AxWindowsMediaPlayer.playlistCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playlistcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d9d2a-135">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d9d2a-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d9d2a-136">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d9d2a-136">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d9d2a-137">**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d9d2a-137">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





