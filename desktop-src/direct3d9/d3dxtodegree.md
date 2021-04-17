---
description: Преобразует радианы в градусы.
ms.assetid: 1b19af39-ca23-4364-9121-f532d7fed099
title: D3DXToDegree (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXToDegree
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: ad77ea661f4d67318566079aa7c1072fe0f86c91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684998"
---
# <a name="d3dxtodegree"></a>D3DXToDegree

Преобразует радианы в градусы.

``` syntax
#define D3DXToDegree(radian) ((radian) * (180.0f / D3DX_PI))
```

## <a name="parameters"></a>Параметры



| Параметр                                                           | Описание                                              |
|---------------------------------------------------------------------|----------------------------------------------------------|
| <span id="radian"></span><span id="RADIAN"></span>диапазоне<br/> | Значение в радианах для преобразования в градусы.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Макрос возвращает значение радианы в градусах.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Макросы](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXToRadian**](d3dxtoradian.md)
</dt> <dt>

[D3DX \_ Pi](other-d3dx-constants.md)
</dt> </dl>

 

 




