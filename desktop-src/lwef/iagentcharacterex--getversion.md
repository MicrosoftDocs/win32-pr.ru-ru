---
title: Иажентчарактерексая версия
description: Иажентчарактерексая версия
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864bd0cf53e9dd94a547a459bb17cd477189401d544aebca047ead2f049c1c6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750477"
---
# <a name="iagentcharacterexgetversion"></a>Иажентчарактерекс::/версия

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

 

 




