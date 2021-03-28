---
title: ps_2_0
description: Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98b0f252d87a1f7e08c3531415d7ebcb93d4f6f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983613"
---
# <a name="ps_2_0"></a>PS \_ 2 \_ 0

Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.

-   [инструкции по PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-instructions-ps-2-0.md) содержат список доступных инструкций.
-   [в \_ \_ регистрах PS 2 0](dx9-graphics-reference-asm-ps-registers-ps-2-0.md) перечислены различные типы регистров, используемые вершиной шейдера ALU.
-   [Модификаторы](dx9-graphics-reference-asm-ps-registers-modifiers.md) Используются для изменения способа работы инструкции.
-   [Маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) определяет, какие компоненты записываются в реестре назначения.
-   [Модификаторы исходного регистра Pixel Shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.
-   [Исходный регистр группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.

## <a name="instruction-count"></a>Число инструкций

Шейдеры имеют ограничения для максимального числа инструкций. Общее число слотов инструкций: 96 (арифметические действия 64 и текстура 32).

## <a name="sampler-count"></a>Число образцов

Число доступных образцов для пробных текстур равно 16.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Шейдеры пикселей](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




