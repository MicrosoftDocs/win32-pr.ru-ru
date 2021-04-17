---
description: Метод GetStringValue извлекает строковое значение (тип VT \_ LPWSTR), заданное ключом.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'Метод Ипортабледевицевалуес:: GetStringValue (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698962"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a>Метод Ипортабледевицевалуес:: GetStringValue

Метод **GetStringValue** извлекает строковое значение (тип VT \_ LPWSTR), заданное ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
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

Указатель на полученное значение **LPWSTR** . Вызывающий объект отвечает за вызов **CoTaskMemFree** для освобождения памяти.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                      |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, заданное *ключом* , не является типом **LPWSTR** .<br/> |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/>  |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: GetAt**](iportabledevicevalues-getat.md)
</dt> <dt>

[**Ипортабледевицевалуес:: SetStringValue**](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[Получение поддерживаемых событий службы](retrieving-supported-events.md)
</dt> <dt>

[Получение поддерживаемых форматов службы](retrieving-supported-formats.md)
</dt> <dt>

[Получение поддерживаемых методов службы](retrieving-supported-methods.md)
</dt> </dl>

 

 




