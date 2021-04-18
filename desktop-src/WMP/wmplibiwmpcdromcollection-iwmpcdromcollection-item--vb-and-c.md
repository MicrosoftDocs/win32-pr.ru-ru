---
title: Метод Ивмпкдромколлектион Item
description: Метод Item возвращает интерфейс Ивмпкдром по заданному индексу.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Метод Item проигрыватель Windows Media Player
- Метод Item проигрыватель Windows Media Player, интерфейс Ивмпкдромколлектион
- Интерфейс Ивмпкдромколлектион Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717956"
---
# <a name="iwmpcdromcollectionitem-method"></a>Метод Ивмпкдромколлектион:: Item

Метод **Item** возвращает интерфейс **ивмпкдром** по заданному индексу.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*Линдекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , который является индексом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпкдром** .

## <a name="remarks"></a>Комментарии

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере **элемент** используется для вывода спецификатора диска и имени списка воспроизведения с каждого компакт-диска, доступного на компьютере в окне списка. Если на самом деле диск содержит содержимое DVD, требуется ОС Windows XP или более поздней версии. Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдром (VB и C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпкдромколлектион (VB и C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромколлектион. Count (VB и C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромколлектион. ЖетбидривеспеЦифиер (VB и C#)**](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.name (VB и C#)**](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





