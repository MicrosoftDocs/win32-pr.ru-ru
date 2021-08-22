---
title: Свойство автозапуска Ивмпсеттингс
description: Свойство автозапуска получает или задает значение, указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- проигрыватель Windows Media свойства автозапуска
- свойство "автозапуск" проигрыватель Windows Media, интерфейс ивмпсеттингс
- проигрыватель Windows Media интерфейса ивмпсеттингс, свойство "автозапуск"
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7be64a030bbfe8abbd81830a7638094cd3da93939f3184ad3a4cfca0063c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568471"
---
# <a name="iwmpsettingsautostart-property"></a>Свойство Ивмпсеттингс:: Автозапуск

Свойство **автозапуска** получает или задает значение, указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Значение свойства

Значение **System. Boolean** , указывающее, начинается ли воспроизведение текущего элемента мультимедиа автоматически. Значение по умолчанию — **true**.

## <a name="remarks"></a>Remarks

Если параметру **автозапуска** присвоено значение **true**, воспроизведение элемента мультимедиа начнется при установке **аксвиндовсмедиаплайер. URL**, **аксвиндовсмедиаплайер. куррентплайлист** или **аксвиндовсмедиаплайер. currentMedia** . В противном случае воспроизведение элемента мультимедиа не начнется до тех пор, пока не будет вызван метод **ивмпконтролс. Play** .

Если не задать для параметра **Автозапуск** значение **true** непосредственно перед указанием элемента мультимедиа, не следует полагаться на этот параметр в качестве замены с помощью метода **ивмпконтролс. Play** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. Куррентплайлист (VB и C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**Аксвиндовсмедиаплайер. URL (VB и C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Ивмпконтролс. Play (VB и C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





