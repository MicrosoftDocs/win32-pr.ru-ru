---
title: dcl_output_sgv (SM4-ASM)
description: дкл \_ OUTPUT \_ СГВ (SM4-ASM)
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2b3214d262b6ed199e86836a2dd997f8efa6a57ecf99cf43f19630e71ff14b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727018"
---
# <a name="dcl_output_sgv-sm4---asm"></a>дкл \_ OUTPUT \_ СГВ (SM4-ASM)

Объявляет выходной регистр, который содержит параметр [System-value](dx-graphics-hlsl-semantics.md) .



| дкл \_ выходной \_ СГВ On *\[ . Mask \]*, *системвалуе* |
|-----------------------------------------------|



 



| Элемент                                                                                                                               | Описание                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*<br/>                                                     | \[в \] реестре выходных данных; *N* — это целое число, которое обозначает номер регистра.<br/>                                                      |
| <span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*<br/>                                                         | \[\]необязательно. Маска компонента (. ксизв), указывающая, какие компоненты регистров следует использовать.<br/>                                        |
| <span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*системвалуенаме*<br/> | \[в \] имени системного значения, которое является строкой (см. раздел [семантика системного значения](dx-graphics-hlsl-semantics.md)) без \_ префикса «ОКП».<br/> |



 

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
|               | x               |              |



 

Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.

## <a name="example"></a>Пример

Ниже приведен пример.


```
dcl_output_sgv o4.x, primitiveID
```



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

 

 





