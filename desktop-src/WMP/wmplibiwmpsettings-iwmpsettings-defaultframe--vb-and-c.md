---
title: Ивмпсеттингс Дефаултфраме, свойство
description: Свойство Дефаултфраме Возвращает или задает имя кадра, используемого для вывода URL-адреса, полученного в \_ \_ событии аксвиндовсмедиаплайер вмпокксевентс скрипткоммандевент.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- проигрыватель Windows Media свойства дефаултфраме
- проигрыватель Windows Media свойства дефаултфраме, интерфейс ивмпсеттингс
- проигрыватель Windows Media интерфейса ивмпсеттингс, свойство дефаултфраме
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39352b2c49bfdcd50f3e5c74d88a9fafef6752034dbd220cda3bb34dc0ed5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053442"
---
# <a name="iwmpsettingsdefaultframe-property"></a>Ивмпсеттингс: свойство Ефаултфраме:d

Свойство **дефаултфраме** Возвращает или задает имя кадра, используемого для вывода URL-адреса, полученного в событии **аксвиндовсмедиаплайер \_ вмпокксевентс \_ скрипткоммандевент** .

## <a name="syntax"></a>Синтаксис


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Значение свойства

**Строка System. String** , которая является значением атрибута Name целевого элемента **Frame** .

## <a name="remarks"></a>Remarks

Если целевой кадр указан в самом событии **\_ вмпокксевентс \_ скрипткоммандевент** , это свойство игнорируется.

Это свойство игнорируется при использовании приложения Netscape Navigator Java. В Netscape Navigator каждая полученная команда сценария URL-адреса будет отображать URL-адрес в новом окне браузера, независимо от значения **дефаултфраме**.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Событие Аксвиндовсмедиаплайер. команду скрипта (VB и C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





