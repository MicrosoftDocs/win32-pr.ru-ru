---
title: Loop-PS
description: Запускает цикл... блок ендлуп-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069352"
---
# <a name="loop---ps"></a>Loop-PS

Запускает цикл... блок [ендлуп-PS](endloop---ps.md) .

## <a name="syntax"></a>Синтаксис



| цикл aL, i\# |
|--------------|



 

Где:

-   aL — это [регистр счетчиков циклов](dx9-graphics-reference-asm-ps-registers-loop-counter.md) , содержащий текущее число циклов.
-   я \# является [постоянным целочисленным регистром](dx9-graphics-reference-asm-ps-registers-constant-integer.md). См. примечания.

## <a name="remarks"></a>Remarks



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| loop                  |      |      |      |      |      |      |       | x    | x     |



 

-   [Регистр счетчика цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) содержит текущее число циклов и может использоваться для относительной адресации в [регистре входных цветов](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) внутри блока цикла.
-   i \# . x указывает число итераций. Допустимый диапазон: \[ 0, 255 \] . Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.
-   i \# . y указывает начальное значение регистра [счетчика циклов](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al). Допустимый диапазон: \[ 0, 255 \] . Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . y.
-   i \# . z указывает размер шага или шаг. Допустимый диапазон — \[ 128, 127 \] .
-   i \# . w не используется блоком цикла и должен быть равен 0.
-   Блоки циклов могут быть вложенными. См. раздел [ограничения управления потоком](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   При вложении значение [регистра счетчика цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) ссылается на непосредственный блок цикла.
-   Блоки циклов могут быть либо полностью внутри \* блока if, либо полностью окружающи его. Помещается в недопустимый.

## <a name="example"></a>Например, .


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера пикселей](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




