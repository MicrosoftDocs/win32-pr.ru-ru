---
title: ishl (sm5 — asm)
description: Сдвиг влево. | Ишл (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230034e66ca9adfbd6c94cc99351b485c6577fdf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353125"
---
# <a name="ishl-sm5---asm"></a>ishl (sm5 — asm)

Сдвиг влево.



| Ишл dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\] |
|--------------------------------------------------------|



 



| Элемент                                                            | Описание                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] содержит результаты сдвига.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] 32-разрядных значениях для сдвига.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] поле число битов для сдвига.<br/>        |



 

## <a name="remarks"></a>Примечания

Эта инструкция выполняет покомпонентную смену каждого 32-битного значения в *src0* влево на число целых чисел без знака, обеспечиваемое значением ЛСБ 5 бит (диапазон 0-31) в *src1*, вставляя 0. Результаты 32-бит на компонент помещаются в *dest*.

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





