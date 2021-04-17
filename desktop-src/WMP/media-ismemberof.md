---
title: Метод Media. isMemberOf
description: Метод isMemberOf возвращает значение, указывающее, является ли элемент мультимедиа элементом указанного списка воспроизведения.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- isMemberOf метод Windows Media Player
- isMemberOf метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод isMemberOf
topic_type:
- apiref
api_name:
- Media.isMemberOf
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41555bd5910ddb3151468a458c5becbf247ea484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694699"
---
# <a name="mediaismemberof-method"></a>Метод Media. isMemberOf

Метод **isMemberOf** возвращает значение, указывающее, является ли элемент мультимедиа элементом указанного списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
bRetVal = Media.isMemberOf(
  playlist
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*список воспроизведения* \[ окне\]
</dt> <dd>

Объект **списка воспроизведения** , который может содержать элемент мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **логическое значение**.

## <a name="remarks"></a>Комментарии

Этот метод не может проверять списки воспроизведения, полученные через объект **медиаколлектион** . Чтобы проверить, является ли элемент мультимедиа членом определенного списка воспроизведения, извлеките список воспроизведения с помощью *проигрывателя*. *плайлистколлектион*. **жетбинаме**(*имя*). **элемент**(0). Этот метод также можно использовать с списками воспроизведения компакт-дисков и списками воспроизведения метафайлов.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *носитель*. **isMemberOf** , чтобы проверить, является ли текущий элемент мультимедиа членом списка воспроизведения с именем Sample Rename. Если это не так, текущий элемент мультимедиа добавляется к образцу списка воспроизведения. Объект **Player** создан с идентификатором "Player".


```JScript
// Store the playlist object named Sample Playlist.
var sPlaylist = Player.playlistcollection.getbyname("Sample Playlist").item(0);

// Test whether the current media item is a member of Sample Playlist.
 var answer = ((Player.currentMedia.isMemberOf(sPlaylist))?"Yes":"No");

// If the current media item is not a member of Sample Playlist,
// append the current media item to the playlist.
if (answer == "No"){
   sPlaylist.appendItem(Player.currentMedia);
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Объект Плайлистколлектион**](playlistcollection-object.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





