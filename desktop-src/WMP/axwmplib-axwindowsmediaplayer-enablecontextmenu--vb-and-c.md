---
title: Аксвиндовсмедиаплайер. Енаблеконтекстмену, свойство
description: Свойство Енаблеконтекстмену получает или задает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- Проигрыватель Windows Media для свойства Енаблеконтекстмену
- Енаблеконтекстмену свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Енаблеконтекстмену
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694460"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>Аксвиндовсмедиаплайер. Енаблеконтекстмену, свойство

Свойство Енаблеконтекстмену получает или задает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Значение свойства

Значение System. Boolean, указывающее, следует ли включить контекстное меню. Значение по умолчанию — true.

## <a name="remarks"></a>Комментарии

Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно «None».

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

 

 





