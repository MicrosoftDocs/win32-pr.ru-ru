---
title: Регистр счетчиков циклов (Справочник по HLSL VS)
description: Единственный регистр в этом банке — регистрация текущего цикла (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b12f57ba3fcfcb41aaff3827be39dbd1b6b07df1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104412262"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a>Регистр счетчиков циклов (Справочник по HLSL VS)

Единственный регистр в этом банке — регистрация текущего цикла (aL). Он автоматически увеличивается при каждом выполнении [цикла-VS](loop---vs.md).. блок [ендлуп-VS](endloop---vs.md) . Поэтому его можно использовать в блоке для относительной адресации, если это необходимо, и недопустимо использовать его за пределами цикла.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




