---
title: Выгрузка Иажент
description: Выгрузка Иажент
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337361"
---
# <a name="iagentunload"></a>Иажент:: unload

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Выгружает символьные данные для указанного символа из коллекции [**символов**](/windows/desktop/lwef/the-characters-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*
</dt> <dd>

ИДЕНТИФИКАТОР символа.

</dd> </dl>

Используйте этот метод, если символ больше не нужен, чтобы освободить память, используемую для хранения сведений об этом символе. При повторном доступе к символу используйте метод [**Load**](load-method.md) .

## <a name="see-also"></a>См. также:

[**Иажент:: Load**](iagent--load.md)


 

 