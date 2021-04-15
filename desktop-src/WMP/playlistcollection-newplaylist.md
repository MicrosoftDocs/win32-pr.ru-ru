---
title: Плайлистколлектион. Невплайлист, метод
description: Метод Невплайлист создает новый список воспроизведения в библиотеке.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- Невплайлист метод Windows Media Player
- Невплайлист метод Windows Media Player, класс Плайлистколлектион
- Класс Плайлистколлектион Windows Media Player, метод Невплайлист
topic_type:
- apiref
api_name:
- PlaylistCollection.newPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d94c25a8dfe6f1eb7c4dac40dd644433a5f0d7e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708437"
---
# <a name="playlistcollectionnewplaylist-method"></a>Плайлистколлектион. Невплайлист, метод

Метод **невплайлист** создает новый список воспроизведения в библиотеке.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = PlaylistCollection.newPlaylist(
  name
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя создаваемого списка воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **списка воспроизведения** .

## <a name="remarks"></a>Комментарии

Этот метод создает пустой список воспроизведения в библиотеке. Чтобы заполнить список воспроизведения с помощью элементов мультимедиа, используйте *список воспроизведения*. **аппендитем** или *список воспроизведения*. **insertItem**.

В библиотеке разрешено несколько списков воспроизведения с одинаковыми именами. Чтобы избежать создания дубликата имени списка воспроизведения с помощью этого метода, используйте **жетбинаме** и *плайлистаррай*. **число** , определяющее, существует ли уже список воспроизведения с определенным именем.

Начальные и конечные пробелы не допускаются в именах списков воспроизведения и автоматически удаляются из значения, указанного для параметра *Name* .

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере JScript создается пустой список воспроизведения с именем «Срилист». Объект **Player** создан с идентификатором "Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Медиаколлектион. Add**](mediacollection-add.md)
</dt> <dt>

[**Список воспроизведения. Аппендитем**](playlist-appenditem.md)
</dt> <dt>

[**Список воспроизведения. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Плайлистаррай. Count**](playlistarray-count.md)
</dt> <dt>

[**Объект Плайлистколлектион**](playlistcollection-object.md)
</dt> <dt>

[**Плайлистколлектион. Жетбинаме**](playlistcollection-getbyname.md)
</dt> <dt>

[**Плайлистколлектион. Импортплайлист**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Плайлистколлектион. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





