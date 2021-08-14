---
description: Метод Копивалуестопропертисторе копирует все значения из коллекции в интерфейс Ипропертисторе.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Метод Ипортабледевицевалуес:: Копивалуестопропертисторе (Портабледевицетипес. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2d134cb61831426451b1c6068bde5ca787b027fbe5b153587b45d9693ef739c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697251"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>Метод Ипортабледевицевалуес:: Копивалуестопропертисторе

Метод **копивалуестопропертисторе** копирует все значения из коллекции в интерфейс **ипропертисторе** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pStore* \[ окне\]
</dt> <dd>

Указатель на объект хранилища.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Этот метод не преобразует значения VT \_ LPWSTR в VT \_ BSTR. Многие внешние приложения или компоненты, взаимодействующие с приложением, например некоторые приложения оболочки, используют интерфейс **ипропертисторе** . Этот метод обеспечивает быстрый и простой способ обмена данными с этими программами.

этот метод поддерживается в Windows Vista и более поздних версиях Windows.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Портабледевицетипес. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Портабледевицегуидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ипортабледевицевалуес**](iportabledevicevalues.md)
</dt> <dt>

[**Ипортабледевицевалуес:: Копивалуесфромпропертисторе**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




