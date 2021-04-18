---
title: Аксвиндовсмедиаплайер. status, свойство
description: Свойство Status получает значение, указывающее состояние проигрывателя Windows Media.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Свойство Status проигрыватель Windows Media
- Свойство Status проигрыватель Windows Media, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Status
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
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695039"
---
# <a name="axwindowsmediaplayerstatus-property"></a>Аксвиндовсмедиаплайер. status, свойство

Свойство Status получает значение, указывающее состояние проигрывателя Windows Media.

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

## <a name="remarks"></a>Комментарии

Значения, содержащиеся в этом свойстве, могут быть изменены в любое время, и их следует использовать только в целях вывода.

Аксвиндовсмедиаплайер. Событие **StatusChange** срабатывает при каждом изменении значения свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Событие Аксвиндовсмедиаплайер. StatusChange (VB и C#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





