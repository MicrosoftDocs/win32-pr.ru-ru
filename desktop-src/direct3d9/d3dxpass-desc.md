---
description: Описывает проход для объекта Effect.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: Структура D3DXPASS_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 9666f0385c592adbc4378cbc693a5ce7a628092bbbb1695fd39527817c7ca04e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894054"
---
# <a name="d3dxpass_desc-structure"></a>\_Структура D3DXPASS DESC

Описывает проход для объекта Effect.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Имя**
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

Строковое значение, используемое для прохода.

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Заметки представляют собой определяемые пользователем данные, которые могут быть присоединены к любому методу, параметру Pass или. См. раздел [Добавление сведений, чтобы параметры вступили в действие с \_ заметками](using-an-effect.md).

</dd> <dt>

**пвертексшадерфунктион**
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Указатель на функцию шейдера вершин. Если результат создается с D3DXFX, [который \_ не может быть \_ клонирован](d3dxfx.md), эта структура возвращает **пустой** указатель при вызове методом [**жетпассдеск**](id3dxbaseeffect--getpassdesc.md).

</dd> <dt>

**ппикселшадерфунктион**
</dt> <dd>

Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***

</dd> <dd>

Указатель на функцию шейдера пикселей. Если результат создается с D3DXFX, [который \_ не может быть \_ клонирован](d3dxfx.md), эта структура возвращает **пустой** указатель при вызове методом [**жетпассдеск**](id3dxbaseeffect--getpassdesc.md).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**жетпассдеск**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
