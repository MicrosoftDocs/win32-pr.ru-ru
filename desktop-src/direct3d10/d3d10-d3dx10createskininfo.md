---
description: Функция D3DX10CreateSkinInfo — создает пустой объект сетки обложки с помощью декларатора.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Функция D3DX10CreateSkinInfo (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103602"
---
# <a name="d3dx10createskininfo-function"></a>Функция D3DX10CreateSkinInfo

Создает пустой объект сетки обложки с помощью декларатора.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппскининфо* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Адрес указателя на [**интерфейс ID3DX10SkinInfo**](id3dx10skininfo.md), представляющий созданный объект сетки обложки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть следующим: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Используйте [**ID3DX10SkinInfo:: сетбонеинфлуенце**](id3dx10skininfo-setboneinfluence.md) для заполнения пустого объекта сетки обложки, возвращаемого этим методом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции сетки](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Функции D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




