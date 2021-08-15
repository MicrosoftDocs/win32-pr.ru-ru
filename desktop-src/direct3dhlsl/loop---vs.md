---
title: цикл — VS
description: Начать цикл... блок ендлуп.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a211014137f35c39a6b89cd16f0e27687b4daafd89841f752312f459531cab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986444"
---
# <a name="loop---vs"></a>цикл — VS

Начать цикл... блок [ендлуп](endloop---vs.md) .

## <a name="syntax"></a>Синтаксис



| цикл aL, i\# |
|--------------|



 

Где:

-   aL — это [регистр счетчиков циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) , содержащий текущее число циклов.
-   я \# является [постоянным целочисленным регистром](dx9-graphics-reference-asm-vs-registers-constant-integer.md). См. примечания.

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| loop                   |      | x    | x    | x     | x    | x     |



 

-   [Регистр счетчика цикла](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) содержит текущее число циклов и может использоваться для относительных адресов в [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) или [выходные регистры](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) внутри блока цикла.
-   i \# . x указывает число итераций. Допустимый диапазон: \[ 0, 255 \] . Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.
-   i \# . y указывает начальное значение регистра [счетчика циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al). Допустимый диапазон: \[ 0, 255 \] . Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . y.
-   i \# . z указывает размер шага или шаг. Допустимый диапазон — \[ 128, 127 \] .
-   i \# . w не используется, и его значение должно быть равно 0.
-   Блоки циклов могут быть вложенными. см. раздел [ограничения вложенности элемента управления Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   При вложении значение [регистра счетчика цикла](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) ссылается на непосредственный блок цикла.
-   Блоки циклов могут быть либо полностью внутри \* блока if, либо полностью окружающи его. Помещается в недопустимый.

## <a name="example"></a>Пример


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




