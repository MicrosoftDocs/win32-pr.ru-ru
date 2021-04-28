---
description: Функция D3DXSHPRTCompSuperCluster — используется со сжатыми результатами эмулятора предварительно вычисленной радианценой пересылки (PRT).
ms.assetid: 0ec28b8c-5010-48a4-8e45-d7f9aa08185f
title: Функция D3DXSHPRTCompSuperCluster (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTCompSuperCluster
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c22c8a3a14fd8af3e9104889b421068c7ff1457
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117862"
---
# <a name="d3dxshprtcompsupercluster-function"></a>Функция D3DXSHPRTCompSuperCluster

Используется с сжатыми результатами симулятора предварительно вычисленной радианценой пересылки (PRT). Создает "подкластеры", которые представляют собой группы кластеров, которые могут быть изображены в одном вызове Draw. Для группирования кластеров используется жадный алгоритм, который уменьшает перерисовки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXSHPRTCompSuperCluster(
  _In_    UINT       *pClusterIDs,
  _In_    LPD3DXMESH pScene,
  _In_    UINT       MaxNumClusters,
  _In_    UINT       NumClusters,
  _Inout_ UINT       *pSClusterIDs,
  _Inout_ UINT       *pNumSCs
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пклустеридс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на идентификаторы кластера Нумвертс (извлеченные из сжатого буфера).

</dd> <dt>

*псцене* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**

Указатель на сетку, которая представляет составной сцену, передаваемой симулятору. См. [**ID3DXMesh**](id3dxmesh.md).

</dd> <dt>

*Макснумклустерс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальное количество кластеров, выделенных на один супер кластер.

</dd> <dt>

*Нумклустерс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество кластеров, вычисленных в симуляторе.

</dd> <dt>

*псклустеридс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Указатель на массив длины *нумклустерс*. Содержит индекс супер кластера, которому был назначен соответствующий кластер.

</dd> <dt>

*пнумскс* \[ в, out\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Количество выделенных супер кластеров.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[Предварительно вычисленные функции пересылки Радианце](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
