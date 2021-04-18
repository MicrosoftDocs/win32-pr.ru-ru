---
title: Ивмплибрарисервицес Жеткаунтбитипе, метод
description: Метод Жеткаунтбитипе возвращает количество доступных библиотек указанного типа.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- Жеткаунтбитипе метод Windows Media Player
- Жеткаунтбитипе метод проигрывателя Windows Media Player, интерфейс Ивмплибрарисервицес
- Интерфейс Ивмплибрарисервицес Windows Media Player, метод Жеткаунтбитипе
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669265"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>Метод Ивмплибрарисервицес:: Жеткаунтбитипе

Метод **жеткаунтбитипе** возвращает количество доступных библиотек указанного типа.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*вмплт* \[ окне\]
</dt> <dd>

Значение из перечисления **вмплиб. вмплибраритипе** , указывающее тип библиотеки для подсчета.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Int32** , которое является счетчиком библиотеки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмплибрарисервицес (VB и C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**вмплибраритипе**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





