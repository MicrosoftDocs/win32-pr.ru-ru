---
title: Ивмпкдромбурн Стартбурн, метод
description: Метод Стартбурн записывает компакт-диск.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- проигрыватель Windows Media метода стартбурн
- проигрыватель Windows Media метода стартбурн, интерфейс ивмпкдромбурн
- проигрыватель Windows Media интерфейса ивмпкдромбурн, метод стартбурн
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7806501a619d6172d9f1ce0715045c822b30326c2b59c268f432708ea13923ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761074"
---
# <a name="iwmpcdromburnstartburn-method"></a>Метод Ивмпкдромбурн:: Стартбурн

Метод **стартбурн** записывает компакт-диск.

## <a name="syntax"></a>Синтаксис


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Перед вызовом этого метода значение **бурнстате** должно быть Вмпбсреади или вмпбсстоппед.

Этот метод не будет работать, если дисковод компакт-дисков не является устройством записи или диск не доступен для записи. Чтобы определить, можно ли записать компакт-диск, воспользуйтесь возможностью **доступа** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромбурн. Бурнстате (VB и C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромбурн. доступ (VB и C#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромбурн. Стопбурн (VB и C#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





