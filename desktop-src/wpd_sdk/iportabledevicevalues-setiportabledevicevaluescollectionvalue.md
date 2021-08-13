---
description: Метод Сетипортабледевицевалуесколлектионвалуе добавляет новое значение Ипортабледевицевалуесколлектион (тип VT \_ Unknown) или перезаписывает существующий.
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: 'Метод Ипортабледевицевалуес:: Сетипортабледевицевалуесколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7f015333a8d384743d0e8ea16000252a4e60fd24ab0637b92ee3d85ddb42a1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697092"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a>Метод Ипортабледевицевалуес:: Сетипортабледевицевалуесколлектионвалуе

Метод **сетипортабледевицевалуесколлектионвалуе** добавляет новое значение **ИПОРТАБЛЕДЕВИЦЕВАЛУЕСКОЛЛЕКТИОН** (тип VT \_ Unknown) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Объект **рефпропертикэй** , указывающий элемент для создания или перезаписи.

</dd> <dt>

*pValue* \[ окне\]
</dt> <dd>

Указатель на интерфейс **ипортабледевицевалуесколлектион** , указывающий новое значение. Пакет SDK копирует ссылку на отправленный интерфейс и вызывает **AddRef** для него.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения. Существующий ключ памяти освобождается соответствующим образом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетипортабледевицевалуесколлектионвалуе**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




