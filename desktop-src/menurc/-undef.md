---
title: " undef"
description: Директива \ undef удаляет текущее определение указанного имени. Все последующие вхождения имени обрабатываются без замены.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710083"
---
# <a name="undef"></a>\#undef

Директива **\# undef** удаляет текущее определение указанного имени. Все последующие вхождения имени обрабатываются без замены.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*безымян*
</dt> <dd>

Удаляемое имя. Это значение представляет собой любое сочетание букв, цифр и знаков препинания, допустимое для препроцессора C/C++.

</dd> </dl>

## <a name="example"></a>Пример

В этом примере удаляются определения имен ненулевых и USERCLASS:

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Директивы препроцессора](preprocessor-directives.md)
</dt> </dl>

 

 




