---
title: Mad (SM4-ASM)
description: Добавление на уровне компонентов.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc4569cc656aa723c2923ad19b601cd37ff850868627db5bc0613b50b016dcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906725"
---
# <a name="mad-sm4---asm"></a>Mad (SM4-ASM)

& добавления на уровне компонентов.



| : Mad No \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src2 \[ \_ ABS \] \[ . свиззле\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Элемент                                                            | Описание                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] результате операции.<br/> *конечный адрес*  =  *src0* \* *src1*  +  *src2*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] множимое.<br/>                                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] множители.<br/>                                                            |
| <span id="src2"></span><span id="SRC2"></span>*src2*<br/> | \[в \] слагаемое.<br/>                                                                |



 

## <a name="remarks"></a>Remarks

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

 

 





