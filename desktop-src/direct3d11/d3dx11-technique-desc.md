---
title: Структура D3DX11_TECHNIQUE_DESC (D3dx11effect. h)
description: Описывает методику воздействия.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821261"
---
# <a name="d3dx11_technique_desc-structure"></a>\_ \_ Структура DESC D3DX11 техника

Описывает методику воздействия.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a>Участники

<dl> <dt>

**имя**;
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Имя этого метода (NULL, если он не является анонимным).

</dd> <dt>

**Соответствующий**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число проходов, содержащихся в методе.

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число заметок на этом приеме.

</dd> </dl>

## <a name="remarks"></a>Примечания

D3DX11 \_ техника \_ DESC используется с [**ID3DX11EffectTechnique:: DESC**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

