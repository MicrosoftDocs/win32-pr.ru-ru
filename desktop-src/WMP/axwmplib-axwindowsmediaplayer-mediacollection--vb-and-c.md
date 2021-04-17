---
title: Аксвиндовсмедиаплайер. Медиаколлектион, свойство
description: Свойство Медиаколлектион получает интерфейс Ивмпмедиаколлектион, который предоставляет способ организации большой коллекции элементов мультимедиа.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- Проигрыватель Windows Media для свойства Медиаколлектион
- Медиаколлектион свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство Медиаколлектион
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699018"
---
# <a name="axwindowsmediaplayermediacollection-property"></a>Аксвиндовсмедиаплайер. Медиаколлектион, свойство

Свойство Медиаколлектион получает интерфейс **ивмпмедиаколлектион** , который предоставляет способ организации большой коллекции элементов мультимедиа.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a>Значение свойства

Интерфейс Вмплиб. Ивмпмедиаколлектион к коллекции элементов мультимедиа.

## <a name="remarks"></a>Комментарии

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

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

[**Интерфейс Ивмпмедиаколлектион (VB и C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





