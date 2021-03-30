---
description: Устанавливает минимальное и максимальное расстояние пересечения между трехмерными объектами.
ms.assetid: da825c70-0c55-4303-b78a-a761ba037182
title: 'Метод ID3DXPRTEngine:: Сетминмаксинтерсектион (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMinMaxIntersection
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 68845f713289c524afc844037ca305909e5b89b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355150"
---
# <a name="id3dxprtenginesetminmaxintersection-method"></a>Метод ID3DXPRTEngine:: Сетминмаксинтерсектион

Устанавливает минимальное и максимальное расстояние пересечения между трехмерными объектами. Эти значения расстояния можно использовать для управления минимальным или максимальным расстоянием, в течение которых объекты могут быть темными или отражать освещение. Например, метод можно использовать для ограничения затенения ближайших функций трехмерной модели.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetMinMaxIntersection(
  [in] FLOAT fMin ,
  [in] FLOAT fMax
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фмин* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Минимальное расстояние пересечения. Должно быть положительным и меньшим, чем fMax.

</dd> <dt>

*fMax* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Максимальное расстояние пересечения. Если 0,0 f, будет использоваться предыдущее значение; в противном случае должен быть больше Фмин.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение D3D \_ ОК. В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Этот метод не может использоваться в моделировании предварительно вычисленных радианценых передач (PRT), которые выполняются в GPU. См. раздел [**ID3DXPRTEngine:: компутедиректлигхтингшгпу**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
