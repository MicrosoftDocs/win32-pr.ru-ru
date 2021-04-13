---
description: Тип данных для управления набором параметров эффектов по умолчанию.
ms.assetid: a3408c0b-b4a6-47b1-b12e-594c13bd3a7d
title: Структура D3DXEFFECTINSTANCE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTINSTANCE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6874da0fd04b34036152d58e94b16006e185e117
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354883"
---
# <a name="d3dxeffectinstance-structure"></a>Структура D3DXEFFECTINSTANCE

Тип данных для управления набором параметров эффектов по умолчанию.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXEFFECTINSTANCE {
  LPSTR               pEffectFilename;
  DWORD               NumDefaults;
  LPD3DXEFFECTDEFAULT pDefaults;
} D3DXEFFECTINSTANCE, *LPD3DXEFFECTINSTANCE;
```



## <a name="members"></a>Члены

<dl> <dt>

**пеффектфиленаме**
</dt> <dd>

Тип: **LPSTR**

</dd> <dd>

Имя файла действия.

</dd> <dt>

**нумдефаултс**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество параметров по умолчанию.

</dd> <dt>

**пдефаултс**
</dt> <dd>

Тип: **[ **LPD3DXEFFECTDEFAULT**](d3dxeffectdefault.md)**

</dd> <dd>

Указатель на массив элементов [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md) , каждый из которых содержит параметр Effect.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
