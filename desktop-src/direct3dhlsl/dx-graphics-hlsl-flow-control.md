---
title: Управление потоком
description: Большинство аппаратных средств предназначены для выполнения кода шейдера построчно, каждый раз выполняя каждую инструкцию HLSL.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aebaf63613aeb3a1d14607971db16602745883ab6b7b9db4723dfa2367f9bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120288"
---
# <a name="flow-control"></a>Управление потоком

Большинство аппаратных средств предназначены для выполнения кода шейдера построчно, каждый раз выполняя каждую инструкцию HLSL. Оператор управления потоком во время выполнения определяет блок инструкций HLSL, которые нужно выполнить следующим. С помощью оператора управления потоком шейдер может циклически прокручивать набор инструкций или переходить (ветвь) к инструкции, отличной от той, которая находится на следующей строке. Некоторые операторы управления потоком поддерживают статический элемент управления, заданный во время компиляции. другие предлагают элемент управления с предикатами, который является решением для каждого компонента, сделанным во время выполнения, и по-прежнему поддерживает динамическое управление, которое является решением, выполняемым во время выполнения на основе содержимого переменной.

HLSL поддерживает следующие инструкции управления потоком.

-   [break](dx-graphics-hlsl-break.md)
-   [continue](dx-graphics-hlsl-continue.md)
-   [исключить](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md) (если);
-   [switch](dx-graphics-hlsl-switch.md)
-   [while](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Синтаксис языка (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




