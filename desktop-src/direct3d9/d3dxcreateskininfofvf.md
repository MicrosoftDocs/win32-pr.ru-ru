---
description: Создает пустой объект сетки обложки, используя код гибкого формата вершин (ФВФ).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: Функция D3DXCreateSkinInfoFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ccf10bad879b51f42c743ddd18112e24d355b366691b7922816164e57ed1b3d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495784"
---
# <a name="d3dxcreateskininfofvf-function"></a>Функция D3DXCreateSkinInfoFVF

Создает пустой объект сетки обложки, используя код гибкого формата вершин (ФВФ).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Нумвертицес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число вершин для сетки обложки.

</dd> <dt>

*Фвф* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание [D3DFVF](d3dfvf.md) , описывающее формат вершины для возвращаемой сетки обложки.

</dd> <dt>

*Нумбонес* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Число костей для сетки обложки.

</dd> <dt>

*ппскининфо* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Адрес указателя на интерфейс [**ID3DXSkinInfo**](id3dxskininfo.md) , представляющий созданный объект сведений о обложке.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Используйте [**сетбонеинфлуенце**](id3dxskininfo--setboneinfluence.md) для заполнения пустого объекта сетки обложки, возвращаемого этим методом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**сетбонеинфлуенце**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
