---
description: Метод Жетипортабледевицевалуесвалуе извлекает значение Ипортабледевицевалуес (тип VT \_ Unknown), заданный ключом.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'Метод Ипортабледевицевалуес:: Жетипортабледевицевалуесвалуе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: aeec29bf3d9cf18bcf54c885d46d159c21c661a1e886903110952cd3a23c540e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055164"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a>Метод Ипортабледевицевалуес:: Жетипортабледевицевалуесвалуе

Метод **жетипортабледевицевалуесвалуе** извлекает значение **ИПОРТАБЛЕДЕВИЦЕВАЛУЕС** (тип VT \_ Unknown), заданный ключом.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
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

Адрес переменной, которая получает указатель на полученный интерфейс [**ипортабледевицевалуес**](iportabledevicevalues.md) . Вызывающий объект отвечает за вызов метода **Release** на полученном интерфейсе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                                            | Описание                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                                   | Метод выполнен успешно.<br/>                                                          |
| <dl> <dt>**\_вытипемисматч E \_**</dt> </dl>                   | Свойство, заданное *ключом* , не является интерфейсом **ипортабледевицевалуес** .<br/> |
| <dl> <dt>**HRESULT \_ из \_ Win32 (ошибка \_ не \_ найдена)**</dt> </dl> | Свойство, указанное *ключом* , отсутствует в коллекции.<br/>                      |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Сетипортабледевицевалуесвалуе**](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[Получение поддерживаемых событий службы](retrieving-supported-events.md)
</dt> <dt>

[Получение возможностей отрисовки, поддерживаемых устройством](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




