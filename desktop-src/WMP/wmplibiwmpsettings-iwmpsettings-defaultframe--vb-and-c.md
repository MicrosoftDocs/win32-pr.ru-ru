---
title: Ивмпсеттингс Дефаултфраме, свойство
description: Свойство Дефаултфраме Возвращает или задает имя кадра, используемого для вывода URL-адреса, полученного в \_ \_ событии аксвиндовсмедиаплайер вмпокксевентс скрипткоммандевент.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- Проигрыватель Windows Media для свойства Дефаултфраме
- Дефаултфраме свойство проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Дефаултфраме
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
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717848"
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

## <a name="remarks"></a>Комментарии

Если целевой кадр указан в самом событии **\_ вмпокксевентс \_ скрипткоммандевент** , это свойство игнорируется.

Это свойство игнорируется при использовании приложения Netscape Navigator Java. В Netscape Navigator каждая полученная команда сценария URL-адреса будет отображать URL-адрес в новом окне браузера, независимо от значения **дефаултфраме**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Событие Аксвиндовсмедиаплайер. команду скрипта (VB и C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





