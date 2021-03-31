---
title: Иажентчарактерексая версия
description: Иажентчарактерексая версия
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067787"
---
# <a name="iagentcharacterexgetversion"></a>Иажентчарактерекс::/версия

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Возвращает номер версии набора стандартных анимаций символов.

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

Номер версии стандартного набора анимации автоматически задается при сборке с помощью редактора символов Microsoft Agent.

 

 




