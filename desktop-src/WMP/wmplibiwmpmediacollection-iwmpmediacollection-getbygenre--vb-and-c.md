---
title: Ивмпмедиаколлектион Жетбиженре, метод
description: Метод Жетбиженре возвращает интерфейс Ивмпплайлист, предоставляющий доступ к элементам мультимедиа указанного жанра.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- проигрыватель Windows Media метода жетбиженре
- проигрыватель Windows Media метода жетбиженре, интерфейс ивмпмедиаколлектион
- проигрыватель Windows Media интерфейса ивмпмедиаколлектион, метод жетбиженре
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72f20182f2bfb3bef0d4de2907165a571009072d234add3b8f89ae2db859c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053602"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a>Метод Ивмпмедиаколлектион:: Жетбиженре

`getByGenre`Метод возвращает интерфейс **ивмпплайлист** , предоставляющий доступ к элементам мультимедиа указанного жанра.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрженре* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем жанра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпплайлист** для извлеченных элементов мультимедиа.

## <a name="remarks"></a>Remarks

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение `getByGenre` метода зависит от того, какой из этих двух способов вы используете. При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md) `getByGenre` метод возвращает все элементы мультимедиа в библиотеке. Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md) `getByGenre` метод возвращает только звуковые элементы в библиотеке с указанным атрибутом и значением.

## <a name="examples"></a>Примеры

В следующем примере используется `getByGenre` для получения списка воспроизведения элементов мультимедиа, когда пользователь нажимает кнопку. Список воспроизведения содержит элементы с жанром, указанным пользователем в текстовом поле. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
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

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





