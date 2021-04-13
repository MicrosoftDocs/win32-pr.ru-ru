---
title: Иаженткомманд
description: Иаженткомманд
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1058c3855214dada0f1567f9fef81a3efc7e20a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412940"
---
# <a name="iagentcommandgetvisible"></a>Иаженткомманд:: Visible

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

Извлекает значение свойства [**Visible**](visible-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*
</dt> <dd>

Адрес переменной, которая получает свойство [**Visible**](visible-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткомманд:: сетвисибле**](iagentcommand--setvisible.md), [**Иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)


 

 