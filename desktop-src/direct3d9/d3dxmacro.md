---
description: Описывает определения препроцессора, используемые объектом Effect.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: Структура D3DXMACRO (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703916"
---
# <a name="d3dxmacro-structure"></a>Структура D3DXMACRO

Описывает определения препроцессора, используемые объектом Effect.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Name**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Имя препроцессора.

</dd> <dt>

**Определение**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Имя определения.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы использовать **D3DXMACRO** s в нескольких строках, перед каждым символом новой строки следует ставить обратную косую черту (как \# определено на языке C). Пример:


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



Обратите внимание на три символа обратной косой черты в конце строки. Первые два необходимы для вывода одного \\ символа "", за которым следует символ новой строки " \\ n". При необходимости можно также завершить строки, используя " \\ \\ \\ r \\ n".

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
