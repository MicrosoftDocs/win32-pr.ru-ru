---
description: Метод Жетфлоатвалуе извлекает значение FLOAT (тип VT \_ R4), заданное ключом.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Метод Ипортабледевицевалуес:: Жетфлоатвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 364b5de9bbf8b3c5bb307b7bbc0e11fc018393c301c0931e065331879ec096fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430827"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>Метод Ипортабледевицевалуес:: Жетфлоатвалуе

Метод **жетфлоатвалуе** извлекает значение **float** (тип VT \_ R4), заданное ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
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

Указатель на полученное значение **float** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                             | Описание                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                    | Метод выполнен успешно.<br/>                                     |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>    | Свойство, указанное *ключом* , не имеет тип **float** .<br/>  |
| <dl> <dt>**идентификатор "E \_ prop" \_ \_ не поддерживается**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетфлоатвалуе**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




