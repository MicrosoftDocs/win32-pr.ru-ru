---
description: Извлекает объект данных с указанным GUID.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'Метод ID3DXFileEnumObject:: Жетдатаобжектбид (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713799"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>Метод ID3DXFileEnumObject:: Жетдатаобжектбид

Извлекает объект данных с указанным GUID.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
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

Тип: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

Адрес указателя на интерфейс [**ID3DXFileData**](id3dxfiledata.md) , представляющий возвращаемый объект данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.

## <a name="remarks"></a>Комментарии

Получите идентификатор GUID ргуид текущего файлового объекта данных с помощью метода [**ID3DXFileData:: GetId**](id3dxfiledata--getid.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
