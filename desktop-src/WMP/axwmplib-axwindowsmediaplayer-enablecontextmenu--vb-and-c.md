---
title: Аксвиндовсмедиаплайер. Енаблеконтекстмену, свойство
description: Свойство Енаблеконтекстмену получает или задает значение, указывающее, следует ли включать контекстное меню, которое появляется при нажатии правой кнопки мыши.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- проигрыватель Windows Media свойства енаблеконтекстмену
- проигрыватель Windows Media свойства енаблеконтекстмену, класс аксвиндовсмедиаплайер
- проигрыватель Windows Media класса аксвиндовсмедиаплайер, свойство енаблеконтекстмену
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
ms.openlocfilehash: 5603762ec9823f7e9896c5c22c1dee33f2399bb02301921057f8502046bcc002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582343"
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

## <a name="remarks"></a>Remarks

во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно "none".

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                          |
| Пространство имен<br/> | **аксвмплиб**<br/>                                                                                                    |
| Сборка<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Аксвиндовсмедиаплайер (VB и C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





