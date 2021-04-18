---
title: Ивмпконтролс Куррентмаркер, свойство
description: Свойство Куррентмаркер Возвращает или задает номер текущего маркера.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- Проигрыватель Windows Media для свойства Куррентмаркер
- Куррентмаркер свойство проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, свойство Куррентмаркер
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689312"
---
# <a name="iwmpcontrolscurrentmarker-property"></a><span data-ttu-id="6eea9-106">Свойство Ивмпконтролс:: Куррентмаркер</span><span class="sxs-lookup"><span data-stu-id="6eea9-106">IWMPControls::currentMarker property</span></span>

<span data-ttu-id="6eea9-107">Свойство **куррентмаркер** Возвращает или задает номер текущего маркера.</span><span class="sxs-lookup"><span data-stu-id="6eea9-107">The **currentMarker** property gets or sets the current marker number.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eea9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6eea9-108">Syntax</span></span>


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6eea9-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6eea9-109">Property value</span></span>

<span data-ttu-id="6eea9-110">Значение **System. Int32** , которое является номером маркера.</span><span class="sxs-lookup"><span data-stu-id="6eea9-110">A **System.Int32** that is the marker number.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eea9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6eea9-111">Remarks</span></span>

<span data-ttu-id="6eea9-112">Установка **куррентмаркер** приводит к запуску воспроизведения с указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="6eea9-112">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="6eea9-113">Прежде чем пытаться задать **куррентмаркер**, определите, есть ли у файла маркеры и сколько он имеет, с помощью **ивмпмедиа. маркеркаунт**.</span><span class="sxs-lookup"><span data-stu-id="6eea9-113">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **IWMPMedia.markerCount**.</span></span> <span data-ttu-id="6eea9-114">Если у файла нет маркеров, установка **куррентмаркер** в любом случае, но ноль приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="6eea9-114">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="6eea9-115">Установка **куррентмаркер** в число, превышающее **маркеркаунт** , также приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="6eea9-115">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="6eea9-116">Свойство **куррентмаркер** всегда возвращает текущий или последний маркер, то есть фактическое расположение файла может находиться либо на текущем маркере, либо перед следующим маркером.</span><span class="sxs-lookup"><span data-stu-id="6eea9-116">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="6eea9-117">Маркеры нумеруются, начиная с 1, поэтому если в файле есть маркеры, можно установить **куррентмаркер** в ноль, чтобы изменить расположение файла на ноль.</span><span class="sxs-lookup"><span data-stu-id="6eea9-117">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="6eea9-118">Пока не задается текущий элемент мультимедиа (с помощью **аксвиндовсмедиаплайер. URL** или **аксвиндовсмедиаплайер. Куррентмедиа**), **куррентмаркер** возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="6eea9-118">Until the current media item is set (using **AxWindowsMediaPlayer.URL** or **AxWindowsMediaPlayer.currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="6eea9-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="6eea9-119">Examples</span></span>

<span data-ttu-id="6eea9-120">В следующем примере используется **куррентмаркер** для запуска воспроизведения видео из маркера, соответствующего свойству SelectedIndex списка, который заполнен идентификаторами маркера.</span><span class="sxs-lookup"><span data-stu-id="6eea9-120">The following example uses **currentMarker** to start video playback from the marker that corresponds to the SelectedIndex property of a list box which has been filled with marker identifiers.</span></span> <span data-ttu-id="6eea9-121">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="6eea9-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6eea9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="6eea9-122">Requirements</span></span>



| <span data-ttu-id="6eea9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="6eea9-123">Requirement</span></span> | <span data-ttu-id="6eea9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="6eea9-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eea9-125">Версия</span><span class="sxs-lookup"><span data-stu-id="6eea9-125">Version</span></span><br/>   | <span data-ttu-id="6eea9-126">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6eea9-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6eea9-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6eea9-127">Namespace</span></span><br/> | <span data-ttu-id="6eea9-128">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="6eea9-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6eea9-129">Сборка</span><span class="sxs-lookup"><span data-stu-id="6eea9-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6eea9-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6eea9-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eea9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6eea9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eea9-132">**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6eea9-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6eea9-133">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6eea9-133">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6eea9-134">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6eea9-134">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6eea9-135">**Ивмпмедиа. Маркеркаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6eea9-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





