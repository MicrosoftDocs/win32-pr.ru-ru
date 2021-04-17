---
title: IWMPSettings2 Дефаултаудиолангуаже, свойство
description: Свойство Дефаултаудиолангуаже получает код локали (LCID) используемого по умолчанию звукового языка, указанного в проигрывателе Windows Media.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- Проигрыватель Windows Media для свойства Дефаултаудиолангуаже
- Дефаултаудиолангуаже свойство проигрывателя Windows Media Player, интерфейс IWMPSettings2
- Интерфейс IWMPSettings2 Windows Media Player, свойство Дефаултаудиолангуаже
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
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685442"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2: свойство Ефаултаудиолангуаже:d

Свойство **дефаултаудиолангуаже** получает код локали (LCID) используемого по умолчанию звукового языка, указанного в проигрывателе Windows Media.

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

## <a name="remarks"></a>Комментарии

Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 9 Series или более поздней версии<br/>                                                                      |
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

 

 





