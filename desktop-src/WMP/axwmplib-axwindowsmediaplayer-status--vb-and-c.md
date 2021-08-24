---
title: Аксвиндовсмедиаплайер. status, свойство
description: свойство status получает значение, указывающее состояние проигрыватель Windows Media.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- свойство status проигрыватель Windows Media
- свойство status проигрыватель Windows Media, класс аксвиндовсмедиаплайер
- класс аксвиндовсмедиаплайер проигрыватель Windows Media, свойство status
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac46eeef411e1d728994d829d95727cdaf4020c2ef1b7511391b6ca0d2e31ff7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864564"
---
# <a name="axwindowsmediaplayerstatus-property"></a>Аксвиндовсмедиаплайер. status, свойство

свойство status получает значение, указывающее состояние проигрыватель Windows Media.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Значение свойства

Строка System. String, которая является состоянием.

## <a name="remarks"></a>Remarks

Значения, содержащиеся в этом свойстве, могут быть изменены в любое время, и их следует использовать только в целях вывода.

Аксвиндовсмедиаплайер. Событие **StatusChange** срабатывает при каждом изменении значения свойства.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Событие Аксвиндовсмедиаплайер. StatusChange (VB и C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





