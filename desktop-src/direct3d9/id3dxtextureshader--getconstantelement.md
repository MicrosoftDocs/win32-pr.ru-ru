---
description: Получить константу из таблицы констант.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'Метод ID3DXTextureShader:: Жетконстантелемент (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02d21efb3ef0ed5d4602833571b2b1a32e73df73b76f82a357cda574e93e84ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747393"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>Метод ID3DXTextureShader:: Жетконстантелемент

Получить константу из таблицы констант.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Маркер](handles.md) массива констант. Это значение не может быть **равно NULL**.

</dd> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс элемента в таблице констант.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает уникальный идентификатор для константы.

## <a name="remarks"></a>Remarks

Чтобы получить константу, которая не является частью массива, используйте [**ID3DXTextureShader::-Constant**](id3dxtextureshader--getconstant.md) или [**ID3DXTextureShader:: жетконстантбинаме**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
