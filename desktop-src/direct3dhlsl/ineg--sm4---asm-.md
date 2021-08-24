---
title: инег (SM4-ASM)
description: 2 дополнение.
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9994d9b21cc7d851c243294eb43e00e84024057f66da59f7ac96e961a30217
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788874"
---
# <a name="ineg-sm4---asm"></a>инег (SM4-ASM)

2 дополнение.



| инег dest \[ . Mask \] , src0 \[ . свиззле |
|------------------------------------|



 



| Элемент                                                            | Описание                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] адресе результата операции.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в параметр \] содержит значения для операции.<br/>      |



 

## <a name="remarks"></a>Remarks

Эта инструкция выполняет дополнение 2 для каждого 32-битного значения в *src0*. 32-разрядные результаты хранятся в *dest*.

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

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

 

 





