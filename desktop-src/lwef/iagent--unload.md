---
title: Выгрузка Иажент
description: Выгрузка Иажент
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e6e457e2acc33c5b34800b8378d82a50d5c4aa6a139366ca1c0d241f676f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610144"
---
# <a name="iagentunload"></a>Иажент:: unload

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 