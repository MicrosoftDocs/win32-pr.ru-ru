---
title: vs_2_0
description: Сведения о vs_2_0, программируемом шейдере вершин, который состоит из набора инструкций, которые работают с данными вершин.
ms.assetid: 6e38c138-5f9c-40a6-9fe2-a93471c3c573
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fe951d62b869a303a0c07839b46840dc8f9fda00
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010857"
---
# <a name="vs_2_0"></a>VS \_ 2 \_ 0

Программируемый шейдер вершин состоит из набора инструкций, которые работают с данными вершин. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.

-   [Инструкции — VS \_ 2 \_ 0](dx9-graphics-reference-asm-vs-instructions-vs-2-0.md) содержит список доступных инструкций.
-   [Регистры — VS \_ 2 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-2-0.md) содержит различные типы регистров, используемые вершиной шейдера ALU.
-   [Модификаторы регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers.md) используются для изменения способа работы инструкции.
-   [Модификаторы исходного регистра вершинного шейдера](dx9-graphics-reference-asm-vs-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.
-   [Исходный регистр группирующие](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.
-   [Маскирование регистров назначения](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md) определяет, какие компоненты записываются в реестре назначения.

## <a name="instruction-count"></a>Число инструкций

Каждый шейдер вершин может содержать до 256 инструкций. Количество выполняемых инструкций может быть намного выше (из-за поддержки цикла или представителя) и ограничено D3DCAPS9. Максвшадеринструктионсексекутед, который должен быть не менее 0xFFFF.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Шейдеры вершин](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 




