---
title: Кдромколлектион. Item, метод
description: Метод Item извлекает объект CDROM по указанному индексу.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс Кдромколлектион
- Класс Кдромколлектион Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699172"
---
# <a name="cdromcollectionitem-method"></a>Кдромколлектион. Item, метод

Метод **Item** извлекает объект **CDROM** по указанному индексу.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **CDROM** .

## <a name="remarks"></a>Комментарии

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *кдромколлектион*. **элемент** для печати имени списка воспроизведения с каждого компакт-диска, доступного на компьютере. Если на самом деле диск содержит содержимое DVD, требуется ОС Windows XP или более поздней версии. Создан HTML-элемент TextArea с ИДЕНТИФИКАТОРом "списки воспроизведения". Объект **Player** создан с идентификатором "Player".


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CDROM. ДривеспеЦифиер**](cdrom-drivespecifier.md)
</dt> <dt>

[**Объект Кдромколлектион**](cdromcollection-object.md)
</dt> <dt>

[**Кдромколлектион. Count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





