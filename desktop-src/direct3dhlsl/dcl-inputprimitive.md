---
title: dcl_inputPrimitive (SM4-ASM)
description: дкл \_ инпутпримитиве (SM4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0660fe4da14a20f074e4f04de8891fc0848f2597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479900"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>дкл \_ инпутпримитиве (SM4-ASM)

Объявляет тип-примитив для входных данных шейдера Geometry.



| \_ *тип* инпутпримитиве дкл |
|----------------------------|



 




| Элемент | Описание | 
|------|-------------|
| <span id="type"></span><span id="TYPE"></span><em>Тип</em><br /> | окне Тип примитива input-Data, который является одним из следующих: <br /><ul><li>список <em>точек</em></li><li>список <em>строк</em></li><li><em>треугольник</em> -треугольниковый список</li><li><em>line_adj</em> -Line List с данными о сосмежном уровне</li><li><em>triangle_adj</em> -треугольниковый список с смежными данными</li></ul> | 




 

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
|               | x               |              |



 

Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.

## <a name="example"></a>Пример

Ниже приведен пример.


```
dcl_inputPrimitive triangle
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

 

 





