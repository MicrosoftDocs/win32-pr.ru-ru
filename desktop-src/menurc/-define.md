---
title: " define"
description: Директива \ define Присваивает заданному значению указанное имя. Все последующие вхождения имени заменяются значением.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777486"
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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Директивы препроцессора](preprocessor-directives.md)
</dt> </dl>

 

 




