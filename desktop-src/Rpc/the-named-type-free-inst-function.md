---
title: Функция named_type_free_inst
description: Заглушки вызывают функцию с именованным \_ типом \_ Free \_ inst для освобождения памяти, связанной с передаваемым типом.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774627"
---
# <a name="the-named_type_free_inst-function"></a>Функция с именованным \_ типом \_ Free \_ inst

Заглушки вызывают функцию **с именованным \_ типом \_ Free \_ inst** для освобождения памяти, связанной с передаваемым типом. Функция определяется следующим образом:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

Параметр указывает на экземпляр переданного типа. Этот объект не должен освобождаться. Обсуждение того, когда следует вызывать функцию, см. [в разделе \_ атрибут представления как](the-represent-as-attribute.md).

 

 




