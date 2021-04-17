---
title: Ивмпкдромбурн Стартбурн, метод
description: Метод Стартбурн записывает компакт-диск.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- Стартбурн метод Windows Media Player
- Стартбурн метод проигрывателя Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод Стартбурн
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
ms.openlocfilehash: fe185d8993286e4be3935b43f6c1e9757623309d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717976"
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

## <a name="remarks"></a>Комментарии

Перед вызовом этого метода значение **бурнстате** должно быть Вмпбсреади или вмпбсстоппед.

Этот метод не будет работать, если дисковод компакт-дисков не является устройством записи или диск не доступен для записи. Чтобы определить, можно ли записать компакт-диск, воспользуйтесь возможностью **доступа** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмпкдромбурн (VB и C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромбурн. Бурнстате (VB и C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромбурн. доступ (VB и C#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**Ивмпкдромбурн. Стопбурн (VB и C#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





