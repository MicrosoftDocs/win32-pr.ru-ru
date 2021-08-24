---
title: Ивмпмедиаколлектион Жетбяттрибуте, метод
description: Метод Жетбяттрибуте возвращает интерфейс Ивмпплайлист, соответствующий указанному атрибуту, имеющему указанное значение.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- проигрыватель Windows Media метода жетбяттрибуте
- проигрыватель Windows Media метода жетбяттрибуте, интерфейс ивмпмедиаколлектион
- проигрыватель Windows Media интерфейса ивмпмедиаколлектион, метод жетбяттрибуте
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fb8dab44cd1f26c080d438c15f545c882d2e4427af7fa04049b539ce8b3cf13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735024"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a>Метод Ивмпмедиаколлектион:: Жетбяттрибуте

Метод **жетбяттрибуте** возвращает интерфейс **ивмпплайлист** , соответствующий указанному атрибуту, имеющему указанное значение.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраттрибуте* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является указанным атрибутом.

</dd> <dt>

*бстрвалуе* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является указанным значением.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпплайлист** для извлеченных элементов мультимедиа.

## <a name="remarks"></a>Remarks

Этот метод можно использовать для создания универсального запроса для элементов мультимедиа, которые соответствуют значению атрибута в библиотеке. Это полезно в случае определяемых пользователем атрибутов. Если атрибут не существует, возникнет ошибка.

Этот метод можно использовать для извлечения всех элементов мультимедиа определенного типа. Используйте имя атрибута **mediaType** и одно из следующих значений.



| Значение    | Описание                                               |
|----------|-----------------------------------------------------------|
| звук    | Музыка и другие звуковые элементы                          |
| др.    | Другие элементы, например файлы ASF или URL-адрес потока. |
| фотография    | Элементы фото. требуется проигрыватель Windows Media 10.            |
| список воспроизведения | Списки воспроизведения, представленные в виде элементов мультимедиа.                     |
| radio    | Элементы радиостанции. не используется проигрыватель Windows Media 10. |
| видео    | Элементы видео.                                              |



 

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибутам](attribute-reference.md).

Существует два способа получения интерфейса **ивмпмедиаколлектион** , и поведение метода **жетбяттрибуте** зависит от того, какой из этих двух способов вы используете. При получении интерфейса путем вызова [аксвиндовсмедиаплайер. медиаколлектион](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)метод **жетбяттрибуте** возвращает все элементы мультимедиа в библиотеке. Однако при получении интерфейса путем вызова [ивмплибрари. медиаколлектион](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md)метод **жетбяттрибуте** возвращает только звуковые элементы в библиотеке с указанным атрибутом и значением.

## <a name="examples"></a>Примеры

В следующем примере кода используется **жетбяттрибуте** для воспроизведения всего содержимого из библиотеки исполнителем с именем триоде 48. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Жеталл (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





