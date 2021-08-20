---
title: или (SM4-ASM)
description: Побитовое или.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a65d6ee2c5e5559d7d5e877a2bdef83b13a45a06ca0f00c980baa4811579f03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088747"
---
# <a name="or-sm4---asm"></a>или (SM4-ASM)

Побитовое или.



| или DEST \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\] |
|------------------------------------------------------|



 



| Элемент                                                            | Описание                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] результате операции.<br/>      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] компонентах или с *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] компонентах или с *src0*.<br/> |



 

## <a name="remarks"></a>Remarks

Эта инструкция выполняет покомпонентную логическую операцию или для каждой пары 32-разрядных значений из *src0* и *src1*. 32-разрядные результаты помещаются в *dest*.

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

 

 





