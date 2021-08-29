---
title: Ивмпконтролс currentItem, свойство
description: Свойство currentItem Возвращает или задает текущий элемент мультимедиа в списке воспроизведения.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- проигрыватель Windows Media свойства currentItem
- проигрыватель Windows Media свойства currentItem, интерфейс ивмпконтролс
- проигрыватель Windows Media интерфейса ивмпконтролс, свойство currentItem
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
ms.openlocfilehash: 8d8193dc349524495e021dc048ac4be3673d38ec7da30aa1bb72d94960a0989f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053662"
---
# <a name="iwmpcontrolscurrentitem-property"></a>Свойство Ивмпконтролс:: currentItem

Свойство **currentItem** Возвращает или задает текущий элемент мультимедиа в списке воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a>Значение свойства

Интерфейс **вмплиб. ивмпмедиа** , представляющий элемент мультимедиа.

## <a name="remarks"></a>Remarks

Это свойство работает только с элементами в текущем списке воспроизведения. Установка **currentItem** для интерфейса сохраненного элемента мультимедиа не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере используется **currentItem** для установки текущего элемента мультимедиа проигрывателя на элемент, выбранный из списка. Список заполнен всеми элементами текущего списка воспроизведения. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


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





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Ивмпконтролсинтерфаце (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиаинтерфаце (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





