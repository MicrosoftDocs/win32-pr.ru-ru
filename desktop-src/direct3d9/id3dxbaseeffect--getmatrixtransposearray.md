---
description: Возвращает массив переданных матриц.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'Метод ID3DXBaseEffect:: Жетматрикстранспосеаррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821500"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a>Метод ID3DXBaseEffect:: Жетматрикстранспосеаррай

Возвращает массив переданных матриц.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпараметер* \[ окне\]
</dt> <dd>

Тип: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Уникальный идентификатор. См. раздел [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*пматрикс* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Возвращает массив переданных матриц. См. [**D3DXMATRIX**](d3dxmatrix.md).

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

Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.

Если целевые матрицы больше, чем исходные матрицы, будут заполнены только верхние левые компоненты каждой целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**сетматрикстранспосеаррай**](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
