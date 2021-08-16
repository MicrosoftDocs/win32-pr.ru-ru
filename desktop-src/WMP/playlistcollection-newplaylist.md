---
title: Плайлистколлектион. Невплайлист, метод
description: Метод Невплайлист создает новый список воспроизведения в библиотеке.
ms.assetid: 428b5779-4dc0-466b-9834-6b2c43324013
keywords:
- проигрыватель Windows Media метода невплайлист
- проигрыватель Windows Media метода невплайлист, класс плайлистколлектион
- класс плайлистколлектион проигрыватель Windows Media, метод невплайлист
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
ms.openlocfilehash: af40d4de424997cb943711d84bf62805f2036afeb551c5d397ce82ae0975e812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334601"
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

## <a name="remarks"></a>Remarks

Этот метод создает пустой список воспроизведения в библиотеке. Чтобы заполнить список воспроизведения с помощью элементов мультимедиа, используйте *список воспроизведения*. **аппендитем** или *список воспроизведения*. **insertItem**.

В библиотеке разрешено несколько списков воспроизведения с одинаковыми именами. Чтобы избежать создания дубликата имени списка воспроизведения с помощью этого метода, используйте **жетбинаме** и *плайлистаррай*. **число** , определяющее, существует ли уже список воспроизведения с определенным именем.

Начальные и конечные пробелы не допускаются в именах списков воспроизведения и автоматически удаляются из значения, указанного для параметра *Name* .

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере JScript создается пустой список воспроизведения с именем «срилист». Объект **Player** создан с идентификатором "Player".


```JScript
//Add a new empty playlist, named ThreeList, to the playlist collection.
var NewList = Player.playlistCollection.newPlaylist("ThreeList");

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
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

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





