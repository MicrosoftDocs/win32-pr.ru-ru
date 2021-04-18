---
title: Плайлистколлектион. Жетбинаме, метод
description: Метод Жетбинаме извлекает объект Плайлистаррай, содержащий списки воспроизведения с указанным именем, если таковые имеются.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- Жетбинаме метод Windows Media Player
- Жетбинаме метод Windows Media Player, класс Плайлистколлектион
- Класс Плайлистколлектион Windows Media Player, метод Жетбинаме
topic_type:
- apiref
api_name:
- PlaylistCollection.getByName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7954df8e0ccc487df77ea31b3a26dce9eea6d2e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718033"
---
# <a name="playlistcollectiongetbyname-method"></a>Плайлистколлектион. Жетбинаме, метод

Метод **жетбинаме** извлекает объект **плайлистаррай** , содержащий списки воспроизведения с указанным именем, если таковые имеются.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = PlaylistCollection.getByName(
  name
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , содержащая имена списков воспроизведения для извлечения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **плайлистаррай** .

## <a name="remarks"></a>Комментарии

Используйте *плайлистаррай*. **количество** , определяющее, существует ли список воспроизведения. Если значение **Count** равно нулю, список воспроизведения не существует.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *плайлистколлектион*. **жетбинаме** , чтобы проверить объект **плайлистколлектион** для списка воспроизведения с именем "срилист". Если существует список воспроизведения "Срилист", **жетбинаме** устанавливает в качестве текущего списка воспроизведения "срилист". Объект **Player** был создан с идентификатором "Player".


```JScript
//Retrieve the count of the playlists named "ThreeList".
var Checkit = Player.playlistCollection.getByName("ThreeList").count;

//Since duplicate playlist names are allowed, the count returned
//will be either zero (no playlist) or greater than zero 
//(playlist exists).
if (Checkit > 0){ 
    
   //Retrieve a playlistArray object containing "ThreeList". Assume that
   //there is only one playlist with that name, and assign it to the 
   //current playlist.
   Player.currentPlaylist = Player.playlistCollection.getByName("ThreeList").item(0);
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Плайлистаррай**](playlistarray-object.md)
</dt> <dt>

[**Плайлистаррай. Count**](playlistarray-count.md)
</dt> <dt>

[**Объект Плайлистколлектион**](playlistcollection-object.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





