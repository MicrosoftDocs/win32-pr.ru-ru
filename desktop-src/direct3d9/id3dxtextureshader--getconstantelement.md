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
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273805"
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

## <a name="remarks"></a>Комментарии

Чтобы получить константу, которая не является частью массива, используйте [**ID3DXTextureShader::-Constant**](id3dxtextureshader--getconstant.md) или [**ID3DXTextureShader:: жетконстантбинаме**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
