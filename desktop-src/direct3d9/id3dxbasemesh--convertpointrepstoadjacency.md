---
description: Преобразует данные репрезентативного указания в сведения о смежности сетки.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'Метод ID3DXBaseMesh:: Конвертпоинтрепстоаджаценци (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b888bc7fe8be0aa8bbac1150717ff90440bb797d84d910f7bcb6ee4f35f49345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296212"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a>Метод ID3DXBaseMesh:: Конвертпоинтрепстоаджаценци

Преобразует данные репрезентативного указания в сведения о смежности сетки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппреп* \[ окне\]
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

Указатель на массив из одного DWORD на вершину сетки, которая содержит данные репрезентативного указания. Это необязательный параметр. Если указать значение **null** , этот параметр будет интерпретирован как массив "Identity".

</dd> <dt>

*паджаценци* \[ в, out\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***

Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сети. Число байтов в этом массиве должно быть не менее 3 \* [**ID3DXBaseMesh:: жетнумфацес**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
