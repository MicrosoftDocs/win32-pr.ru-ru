---
title: Формат пары идентификатор/смещение
description: Вторая часть потока набора свойств содержит одну пару идентификаторов и смещений формата.
ms.assetid: cc3a748d-e81c-45da-b04f-ea986158a4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f80a85175278b92fedbfd7b2d50d94007b7e4a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329539"
---
# <a name="format-identifieroffset-pair"></a>Формат пары идентификатор/смещение

Вторая часть потока набора свойств содержит одну пару идентификаторов и смещений формата. FMTID — это имя набора свойств; Он однозначно определяет способ интерпретации содержимого следующего раздела. Смещение — это расстояние в байтах от начала всего потока до начала раздела.

Следующая структура полезна при обработке пар идентификаторов и смещений формата.

``` syntax
typedef struct tagFORMATIDOFFSET 
{ 
    FMTID  fmtid ;     // Name of the section. 
    DWORD  dwOffset ;  // Offset for the section. 
} FORMATIDOFFSET;
```

 

 




