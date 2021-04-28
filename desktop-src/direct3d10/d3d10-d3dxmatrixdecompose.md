---
description: Функция D3DXMatrixDecompose (D3DX10Math. h) — разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Функция D3DXMatrixDecompose (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc87de99d72283c20f25b15ea8d0e5864e2550d9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113212"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>Функция D3DXMatrixDecompose (D3DX10Math. h)

Разделяет общую матрицу трехмерного преобразования на скалярные, ротации и преобразованные компоненты.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паутскале* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на выходную [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , содержащую коэффициенты масштабирования, применяемые вдоль осей x, y и z.

</dd> <dt>

*паутротатион* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Указатель на [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , описывающий поворот.

</dd> <dt>

*пауттранслатион* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Указатель на вектор D3DXVECTOR3, описывающий преобразование.

</dd> <dt>

*PM* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Указатель на входную матрицу [**D3DXMATRIX**](d3d10-d3dxmatrix.md) для разложения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть следующим: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
