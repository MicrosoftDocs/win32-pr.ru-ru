---
description: Метод Жетунсигнединтежервалуе извлекает значение типа ULONG (тип VT \_ UI4), заданное ключом.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'Метод Ипортабледевицевалуес:: Жетунсигнединтежервалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: eeb418d3d0aa42675f3d5766f2a8d08e1ad2377bbaa4a2a07f4ba96524d3dec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026842"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a>Метод Ипортабледевицевалуес:: Жетунсигнединтежервалуе

Метод **жетунсигнединтежервалуе** извлекает значение типа **ulong** (тип VT \_ UI4), заданное ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
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



| Код возврата                                                                                                            | Описание                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                     |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, указанное *ключом* , не является типом **ulong** .<br/>  |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/> |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетунсигнединтежервалуе**](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[Получение поддерживаемых событий службы](retrieving-supported-events.md)
</dt> <dt>

[Получение поддерживаемых методов службы](retrieving-supported-methods.md)
</dt> <dt>

[Получение возможностей отрисовки, поддерживаемых устройством](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




