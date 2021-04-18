---
description: Определяет поддерживаемые операции смешения. Определения терминов см. в разделе Примечания.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Перечисление D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713576"
---
# <a name="d3dblendop-enumeration"></a>Перечисление D3DBLENDOP

Определяет поддерживаемые операции смешения. Определения терминов см. в разделе Примечания.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Добавить**
</dt> <dd>

Результатом является назначение, добавленное в источник. Result = источник + назначение

</dd> <dt>

<span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**\_Вычитание D3DBLENDOP**
</dt> <dd>

Результат — это назначение, вычитаемое из в источник. Result = источник-назначение

</dd> <dt>

<span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ ревсубтракт**
</dt> <dd>

Результат — источник, вычитаемый из назначения. Result = целевой источник

</dd> <dt>

<span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ мин**
</dt> <dd>

Результат — минимум источника и назначения. Результат = MIN (источник, назначение)

</dd> <dt>

<span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**
</dt> <dd>

Результат — максимум источника и назначения. Result = MAX (источник, назначение)

</dd> <dt>

<span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Источник, назначение и результат определяются следующим образом:



| Термин        | Тип   | Описание                                                            |
|-------------|--------|------------------------------------------------------------------------|
| Источник      | Входные данные  | Цвет исходного пикселя перед операцией.                        |
| Назначение | Входные данные  | Цвет пикселя в целевом буфере перед операцией.     |
| Результат      | Выходные данные | Возвращаемое значение, которое является смешением цвета, полученным в результате операции. |



 

Этот перечислимый тип определяет значения, используемые следующими состояниями визуализации:

-   D3DRS \_ блендоп
-   D3DRS \_ блендопалфа

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
