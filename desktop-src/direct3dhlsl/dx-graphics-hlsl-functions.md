---
title: Функции (Справочник по HLSL)
description: Функции инкапсулируют инструкции HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335659"
---
# <a name="functions-hlsl-reference"></a>Функции (Справочник по HLSL)

Функции инкапсулируют инструкции HLSL. Это позволяет отлаживать набор функций, а затем повторно использовать их в шейдерах или эффектах. Может потребоваться создать функцию, которая инкапсулирует функциональные возможности шейдера вершин, шейдера пикселей или шейдера текстуры. В других случаях может потребоваться написать вспомогательную функцию, которая выполняет некоторую часто используемую задачу, а затем вызывать эту вспомогательную функцию из функции шейдера. Правила написания функций шейдера для HLSL очень похожи на написание функций C.

-   [Синтаксис](dx-graphics-hlsl-function-syntax.md)
-   [Параметры](dx-graphics-hlsl-function-parameters.md)
-   [Оператор Return](dx-graphics-hlsl-return.md)
-   [Сигнатуры](dx-graphics-hlsl-signatures.md)

HLSL также имеет ряд встроенных встроенных [**функций (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md). Так как все встроенные функции протестированы и оптимизированы для производительности, рекомендуется использовать встроенную функцию, где это возможно, вместо создания собственной функции.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Синтаксис языка (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




