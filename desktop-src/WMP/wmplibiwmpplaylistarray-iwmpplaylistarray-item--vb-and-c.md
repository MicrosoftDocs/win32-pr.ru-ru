---
title: Метод Ивмпплайлистаррай Item
description: Метод Item возвращает интерфейс Ивмпплайлист, представляющий список воспроизведения по указанному индексу.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- проигрыватель Windows Media метода элемента
- метод Item проигрыватель Windows Media, интерфейс ивмпплайлистаррай
- проигрыватель Windows Media интерфейса ивмпплайлистаррай, метод Item
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
ms.openlocfilehash: 9e73614e1ef00f29d6b09d3d49e2c7e514bae807245f00f30f4d3382d8f1a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331163"
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

## <a name="remarks"></a>Remarks

Перед вызовом этого метода необходимо иметь доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                                                     |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпплайлист (VB и C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпплайлистаррай (VB и C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





