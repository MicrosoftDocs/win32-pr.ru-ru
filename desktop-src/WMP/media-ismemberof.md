---
title: Метод Media. isMemberOf
description: Метод isMemberOf возвращает значение, указывающее, является ли элемент мультимедиа элементом указанного списка воспроизведения.
ms.assetid: e620741f-6807-4a61-ba9b-f45426d6e33e
keywords:
- проигрыватель Windows Media метода isMemberOf
- проигрыватель Windows Media метода isMemberOf, класс мультимедиа
- класс мультимедиа проигрыватель Windows Media, метод isMemberOf
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
ms.openlocfilehash: ef9fc5eb55a306dad8b9d5de6d6501b615a9156c026c8e0fc12664795a23ab21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574806"
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

## <a name="remarks"></a>Remarks

Этот метод не может проверять списки воспроизведения, полученные через объект **медиаколлектион** . Чтобы проверить, является ли элемент мультимедиа членом определенного списка воспроизведения, извлеките список воспроизведения с помощью *проигрывателя*. *плайлистколлектион*. **жетбинаме**(*имя*). **элемент**(0). Этот метод также можно использовать с списками воспроизведения компакт-дисков и списками воспроизведения метафайлов.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **isMemberOf** , чтобы проверить, является ли текущий элемент мультимедиа членом списка воспроизведения с именем Sample Rename. Если это не так, текущий элемент мультимедиа добавляется к образцу списка воспроизведения. Объект **Player** создан с идентификатором "Player".


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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Объект Плайлистколлектион**](playlistcollection-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





