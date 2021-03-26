---
title: Различия шейдера пикселей
description: Различия шейдера пикселей
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413149"
---
# <a name="pixel-shader-differences"></a>Различия шейдера пикселей

## <a name="instruction-slots"></a>Слоты инструкций

Каждая версия поддерживает разное число максимальных слотов инструкций.



| Version  | Максимальное число слотов инструкций                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| PS \_ 1 \_ 1 | 4. текстура + 8 арифметических операций                                                                                              |
| PS \_ 1 \_ 2 | 4. текстура + 8 арифметических операций                                                                                              |
| PS \_ 1 \_ 3 | 4. текстура + 8 арифметических операций                                                                                              |
| PS \_ 1 \_ 4 | 6 текстур + 8 арифметических операций на один этап                                                                                    |
| PS \_ 2 \_ 0 | 32. текстура + 64, арифметический                                                                                            |
| PS \_ 2 \_ x | 96 минимум и до количества слотов в D3DCAPS9. D3DPSHADERCAPS2 \_ 0. нуминструктионслотс. См \_ . D3DPSHADERCAPS2 0. |
| PS \_ 3 \_ 0 | 512 минимум и до количества слотов в D3DCAPS9. MaxPixelShader30InstructionSlots. См \_ . D3DPSHADERCAPS2 0.      |



 

Сведения об ограничениях шейдеров программного обеспечения см. в разделе [программные шейдеры](dx9-graphics-reference-asm-software-shaders.md).

## <a name="flow-control-nesting-limits"></a>Ограничения вложенности управления потоком

-   См. раздел [ограничения управления потоком](dx9-graphics-reference-asm-ps-instructions-flow-control.md).

## <a name="ps_1_x-features"></a>\_функции PS 1 \_ x

Новые инструкции:

См [. \_ \_ инструкции по PS 1 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, \_ \_ ](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md)PS 1 4.

Новые регистры:

См. Дополнительные сведения о [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистрах PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.

## <a name="ps_2_0-features"></a>\_функции PS 2 \_ 0

Новые функции

-   Три новых свиззлес-. изксв,. зксив,. взикс
-   Количество [временных регистров](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), увеличенное до 12
-   Число постоянных регистров [регистра с плавающей запятой](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) увеличилось до 32
-   Количество [регистров координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t \# ) увеличилось до 8

Новые инструкции:

-   Инструкции по установке — [дкл-(SM2, SM3-PS ASM)](dcl---ps.md), [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)
-   Арифметические инструкции [— ABS-PS](abs---ps.md), [CR-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [ФРК-PS](frc---ps.md), [log-](log---ps.md)PS, [m3x2-](m3x2---ps.md)PS [, m3x3-](m3x3---ps.md)PS, [m3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md) [, m4x4-](m4x4---ps.md)PS, [Max-](max---ps.md)PS [, min-PS](min---ps.md), [НРМ-](nrm---ps.md)PS, [Pow-](pow---ps.md)PS, [rcp](rcp---ps.md)-PS, [РСК-](rsq---ps.md)PS, [синкос-PS](sincos---ps.md)
-   Инструкции по текстуре — [текслд-PS \_ 2 \_ 0 и up](texld---ps-2-0.md) (другой синтаксис), [текслдб-PS](texldb---ps.md), [текслдп-PS](texldp---ps.md)

Новые регистры:

-   [Образцы (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \#

## <a name="ps_2_x-features"></a>\_функции PS 2 \_ x

Новые возможности (см. [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):

-   Динамическое управление потоком
-   Статическое управление потоком
-   Инструкции по вложению для динамических и статических функций управления потоком
-   Число увеличенных [временных регистров](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# )
-   Произвольный исходный свиззле
-   Инструкции по градиенту
-   Предикация
-   Нет ограничения на чтение зависимой текстуры
-   Предел для инструкции текстуры отсутствует

Новые инструкции:

-   Статические инструкции по управлению потоком — [Если bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [каллнз bool-](callnz-bool---ps.md)PS, [else-PS](else---ps.md), [endif-PS](endif---ps.md), [представитель-PS](rep---ps.md), [ендреп-](endrep---ps.md)PS, [Label-PS](label---ps.md), [RET-PS](ret---ps.md)
-   Динамическое управление потоком инструкции [-break-PS](break---ps.md), Break-PS, [бреакп-PS](break-p---ps.md), [каллнз пред-PS](callnz-pred---ps.md), [if \_ comp-PS](if-comp---ps.md), [Если пред-](if-pred---ps.md)PS, [сетп \_ comp-PS](setp-comp---ps.md) [ \_ ](break-comp---ps.md)
-   Арифметические инструкции — [ДСКС-PS](dsx---ps.md), [ДСИ-PS](dsy---ps.md)
-   Текстурная инструкция- [текслдд-PS](texldd---ps.md)

Новые регистры:

-   [Регистр предиката](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)

## <a name="ps_3_0-features"></a>\_функции PS 3 \_ 0

Новые функции

-   Консолидированный 10 [входных регистров](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)(v \# )
-   Индексируемый [входной цветовой регистр](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) с [регистром счетчика цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al)
-   Количество [временных регистров](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ), увеличенное до 32
-   Число [постоянных регистров с плавающей запятой](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) увеличилось до 224

Новые инструкции:

-   Инструкция Setup — [ \_ семантика дкл (SM3-PS ASM)](dcl-usage---ps.md)
-   Статические инструкции потока- [Loop-PS](loop---ps.md), [ендлуп-PS](endloop---ps.md)
-   Арифметическая инструкция- [синкос-PS](sincos---ps.md) (новый синтаксис)
-   Текстурная инструкция- [текслдл-PS](texldl---ps.md)

Новые регистры:

-   [Входной регистр](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )
-   [Регистр позиций](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (впос)
-   [Регистр лиц](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (вфаце)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шейдеры пикселей](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 