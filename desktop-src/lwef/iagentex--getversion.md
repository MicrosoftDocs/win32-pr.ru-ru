---
title: Иажентексая версия
description: Иажентексая версия
ms.assetid: e5d55fcd-c1b4-4c9e-b3c7-4471af2f86af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebec46a242dc18aa47dd1024c9a80856bdf7c000625d765a2a013af33b5ca2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961544"
---
# <a name="iagentexgetversion"></a>Иажентекс::/версия

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Возвращает номер версии сервера Microsoft Agent Server.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*псмажор*
</dt> <dd>

Адрес переменной, которая получает основной номер версии.

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*псминор*
</dt> <dd>

Адрес переменной, которая получает дополнительный номер версии.

</dd> </dl>

 

 




