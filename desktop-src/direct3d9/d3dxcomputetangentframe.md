---
description: Вычисление векторов тангенса, бинормал и нормали для сетки.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Функция D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713925"
---
# <a name="d3dxcomputetangentframe-function"></a>Функция D3DXComputeTangentFrame

Вычисление векторов тангенса, бинормал и нормали для сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DXMesh**](id3dxmesh.md)\***

Указатель на входной объект сетки [**ID3DXMesh**](id3dxmesh.md) .

</dd> <dt>

*двоптионс* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Сочетание одного или нескольких флагов [**D3DXTANGENT**](./d3dxtangent.md) .

Используйте **значение NULL** , чтобы указать следующие параметры:

-   Установите вес обычной векторной длины на угол в радианах, который выдается двумя краями, оставляемыми вершиной.
-   Вычисление ортогональной декартовой координаты из координат текстуры UV.
-   Текстуры не упаковываются в направлениях U или V
-   Частичные производные от относительно координат текстуры нормализованы.
-   Вершины упорядочиваются в направлении против часовой стрелки вокруг каждого треугольника.
-   Используйте одновершинные векторы, уже имеющиеся во входной сетке.
-   Результаты будут храниться в исходной входной сетке. Функция завершится ошибкой, если необходимо создать новые вершины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Эта функция просто вызывает [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) со следующими входными параметрами:


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



Единственные числа обрабатываются по мере необходимости путем группирования краев и разделения вершин. Если необходимо разделить какие бы то ни было вершины, функция завершится ошибкой. Вычисленный Стандартный вектор в каждой вершине всегда нормализуется с длиной единицы.

Наиболее надежное решение для вычисления ортогональных декартных координат — не устанавливать флаги D3DXTANGENT \_ орсогонализе \_ от \_ вас и D3DXTANGENT \_ орсогонализе \_ из \_ V, чтобы ортогональные координаты ВЫчисляться из обеих координат UV-текстуры. Однако в этом случае, если значение U или V равно нулю, функция будет рассчитывать ортогональные координаты с помощью D3DXTANGENT \_ орсогонализе \_ из \_ V или D3DXTANGENT \_ орсогонализе \_ от \_ U соответственно.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> <dt>

[**D3DXTANGENT**](./d3dxtangent.md)
</dt> </dl>

 

 
