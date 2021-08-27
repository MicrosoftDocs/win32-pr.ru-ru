---
title: Ивмпплайлист Аппендитем, метод
description: Метод Аппендитем добавляет элемент мультимедиа в конец списка воспроизведения.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- проигрыватель Windows Media метода аппендитем
- проигрыватель Windows Media метода аппендитем, интерфейс ивмпплайлист
- проигрыватель Windows Media интерфейса ивмпплайлист, метод аппендитем
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de67c7bbd3448e4b4fcdb562b2b10ace68ed7a2c92020650c79fdd90b05366b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098704"
---
# <a name="iwmpplaylistappenditem-method"></a>Метод Ивмпплайлист:: Аппендитем

Метод **аппендитем** добавляет элемент мультимедиа в конец списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*пивмпмедиа* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпмедиа** , представляющий добавляемый элемент мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Перед вызовом этого метода необходимо иметь полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере **аппендитем** используется для добавления текущего элемента мультимедиа в список воспроизведения с именем «срилист». Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпмедиа (VB и C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





