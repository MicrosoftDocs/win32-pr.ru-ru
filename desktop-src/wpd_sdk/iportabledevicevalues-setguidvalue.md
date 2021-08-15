---
description: Метод Сетгуидвалуе добавляет новое значение GUID (Type VT \_ CLSID) или перезаписывает существующий.
ms.assetid: 429a83c0-59b6-4e2f-a657-cbec1dfb9070
title: 'Метод Ипортабледевицевалуес:: Сетгуидвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de2554422ca9df16a1a1df98a5f4888e4914909885c6661818b0692b33b66763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963593"
---
# <a name="iportabledevicevaluessetguidvalue-method"></a>Метод Ипортабледевицевалуес:: Сетгуидвалуе

Метод **сетгуидвалуе** добавляет новое значение **GUID** (Type VT \_ CLSID) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetGuidValue(
  [in] REFPROPERTYKEY key,
  [in] REFGUID        Value
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

Объект **рефгуид** , содержащий новое значение.

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



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Добавление ресурса в объект](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетгуидвалуе**](iportabledevicevalues-getguidvalue.md)
</dt> </dl>

 

 




