---
description: Метод Жетгуидвалуе извлекает значение GUID (тип VT \_ CLSID), заданное ключом.
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'Метод Ипортабледевицевалуес:: Жетгуидвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6389b426aca52f20b082ed4730778432bdbe56c4a6a1e0a4495060f13dbb5d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963683"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a>Метод Ипортабледевицевалуес:: Жетгуидвалуе

Метод **жетгуидвалуе** извлекает значение **GUID** (тип VT \_ CLSID), заданное ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
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

Указатель на полученное значение **GUID** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                     |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, указанное *ключом* , не является типом **GUID** .<br/>   |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/> |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Получение поддерживаемых методов службы](retrieving-supported-methods.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетгуидвалуе**](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[Получение поддерживаемых методов службы](retrieving-supported-methods.md)
</dt> <dt>

[Получение возможностей отрисовки, поддерживаемых устройством](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




