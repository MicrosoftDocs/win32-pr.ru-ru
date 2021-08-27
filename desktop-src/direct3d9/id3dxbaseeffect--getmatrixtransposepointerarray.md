---
description: Возвращает массив указателей на перелагаемые матрицы.
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: 'Метод ID3DXBaseEffect:: Жетматрикстранспосепоинтераррай (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 42014ed5a829f6dc0d45d7fe0dbcc96f52e945d47ae02b8effd217329e92bda8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118834"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a>Метод ID3DXBaseEffect:: Жетматрикстранспосепоинтераррай

Возвращает массив указателей на перелагаемые матрицы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
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

*ппматрикс* \[ заполняет\]
</dt> <dd>

Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***

Массив указателей на переликвидированные матрицы. См. [**D3DXMATRIX**](d3dxmatrix.md).

</dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число матриц в массиве.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

Переданная матрица содержит основные данные столбца. то есть каждый вектор содержится в столбце.

Если целевые матрицы больше, чем исходные матрицы, будут заполнены только верхние левые компоненты каждой целевой матрицы, а остальные компоненты матрицы назначения будут иметь нулевое значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**жетматрикстранспосеаррай**](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
