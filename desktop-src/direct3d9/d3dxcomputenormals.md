---
description: Вычисление нормалей единицы для каждой вершины в сетке. Предоставляется для поддержки устаревших приложений. Используйте D3DXComputeTangentFrameEx для улучшения результатов.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Функция D3DXComputeNormals (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d136e7c3d01b595273127c500ccc52cd310357df2147f3df5d97df9dbd38d38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069314"
---
# <a name="d3dxcomputenormals-function"></a>Функция D3DXComputeNormals

Вычисление нормалей единицы для каждой вершины в сетке. Предоставляется для поддержки устаревших приложений. Используйте [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) для улучшения результатов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пмеш* \[ в, out\]
</dt> <dd>

Тип: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Указатель на интерфейс [**ID3DXBaseMesh**](id3dxbasemesh.md) , представляющий Нормализованный объект сетки.

</dd> <dt>

*паджаценци* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждого лица в созданной прогрессивной сетке. Этот параметр является необязательным и должен иметь значение **null** , если он не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarks

Входная сетка должна иметь флаг [D3DFVF " \_ стандартный](d3dfvf.md) ", заданный в его гибком формате вершин (фвф).

Нормальная вершина создается путем усреднения нормалей всех граней, совместно использующих эту вершину.

Если задано соседство, реплицированные вершины игнорируются и «сглажены». Если значение соседа не задано, то реплицированные вершины будут иметь среднее значение среднего значения в только для лиц, явно ссылающихся на них.

Эта функция просто вызывает [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) со следующими входными параметрами:


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции сетки](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
