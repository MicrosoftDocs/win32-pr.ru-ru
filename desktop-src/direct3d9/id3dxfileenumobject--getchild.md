---
description: 'Метод ID3DXFileEnumObject:: Child — получает дочерний объект в этом объекте данных файла.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: Метод ID3DXFileEnumObject::-Child (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b26cf058b31d1016c68cccf3dde6ade9f84cde1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090362"
---
# <a name="id3dxfileenumobjectgetchild-method"></a>Метод ID3DXFileEnumObject:: Child

Извлекает дочерний объект в этом объекте данных файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор* \[ в\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

ИДЕНТИФИКАТОР получаемого дочернего объекта.

</dd> <dt>

*ппобж* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Адрес указателя для получения указателя интерфейса дочернего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ номореобжектс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
