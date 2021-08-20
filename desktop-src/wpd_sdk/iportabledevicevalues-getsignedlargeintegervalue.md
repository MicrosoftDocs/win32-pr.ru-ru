---
description: Метод Жетсигнедларжеинтежервалуе извлекает значение ЛОНГЛОНГ (Type VT \_ I8), заданное ключом.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'Метод Ипортабледевицевалуес:: Жетсигнедларжеинтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 516d7c08b68e4480b3240ea9335793589114070859cf28d5cf91e645b616a2db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055114"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a>Метод Ипортабледевицевалуес:: Жетсигнедларжеинтежервалуе

Метод **жетсигнедларжеинтежервалуе** извлекает значение **ЛОНГЛОНГ** (Type VT \_ I8), заданное ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Ключ **рефпропертикэй** , указывающий извлекаемый элемент.

</dd> <dt>

*pValue* \[ заполняет\]
</dt> <dd>

Указатель на полученное значение **ulong** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                       |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, указанное *ключом* , не является типом **лонглонг** .<br/> |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/>   |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетсигнедларжеинтежервалуе**](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




