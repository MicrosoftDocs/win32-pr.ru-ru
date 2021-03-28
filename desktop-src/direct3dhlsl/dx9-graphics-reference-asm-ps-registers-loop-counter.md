---
title: Регистр счетчиков циклов (Справочник по HLSL PS)
description: Единственный регистр в этом банке — регистрация текущего цикла (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785076"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Регистр счетчиков циклов (Справочник по HLSL PS)

Единственный регистр в этом банке — регистрация текущего цикла (aL). Он автоматически увеличивается при каждом выполнении блока [Loop-PS](loop---ps.md) / [ендлуп-PS](endloop---ps.md) . Поэтому его можно использовать в блоке для относительной адресации, если это необходимо, и недопустимо использовать его за пределами цикла.



| Версии шейдеров пикселей | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Регистр счетчика цикла |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Регистры](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




