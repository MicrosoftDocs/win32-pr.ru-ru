---
description: Определяет константы, описывающие тип заднего буфера.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: Перечисление D3DBACKBUFFER_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000329"
---
# <a name="d3dbackbuffer_type-enumeration"></a>\_Перечисление типов D3DBACKBUFFER

Определяет константы, описывающие тип заднего буфера.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**\_Тип D3DBACKBUFFER \_ Mono**
</dt> <dd>

Указывает нестерео цепочку подкачки.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**\_Тип D3DBACKBUFFER \_ Left**
</dt> <dd>

Задает левую сторону пары стерео в цепочке буферов.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**\_Тип D3DBACKBUFFER \_ right**
</dt> <dd>

Указывает правую сторону пары стерео в цепочке буферов.

</dd> <dt>

<span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER \_ тип \_ \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Direct3D 9 не поддерживает стерео представление, поэтому Direct3D не использует D3DBACKBUFFER \_ типа \_ Left и D3DBACKBUFFER \_ Type \_ right для этого перечислимого типа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: Жетбаккбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[**IDirect3DSwapChain9:: Жетбаккбуффер**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
