---
title: Player. Куррентплайлист
description: Свойство Куррентплайлист указывает или получает текущий объект списка воспроизведения.
ms.assetid: fabfb927-5f64-4fc4-8ee5-e2449082dfbc
keywords:
- проигрыватель Windows Media Player. куррентплайлист
topic_type:
- apiref
api_name:
- Player.currentPlaylist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7139c567eab5fbb3c324916dec260d34f57429cb50bb99d199f35be8aee7a1c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118573219"
---
# <a name="playercurrentplaylist"></a>Player. Куррентплайлист

Свойство Куррентплайлист указывает или получает текущий объект **списка воспроизведения** .

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **куррентплайлист**

## <a name="possible-values"></a>Возможные значения

Это свойство является объектом **списка воспроизведения** для чтения и записи.

## <a name="remarks"></a>Remarks

если *Параметры*. Свойство **автозапуска** имеет значение true, воспроизведение начинается автоматически при установке **куррентплайлист**.

Это свойство принимает объект списка воспроизведения, который может быть получен несколькими способами, например путем вызова *плайлистаррай*. **Item** или *плайлистколлектион*. **невплайлист**. Чтобы загрузить элемент **списка воспроизведения** с помощью имени файла, задайте свойство URL-адреса или используйте *проигрыватель*. **невплайлист**.

## <a name="examples"></a>Примеры

в следующем примере JScript извлекается первый список воспроизведения в библиотеке. Затем он использует **куррентплайлист** , чтобы сделать полученный список воспроизведения текущим списком воспроизведения, а затем отобразить имя текущего списка воспроизведения. Объект **Player** создан с идентификатором "Player".


```JScript
// Retrieve the first playlist from the library.
var firstPL = Player.playlistCollection.getAll().item(0);

// Make the retrieved playlist the current playlist.
Player.currentPlaylist = firstPL;

// Display the name of the current playlist.
document.write("Found first playlist. Name: " + Player.currentPlaylist.name);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Невплайлист**](player-newplaylist.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Плайлистаррай. Item**](playlistarray-item.md)
</dt> <dt>

[**Плайлистколлектион. Невплайлист**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Параметры. автозапуск**](settings-autostart.md)
</dt> </dl>

 

 





