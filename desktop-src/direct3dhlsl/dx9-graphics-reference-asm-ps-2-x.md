---
title: ps_2_x
description: Сведения о ps_2_x, программируемом шейдере пикселей, который состоит из набора инструкций, которые работают с данными пикселей.
ms.assetid: 06f657a9-6521-404e-b012-7c8e972e9d5c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9efedc6011cb63b6465fd2d3ced4a7807c09f4da
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010877"
---
# <a name="ps_2_x"></a>PS \_ 2 \_ x

Программируемый шейдер пикселей состоит из набора инструкций, которые работают с данными пикселей. Регистрирует перенос данных в ALU и из него. Можно применить дополнительный элемент управления для изменения инструкции, результатов или данных, которые будут записаны.

-   [инструкции по PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-instructions-ps-2-x.md) содержат список доступных инструкций.
-   [в \_ \_ регистрах PS 2 x](dx9-graphics-reference-asm-ps-registers-ps-2-x.md) перечислены различные типы регистров, используемые вершиной шейдера ALU.
-   [Модификаторы](dx9-graphics-reference-asm-ps-registers-modifiers.md) Используются для изменения способа работы инструкции.
-   [Маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) определяет, какие компоненты записываются в реестре назначения.
-   [Модификаторы исходного регистра Pixel Shader](dx9-graphics-reference-asm-ps-registers-modifiers-source.md) изменяют данные исходной регистрации перед выполнением инструкции.
-   [Исходный регистр группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) обеспечивает дополнительный контроль над тем, какие компоненты регистрации считываются, копируются или записываются.

## <a name="dynamic-flow-control"></a>Динамическое управление потоком

[**Динамикфловконтролдепс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) представляет глубину вложения динамических инструкций по управлению потоком: [Если](if-bool---ps.md), если задано [значение \_](if-pred---ps.md) [, if, \_](if-comp---ps.md)то if [-PS](break---ps.md)или [break- \_ PS](break-comp---ps.md). Значение равно глубине вложения \_ блока if. Если это ограничение равно нулю, устройство не поддерживает инструкции динамического управления потоком.

## <a name="number-of-temporary-registers"></a>Количество временных регистров

Количество временных регистров, поддерживаемое устройством. Диапазон — от 12 до 32.

## <a name="static-flow-control-nesting-depth"></a>Глубина вложения статического управления потоком

[**Статикфловконтролдепс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) представляет глубину вложения двух типов статических инструкций по управлению потоком: « [цикл](loop---ps.md)  / [](rep---ps.md) » и « [вызов](call---ps.md)  / [каллнз](callnz-bool---ps.md)». инструкции цикла/REP могут быть вложены до **статикфловконтролдепс** Deep. По отдельности, инструкции Call/каллнз можно вложить в **статикфловконтролдепс** глубину.

## <a name="number-of-instruction-slots"></a>Число слотов инструкций

Число слотов инструкций может варьироваться от 96 до 512 и задается параметром [**макспикселшадеринструктионслотс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0). Общее число инструкций, которые могут выполняться, определяется **макспикселшадеринструктионсексекутед**. Это значение может быть больше, чем количество слотов инструкций из-за вызовов циклов и подпрограмм.

## <a name="arbitrary-swizzle"></a>Произвольный Свиззле

Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ арбитрарисвиззле**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , то поддерживается произвольный свиззле. См. раздел [Source Register группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="gradient-instructions"></a>Инструкции по градиенту

Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ градиентинструктионс**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , то поддерживаются инструкции градиента. См. раздел [ДСКС-PS](dsx---ps.md), [ДСИ-PS](dsy---ps.md)и [текслдд-PS](texldd---ps.md).

## <a name="predication"></a>Предикация

Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ затенения**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , инструкция затенения поддерживается. См. раздел [Регистрация предиката](dx9-graphics-reference-asm-ps-registers-predicate.md).

## <a name="dependent-read-limit"></a>Зависимое ограничение чтения

Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ нодепендентреадлимит**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , зависимые ограничения чтения отсутствуют.

## <a name="texture-instruction-limit"></a>Предел для инструкции текстуры

Если задано значение [**D3DD3DPSHADERCAPS2 \_ 0 \_ нотексинструктионлимит**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0) , инструкции по текстуре не превышены.

## <a name="sampler-count"></a>Число образцов

Число доступных образцов для пробных текстур равно 16.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Шейдеры пикселей](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 