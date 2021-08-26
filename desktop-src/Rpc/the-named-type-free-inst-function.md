---
title: Функция named_type_free_inst
description: Заглушки вызывают функцию с именованным \_ типом \_ Free \_ inst для освобождения памяти, связанной с передаваемым типом.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa55e896b89fccc513795a62634e805c2ad6e21b7bdecdd99a0b9cfe2d71cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016893"
---
# <a name="the-named_type_free_inst-function"></a>Функция с именованным \_ типом \_ Free \_ inst

Заглушки вызывают функцию **с именованным \_ типом \_ Free \_ inst** для освобождения памяти, связанной с передаваемым типом. Функция определяется следующим образом:

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

Параметр указывает на экземпляр переданного типа. Этот объект не должен освобождаться. Обсуждение того, когда следует вызывать функцию, см. [в разделе \_ атрибут представления как](the-represent-as-attribute.md).

 

 




