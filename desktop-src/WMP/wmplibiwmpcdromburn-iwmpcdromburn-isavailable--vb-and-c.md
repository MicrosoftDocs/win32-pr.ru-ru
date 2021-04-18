---
title: Ивмпкдромбурн доступный метод
description: Метод Available предоставляет сведения о дисководе компакт-дисков и носителях.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- метод Available проигрыватель Windows Media Player
- метод Available проигрыватель Windows Media Player, интерфейс Ивмпкдромбурн
- Интерфейс Ивмпкдромбурн Windows Media Player, метод Available
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717980"
---
# <a name="iwmpcdromburnisavailable-method"></a>Метод Ивмпкдромбурн:: Available

Метод **Available** предоставляет сведения о ДИСКОВОДЕ компакт-дисков и носителях.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстритем* \[ окне\]
</dt> <dd>

**Строка System. String** , которая содержит одно из следующих значений.



| Значение | Описание                 |
|-------|-----------------------------|
| Записать  | Диск является устройством записи компакт-дисков.   |
| Корр  | В дисководе есть компакт-диск. |
| Очистка | Компакт-диск можно стереть.       |
| запись | Компакт-диск можно записать в.   |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Boolean** , указывающее результат.

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

 

 





