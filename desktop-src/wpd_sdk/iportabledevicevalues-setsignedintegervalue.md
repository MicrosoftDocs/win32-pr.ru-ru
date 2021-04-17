---
description: Метод Сетсигнединтежервалуе добавляет новое ДЛИННое значение (тип VT \_ i4) или перезаписывает существующий.
ms.assetid: b0bb2992-2906-446c-be9a-20bff13f8e1d
title: 'Метод Ипортабледевицевалуес:: Сетсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 26a5d01ec69203c39008de394e3693acc833d262
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704267"
---
# <a name="iportabledevicevaluessetsignedintegervalue-method"></a>Метод Ипортабледевицевалуес:: Сетсигнединтежервалуе

Метод **сетсигнединтежервалуе** добавляет новое **длинное** значение (тип VT \_ i4) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetSignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONG           Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.

</dd> <dt>

*Значение* \[ окне\]
</dt> <dd>

**Целое** число, указывающее новое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетсигнединтежервалуе**](iportabledevicevalues-getsignedintegervalue.md)
</dt> </dl>

 

 




