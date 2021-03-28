---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068882"
---
# <a name="texture3d"></a>Texture3D

Тип Texture3D ([как он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурсов. Этот объект текстуры поддерживает следующие методы в дополнение к методам в модели шейдера 4.



| Метод                                                                  | Описание                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Возвращает размеры ресурсов.                                                              |
| [**Загрузить**](texture3d-load.md)                                          | Считывает данные текстуры.                                                                        |
| [**MIPS. Станции\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Возвращает переменную ресурса, доступную только для чтения.                                                        |
| [**Оператор\[\]**](sm5-object-texture3d-operatorindex.md)              | Возвращает переменную ресурса, доступную только для чтения.                                                        |
| [**Пример**](texture3d-sample.md)                                      | Выбор текстуры.                                                                         |
| [**самплебиас**](texture3d-samplebias.md)                              | Выбор текстуры после применения значения смещения к уровню mipmap.                      |
| [**самплеград**](texture3d-samplegrad.md)                              | Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца. |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Выбирает текстуру на указанном уровне mipmap.                                           |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Этот объект поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | да       |



 

Этот объект поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты модели шейдеров 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




