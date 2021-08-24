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
ms.openlocfilehash: 6e800f2ef313cd5c9a4fc90d7205502db5532ae24f51ec0f1255d05cc9a589bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853794"
---
# <a name="rep---vs"></a>Представитель-VS

Запустить представителя... блок [ендреп](endrep---vs.md) .

## <a name="syntax"></a>Синтаксис



| Представитель\# |
|---------|



 

где i \# — это целочисленный регистр, указывающий число повторов в компоненте. x. См. раздел [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md).

## <a name="remarks"></a>Remarks



| Версии шейдеров вершин | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| склад                    |      | x    | x    | x     | x    | x     |



 

-   i \# . x указывает число итераций. Допустимый диапазон: \[ 0, 255 \] . Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.
-   i \# . ИЗВ не используются в блоке REPEAT.
-   Блоки Repeat могут быть вложенными. см. раздел [ограничения вложенности элемента управления Flow](dx9-graphics-reference-asm-vs-instructions-flow-control.md).
-   Блоки Repeat могут быть либо полностью внутри \* блока if, либо полностью окружающи ее. Помещается в недопустимый.
-   Использование одного и того же i \# для различных или вложенных инструкций — Точная — каждый цикл выполняет итерацию в зависимости от указанного числа.

## <a name="example"></a>Пример


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Инструкции шейдера вершин](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




