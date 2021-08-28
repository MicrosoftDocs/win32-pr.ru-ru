---
description: Флаги, используемые для получения сведений о обратном вызове.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Перечисление D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 0a050263934684f766bb9b7d58b83665a31a5edbd099a43ad1947eba74ca25bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676384"
---
# <a name="d3dxcallback_search_flags-enumeration"></a>\_ \_ Перечисление флагов поиска D3DXCALLBACK

Флаги, используемые для получения сведений о обратном вызове.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**Поиск D3DXCALLBACK, \_ \_ исключая \_ начальную \_ точку**
</dt> <dd>

Исключить обратные вызовы, расположенные в начальной позиции из поиска.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**\_Поиск D3DXCALLBACK \_ за \_ начальной \_ позицией**
</dt> <dd>

Измените направление поиска обратного вызова.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ Поиск \_ принудительный \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




