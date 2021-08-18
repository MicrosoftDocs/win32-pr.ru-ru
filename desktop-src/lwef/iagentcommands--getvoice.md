---
title: Иаженткоммандс Voice
description: Иаженткоммандс Voice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b348904020a53eb11d2bb7884a05f8d98e223a359f796e7d891dafb3dcc402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105339"
---
# <a name="iagentcommandsgetvoice"></a>Иаженткоммандс:: Voice

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иаженткоммандс:: сетвоице**](iagentcommands--setvoice.md), [**иаженткоммандс:: oncaption**](iagentcommands--getcaption.md), [**иаженткоммандс::**](iagentcommands--getvisible.md)


 

 