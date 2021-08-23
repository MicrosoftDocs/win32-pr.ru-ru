---
title: Аксвиндовсмедиаплайер. Кдромколлектион, свойство
description: Свойство Кдромколлектион получает интерфейс Ивмпкдромколлектион, предоставляющий доступ к коллекции компакт-дисков или DVD-дисководов.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- проигрыватель Windows Media свойства кдромколлектион
- проигрыватель Windows Media свойства кдромколлектион, класс аксвиндовсмедиаплайер
- проигрыватель Windows Media класса аксвиндовсмедиаплайер, свойство кдромколлектион
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec885de319153383b82359e35208d19031fa7378749b39033402aba11f8dbd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055020"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a>Аксвиндовсмедиаплайер. Кдромколлектион, свойство

Свойство Кдромколлектион получает интерфейс **ивмпкдромколлектион** , предоставляющий доступ к коллекции компакт-дисков или DVD-дисководов.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a>Значение свойства

Интерфейс Вмплиб. Ивмпкдромколлектион.

## <a name="remarks"></a>Remarks

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

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

[**Интерфейс Ивмпкдромколлектион (VB и C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Медиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. Рекуестмедиаакцессригхтс (VB и C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





