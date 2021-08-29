---
description: Проецирует функцию, представленную в сопоставлении кубов, в сферические гармонические колебания.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: Функция D3DX10SHProjectCubeMap (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fa30724bed56e86d16626133ab32e3494d3c71d6ffa839be1520518c97a77fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990464"
---
# <a name="d3dx10shprojectcubemap-function"></a>Функция D3DX10SHProjectCubeMap

Проецирует функцию, представленную в сопоставлении кубов, в сферические гармонические колебания.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Заказ* 
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Порядок оценки SH, создание заказа ^ 2 коефс, degree — Order-1.

</dd> <dt>

*пкубемап* 
</dt> <dd>

Тип: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Кубической карты, который планируется прогнозировать на сферические гармонические колебания. См. [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).

</dd> <dt>

*праут* 
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Выходной вектор SH для Red.

</dd> <dt>

*пгаут* 
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Выходной вектор SH для зеленого цвета.

</dd> <dt>

*пбаут* 
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)\***

Выходной вектор SH для синего.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10Tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[Математические функции](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
