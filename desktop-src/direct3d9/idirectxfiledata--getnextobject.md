---
description: Извлекает следующий дочерний объект данных, объект ссылки на данные или двоичный объект в файле DirectX. Не рекомендуется.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Метод Идиректксфиледата:: Жетнекстобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713867"
---
# <a name="idirectxfiledatagetnextobject-method"></a>Метод Идиректксфиледата:: Жетнекстобжект

Извлекает следующий дочерний объект данных, объект ссылки на данные или двоичный объект в файле DirectX. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппчилдобж* \[ out, retval\]
</dt> <dd>

Тип: **[ **лпдиректксфилеобжект**](idirectxfileobject.md)\***

Адрес указателя на интерфейс [**идиректксфилеобжект**](idirectxfileobject.md) , представляющий интерфейс объектного объекта, возвращенного дочерним объектом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ номореобжектс.

## <a name="remarks"></a>Комментарии

Чтобы определить тип извлекаемого объекта, используйте QueryInterface для запроса полученного объекта для поддержки интерфейсов [**идиректксфиледата**](idirectxfiledata.md), [**идиректксфиледатареференце**](idirectxfiledatareference.md)или [**идиректксфилебинари**](idirectxfilebinary.md) . Поддерживаемый интерфейс указывает тип объекта (данные, ссылку на данные или двоичный).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идиректксфилебинари**](idirectxfilebinary.md)
</dt> <dt>

[**идиректксфиледата**](idirectxfiledata.md)
</dt> <dt>

[**идиректксфиледатареференце**](idirectxfiledatareference.md)
</dt> </dl>

 

 




