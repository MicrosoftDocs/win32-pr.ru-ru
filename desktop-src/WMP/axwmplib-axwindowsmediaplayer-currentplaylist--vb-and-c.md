---
title: Аксвиндовсмедиаплайер. Куррентплайлист, свойство
description: Свойство Куррентплайлист Возвращает или задает текущий интерфейс Ивмпплайлист, предоставляющий простой способ организации и управления мультимедийными элементами в списке.
ms.assetid: d5a9f126-a628-499c-a012-8a47c6c987ef
keywords:
- Проигрыватель Windows Media для свойства Куррентплайлист
- Куррентплайлист свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Куррентплайлист
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentPlaylist
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f5b91a2e65b81fd1f13da0bad5f77c5ea1415
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698800"
---
# <a name="axwindowsmediaplayercurrentplaylist-property"></a><span data-ttu-id="f249b-106">Аксвиндовсмедиаплайер. Куррентплайлист, свойство</span><span class="sxs-lookup"><span data-stu-id="f249b-106">AxWindowsMediaPlayer.currentPlaylist property</span></span>

<span data-ttu-id="f249b-107">Свойство Куррентплайлист Возвращает или задает текущий интерфейс **ивмпплайлист** , предоставляющий простой способ организации и управления мультимедийными элементами в списке.</span><span class="sxs-lookup"><span data-stu-id="f249b-107">The currentPlaylist property gets or sets the current **IWMPPlaylist** interface that provides an easy way to organize and manipulate media items in a list.</span></span>

## <a name="syntax"></a><span data-ttu-id="f249b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f249b-108">Syntax</span></span>


```CSharp
public IWMPPlaylist currentPlaylist {get; set;}
```


```VB

Public Property currentPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="f249b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f249b-109">Property value</span></span>

<span data-ttu-id="f249b-110">Интерфейс Вмплиб. Ивмпплайлист, предоставляющий доступ к текущему списку воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="f249b-110">The WMPLib.IWMPPlaylist interface that provides access to the current playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="f249b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f249b-111">Remarks</span></span>

<span data-ttu-id="f249b-112">Значение, если свойство Ивмпсеттингс. Автозапуск (также доступно через Аксвиндовсмедиаплайер. Settings **). Автозапуск**) имеет значение true, воспроизведение начинается автоматически при установке **куррентплайлист**.</span><span class="sxs-lookup"><span data-stu-id="f249b-112">If the IWMPSettings.autoStart property (also accessed via AxWindowsMediaPlayer.settings.**autoStart**) is true, playback begins automatically whenever you set **currentPlaylist**.</span></span>

<span data-ttu-id="f249b-113">Это свойство принимает интерфейс Ивмпплайлист, который может быть получен несколькими способами, например путем получения значения из *ивмпплайлистаррай*. **Item** или *ивмпплайлистколлектион*. свойства **невплайлист** .</span><span class="sxs-lookup"><span data-stu-id="f249b-113">This property takes an IWMPPlaylist interface, which can be acquired in several ways, such as by getting the value from the *IWMPPlaylistArray*.**Item** or *IWMPPlaylistCollection*.**newPlaylist** properties.</span></span> <span data-ttu-id="f249b-114">Чтобы загрузить элемент **списка воспроизведения** с помощью имени файла, задайте свойство URL-адреса или используйте аксвиндовсмедиаплайер. **невплайлист**.</span><span class="sxs-lookup"><span data-stu-id="f249b-114">To load a **playlist** item using a file name, set the URL property or use AxWindowsMediaPlayer.**newPlaylist**.</span></span>

## <a name="examples"></a><span data-ttu-id="f249b-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="f249b-115">Examples</span></span>

<span data-ttu-id="f249b-116">В следующем примере извлекается первый список воспроизведения в библиотеке и используется свойство Куррентплайлист для задания полученного списка воспроизведения в качестве текущего списка воспроизведения и вывода его имени.</span><span class="sxs-lookup"><span data-stu-id="f249b-116">The following example retrieves the first playlist in the library and uses the currentPlaylist property to set the retrieved playlist as the current playlist, and display its name.</span></span> <span data-ttu-id="f249b-117">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="f249b-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first playlist from the library. 
WMPLib.IWMPPlaylist firstPlaylist = player.playlistCollection.getAll().Item(0);

// Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist;

// Display the name of the current playlist.
currentPlaylistLabel.Text = ("Found first playlist. Name = " + player.currentPlaylist.name);
```


```VB

' Get an interface to the first playlist from the library. 
Dim firstPlaylist As WMPLib.IWMPPlaylist = player.playlistCollection.getAll().Item(0)

&#39; Make the retrieved playlist the current playlist.
player.currentPlaylist = firstPlaylist

&#39; Display the name of the current playlist.
currentPlaylistLabel.Text = (&quot;Found first playlist. Name = &quot; + player.currentPlaylist.name)
```





## <a name="requirements"></a><span data-ttu-id="f249b-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f249b-118">Requirements</span></span>



| <span data-ttu-id="f249b-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f249b-119">Requirement</span></span> | <span data-ttu-id="f249b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f249b-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f249b-121">Версия</span><span class="sxs-lookup"><span data-stu-id="f249b-121">Version</span></span><br/>   | <span data-ttu-id="f249b-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f249b-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f249b-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f249b-123">Namespace</span></span><br/> | <span data-ttu-id="f249b-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="f249b-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f249b-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="f249b-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f249b-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f249b-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f249b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f249b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f249b-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f249b-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f249b-129">**Аксвиндовсмедиаплайер. Невплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f249b-129">**AxWindowsMediaPlayer.newPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newplaylist.md)
</dt> <dt>

[<span data-ttu-id="f249b-130">**Аксвиндовсмедиаплайер. Settings (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f249b-130">**AxWindowsMediaPlayer.settings (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-settings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f249b-131">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f249b-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f249b-132">**Ивмпплайлистаррай. Item (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f249b-132">**IWMPPlaylistArray.Item (VB and C#)**</span></span>](wmplibiwmpplaylistarray-iwmpplaylistarray-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f249b-133">**Ивмпплайлистколлектион. Невплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f249b-133">**IWMPPlaylistCollection.newPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-newplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f249b-134">**Ивмпсеттингс. Автозапуск (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f249b-134">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





