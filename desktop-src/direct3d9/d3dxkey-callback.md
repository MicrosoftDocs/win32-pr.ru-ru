---
description: Описывает ключ обратного вызова для использования в анимации по ключевым кадрам.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: Структура D3DXKEY_CALLBACK (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f488445bbb018b62445ff802abcf5a82c22b4e31c9d71618e61437efd5e36a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123072"
---
# <a name="d3dxkey_callback-structure"></a>\_Структура обратного вызова D3DXKEY

Описывает ключ обратного вызова для использования в анимации по ключевым кадрам.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a>Члены

<dl> <dt>

**Время**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Метка времени ключевого кадра.

</dd> <dt>

**пкаллбаккдата**
</dt> <dd>

Тип: **[ **лпвоид**](../winprog/windows-data-types.md)**

</dd> <dd>

Указатель на данные обратного вызова пользователя.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
