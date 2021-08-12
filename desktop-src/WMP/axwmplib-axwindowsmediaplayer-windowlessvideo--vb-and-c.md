---
title: Аксвиндовсмедиаплайер. Виндовлессвидео, свойство
description: свойство виндовлессвидео получает или задает значение, указывающее, визуализирует ли элемент управления проигрыватель Windows Media видео в режиме без окон.
ms.assetid: 70386aae-cd30-405d-90dd-9b3fa63dad17
keywords:
- проигрыватель Windows Media свойства виндовлессвидео
- проигрыватель Windows Media свойства виндовлессвидео, класс аксвиндовсмедиаплайер
- проигрыватель Windows Media класса аксвиндовсмедиаплайер, свойство виндовлессвидео
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
ms.openlocfilehash: 3a63a7246e730f73bd6d6f27111112a3db2029e3b53c80569e2e013771da6708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581524"
---
# <a name="axwindowsmediaplayerwindowlessvideo-property"></a>Аксвиндовсмедиаплайер. Виндовлессвидео, свойство

свойство виндовлессвидео получает или задает значение, указывающее, визуализирует ли элемент управления проигрыватель Windows Media видео в режиме без окон.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean windowlessVideo {get; set;}
```


```VB

Public Property windowlessVideo As System.Boolean
```





## <a name="property-value"></a>Значение свойства

значение System. Boolean, указывающее, визуализирует ли элемент управления проигрыватель Windows Media видео в режиме без окон. Значение по умолчанию — false.

## <a name="remarks"></a>Remarks

по умолчанию встроенный элемент управления проигрыватель Windows Media визуализирует видео в отдельном окне в клиентской области. если для **виндовлессвидео** задано значение true, то объект проигрыватель Windows Media визуализирует видео непосредственно в клиентской области, поэтому можно применять специальные эффекты или распространять видео с текстом.

в Windows Vista отрисовка видео в режиме без окон может привести к снижению производительности.

Получение значения для этого свойства не поддерживается для Netscape Navigator. Установка значения этого свойства в Netscape Navigator может привести к непредвиденным результатам.

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

 

 





