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
ms.openlocfilehash: 37086a030ad902f2bfb5deab52ffba620e97890bd13e7c6957170572087ce7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514582"
---
# <a name="functions-hlsl-reference"></a>Функции (Справочник по HLSL)

Функции инкапсулируют инструкции HLSL. Это позволяет отлаживать набор функций, а затем повторно использовать их в шейдерах или эффектах. Может потребоваться создать функцию, которая инкапсулирует функциональные возможности шейдера вершин, шейдера пикселей или шейдера текстуры. В других случаях может потребоваться написать вспомогательную функцию, которая выполняет некоторую часто используемую задачу, а затем вызывать эту вспомогательную функцию из функции шейдера. Правила написания функций шейдера для HLSL очень похожи на написание функций C.

-   [Синтаксис](dx-graphics-hlsl-function-syntax.md)
-   [Параметры](dx-graphics-hlsl-function-parameters.md)
-   [Оператор Return](dx-graphics-hlsl-return.md)
-   [Сигнатуры](dx-graphics-hlsl-signatures.md)

HLSL также имеет ряд встроенных встроенных [**функций (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md). Так как все встроенные функции протестированы и оптимизированы для производительности, рекомендуется использовать встроенную функцию, где это возможно, вместо создания собственной функции.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Синтаксис языка (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




