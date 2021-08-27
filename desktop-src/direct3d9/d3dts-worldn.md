---
description: Определяет последующие матрицы преобразования, которые можно использовать для смешения вершин с помощью соответствующей матрицы и значения веса смешения (бета-версии), указанного в формате вершины.
ms.assetid: cab444c2-b245-4d1a-a90c-745c92a2ea89
title: D3DTS_WORLDn (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLDn
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 7026308192f43b7290dedcb9572772c9eda45acdc87d018480bd59202a2dc2df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119404"
---
# <a name="d3dts_worldn"></a>D3DTS \_ ворлдн

Определяет последующие матрицы преобразования, которые можно использовать для смешения вершин с помощью соответствующей матрицы и значения веса смешения (бета-версии), указанного в формате вершины.

``` syntax
#define D3DTS_WORLDn 
#define D3DTS_WORLD1 D3DTS_WORLDMATRIX(1)
#define D3DTS_WORLD2 D3DTS_WORLDMATRIX(2)
#define D3DTS_WORLD3 D3DTS_WORLDMATRIX(3)
```

## <a name="remarks"></a>Remarks

Эти макросы предназначены для упрощения переноса существующих приложений на Direct3D 9.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Макросы](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**сеттрансформ**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ ворлдматрикс**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
