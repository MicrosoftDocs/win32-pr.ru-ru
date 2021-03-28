---
title: Модель шейдера 5
description: Этот раздел содержит справочные страницы для HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413158"
---
# <a name="shader-model-5"></a>Модель шейдера 5

Этот раздел содержит справочные страницы для HLSL Shader Model 5.

Shader Model 5 является надмножеством возможности в [модели шейдера 4](dx-graphics-hlsl-sm4.md). Она была разработана с использованием ядра общего шейдера, предоставляющего общий набор функций для всех программируемых шейдеров, которые можно программировать только с помощью HLSL.



| Компонент                   | Возможностями.                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Набор инструкций           | [**Встроенные функции HLSL**](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| Максимум вершинного шейдера         | Без ограничений                                                                                                                                         |
| Максимальный размер шейдера пикселей          | Без ограничений                                                                                                                                         |
| Добавлены новые профили шейдеров | CS \_ 4 \_ 0, GS \_ 4 \_ 0, \* PS \_ 4 \_ 0 \* , VS \_ 4 \_ 0 \* , CS \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , VS \_ 4 \_ 1 \* , CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 0, HS 5 0, \_ \_ \_ PS \_ 5 \_ 0, VS \_ 5 \_ 0 |



 

\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS 4 0 \_ \_ , PS \_ 4 1 \_ , VS \_ 4 \_ 0 и vs \_ 4 \_ 1 были введены в модель шейдеров 4,0, однако в DirectX 11 добавлена поддержка [структурированных буферов](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) и буферов байтовых адресов для модели шейдеров 4, работающей на оборудовании DirectX 10.

В модели шейдеров 5 появился [вычислительный шейдер](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) , который обеспечивает высокоскоростные вычисления общего назначения.

Более полный список функций шейдера 5 включен в список [функций Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).

В разделе [Assembly модель шейдеров 5](shader-model-5-assembly--directx-hlsl-.md) описаны инструкции ассемблера, поддерживаемые моделью шейдеров 5.

## <a name="in-this-section"></a>в этом разделе



| Элемент                                                                                                                                                                                                                                                        | Описание                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Атрибуты модели шейдеров 5](d3d11-graphics-reference-sm5-attributes.md)<br/>                                     | Справочные страницы для атрибутов Shader модели 5.<br/>          |
| <span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Встроенные функции модели шейдеров 5](d3d11-graphics-reference-sm5-intrinsics.md)<br/> | Справочные страницы для встроенных функций модели шейдеров 5.<br/> |
| <span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Объекты модели шейдеров 5](d3d11-graphics-reference-sm5-objects.md)<br/>                                                    | Справочные страницы для объектов и методов модели шейдеров 5.<br/> |
| <span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Системные значения модели шейдеров 5](d3d11-graphics-reference-sm5-system-values.md)<br/>                      | Справочные страницы для системных значений модели шейдеров 5.<br/>       |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Модели шейдеров и профили шейдеров](dx-graphics-hlsl-models.md)
</dt> </dl>

 

