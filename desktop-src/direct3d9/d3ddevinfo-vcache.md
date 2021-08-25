---
description: Указания по оптимизации кэша вершин.
ms.assetid: 891624cd-03dd-4ddd-93f5-4899e1470325
title: Структура D3DDEVINFO_VCACHE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_VCACHE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e065c981cc42db6adbad8cfa7a14e415712aae74942e9f3aab3ecb0b353f5ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894504"
---
# <a name="d3ddevinfo_vcache-structure"></a>\_Структура ВКАЧЕ D3DDEVINFO

Указания по оптимизации кэша вершин.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_VCACHE {
  DWORD Pattern;
  DWORD OptMethod;
  DWORD CacheSize;
  DWORD MagicNumber;
} D3DDEVINFO_VCACHE, *LPD3DDEVINFO_VCACHE;
```



## <a name="members"></a>Члены

<dl> <dt>

**Шаблон**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Битовый шаблон. Возвращаемое значение должно быть FOURCC ("C", "A", "C", "H").

</dd> <dt>

**оптмесод**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Метод оптимизации. Чтобы получить самые длинные полосы, используйте значение 0. Чтобы оптимизировать использование кэша вершин, используйте значение 1.

</dd> <dt>

**CacheSize**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Размер кэша, используемый в качестве целевого объекта для оптимизации. Это необходимо, только если Оптмесод имеет значение 1.

</dd> <dt>

**MagicNumber**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Используется внутренними методами оптимизации для определения времени перезапуска полос. Он не может быть установлен или изменен пользователем. Это необходимо, только если Оптмесод имеет значение 1.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
