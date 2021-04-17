---
title: Аксвиндовсмедиаплайер. Стретчтофит, свойство
description: Свойство Стретчтофит получает или задает значение, указывающее, будет ли видео, отображаемое элементом управления проигрывателя Windows Media, автоматически соответствовать размеру окна видео, если видеоокно больше размеров изображения видео.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- Проигрыватель Windows Media для свойства Стретчтофит
- Стретчтофит свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Стретчтофит
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd6937ffa556817a80f0b21dfaed6d270c2e351
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698818"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>Аксвиндовсмедиаплайер. Стретчтофит, свойство

Свойство Стретчтофит получает или задает значение, указывающее, будет ли видео, отображаемое элементом управления проигрывателя Windows Media, автоматически соответствовать размеру окна видео, если видеоокно больше размеров изображения видео.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Значение свойства

Значение System. Boolean, указывающее, будет ли видео растягиваться в соответствии с размерами окна. Значением по умолчанию является false.

## <a name="remarks"></a>Комментарии

Если **стретчтофит** имеет значение true, элемент управления проигрывателя Windows Media сохраняет исходные пропорции видео. Если пропорции видео не соответствуют пропорциям видеоокна, то области с черной маской могут отображаться в верхней и нижней, левой и правой частях изображения видео.

Это свойство применяется к элементу управления проигрывателя Windows Media только при его внедрении в веб-страницу.

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

 

 





