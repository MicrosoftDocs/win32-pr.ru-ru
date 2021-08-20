---
title: Ивмпкдромбурн, метод erase
description: Метод Erase стирает текущий компакт-диск.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- метод erase проигрыватель Windows Media
- метод erase проигрыватель Windows Media, интерфейс ивмпкдромбурн
- проигрыватель Windows Media интерфейса ивмпкдромбурн, метод erase
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
ms.openlocfilehash: 356b7bcdd332198c40760860e69741e76e0e993b6b47b3c5a5ff207d3d55bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116337"
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

## <a name="remarks"></a>Remarks

Этот метод не будет работать, если диск в устройстве не может быть перезаписываемым. Используйте [ивмпкдромбурн. Available](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) , чтобы определить, можно ли стереть компакт-диск.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





