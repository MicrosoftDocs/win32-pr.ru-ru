---
title: Представитель-VS
description: Запустить представителя... блок ендреп.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412165"
---
# <a name="rep---vs"></a>Представитель-VS

Запустить представителя... блок [ендреп](endrep---vs.md) .

## <a name="syntax"></a>Синтаксис



| Представитель\# |
|---------|



 

где i \# — это целочисленный регистр, указывающий число повторов в компоненте. x. См. раздел [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md).

## <a name="remarks"></a>Примечания



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| склад                    |      | x    | x    | x     | x    | x     |



 

-   i \# . x указывает число итераций. Допустимый диапазон: \[ 0, 255 \] . Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.
-   i \# . ИЗВ не используются в блоке REPEAT.
-   Блоки Repeat могут быть вложенными. См. раздел [ограничения вложений управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Блоки Repeat могут быть либо полностью внутри \* блока if, либо полностью окружающи ее. Помещается в недопустимый.
-   Использование одного и того же i \# для различных или вложенных инструкций — Точная — каждый цикл выполняет итерацию в зависимости от указанного числа.

## <a name="example"></a>Например, .


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




