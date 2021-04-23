---
title: Ивмпмедиа Саурцеурл, свойство
description: Свойство Саурцеурл получает URL-адрес элемента мультимедиа.
ms.assetid: adaef82c-eeed-4cce-859b-c54b9c8fa085
keywords:
- Проигрыватель Windows Media для свойства Саурцеурл
- Саурцеурл свойство проигрывателя Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Саурцеурл
topic_type:
- apiref
api_name:
- IWMPMedia.sourceURL
- IWMPMedia.get_sourceURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ad2cdb2c0a67f65f7b0cf722d1b613307806d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668585"
---
# <a name="iwmpmediasourceurl-property"></a><span data-ttu-id="ac01a-106">Свойство Ивмпмедиа:: Саурцеурл</span><span class="sxs-lookup"><span data-stu-id="ac01a-106">IWMPMedia::sourceURL property</span></span>

<span data-ttu-id="ac01a-107">Свойство **саурцеурл** получает URL-адрес элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ac01a-107">The **sourceURL** property gets the URL of the media item.</span></span>

<span data-ttu-id="ac01a-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac01a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac01a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac01a-109">Syntax</span></span>


```CSharp
public System.String sourceURL {get;}
```


```VB

Public ReadOnly Property sourceURL As System.String
```





## <a name="property-value"></a><span data-ttu-id="ac01a-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac01a-110">Property value</span></span>

<span data-ttu-id="ac01a-111">**Строка System. String** , которая является URL-адресом источника.</span><span class="sxs-lookup"><span data-stu-id="ac01a-111">A **System.String** that is the source URL.</span></span>

## <a name="examples"></a><span data-ttu-id="ac01a-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="ac01a-112">Examples</span></span>

<span data-ttu-id="ac01a-113">В следующем примере **саурцеурл** используется для получения URL-адреса первого элемента мультимедиа в списке воспроизведения «все музыкальные файлы». затем URL-адрес элемента мультимедиа присваивается свойству URL-адрес объекта Player.</span><span class="sxs-lookup"><span data-stu-id="ac01a-113">The following example uses **sourceURL** to retrieve the URL of the first media item in the "All Music" playlist; the URL of the media item is then assigned to the player object URL property.</span></span> <span data-ttu-id="ac01a-114">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="ac01a-114">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the All Music Playlist. 
WMPLib.IWMPPlaylist pl = player.playlistCollection.getByName("All Music").Item(0);

// Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)pl.get_Item(0);

// Change the URL property of the player to the URL of the media item.
player.URL = media.sourceURL;

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Get an interface to the All Music Playlist. 
Dim pl As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;All Music&quot;).Item(0)

&#39; Store a WMPLib.IWMPMedia3 interface to the first media item in the playlist. 
Dim media As WMPLib.IWMPMedia3 = pl.Item(0)

&#39; Change the URL property of the player to the URL of the media item.
player.URL = Media.sourceURL

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="ac01a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ac01a-115">Requirements</span></span>



| <span data-ttu-id="ac01a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ac01a-116">Requirement</span></span> | <span data-ttu-id="ac01a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ac01a-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac01a-118">Версия</span><span class="sxs-lookup"><span data-stu-id="ac01a-118">Version</span></span><br/>   | <span data-ttu-id="ac01a-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ac01a-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ac01a-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ac01a-120">Namespace</span></span><br/> | <span data-ttu-id="ac01a-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="ac01a-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ac01a-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="ac01a-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ac01a-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ac01a-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac01a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac01a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac01a-125">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="ac01a-125">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





