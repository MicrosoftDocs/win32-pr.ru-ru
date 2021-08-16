---
description: Метод Сетиункновнвалуе добавляет новое значение IUnknown (тип VT \_ Unknown) или перезаписывает существующий.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'Метод Ипортабледевицевалуес:: Сетиункновнвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c4a7c8a77cfef505b2a507b6281b931eea7f09c4ea1fbc79e651e7f517593799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697055"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a>Метод Ипортабледевицевалуес:: Сетиункновнвалуе

Метод **сетиункновнвалуе** добавляет новое значение **IUnknown** (тип VT \_ Unknown) или перезаписывает существующий.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
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

Указатель на интерфейс **IUnknown** , указывающий новое значение. Пакет SDK копирует ссылку на отправленный интерфейс и вызывает **AddRef** для него.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Если существующее значение имеет тот же ключ, что и параметр *Key* , он перезаписывает существующее значение без предупреждения. Существующий ключ памяти освобождается соответствующим образом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Жетиункновнвалуе**](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




