---
description: Указывает, как поворачивается монитор, используемый для отображения полноэкранного приложения.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: Перечисление D3DDISPLAYROTATION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8defdc206e88750125d88c50e86484428c0dedbd7c18575e26504d7445cd3f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804945"
---
# <a name="d3ddisplayrotation-enumeration"></a>Перечисление D3DDISPLAYROTATION

Указывает, как поворачивается монитор, используемый для отображения полноэкранного приложения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**\_Удостоверение D3DDISPLAYROTATION**
</dt> <dd>

Отображение не поворачивается.

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

Экран поворачивается на 90 градусов.

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

Экран поворачивается на 180 градусов.

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

Экран поворачивается на 270 градусов.

</dd> </dl>

## <a name="remarks"></a>Remarks

Это перечисление используется в [**IDirect3D9Ex:: жетадаптердисплаймодикс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex:: жетдисплаймодикс**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)и [**IDirect3DSwapChain9Ex:: жетдисплаймодикс**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).

Приложения могут самостоятельно управлять поворотом монитора с помощью [D3DPRESENTFLAG \_ ноауторотате](d3dpresentflag.md). в этом случае приложению необходимо знать, как будет поворачиваться монитор, чтобы он мог соответствующим образом скорректировать его отрисовку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




