---
title: Иаженткомманд
description: Иаженткомманд
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487628"
---
# <a name="iagentcommandgetenabled"></a>Иаженткомманд:: enable

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

Извлекает значение свойства [**Enabled**](enabled-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*
</dt> <dd>

Адрес переменной, принимающей **значение true** , если [**команда**](/windows/desktop/lwef/the-command-object) включена, или **значение false** , если она отключена. Невозможно выбрать отключенную **команду** .

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md), [**Иаженткомманд:: сетвисибле**](iagentcommand--setvisible.md), [**иаженткомманд:: Сетвоице**](iagentcommand--setvoice.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)


 

 