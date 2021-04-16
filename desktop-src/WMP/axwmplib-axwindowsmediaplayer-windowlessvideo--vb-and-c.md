---
title: Аксвиндовсмедиаплайер. Виндовлессвидео, свойство
description: Свойство Виндовлессвидео получает или задает значение, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- Проигрыватель Windows Media для свойства Виндовлессвидео
- Виндовлессвидео свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Виндовлессвидео
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.windowlessVideo
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d22ecc0f39b03201809877fe8ebc667d62e16d0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699254"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>Аксвиндовсмедиаплайер. Виндовлессвидео, свойство

Свойство Виндовлессвидео получает или задает значение, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Значение свойства

Значение System. Boolean, указывающее, визуализирует ли элемент управления проигрывателем Windows Media видео в режиме без окон. Значением по умолчанию является false.

## <a name="remarks"></a>Комментарии

По умолчанию встроенный элемент управления проигрывателя Windows Media визуализирует видео в отдельном окне в клиентской области. Если для **виндовлессвидео** задано значение true, объект проигрывателя Windows Media визуализирует видео непосредственно в клиентской области, поэтому можно применять специальные эффекты или распространять видео с текстом.

В Windows Vista отрисовка видео в режиме без окон может привести к снижению производительности.

Получение значения для этого свойства не поддерживается для Netscape Navigator. Установка значения этого свойства в Netscape Navigator может привести к непредвиденным результатам.

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

 

 





