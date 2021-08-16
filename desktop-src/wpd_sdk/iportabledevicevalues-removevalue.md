---
description: Метод Ремовевалуе удаляет элемент из коллекции.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'Метод Ипортабледевицевалуес:: Ремовевалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2cc21976b72c0d493f1534d63ea5da56fac059db6444ed81c310b9c154f3ee3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963623"
---
# <a name="iportabledevicevaluesremovevalue-method"></a>Метод Ипортабледевицевалуес:: Ремовевалуе

Метод **ремовевалуе** удаляет элемент из коллекции.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Объект **рефпропертикэй** , указывающий удаляемый элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**Ипортабледевицевалуес:: SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




