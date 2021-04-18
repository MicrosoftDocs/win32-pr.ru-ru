---
description: Описывает функцию, используемую в результате действия.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: Структура D3DXFUNCTION_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694152"
---
# <a name="d3dxfunction_desc-structure"></a>\_Структура D3DXFUNCTION DESC

Описывает функцию, используемую в результате действия.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Name**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Имя функции.

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Не используется. Этому элементу всегда будет присвоено значение 0, [**жетфунктиондеск**](id3dxbaseeffect--getfunctiondesc.md).

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
