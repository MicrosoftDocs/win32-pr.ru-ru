---
description: Метод Сетунсигнединтежервалуе добавляет новое значение типа ULONG (тип VT \_ UI4) или перезаписывает существующий.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'Метод Ипортабледевицевалуес:: Сетунсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704264"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a>Метод Ипортабледевицевалуес:: Сетунсигнединтежервалуе

Метод **сетунсигнединтежервалуе** добавляет новое значение типа **ulong** (тип VT \_ UI4) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
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

**Ulong** , задающее новое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [**Указание сведений о клиенте**](specifying-client-information.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетунсигнединтежервалуе**](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[**Указание сведений о клиенте**](specifying-client-information.md)
</dt> </dl>

 

 




