---
title: Различия шейдеров вершин
description: Различия шейдеров вершин
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 411a3a742fca508839651d56912fa00b2a6d8b82908b159694a3b1eff88f2318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982824"
---
# <a name="vertex-shader-differences"></a>Различия шейдеров вершин

## <a name="instruction-slots"></a>Слоты инструкций

Каждая версия поддерживает разное число максимальных слотов инструкций.



| Версия  | Максимальное число слотов инструкций                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| VS \_ 1 \_ 1 | 128                                                                                                                               |
| VS \_ 2 \_ 0 | 256                                                                                                                               |
| VS \_ 2 \_ x | 256                                                                                                                               |
| VS \_ 3 \_ 0 | 512 минимум и до количества слотов в D3DCAPS9. MaxVertexShader30InstructionSlots. См. [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9). |



 

Сведения об ограничениях шейдеров программного обеспечения см. в разделе [программные шейдеры](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Flow Управление ограничениями вложенности

-   см. раздел [ограничения вложенности элемента управления Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).

## <a name="vs_1_1-features"></a>\_функции VS 1 \_ 1

Новые инструкции:

См. [инструкции — VS \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).

Новые регистры:

См. раздел [регистры-VS \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).

## <a name="vs_2_0-features"></a>\_функции vs 2 \_ 0

Новые функции

-   Статическое управление потоком
-   Доступны все четыре компонента [регистра адресов](dx9-graphics-reference-asm-vs-registers-address.md) (a0).

Новые инструкции:

-   Инструкции по установке — [дефб-VS](defb---vs.md), [дефи-VS](defi---vs.md)
-   Арифметические инструкции — [ABS-VS](abs---vs.md), [CR-VS](crs---vs.md), [ЛРП-VS](lrp---vs.md), [МОВА-VS](mova---vs.md), [НРМ-VS](nrm---vs.md), [Pow-VS](pow---vs.md), [СГН-VS](sgn---vs.md), [синкос-VS](sincos---vs.md)
-   Статические инструкции по управлению потоком — [вызов-VS](call---vs.md), [каллнз bool-VS](callnz-bool---vs.md), [else-VS](else---vs.md), [endif-VS](endif---vs.md), [ендлуп-VS](endloop---vs.md), [ендреп-VS](endrep---vs.md), [Если bool-VS](if-bool---vs.md), [Label-VS](label---vs.md), [цикл-VS](loop---vs.md), [представитель-VS](rep---vs.md), [RET-VS](ret---vs.md)

Новые регистры:

-   [Константный логический регистр](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )
-   [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )
-   [Регистр счетчика циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al)

## <a name="vs_2_x-features"></a>\_функции vs 2 \_ x

Новые возможности (D3DCAPS9. VS20Caps):

-   Динамическое управление потоком
-   Инструкции по вложению для динамических и статических функций управления потоком
-   Число увеличенных [временных регистров](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# )
-   Предикация

Новые инструкции:

-   Инструкции по динамическому управлению потоком — [break-VS](break---vs.md), [break \_ -VS](break-comp---vs.md), [бреакп-VS](breakp---vs.md), [каллнз "пред-](callnz-pred---vs.md)VS", if-VS,, [Если "пред](if-pred---vs.md)-VS", " [сетп \_ comp-](setp-comp---vs.md) VS" [ \_ ](if-comp---vs.md)

Новые регистры:

-   [Регистр предиката](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)

## <a name="vs_3_0-features"></a>\_функции VS 3 \_ 0

Новые возможности:

-   Поиск текстур
-   Индексируемые [выходные регистры](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )
-   Количество [временных регистров](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ), увеличенное до 32

Новые инструкции:

-   Инструкция Setup- [дкл \_ самплертипе (SM3-VS ASM)](dcl-samplertype---vs.md)
-   Текстурная инструкция — [текслдл-VS](texldl---vs.md)

Новые регистры:

-   [Образцы (Direct3D 9 ASM-VS)](dx9-graphics-reference-asm-vs-registers-sampler.md) \#

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Шейдеры вершин](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 