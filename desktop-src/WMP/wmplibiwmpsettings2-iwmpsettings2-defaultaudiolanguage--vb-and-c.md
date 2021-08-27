---
title: IWMPSettings2 Дефаултаудиолангуаже, свойство
description: свойство дефаултаудиолангуаже получает идентификатор локали (LCID) для используемого по умолчанию аудио языка, указанного в проигрыватель Windows Media.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- проигрыватель Windows Media свойства дефаултаудиолангуаже
- проигрыватель Windows Media свойства дефаултаудиолангуаже, интерфейс IWMPSettings2
- проигрыватель Windows Media интерфейса IWMPSettings2, свойство дефаултаудиолангуаже
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09df11cc53e9b813de2e40e40eca1e31a88afeff0c16ce1f9c0c5ba4745277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331104"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2: свойство Ефаултаудиолангуаже:d

свойство **дефаултаудиолангуаже** получает идентификатор локали (LCID) для используемого по умолчанию аудио языка, указанного в проигрыватель Windows Media.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Значение свойства

Значение **System. Int32** , которое является LCID.

## <a name="remarks"></a>Remarks

Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IWMPControls3. Куррентаудиолангуаже (VB и C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Интерфейс Ивмпсеттингс (VB и C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**Интерфейс IWMPSettings2 (VB и C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





