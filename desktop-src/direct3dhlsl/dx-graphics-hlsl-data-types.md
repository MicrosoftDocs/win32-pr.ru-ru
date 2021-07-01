---
title: Типы данных (HLSL)
description: HLSL поддерживает множество различных встроенных типов данных. В этой таблице показано, какие типы следует использовать для определения переменных шейдера.
ms.assetid: e4b7738d-e865-4151-a204-0a5b88a913b3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c4cb8f6fd15db857daa3005c99381d437a5289f6
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129651"
---
# <a name="data-types-hlsl"></a>Типы данных (HLSL)

HLSL поддерживает множество различных встроенных типов данных. В этой таблице показано, какие типы следует использовать для определения переменных шейдера.



| Использовать этот встроенный тип                                                                                                                         | Определение переменной шейдера                                            |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [скалярная](dx-graphics-hlsl-scalar.md)                                                                                   | Скаляр в одном компоненте                       |
| [Вектор](dx-graphics-hlsl-vector.md), [Матрица](dx-graphics-hlsl-matrix.md)                                            | Вектор или матрица с несколькими компонентами        |
| [Образец](dx-graphics-hlsl-sampler.md), [текстура](dx-graphics-hlsl-texture.md) или [буфер](dx-graphics-hlsl-buffer.md)   | Образец, текстура или объект buffer         |
| [Структура](dx-graphics-hlsl-struct.md), [определяемая пользователем](dx-graphics-hlsl-user-defined.md)                                | Пользовательская структура или typedef                |
| Array                                                                                   | Объявленные литеральные скалярные выражения, содержащие большинство других типов                       |
| [Объект State](dx-graphics-hlsl-state-object.md) | HLSL представления объектов состояния |


 

Чтобы лучше понять, как использовать векторы и матрицы в HLSL, вам может потребоваться ознакомиться с этой информацией о том, как HLSL использует математические функции [для каждого компонента](dx-graphics-hlsl-per-component-math.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Переменные (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 




