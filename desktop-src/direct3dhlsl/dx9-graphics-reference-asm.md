---
title: Справочник по шейдеру ASM
description: Шейдеры управляют программируемым графическим конвейером.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2941f4c32d03187ce08266bf1382cd1d94301ce0
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2019
ms.locfileid: "104983932"
---
# <a name="asm-shader-reference"></a>Справочник по шейдеру ASM

Шейдеры управляют программируемым графическим конвейером.

## <a name="vertex-shader-reference"></a>Справочник по шейдеру вершин

-   [VS \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [VS \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [VS \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [VS \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Различия в шейдере вершин](dx9-graphics-reference-asm-vs-differences.md) обобщены различия между версиями шейдеров вершин.

## <a name="pixel-shader-reference"></a>Справочник по шейдеру пикселей

-   [PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Различия шейдера пикселей](dx9-graphics-reference-asm-ps-differences.md) обобщены различия между версиями построителей текстуры.

## <a name="shader-model-4-and-5-reference"></a>Справочник по модели шейдеров 4 и 5

В разделах [«Сборка» и «](dx-graphics-hlsl-sm4-asm.md) шейдер» модели построителя текстур [5](shader-model-5-assembly--directx-hlsl-.md) описываются инструкции, поддерживаемые в модели шейдеров 4 и 5.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Поведение регистров констант в шейдерах сборки

Существует два способа установки регистров констант в шейдере сборки:

-   Объявите константу шейдера в коде сборки с помощью одной из \* инструкций DEF.
-   Используйте один из \* \* \* \* методов API Set шадерконстант.

### <a name="direct3d-9-shader-constants"></a>Константы шейдера Direct3D 9

В Direct3D 9 время существования определенных констант в заданном шейдере ограничено выполнением только этого шейдера (и не может быть переопределяемым). Определенные константы в Direct3D 9 не имеют побочных эффектов вне шейдера.

Ниже приведен пример использования Direct3D 9.


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



В Direct3D 9 вызов get \* \* \* шадерконстант \* будет получать только постоянные значения, заданные через Set \* \* \* шадерконстант \* .

### <a name="direct3d-8-shader-constants"></a>Константы шейдера Direct3D 8

Это поведение отличается в Direct3D 8. x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



В Direct3D 8. x Set \* \* \* шадерконстант вступает в силу немедленно. Рассмотрим следующий сценарий.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



Нежелательный результат заключается в том, что порядок, в котором задаются шейдеры, может повлиять на наблюдаемое поведение отдельных шейдеров.

## <a name="shader-driver-model-requirements"></a>Требования к модели драйвера шейдеров

Интерфейсы Direct3D 9 ограничены драйверами интерфейса драйвера устройства (DDI), поддерживающими DirectX 7 и выше. Чтобы проверить уровень DDI, запустите [средство диагностики DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) и изучите сохраненный текстовый файл.

Для справки интерфейсы Direct3D 8 работают только с драйверами DDI, которые имеют версию DirectX 6 и выше.

## <a name="shader-binary-format"></a>Двоичный формат шейдера

Побитовая структура потока инструкций шейдера определена в D3d9types. h. Если вы хотите разработать собственные компиляторы шейдеров или средства построения и хотите получить дополнительные сведения о потоке маркера шейдера, обратитесь к комплекту средств разработки драйверов Direct3D 9 (DDK).

## <a name="c-like-shader-language"></a>Язык шейдера, похожего на C

См. раздел [Справочник по HLSL](dx-graphics-hlsl-reference.md) для работы с языком шейдера, похожим на C.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




