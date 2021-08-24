---
title: Emit (SM4-ASM)
description: Выдает вершину.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce90ed4ea87c74c09c6f45d590e8bc7a70bbb8178988b059c2b3a79726aabcb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673084"
---
# <a name="emit-sm4---asm"></a>Emit (SM4-ASM)

Выдает вершину.



| давать |
|------|



 

## <a name="remarks"></a>Remarks

**выдача** приводит к считыванию всех объявленных \# регистров o из шейдера Geometry для создания вершины.

При выдаче нескольких вызовов **выдачи** создаются примитивы.

**выдача** может появляться любое количество раз в шейдере Geometry, в том числе в элементе управления потоком.

Если были объявлены потоки, необходимо использовать [отражательный \_ поток](emit-stream--sm5---asm-.md).

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
|               | x               |              |



 

### <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | Да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Да       |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




