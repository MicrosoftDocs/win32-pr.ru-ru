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
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354150"
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

**Name**
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры эффектов](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[**жетпассдеск**](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
