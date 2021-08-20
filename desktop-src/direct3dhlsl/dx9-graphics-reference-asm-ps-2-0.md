---
title: ps_2_0
description: Сведения о ps_2_0, программируемом шейдере пикселей, который состоит из набора инструкций, которые работают с данными пикселей.
ms.assetid: 15f2e4a4-9c39-434b-bea7-5d2d31cae1d9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c9e52b912560cea3b9eb04f9659a27accbbdcd11252b827da6f6dec7df7498c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908680"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Шейдеры пикселей](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 




