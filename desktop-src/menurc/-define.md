---
title: " define"
description: Директива \ define Присваивает заданному значению указанное имя. Все последующие вхождения имени заменяются значением.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8e8f99dc592eefb1fb79201883e8a32837633814b79d7819e84d283709a46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826054"
---
# <a name="define"></a>\#определенно

Директива **\# define** Присваивает заданному значению указанное имя. Все последующие вхождения имени заменяются значением.

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*безымян*
</dt> <dd>

Имя, которое необходимо определить. Это значение представляет собой любое сочетание букв, цифр и знаков препинания, допустимое для препроцессора C/C++.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*значений*
</dt> <dd>

Целое число, символьная строка или строка текста.

</dd> </dl>

## <a name="example"></a>Пример

В этом примере значения присваиваются именам ненулевые и USERCLASS:

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Директивы препроцессора](preprocessor-directives.md)
</dt> </dl>

 

 




