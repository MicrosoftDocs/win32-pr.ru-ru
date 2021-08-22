---
title: " undef"
description: Директива \ undef удаляет текущее определение указанного имени. Все последующие вхождения имени обрабатываются без замены.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adf208ecca3f130aefc99de8d2926028f25bcd46be46d42e4cbf92e708fa0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473064"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Директивы препроцессора](preprocessor-directives.md)
</dt> </dl>

 

 




