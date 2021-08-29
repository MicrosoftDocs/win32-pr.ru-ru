---
title: Свойство отключения Ивмпсеттингс
description: Свойство выкл. Получает или задает значение, указывающее, отключено ли звуковое сопровождение.
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- выключить проигрыватель Windows Media свойств
- выключить проигрыватель Windows Media свойств, интерфейс ивмпсеттингс
- интерфейс ивмпсеттингс проигрыватель Windows Media, выключение свойства
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d4cb13fd8884df7779b2780fd7014d058f32086d67ace286d9d8a9fd57cb8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053412"
---
# <a name="iwmpsettingsmute-property"></a>Свойство Ивмпсеттингс:: выкл.

Свойство **выкл** . Получает или задает значение, указывающее, отключено ли звуковое сопровождение.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a>Значение свойства

Значение **System. Boolean** , указывающее, отключено ли звуковое сопровождение. Значение по умолчанию — **false**.

## <a name="examples"></a>Примеры

В следующем примере создается флажок и переключается на свойство выкл. при изменении состояния флажка значение параметра **выключить** звук будет отключено. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

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

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Ивмпсеттингс. rate (VB и C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





