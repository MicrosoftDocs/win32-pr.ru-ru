---
description: Метод GetAt извлекает объект PROPERTYKEY из коллекции по индексу.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Метод Ипортабледевицекэйколлектион:: GetAt (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708349"
---
# <a name="iportabledevicekeycollectiongetat-method"></a>Метод Ипортабледевицекэйколлектион:: GetAt

Метод **GetAt** извлекает объект **PROPERTYKEY** из коллекции по индексу.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

**Параметр DWORD** , содержащий индекс извлекаемого ключа.

</dd> <dt>

*pKey* \[ заполняет\]
</dt> <dd>

Указатель на объект **PROPERTYKEY** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                                  | Описание                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод выполнен успешно.<br/>                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Переданный индекс был вне допустимого диапазона.<br/>     |
| <dl> <dt>**\_указатель E**</dt> </dl>    | Обязательный аргумент-указатель имеет **значение NULL**.<br/> |



 

## <a name="examples"></a>Примеры

Пример использования этого метода см. в разделе [Получение поддерживаемых событий службы](retrieving-supported-events.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицекэйколлектион**](iportabledevicekeycollection.md)
</dt> <dt>

[Получение поддерживаемых событий службы](retrieving-supported-events.md)
</dt> <dt>

[Получение поддерживаемых методов службы](retrieving-supported-methods.md)
</dt> </dl>

 

 




