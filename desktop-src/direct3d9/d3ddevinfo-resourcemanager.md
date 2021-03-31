---
description: Статистика использования ресурсов.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Структура D3DDEVINFO_ResourceManager (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820980"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>\_Структура RESOURCEMANAGER D3DDEVINFO

Статистика использования ресурсов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a>Члены

<dl> <dt>

**Статистика**
</dt> <dd>

Тип: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

Массив элементов статистики ресурсов. См. [**D3DRESOURCESTATS**](d3dresourcestats.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

D3DRTYPECOUNT относится к числу перечислений в [**D3DRESOURCETYPE**](./d3dresourcetype.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
