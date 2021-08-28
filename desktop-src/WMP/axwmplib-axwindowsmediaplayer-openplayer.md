---
title: Аксвиндовсмедиаплайер. Опенплайер, метод
description: метод опенплайер открывается проигрыватель Windows Media с использованием указанного URL-адреса. | Аксвиндовсмедиаплайер. Опенплайер, метод
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- проигрыватель Windows Media метода опенплайер
- проигрыватель Windows Media метода опенплайер, класс аксвиндовсмедиаплайер
- класс аксвиндовсмедиаплайер проигрыватель Windows Media, метод опенплайер
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
ms.openlocfilehash: c9a2ae5660969e78aeb165c5f9fd9420ea04c79a6aeec9a57c4627cd61d32ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764714"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>Аксвиндовсмедиаплайер. Опенплайер, метод

метод **опенплайер** открывается проигрыватель Windows Media с использованием указанного URL-адреса.

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

## <a name="remarks"></a>Remarks

этот метод запускает проигрыватель Windows Media с указанным URL-адресом, установленным в качестве текущего элемента мультимедиа. Если проигрыватель был ранее закрыт в режиме обложки, он будет открыт с использованием обложки, последней выбранной пользователем. В противном случае проигрыватель откроется в полноэкранном режиме.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





