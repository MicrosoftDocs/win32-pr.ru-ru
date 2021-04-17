---
title: Иаженткоммандс
description: Иаженткоммандс
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691506"
---
# <a name="iagentcommandsgetvisible"></a>Иаженткоммандс:: Visible

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

Извлекает значение свойства [**Visible**](visible-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*
</dt> <dd>

Адрес переменной, получающей значение [**видимого**](visible-property.md) свойства для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткоммандс:: сетвисибле**](iagentcommands--setvisible.md), [ **иаженткоммандс:: сеткаптион**](iagentcommands--setcaption.md)


 

 