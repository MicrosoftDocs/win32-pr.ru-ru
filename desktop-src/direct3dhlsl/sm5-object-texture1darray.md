---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 11573dc84c46149073ca3a7e192ed8541d9cfd4a78494a43f6130a7999534880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508680"
---
# <a name="texture1darray"></a>Texture1DArray

Тип Texture1DArray ([как он существует в модели шейдеров 4](dx-graphics-hlsl-to-type.md)) и переменные ресурсов. Этот объект текстуры поддерживает следующие методы в дополнение к методам в модели шейдера 4.



| Метод                                                                       | Описание                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Возвращает размеры ресурсов.                                                              |
| [**Загрузить**](texture1darray-load.md)                                          | Считывает данные текстуры.                                                                        |
| [**MIPS. Станции\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Возвращает переменную ресурса, доступную только для чтения.                                                        |
| [**Оператор\[\]**](sm5-object-texture1darray-operatorindex.md)              | Возвращает переменную ресурса, доступную только для чтения.                                                        |
| [**Следующий**](texture1darray-sample.md)                                      | Выбор текстуры.                                                                         |
| [**самплебиас**](texture1darray-samplebias.md)                              | Выбор текстуры после применения значения смещения к уровню mipmap.                      |
| [**самплекмп**](texture1darray-samplecmp.md)                                | Выбор текстуры с использованием значения сравнения для отклонения выборок.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Производит выборку текстуры (только mipmap уровень 0), используя значение сравнения для отклонения выборок.       |
| [**самплеград**](texture1darray-samplegrad.md)                              | Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Выбирает текстуру на указанном уровне mipmap.                                           |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Этот объект поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                | Поддерживается |
|-----------------------------------------------------------------------------|-----------|
| [Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров | Да       |



 

Этот объект поддерживается для следующих типов шейдеров:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Службы вычислений |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Объекты модели шейдеров 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




