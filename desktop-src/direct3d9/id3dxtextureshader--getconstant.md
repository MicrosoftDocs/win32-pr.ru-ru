---
description: Метод ID3DXTextureShader::-Constant — возвращает константу путем поиска своего индекса.
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: Метод ID3DXTextureShader::-Constant (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117672"
---
# <a name="id3dxtextureshadergetconstant-method"></a>Метод ID3DXTextureShader:: with Constant

Возвращает константу путем поиска своего индекса.

## <a name="syntax"></a>Синтаксис


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хконстант* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

[Маркер](handles.md) родительской структуры данных. Если константа является параметром верхнего уровня (отсутствует родительская структура данных), используйте **значение NULL**.

</dd> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Отсчитываемый от нуля индекс константы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Возвращает уникальный идентификатор для константы.

## <a name="remarks"></a>Remarks

Чтобы получить константу из массива констант, используйте [**ID3DXTextureShader:: жетконстантелемент**](id3dxtextureshader--getconstantelement.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
