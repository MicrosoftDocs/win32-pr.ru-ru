---
title: Ивмпкдромбурн, метод erase
description: Метод Erase стирает текущий компакт-диск.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- Стирание метода проигрывателя Windows Media Player
- Стирание метода проигрыватель Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4e168142a6ee77081871bb7dbefa79de8031d71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717983"
---
# <a name="iwmpcdromburnerase-method"></a>Метод Ивмпкдромбурн:: Erase

Метод **Erase** стирает текущий компакт-диск.

## <a name="syntax"></a>Синтаксис


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод не будет работать, если диск в устройстве не может быть перезаписываемым. Используйте [ивмпкдромбурн. Available](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) , чтобы определить, можно ли стереть компакт-диск.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





