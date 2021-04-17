---
description: Статистика ресурсов, собираемая \_ RESOURCEMANAGER D3DDEVINFO при использовании механизма асинхронных запросов.
ms.assetid: f4d9c6db-4002-439c-9a88-485763badc82
title: Структура D3DRESOURCESTATS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRESOURCESTATS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f6f549011b9750f69187c0e0cbf34ec94764c9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713538"
---
# <a name="d3dresourcestats-structure"></a>Структура D3DRESOURCESTATS

Статистика ресурсов, собираемая [**\_ ResourceManager D3DDEVINFO**](d3ddevinfo-resourcemanager.md) при использовании механизма асинхронных запросов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DRESOURCESTATS {
  BOOL  bThrashing;
  DWORD ApproxBytesDownloaded;
  DWORD NumEvicts;
  DWORD NumVidCreates;
  DWORD LastPri;
  DWORD NumUsed;
  DWORD NumUsedInVidMem;
  DWORD WorkingSet;
  DWORD WorkingSetBytes;
  DWORD TotalManaged;
  DWORD TotalBytes;
} D3DRESOURCESTATS, *LPD3DRESOURCESTATS;
```



## <a name="members"></a>Члены

<dl> <dt>

**бсрашинг**
</dt> <dd>

Тип: **[ **bool** .](../winprog/windows-data-types.md)**

</dd> <dd>

Указывает, происходит ли пробуксовка.

</dd> <dt>

**аппроксбитесдовнлоадед**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Приблизительное число байтов, скачанных диспетчером ресурсов.

</dd> <dt>

**нумевиктс**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число исключенных объектов.

</dd> <dt>

**нумвидкреатес**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество объектов, созданных в видеопамяти.

</dd> <dt>

**ластпри**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Приоритет последнего исключенного объекта.

</dd> <dt>

**нумусед**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число объектов, заданное для устройства.

</dd> <dt>

**нумусединвидмем**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число объектов, заданных на устройстве, которые уже находятся в видеопамяти.

</dd> <dt>

**WorkingSet**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Количество объектов в видеопамяти.

</dd> <dt>

**воркингсетбитес**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Число байтов в видеопамяти.

</dd> <dt>

**тоталманажед**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Общее число управляемых объектов.

</dd> <dt>

**TotalBytes**
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Общее число байтов управляемых объектов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[Асинхронное уведомление (Direct3D 9)](asynchronous-notification.md)
</dt> </dl>

 

 
