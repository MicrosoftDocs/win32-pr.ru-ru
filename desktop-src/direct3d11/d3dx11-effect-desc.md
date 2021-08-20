---
title: Структура D3DX11_EFFECT_DESC (D3dx11effect. h)
description: Описывает результат.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f2c3a205a4849aed755bee01302da813cccf77bbf8255036f287d488b76591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989994"
---
# <a name="d3dx11_effect_desc-structure"></a>\_Структура D3DX11 влияния на \_ структуру

Описывает результат.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**константбуфферс**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число буферов констант в этом результате.

</dd> <dt>

**глобалвариаблес**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число глобальных переменных в этом результате.

</dd> <dt>

**интерфацевариаблес**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число глобальных интерфейсов в этом результате.

</dd> <dt>

**Технологий**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Количество методов в этом результате.

</dd> <dt>

**Группы**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число групп в этом результате.

</dd> </dl>

## <a name="remarks"></a>Remarks

D3DX11 \_ Effect \_ DESC используется с [**ID3DX11Effect:: DESC**](id3dx11effect-getdesc.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

