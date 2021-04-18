---
title: Структура D3DX11_EFFECT_VARIABLE_DESC (D3dx11effect. h)
description: Описывает переменную Effect.
ms.assetid: 9c975ad4-b90e-4e69-b78f-4f5cc61083ff
keywords:
- D3DX11_EFFECT_VARIABLE_DESC структура Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_VARIABLE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a83121c930c5a634434161c998c72215e227f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998693"
---
# <a name="d3dx11_effect_variable_desc-structure"></a>\_ \_ Структура desc переменной влияния D3DX11 \_

Описывает переменную Effect.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DX11_EFFECT_VARIABLE_DESC {
  LPCSTR Name;
  LPCSTR Semantic;
  UINT   Flags;
  UINT   Annotations;
  UINT   BufferOffset;
  UINT   ExplicitBindPoint;
} D3DX11_EFFECT_VARIABLE_DESC;
```



## <a name="members"></a>Участники

<dl> <dt>

**имя**;
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Имя этой переменной, заметки или члена структуры.

</dd> <dt>

**Семантическ**
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Семантическая строка этой переменной или члена структуры (значение NULL для заметок или если отсутствует).

</dd> <dt>

**Флаги**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Необязательные флаги для переменных эффектов.

</dd> <dt>

**Заметки**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Число заметок для этой переменной (для заметок значение всегда равно 0).

</dd> <dt>

**буффероффсет**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Смещение, содержащее кбуффер или тбуффер (всегда 0 для заметок или переменных, не содержащихся в буферах констант).

</dd> <dt>

**експлиЦитбиндпоинт**
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Используется, если переменная была явно привязана с помощью ключевого слова Register. Проверьте флаги для \_ переменной влияния D3DX11 \_ \_ явной \_ \_ точки привязки.

</dd> </dl>

## <a name="remarks"></a>Примечания

\_ПЕРЕМЕННАЯ D3DX11 \_ Effect \_ DESC используется с [**ID3DX11EffectVariable:: DESC**](id3dx11effectvariable-getdesc.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Эффекты с 11 по структурам](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

