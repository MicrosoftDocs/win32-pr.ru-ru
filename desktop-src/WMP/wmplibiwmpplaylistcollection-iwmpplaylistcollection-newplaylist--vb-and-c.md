---
title: Ивмпплайлистколлектион Невплайлист, метод
description: Метод Невплайлист возвращает интерфейс Ивмпплайлист для нового пустого списка воспроизведения в библиотеке.
ms.assetid: cc0cb356-9a90-421c-8d1a-b79585f71124
keywords:
- Невплайлист метод Windows Media Player
- Невплайлист метод проигрывателя Windows Media Player, интерфейс Ивмпплайлистколлектион
- Интерфейс Ивмпплайлистколлектион Windows Media Player, метод Невплайлист
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.newPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbc455c5815cee1aaac139886bca1d847ddc62b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704125"
---
# <a name="iwmpplaylistcollectionnewplaylist-method"></a>Метод Ивмпплайлистколлектион:: Невплайлист

Метод **невплайлист** возвращает интерфейс **ивмпплайлист** для нового пустого списка воспроизведения в библиотеке.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist newPlaylist(
  System.String bstrName
);
```


```VB

Public Function newPlaylist( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPPlaylistCollection.newPlaylist
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*bstrName* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем нового списка воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпплайлист** для нового списка воспроизведения.

## <a name="remarks"></a>Комментарии

Этот метод создает пустой список воспроизведения в библиотеке. Чтобы заполнить список воспроизведения с помощью элементов мультимедиа, используйте **ивмпплайлист. аппендитем** или **ивмпплайлист. insertItem**.

В библиотеке разрешено несколько списков воспроизведения с одинаковыми именами. Чтобы избежать создания дубликата имени списка воспроизведения с помощью этого метода, используйте метод **жетбинаме** и **ивмпплайлистаррай. Count** , чтобы узнать, существует ли уже список воспроизведения с определенным именем.

Начальные и конечные пробелы не допускаются в именах списков воспроизведения и автоматически удаляются из значения, указанного для параметра *bstrName* .

Перед вызовом этого метода необходимо иметь полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере создается пустой список воспроизведения с именем «Срилист», который добавляется в коллекцию списков воспроизведения и возвращается в него интерфейс. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Add a new empty playlist, named ThreeList, to the playlist collection.
WMPLib.IWMPPlaylist newList = player.playlistCollection.newPlaylist("ThreeList");
```


```VB

'  Add a new empty playlist, named ThreeList, to the playlist collection.
Dim newList As WMPLib.IWMPPlaylist = player.playlistCollection.newPlaylist(&quot;ThreeList&quot;)
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                                                     |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. Аппендитем (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-appenditem--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлист. insertItem (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистаррай. Count (VB и C#)**](wmplibiwmpplaylistarray-iwmpplaylistarray-count--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлистколлектион (VB и C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





