---
title: Плайлистколлектион. Жетбинаме, метод
description: Метод Жетбинаме извлекает объект Плайлистаррай, содержащий списки воспроизведения с указанным именем, если таковые имеются.
ms.assetid: 0308a98d-1149-4367-b602-33fa54c1760f
keywords:
- проигрыватель Windows Media метода жетбинаме
- проигрыватель Windows Media метода жетбинаме, класс плайлистколлектион
- класс плайлистколлектион проигрыватель Windows Media, метод жетбинаме
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
ms.openlocfilehash: 300307ff011abf8b28c645901422291ccab4cf7c66a7a3ba81121ffe1c22e573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334645"
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

## <a name="remarks"></a>Remarks

Используйте *плайлистаррай*. **количество** , определяющее, существует ли список воспроизведения. Если значение **Count** равно нулю, список воспроизведения не существует.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *плайлистколлектион*. **жетбинаме** , чтобы проверить объект **плайлистколлектион** для списка воспроизведения с именем "срилист". Если существует список воспроизведения "Срилист", **жетбинаме** устанавливает в качестве текущего списка воспроизведения "срилист". Объект **Player** был создан с идентификатором "Player".


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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Плайлистаррай**](playlistarray-object.md)
</dt> <dt>

[**Плайлистаррай. Count**](playlistarray-count.md)
</dt> <dt>

[**Объект Плайлистколлектион**](playlistcollection-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





