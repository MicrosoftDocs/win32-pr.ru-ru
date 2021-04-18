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
# <a name="iwmpcontrolscurrentmarker-property"></a>Свойство Ивмпконтролс:: Куррентмаркер

Свойство **куррентмаркер** Возвращает или задает номер текущего маркера.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является номером маркера.

## <a name="remarks"></a>Комментарии

Установка **куррентмаркер** приводит к запуску воспроизведения с указанного маркера. Прежде чем пытаться задать **куррентмаркер**, определите, есть ли у файла маркеры и сколько он имеет, с помощью **ивмпмедиа. маркеркаунт**. Если у файла нет маркеров, установка **куррентмаркер** в любом случае, но ноль приводит к ошибке. Установка **куррентмаркер** в число, превышающее **маркеркаунт** , также приводит к ошибке.

Свойство **куррентмаркер** всегда возвращает текущий или последний маркер, то есть фактическое расположение файла может находиться либо на текущем маркере, либо перед следующим маркером. Маркеры нумеруются, начиная с 1, поэтому если в файле есть маркеры, можно установить **куррентмаркер** в ноль, чтобы изменить расположение файла на ноль.

Пока не задается текущий элемент мультимедиа (с помощью **аксвиндовсмедиаплайер. URL** или **аксвиндовсмедиаплайер. Куррентмедиа**), **куррентмаркер** возвращает ноль.

## <a name="examples"></a>Примеры

В следующем примере используется **куррентмаркер** для запуска воспроизведения видео из маркера, соответствующего свойству SelectedIndex списка, который заполнен идентификаторами маркера. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


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





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. URL (VB и C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпконтролс (VB и C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**Ивмпмедиа. Маркеркаунт (VB и C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





