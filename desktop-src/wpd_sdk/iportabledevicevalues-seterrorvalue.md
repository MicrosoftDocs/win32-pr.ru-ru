---
description: Метод Сетеррорвалуе добавляет новое значение HRESULT (тип \_ "ошибка VT") или перезаписывает существующую.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'Метод Ипортабледевицевалуес:: Сетеррорвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 41bb9a6d8f2878b9bcfac6584c39fd55153ecae8a539c7f8886a5d0eb90d1bb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026792"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a>Метод Ипортабледевицевалуес:: Сетеррорвалуе

Метод **сетеррорвалуе** добавляет новое значение **HRESULT** (тип \_ "ошибка VT") или перезаписывает существующую.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
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

Значение **HRESULT** , содержащее новое значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетеррорвалуе**](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




