---
description: Задает индекс грани сетки, к которой принадлежит каждый шаг текселя.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'Метод ID3DXTextureGutterHelper:: Сетфацемап (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a7de812f5445d0d8d704aeba939cf8cbc4441d4ed542bf716371a7fc12a1ba6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747384"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a>Метод ID3DXTextureGutterHelper:: Сетфацемап

Задает индекс грани сетки, к которой принадлежит каждый шаг текселя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetFaceMap(
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

## <a name="remarks"></a>Remarks

Входные данные грани сетки для этого метода допустимы только для допустимых пикселей текстуры (не являющихся классами 0). [**ID3DXTextureGutterHelper:: жетгуттермап**](id3dxtexturegutterhelper--getguttermap.md) будет возвращать ненулевые значения для допустимого пикселей текстуры.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
