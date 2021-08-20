---
description: Метод Сеткэйвалуе добавляет новое значение РЕФПРОПЕРТИКЭЙ (тип VT \_ Unknown) или перезаписывает существующий.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'Метод Ипортабледевицевалуес:: Сеткэйвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 850c9752d83e95aa6d602aec5a8d44fa43deb83728d0bc0c3130c30e04151a04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584304"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a>Метод Ипортабледевицевалуес:: Сеткэйвалуе

Метод **сеткэйвалуе** добавляет новое значение **РЕФПРОПЕРТИКЭЙ** (тип VT \_ Unknown) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
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

Объект **рефпропертикэй** , указывающий новое значение.

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



## <a name="see-also"></a>См. также

<dl> <dt>

[Добавление ресурса в объект](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жеткэйвалуе**](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




