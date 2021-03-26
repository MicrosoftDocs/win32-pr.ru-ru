---
title: Сравнение DEF и
description: Определяет константы шейдера вершин.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104261000"
---
# <a name="def---vs"></a>Сравнение DEF и

Определяет константы шейдера вершин.

## <a name="syntax"></a>Синтаксис



| DEF, float1, float2, float3, float4 |
|-----------------------------------------|



 

где

-   DST — это регистр назначения.
-   float1, float2, float3, float4 — четыре числа с плавающей запятой.

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

Инструкция DEF определяет константу шейдера, значение которой загружается в любое время в качестве шейдера для устройства. Они называются прямыми константами. Немедленные константы имеют приоритет над константами, заданными методами API Сетвертексшадерконстантф.

Существует два способа задать константу в шейдере.

1.  Используйте DEF-и для определения константы непосредственно внутри шейдера.

    DEF-VS может определять только константы с плавающей запятой.

2.  Используйте методы API для задания константы.
    -   Используйте [**сетвертексшадерконстантф**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) для установки константы с плавающей запятой.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[дефи — VS](defi---vs.md)
</dt> <dt>

[дефб — VS](defb---vs.md)
</dt> </dl>

 

 