---
title: Метод Ивмпплайлистаррай Item
description: Метод Item возвращает интерфейс Ивмпплайлист, представляющий список воспроизведения по указанному индексу.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Метод Item проигрыватель Windows Media Player
- Метод Item проигрыватель Windows Media Player, интерфейс Ивмпплайлистаррай
- Интерфейс Ивмпплайлистаррай Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718021"
---
# <a name="iwmpplaylistarrayitem-method"></a>Метод Ивмпплайлистаррай:: Item

Метод **Item** возвращает интерфейс **ивмпплайлист** , представляющий список воспроизведения по указанному индексу.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*Линдекс* \[ окне\]
</dt> <dd>

Объект **System. Int32** , содержащий индекс, определяющий список воспроизведения, который должен быть извлечен методом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Интерфейс **вмплиб. ивмпплайлист** для полученного списка воспроизведения.

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

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

[**Интерфейс Ивмпплайлистаррай (VB и C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





