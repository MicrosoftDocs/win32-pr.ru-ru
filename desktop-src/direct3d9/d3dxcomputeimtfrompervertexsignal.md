---
description: Вычисление ИМТ для каждого треугольника из данных на вершину. Эта функция позволяет вычислить ИМТ на основе любого значения в сетке (цвет, обычная и т. д.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Функция D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713745"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>Функция D3DXComputeIMTFromPerVertexSignal

Вычисление ИМТ для каждого треугольника из данных на вершину. Эта функция позволяет вычислить ИМТ на основе любого значения в сетке (цвет, обычная и т. д.).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на входную сетку (см. [**ID3DXMesh**](id3dxmesh.md)), которая содержит объект Geometry для вычисления ИМТ.

</dd> <dt>

*пфвертекссигнал* \[ окне\]
</dt> <dd>

Тип: **const [**float**](../winprog/windows-data-types.md) \***

Указатель на массив данных на вершину, из которого будут вычисляться ИМТ. Размер массива — Усигналстриде \* v, где v — это количество вершин в сетке.

</dd> <dt>

*усигналдименсион* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество плавающих элементов на вершину.

</dd> <dt>

*усигналстриде* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число байтов на вершину в массиве. Это должен быть кратный sizeof (float)

</dd> <dt>

*двоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Параметры переноса текстур. Это сочетание одного или нескольких [**флагов D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*пстатускаллбакк* 
</dt> <dd>

Тип: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Указатель на функцию обратного вызова, чтобы отслеживать ход выполнения вычисления ИМТ.

</dd> <dt>

*пусерконтекст* 
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

Указатель на определяемую пользователем переменную, которая передается функции обратного вызова состояния. Обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.

</dd> <dt>

*ппимтдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Указатель на буфер (см. [**ID3DXBuffer**](id3dxbuffer.md)), содержащий возвращенный массив ИМТ. Этот массив может быть предоставлен в качестве входных данных для [функций D3DX уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md) , чтобы определить приоритет распределения пространства текстуры в параметризации текстуры.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. в противном случае — значение D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции Уватлас](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Использование Уватлас (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
