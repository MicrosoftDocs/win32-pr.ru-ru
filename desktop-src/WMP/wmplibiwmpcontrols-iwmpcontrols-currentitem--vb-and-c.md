---
title: Ивмпконтролс currentItem, свойство
description: Свойство currentItem Возвращает или задает текущий элемент мультимедиа в списке воспроизведения.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- Проигрыватель Windows Media для свойства currentItem
- currentItem свойство проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, свойство currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689313"
---
# <a name="iwmpcontrolscurrentitem-property"></a><span data-ttu-id="fd63d-106">Свойство Ивмпконтролс:: currentItem</span><span class="sxs-lookup"><span data-stu-id="fd63d-106">IWMPControls::currentItem property</span></span>

<span data-ttu-id="fd63d-107">Свойство **currentItem** Возвращает или задает текущий элемент мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fd63d-107">The **currentItem** property gets or sets the current media item in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd63d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd63d-108">Syntax</span></span>


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="fd63d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fd63d-109">Property value</span></span>

<span data-ttu-id="fd63d-110">Интерфейс **вмплиб. ивмпмедиа** , представляющий элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="fd63d-110">A **WMPLib.IWMPMedia** interface that represents the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd63d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fd63d-111">Remarks</span></span>

<span data-ttu-id="fd63d-112">Это свойство работает только с элементами в текущем списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fd63d-112">This property works only with items in the current playlist.</span></span> <span data-ttu-id="fd63d-113">Установка **currentItem** для интерфейса сохраненного элемента мультимедиа не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fd63d-113">Setting **currentItem** to the interface of a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="fd63d-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="fd63d-114">Examples</span></span>

<span data-ttu-id="fd63d-115">В следующем примере используется **currentItem** для установки текущего элемента мультимедиа проигрывателя на элемент, выбранный из списка.</span><span class="sxs-lookup"><span data-stu-id="fd63d-115">The following example uses **currentItem** to set the player's current media item to an item selected from a list box.</span></span> <span data-ttu-id="fd63d-116">Список заполнен всеми элементами текущего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="fd63d-116">The list box has been filled with all of the items in the current playlist.</span></span> <span data-ttu-id="fd63d-117">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="fd63d-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="fd63d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="fd63d-118">Requirements</span></span>



| <span data-ttu-id="fd63d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="fd63d-119">Requirement</span></span> | <span data-ttu-id="fd63d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="fd63d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd63d-121">Версия</span><span class="sxs-lookup"><span data-stu-id="fd63d-121">Version</span></span><br/>   | <span data-ttu-id="fd63d-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="fd63d-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fd63d-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fd63d-123">Namespace</span></span><br/> | <span data-ttu-id="fd63d-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="fd63d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fd63d-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="fd63d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fd63d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fd63d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd63d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd63d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd63d-128">**Ивмпконтролсинтерфаце (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="fd63d-128">**IWMPControlsInterface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fd63d-129">**Ивмпмедиаинтерфаце (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="fd63d-129">**IWMPMediaInterface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fd63d-130">**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="fd63d-130">**IWMPPlaylistCollection.getByName(VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





