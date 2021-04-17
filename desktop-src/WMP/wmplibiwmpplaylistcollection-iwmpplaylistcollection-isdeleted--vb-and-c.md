---
title: Ивмпплайлистколлектион метод isDeleted
description: Метод IsDeleted возвращает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.
ms.assetid: 02bc4b9f-6149-4fe2-8417-6484b22f2d74
keywords:
- метод IsDeleted Windows Media Player
- метод IsDeleted Windows Media Player, интерфейс Ивмпплайлистколлектион
- Интерфейс Ивмпплайлистколлектион Windows Media Player, метод isDeleted
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.isDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4ce4a314378c5a4a211a52b99ea1b36ae1fda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704052"
---
# <a name="iwmpplaylistcollectionisdeleted-method"></a>Метод Ивмпплайлистколлектион:: isDeleted

Метод **IsDeleted** возвращает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean isDeleted(
  IWMPPlaylist pItem
);
```


```VB

Public Function isDeleted( _
  ByVal pItem As IWMPPlaylist _
) As System.Boolean
Implements IWMPPlaylistCollection.isDeleted
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*питем* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмпплайлист** для запрашиваемого списка воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Boolean** , указывающее, был ли удален список воспроизведения.

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

[**Интерфейс Ивмпплайлистколлектион (VB и C#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





