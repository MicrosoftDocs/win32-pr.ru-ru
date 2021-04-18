---
description: Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'Метод ID3DXMATRIXStack:: сдвиг (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 228b4302a512e96d5c009edcb3f0b673ee61e047
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105704029"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a>Метод ID3DXMATRIXStack:: сдвиг (D3dx9math. h)

Определяет продукт текущей матрицы и вычисленную матрицу смещения, определяемую заданными факторами (x, y и z).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*x* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент перевода по оси x.

</dd> <dt>

*y* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент преобразования в направлении y.

</dd> <dt>

*z* \[ в\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент перевода в направлении z.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК.

## <a name="remarks"></a>Комментарии

Этот метод дает право на Умножение текущей матрицы на вычисленную матрицу перевода (преобразование относится к текущему источнику мира).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: Транслателокал**](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
