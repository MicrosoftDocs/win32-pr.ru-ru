---
description: Извлекает индекс грани сетки, к которой принадлежит каждый шаг текселя.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'Метод ID3DXTextureGutterHelper:: Жетфацемап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703855"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a>Метод ID3DXTextureGutterHelper:: Жетфацемап

Извлекает индекс грани сетки, к которой принадлежит каждый шаг текселя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфацедата* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на индекс грани сетки, к которой принадлежит каждый шаг текселя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение. D3DERR \_ инвалидкалл

## <a name="remarks"></a>Комментарии

Данные о грани сетки, возвращаемые этим методом, допустимы только для допустимых пикселей текстуры (не являющихся классами 0). [**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого (не класса 0) пикселей текстуры.

Для [**класса 2 пикселей текстуры**](id3dxtexturegutterhelper.md)этот метод извлекает ближайшее лицо.

Приложение должно выделить Пфацедата и управлять им.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
