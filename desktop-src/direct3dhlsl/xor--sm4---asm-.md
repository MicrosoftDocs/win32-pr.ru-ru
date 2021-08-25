---
title: XOR (SM4-ASM)
description: Битовая операция XOR.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a4dae86a4c6ade427b749c2bb72974564b8a4b7a6baae6821edb3c0d63b2164
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892414"
---
# <a name="xor-sm4---asm"></a>XOR (SM4-ASM)

Битовая операция XOR.



| XOR dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\] |
|-------------------------------------------------------|



 



| Элемент                                                            | Описание                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] результате операции.<br/>       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] компонентах для XOR с *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] компонентах для XOR с *src0*.<br/> |



 

## <a name="remarks"></a>Remarks

Эта инструкция выполняет покомпонентное Логическое исключающее XOR каждой пары 32-разрядных значений из *src0* и *src1*. 32-разрядные результаты помещаются в *dest*.

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

 

 





