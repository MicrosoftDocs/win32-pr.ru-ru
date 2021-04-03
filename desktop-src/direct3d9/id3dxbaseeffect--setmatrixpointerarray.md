---
description: Задает массив указателей для нонтранспосед матриц.
ms.assetid: f2e62470-6882-49d8-ae12-6c5b79dd5c99
title: 'Метод ID3DXBaseEffect:: Сетматрикспоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0f199c3db335dfc6b9966987678c07b4b3a22402
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000306"
---
# <a name="id3dxbaseeffectsetmatrixpointerarray-method"></a>Метод ID3DXBaseEffect:: Сетматрикспоинтераррай

Задает массив указателей для нонтранспосед матриц.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMatrixPointerArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX **ppMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*ппматрикс* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](d3dxmatrix.md) \* \***

Массив указателей на матрицы нонтранспосед. См. [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число матриц в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Матрица нонтранспосед содержит основные данные строки. то есть каждый вектор содержится в строке.

Если целевые матрицы меньше исходных матриц, то дополнительные компоненты исходных матриц будут игнорироваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**жетматриксаррай**](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
