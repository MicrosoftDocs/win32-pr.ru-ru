---
description: Извлекает объект данных с указанным GUID. Не рекомендуется.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'Метод Идиректксфилинумобжект:: Жетдатаобжектбид (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713443"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a>Метод Идиректксфилинумобжект:: Жетдатаобжектбид

Извлекает объект данных с указанным GUID. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ргуид* \[ окне\]
</dt> <dd>

Тип: **[рефгуид](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

Ссылка на запрошенный GUID.

</dd> <dt>

*ппдатаобж* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***

Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий возвращаемый объект данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилинумобжект](idirectxfileenumobject.md)
</dt> </dl>

 

 
