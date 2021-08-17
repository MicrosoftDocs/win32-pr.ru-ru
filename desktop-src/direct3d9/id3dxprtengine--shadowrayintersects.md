---
description: Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой. Обычно используется для определения того, находится ли заданная точка в теневом виде.
ms.assetid: fcd53a0f-80e8-4013-8efd-125e38f4ccd0
title: 'Метод ID3DXPRTEngine:: Шадоврайинтерсектс (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ShadowRayIntersects
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5064e788d89de6e5143ad826a4f61a4afd802931c6964193c8fa46626edf955d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729598"
---
# <a name="id3dxprtengineshadowrayintersects-method"></a>Метод ID3DXPRTEngine:: Шадоврайинтерсектс

Использует эффективную трассировку лучей в предварительно вычисленном моделировании радианце (PRT), чтобы определить, пересекаются ли луч с сеткой. Обычно используется для определения того, находится ли заданная точка в теневом виде.

## <a name="syntax"></a>Синтаксис


```C++
BOOL ShadowRayIntersects(
  [in] const D3DXVECTOR3 *pRayPos,
  [in] const D3DXVECTOR3 *pRayDir
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*прайпос* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , указывающий точку, с которой начинается луч.

</dd> <dt>

*прайдир* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , в которой указывается нормализованное направление луча.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

Возвращает **значение true** , если луч пересекает текущую сетку; в противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

Используйте [**ID3DXPRTEngine:: сетминмаксинтерсектион**](id3dxprtengine--setminmaxintersection.md) , чтобы задать минимальное и максимальное расстояние пересечения с лучом.

Этот метод выполняется быстрее, чем [**ID3DXPRTEngine:: клосестрайинтерсектс**](id3dxprtengine--closestrayintersects.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Клосестрайинтерсектс**](id3dxprtengine--closestrayintersects.md)
</dt> <dt>

[**ID3DXPRTEngine:: Сетминмаксинтерсектион**](id3dxprtengine--setminmaxintersection.md)
</dt> </dl>

 

 
