---
description: Метод ID3DXSkinInfo::-Декларация Возвращает объявление вершины.
ms.assetid: 49738e9b-09cb-489f-b9af-32d220fbede8
title: Метод ID3DXSkinInfo::-декларация (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83554b13fe8e20890b1edecd690c540c2e14d4d7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093142"
---
# <a name="id3dxskininfogetdeclaration-method"></a>ID3DXSkinInfo:: метод объявления

Возвращает объявление вершины.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetDeclaration(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Объявление* \[ в, out\]
</dt> <dd>

Тип: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , описывающих формат вершин вершин сетки. Верхний предел этого массива декларатора — [**Max \_ фвф \_ DECL \_ size**](./max-fvf-decl-size.md). Массив элементов вершин заканчивается макросом [**D3DDECL \_ End**](d3ddecl-end.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Массив элементов включает макрос [**D3DDECL \_ End**](d3ddecl-end.md) , который завершает объявление.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> <dt>

[**ID3DXSkinInfo:: Сетдекларатион**](id3dxskininfo--setdeclaration.md)
</dt> </dl>

 

 
