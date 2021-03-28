---
title: dcl_thread_group (SM5-ASM)
description: Объявить размер группы потоков.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069372"
---
# <a name="dcl_thread_group-sm5---asm"></a>\_группа потоков дкл \_ (SM5-ASM)

Объявить размер группы потоков.



| \_группа потоков дкл \_ x, y, z |
|----------------------------|



 



| Элемент                                                   | Описание                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] усигнед 32-разрядное целое число. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*&*<br/> | \[в \] усигнед 32-разрядное целое число. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*гармошкой*<br/> | \[в \] усигнед 32-разрядное целое число. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Примечания

x \* y \* z <= 1024

Это объявление группы потоков должно появиться в шейдере вычислений один раз.

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта инструкция поддерживается в следующих моделях шейдеров:



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Нет        |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Нет        |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сборка Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





