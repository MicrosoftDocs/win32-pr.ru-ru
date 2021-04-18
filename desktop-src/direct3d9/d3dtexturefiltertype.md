---
description: Определяет режимы фильтрации текстур для этапа текстуры.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Перечисление D3DTEXTUREFILTERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713537"
---
# <a name="d3dtexturefiltertype-enumeration"></a>Перечисление D3DTEXTUREFILTERTYPE

Определяет режимы фильтрации текстур для этапа текстуры.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ None**
</dt> <dd>

При использовании с [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md)отключает функции текстурирования.

</dd> <dt>

<span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**\_Точка D3DTEXF**
</dt> <dd>

При использовании с [**D3DSAMP \_ Магфилтер**](./d3dsamplerstatetype.md) или [**D3DSAMP \_ минфилтер**](./d3dsamplerstatetype.md)указывает, что фильтрация точек должна использоваться как значение увеличения текстуры или фильтр минификации соответственно. При использовании с **D3DSAMP \_ мипфилтер** включает функции текстурирования и указывает, что средство программной прорисовки выбирает цвет из шаг текселя ближайшего уровня MIP.

</dd> <dt>

<span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**\_Линейная D3DTEXF**
</dt> <dd>

При использовании с [**D3DSAMP \_ Магфилтер**](./d3dsamplerstatetype.md) или [**D3DSAMP \_ минфилтер**](./d3dsamplerstatetype.md)указывает, что Линейная фильтрация используется в качестве коэффициента увеличения текстуры или фильтра минификации соответственно. При использовании с **D3DSAMP \_ мипфилтер** включает фильтрацию функции текстурирования и трилинейной; она указывает, что средство программной прорисовки выполняет интерполяцию между двумя ближайшими уровнями MIP.

</dd> <dt>

<span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ анизотропный**
</dt> <dd>

При использовании с [**D3DSAMP \_ Магфилтер**](./d3dsamplerstatetype.md) или [**D3DSAMP \_ минфилтер**](./d3dsamplerstatetype.md)указывает, что анизотропная фильтрация текстур используется в качестве фильтра увеличения текстуры или фильтр минификации соответственно. Компенсирует искажения, вызванные различием угла между многоугольником текстуры и плоскостью экрана. Использование WITH **D3DSAMP \_ мипфилтер** не определено.

</dd> <dt>

<span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ пирамидалкуад**
</dt> <dd>

4-примерный фильтр, используемый в качестве фильтра увеличения текстуры или минификации. Использование WITH [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md) не определено.

</dd> <dt>

<span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ гауссианкуад**
</dt> <dd>

4-примерный фильтр по Гауссу, используемый в качестве фильтра увеличения текстуры или минификации. Использование WITH [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md) не определено.

</dd> <dt>

<span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ конволутионмоно**
</dt> <dd>

Фильтр свертки для монохромных текстур. См. [D3DFMT \_ a1](d3dformat.md).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Различия между Direct3D 9 и Direct3D 9Ex:<br/> Этот флаг доступен только в Direct3D 9Ex.<br/> |



 

Использование WITH [**D3DSAMP \_ мипфилтер**](./d3dsamplerstatetype.md) не определено.

</dd> <dt>

<span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

D3DTEXTUREFILTERTYPE используется [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) вместе с [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) для определения режимов фильтрации текстур для этапа текстуры.

Чтобы проверить, поддерживает ли формат типы фильтров текстур, отличные от D3DTEXF \_ Point (которая всегда поддерживается), вызовите [**IDirect3D9:: чеккдевицеформат**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) с \_ \_ фильтром запросов D3DUSAGE.

Задайте фильтр увеличения масштаба для этапа текстуры, вызвав [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) со значением D3DSAMP \_ магфилтер в качестве второго параметра и одним элементом этого перечисления в качестве третьего.

Задайте фильтр минификации для этапа текстуры, вызвав [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) со значением D3DSAMP \_ минфилтер в качестве второго параметра и одним членом этого перечисления в качестве третьего параметра.

Задайте фильтр текстуры для использования уровней между-mipmap, вызвав [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) со значением D3DSAMP \_ мипфилтер в качестве второго параметра и одним членом этого перечисления в качестве третьего параметра.

Не все допустимые режимы фильтрации для устройства будут применяться к картам томов. В общем случае \_ \_ для карт томов будут поддерживаться линейные фильтры увеличения D3DTEXF Point и D3DTEXF. Если \_ задано значение D3DPTEXTURECAPS мипволумемап, то \_ \_ \_ для карт томов будут поддерживаться фильтры D3DTEXF Point mipmap и D3DTEXF Point и D3DTEXF линейные минификации. Устройство может иметь или не поддерживать \_ Фильтр линейного mipmap D3DTEXF для карт томов. Устройства, поддерживающие анизотропную фильтрацию для двумерных карт, не обязательно поддерживают анизотропную фильтрацию для карт томов. Однако приложения, которые включают анизотропную фильтрацию, получат наилучшую доступную фильтрацию (возможно, линейную), если анизотропная фильтрация не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**ID3DXPatchMesh:: Жетдисплацепарам**](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[**ID3DXPatchMesh:: Сетдисплацепарам**](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> <dt>

[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
