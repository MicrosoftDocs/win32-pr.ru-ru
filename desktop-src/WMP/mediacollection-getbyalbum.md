---
title: Медиаколлектион. Жетбялбум, метод
description: Метод Жетбялбум извлекает список воспроизведения, содержащий элементы мультимедиа из указанного альбома.
ms.assetid: e7e72f0e-e0ae-4bbd-a8b7-966f0fc50059
keywords:
- Жетбялбум метод Windows Media Player
- Жетбялбум метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбялбум
topic_type:
- apiref
api_name:
- MediaCollection.getByAlbum
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d94cdfa880288893e9659b73b01bc754ac59bbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689059"
---
# <a name="mediacollectiongetbyalbum-method"></a>Медиаколлектион. Жетбялбум, метод

Метод **жетбялбум** извлекает список воспроизведения, содержащий элементы мультимедиа из указанного альбома.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.getByAlbum(
  album
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*альбом* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя альбома.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **списка воспроизведения** .

## <a name="remarks"></a>Комментарии

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере используется *медиаколлектион*. **жетбялбум** для получения списка воспроизведения элементов мультимедиа. Список воспроизведения содержит элементы с альбомом, указанным пользователем в HTML-элементе input TEXT с именем GetText. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and 
then play the digital media items. -->
<INPUT TYPE = "BUTTON"
       NAME = "PlayAlbum" 
       ID = "PlayAlbum"  
       VALUE = "Play Album"

onClick = "
    /* Retrieve the album title text from the user. */
    var album = GetAlbum.value;

    /* Create the playlist using getByAlbum. */
    var pl = Player.mediaCollection.getByAlbum(album);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media in the new playlist. */
    Player.controls.play();
">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





