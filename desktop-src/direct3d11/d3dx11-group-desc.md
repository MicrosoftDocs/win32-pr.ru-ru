---
title: Структура D3DX11_GROUP_DESC (D3dx11effect. h)
description: Описывает группу эффектов.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a189417b997647fd9c48a55010e96b32053c64031a03a8ac845e48c9a8e870a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096314"
---
# <a name="d3dx11_group_desc-structure"></a>\_ \_ Структура DESC группы D3DX11

Описывает группу эффектов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Имя**
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Имя этой группы (только **значение NULL** , если глобальная).

</dd> <dt>

**Технологий**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Количество методов, содержащихся в группе.

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число заметок в этой группе.

</dd> </dl>

## <a name="remarks"></a>Remarks

D3DX11 \_ Group \_ DESC используется с [**ID3DX11EffectTechnique:: DESC**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

