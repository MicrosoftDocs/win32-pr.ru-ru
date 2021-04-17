---
description: Метод Жетипортабледевицекэйколлектионвалуе извлекает значение Ипортабледевицекэйколлектион (тип VT \_ Unknown), заданный ключом.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'Метод Ипортабледевицевалуес:: Жетипортабледевицекэйколлектионвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675501"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a>Метод Ипортабледевицевалуес:: Жетипортабледевицекэйколлектионвалуе

Метод **жетипортабледевицекэйколлектионвалуе** извлекает значение **ИПОРТАБЛЕДЕВИЦЕКЭЙКОЛЛЕКТИОН** (тип VT \_ Unknown), заданный ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ключ* \[ окне\]
</dt> <dd>

Ключ **рефпропертикэй** , указывающий извлекаемый элемент.

</dd> <dt>

*ппвалуе* \[ заполняет\]
</dt> <dd>

Указатель на полученный указатель интерфейса [**ипортабледевицекэйколлектион**](iportabledevicekeycollection.md) . Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                                                 |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, заданное *ключом* , не является интерфейсом **ипортабледевицекэйколлектион** .<br/> |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/>                             |



 

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

[**Ипортабледевицевалуес:: Сетипортабледевицекэйколлектионвалуе**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[Получение поддерживаемых событий службы](retrieving-supported-events.md)
</dt> <dt>

[Получение поддерживаемых методов службы](retrieving-supported-methods.md)
</dt> </dl>

 

 




