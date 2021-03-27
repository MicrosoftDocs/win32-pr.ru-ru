---
title: Сборка Shader Model 4
description: Сборка Shader Model 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068011"
---
# <a name="shader-model-4-assembly"></a>Сборка Shader Model 4

Шейдер Model 4 требует программирования шейдеров в HLSL. Однако компилятор шейдера компилирует код HLSL в сборку, которая выполняется на устройстве. Если для отладки шейдеров используется PIX для Windows, можно выбрать отображение кода шейдера либо в HLSL, либо в сборке. В этом разделе перечислены инструкции по сборке шейдера 4 и шейдера 4,1, которые могут возникнуть при отладке шейдера.

<dl>

[Модификаторы инструкций](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[бреакк](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[каллк](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[continue](continue--sm4---asm-.md)  
[континуек](continuec--sm4---asm-.md)  
[бавьте](cut--sm4---asm-.md)  
[дкл \_ константбуффер](dcl-constantbuffer.md)  
[дкл \_ глобалфлагс](dcl-globalflags.md)  
[дкл \_ иммедиатеконстантбуффер](dcl-immediateconstantbuffer.md)  
[дкл \_ индексаблетемп](dcl-indexabletemp.md)  
[дкл \_ индексранже](dcl-indexrange.md)  
[\_входные данные дкл](dcl-input.md)  
[дкл \_ входное \_ SV](dcl-input-sv.md)  
[дкл \_ входные вприм](dcl-input-vprim.md)  
[дкл \_ максаутпутвертекскаунт](dcl-maxoutputvertexcount.md)  
[\_выходные данные дкл](dcl-output.md)  
[дкл \_ выходной \_ одепс](dcl-output-odepth.md)  
[дкл \_ выходной \_ СГВ](dcl-output-sgv.md)  
[дкл \_ выходной \_ Сив](dcl-output-siv.md)  
[дкл \_ аутпуттопологи](dcl-outputtopology.md)  
[\_ресурс дкл](dcl-resource.md)  
[\_образец дкл](dcl-sampler.md)  
[дкл \_ временные температуры](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[наследование \_ RTX](deriv-rtx--sm4---asm-.md)  
[наследование \_ РТИ](deriv-rty--sm4---asm-.md)  
[исключить](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[давать](emit--sm4---asm-.md)  
[емитсенкут](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[ендлуп](endloop--sm4---asm-.md)  
[ендсвитч](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[фрк](frc--sm4---asm-.md)  
[фтои](ftoi--sm4---asm-.md)  
[фтау](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[IAdd](iadd--sm4---asm-.md)  
[ибфе](dne--sm5---asm-.md)  
[иек](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[иже](ige--sm4---asm-.md)  
[илт](ilt--sm4---asm-.md)  
[имад](imad--sm4---asm-.md)  
[имин](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[Строка](ine--sm4---asm-.md)  
[инег](ineg--sm4---asm-.md)  
[ишл](ishl--sm4---asm-.md)  
[ишр](ishr--sm4---asm-.md)  
[итоф](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[LD](ld--sm4---asm-.md)  
[Журналь](log--sm4---asm-.md)  
[loop](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[отслеживания](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[функцию](mov--sm4---asm-.md)  
[мовк](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[NOP](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md) (не);  
[или диспетчер конфигурации служб](or--sm4---asm-.md)  
[Resinfo:](resinfo--sm4---asm-.md)  
[обратно](ret--sm4---asm-.md)  
[ретк](retc--sm4---asm-.md)  
[Round \_ Ne](round-ne--sm4---asm-.md)  
[Round \_ Ni](round-ni--sm4---asm-.md)  
[скругленное число \_ Пи](round-pi--sm4---asm-.md)  
[округлить по \_ оси z](round-z--sm4---asm-.md)  
[рск](rsq--sm4---asm-.md)  
[Следующий](sample--sm4---asm-.md)  
[Пример \_ б](sample-b--sm4---asm-.md)  
[Пример \_ с](sample-c--sm4---asm-.md)  
[Пример \_ c \_ LZ](sample-c-lz--sm4---asm-.md)  
[Пример \_ г](sample-d--sm4---asm-.md)  
[Пример \_ l](sample-l--sm4---asm-.md)  
[синкос](sincos--sm4---asm-.md)  
[МНИМ](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[удив](udiv--sm4---asm-.md)  
[уже](uge--sm4---asm-.md)  
[метры](ult--sm4---asm-.md)  
[умад](umad--sm4---asm-.md)  
[Компания](umax--sm4---asm-.md)  
[умин](umin--sm4---asm-.md)  
[умул](umul--sm4---asm-.md)  
[ушр](ushr--sm4---asm-.md)  
[утоф](utof--sm4---asm-.md)  
[xor](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Сборка Shader модели 4,1

Модель шейдеров 4,1 поддерживает все инструкции и следующие дополнительные инструкции для 4,0 модели шейдера.

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[лод](lod--sm4-1---asm-.md)  
[самплеинфо](sampleinfo--sm4-1---asm-.md)  
[самплепос](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по шейдеру ASM](dx9-graphics-reference-asm.md)
</dt> <dt>

[Модель шейдера 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




