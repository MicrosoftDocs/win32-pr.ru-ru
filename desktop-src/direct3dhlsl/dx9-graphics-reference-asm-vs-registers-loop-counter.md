---
title: Регистр счетчиков циклов (Справочник по HLSL VS)
description: Ознакомьтесь с регистром счетчиков циклов для шейдеров вершин. Единственный регистр в этом банке — регистрация текущего цикла (aL).
ms.assetid: b32fabf8-38d3-446c-bb80-c647d5aa028d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa0bf4d44d33f6939c8c45af4509e15e96adf9c4c36a611e049097120db2ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023944"
---
# <a name="loop-counter-register-hlsl-vs-reference"></a>Регистр счетчиков циклов (Справочник по HLSL VS)

Единственный регистр в этом банке — регистрация текущего цикла (aL). Он автоматически увеличивается при каждом выполнении [цикла-VS](loop---vs.md).. блок [ендлуп-VS](endloop---vs.md) . Поэтому его можно использовать в блоке для относительной адресации, если это необходимо, и недопустимо использовать его за пределами цикла.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Регистры шейдеров вершин](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




