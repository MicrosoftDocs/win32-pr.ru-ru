---
title: Аксвиндовсмедиаплайер. Опенплайер, метод
description: Метод Опенплайер открывает проигрыватель Windows Media с использованием указанного URL-адреса. | Аксвиндовсмедиаплайер. Опенплайер, метод
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- Опенплайер метод Windows Media Player
- Опенплайер метод Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, метод Опенплайер
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58416a1f20969b0bd223f653f44b5633f19cb096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694734"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>Аксвиндовсмедиаплайер. Опенплайер, метод

Метод **опенплайер** открывает проигрыватель Windows Media с использованием указанного URL-адреса.

## <a name="syntax"></a>Синтаксис


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бструрл* 
</dt> <dd>

**Строка System. String** , которая является URL-адресом элемента мультимедиа для воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод запускает проигрыватель Windows Media с указанным URL-адресом в качестве текущего элемента мультимедиа. Если проигрыватель был ранее закрыт в режиме обложки, он будет открыт с использованием обложки, последней выбранной пользователем. В противном случае проигрыватель откроется в полноэкранном режиме.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





