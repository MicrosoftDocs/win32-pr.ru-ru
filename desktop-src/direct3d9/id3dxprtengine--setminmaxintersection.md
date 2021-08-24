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
ms.openlocfilehash: 2182714588e5d408c6928a677433e68dac44f09abf5ec6bd4cb4d6df7e4acf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629064"
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

## <a name="remarks"></a>Remarks

Этот метод не может использоваться в моделировании предварительно вычисленных радианценых передач (PRT), которые выполняются в GPU. См. раздел [**ID3DXPRTEngine:: компутедиректлигхтингшгпу**](id3dxprtengine--computedirectlightingshgpu.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
