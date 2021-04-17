---
description: Извлекает объект данных с указанным именем.
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'Метод ID3DXFileEnumObject:: Жетдатаобжектбинаме (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 41850615726ac15e890162c6e28df9b638c582a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703875"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a>Метод ID3DXFileEnumObject:: Жетдатаобжектбинаме

Извлекает объект данных с указанным именем.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*szName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на запрошенное имя.

</dd> <dt>

*ппобж* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Адрес указателя на интерфейс [**ID3DXFileData**](id3dxfiledata.md) , представляющий возвращаемый объект данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ NotFound.

## <a name="remarks"></a>Комментарии

Получите имя szName объекта данных текущего файла с помощью метода [**ID3DXFileData::**](id3dxfiledata--getname.md) GetObject.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
