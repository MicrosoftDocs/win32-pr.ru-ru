---
title: Иаженткоммандс Voice
description: Иаженткоммандс Voice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412962"
---
# <a name="iagentcommandsgetvoice"></a>Иаженткоммандс:: Voice

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

Возвращает значение свойства [**Voice**](voice-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*пбсзвоице*
</dt> <dd>

Адрес объекта BSTR, который получает значение параметра текста [**голоса**](voice-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: сетвоице**](iagentcommands--setvoice.md), [**иаженткоммандс:: oncaption**](iagentcommands--getcaption.md), [**иаженткоммандс::**](iagentcommands--getvisible.md)


 

 