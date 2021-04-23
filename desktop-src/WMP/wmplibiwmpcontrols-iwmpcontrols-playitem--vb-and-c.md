---
title: Ивмпконтролс Плайитем, метод
description: Метод Плайитем воспроизводит указанный элемент мультимедиа. | Ивмпконтролс Плайитем, метод
ms.assetid: ddd4e4f7-475c-4964-a623-9123ed66be8e
keywords:
- Плайитем метод Windows Media Player
- Плайитем метод проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Плайитем
topic_type:
- apiref
api_name:
- IWMPControls.playItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2ac11f93409128eccc88c1d916144615d77476
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689296"
---
# <a name="iwmpcontrolsplayitem-method"></a><span data-ttu-id="03f24-107">Ивмпконтролс: метод:p Лайитем</span><span class="sxs-lookup"><span data-stu-id="03f24-107">IWMPControls::playItem method</span></span>

<span data-ttu-id="03f24-108">Метод **плайитем** воспроизводит указанный элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="03f24-108">The **playItem** method plays the specified media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f24-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03f24-109">Syntax</span></span>


```CSharp
public void playItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub playItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPControls.playItem
```





## <a name="parameters"></a><span data-ttu-id="03f24-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="03f24-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03f24-111">*пивмпмедиа* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="03f24-111">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03f24-112">Интерфейс **вмплиб. ивмпмедиа** для элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="03f24-112">A **WMPLib.IWMPMedia** interface to the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03f24-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03f24-113">Return value</span></span>

<span data-ttu-id="03f24-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="03f24-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f24-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03f24-115">Remarks</span></span>

<span data-ttu-id="03f24-116">Элемент мультимедиа будет загружаться и воспроизводиться автоматически независимо от значения свойства **ивмпсеттингс. Автозапуск** .</span><span class="sxs-lookup"><span data-stu-id="03f24-116">The media item will load and play automatically, regardless of the value of the **IWMPSettings.autoStart** property.</span></span> <span data-ttu-id="03f24-117">Чтобы загрузить элемент без автоматического воспроизведения, задайте для **ивмпсеттингс. автозапуска** значение **false** и присвойте значение **аксвиндовсмедиаплайер. URL**, после чего можно вызвать **ивмпконтролс. Play** , чтобы начать воспроизведение элемента.</span><span class="sxs-lookup"><span data-stu-id="03f24-117">To load an item without playing it automatically, set **IWMPSettings.autoStart** to **false** and assign a value to **AxWindowsMediaPlayer.URL**, after which **IWMPControls.play** can be called to start playing the item.</span></span>

<span data-ttu-id="03f24-118">Примечание</span><span class="sxs-lookup"><span data-stu-id="03f24-118">Note</span></span>

<span data-ttu-id="03f24-119">**плайитем** работает только с элементами в **аксвиндовсмедиаплайер. куррентплайлист**.</span><span class="sxs-lookup"><span data-stu-id="03f24-119">**playItem** works only with items in **AxWindowsMediaPlayer.currentPlaylist**.</span></span> <span data-ttu-id="03f24-120">Вызов **плайитем** со ссылкой на сохраненный элемент мультимедиа не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="03f24-120">Calling **playItem** with a reference to a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="03f24-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="03f24-121">Examples</span></span>

<span data-ttu-id="03f24-122">В следующем примере **плайитем** используется для воспроизведения элемента мультимедиа из текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="03f24-122">The following example uses **playItem** to play a media item from the current playlist.</span></span> <span data-ttu-id="03f24-123">Элемент для воспроизведения выбирается в зависимости от его позиции в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="03f24-123">The item to play is chosen based upon its position in the playlist.</span></span> <span data-ttu-id="03f24-124">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="03f24-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
int index = 3;

// Get the media item at the fourth position in the current playlist.
WMPLib.IWMPMedia media = player.currentPlaylist.get_Item(index);

// Play the media item.
player.Ctlcontrols.playItem(media);
```


```VB

' Declare a variable to hold the position of the media item 
&#39; in the current playlist. An arbitrary value is supplied here.
Dim index As Integer = 3

&#39; Get the media item at the fourth position in the current playlist.
Dim Media As WMPLib.IWMPMedia = player.currentPlaylist.Item(index)

&#39; Play the media item.
player.Ctlcontrols.playItem(Media)
```





## <a name="requirements"></a><span data-ttu-id="03f24-125">Требования</span><span class="sxs-lookup"><span data-stu-id="03f24-125">Requirements</span></span>



| <span data-ttu-id="03f24-126">Требование</span><span class="sxs-lookup"><span data-stu-id="03f24-126">Requirement</span></span> | <span data-ttu-id="03f24-127">Значение</span><span class="sxs-lookup"><span data-stu-id="03f24-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f24-128">Версия</span><span class="sxs-lookup"><span data-stu-id="03f24-128">Version</span></span><br/>   | <span data-ttu-id="03f24-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="03f24-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="03f24-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="03f24-130">Namespace</span></span><br/> | <span data-ttu-id="03f24-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="03f24-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="03f24-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="03f24-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="03f24-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="03f24-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f24-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03f24-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f24-135">**Аксвиндовсмедиаплайер. Куррентплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="03f24-135">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03f24-136">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="03f24-136">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03f24-137">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="03f24-137">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03f24-138">**Ивмпконтролс. Play (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="03f24-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03f24-139">**Ивмпплайлист. Item (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="03f24-139">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="03f24-140">**Ивмпсеттингс. Автозапуск (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="03f24-140">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





