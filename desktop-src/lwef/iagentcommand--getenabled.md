---
title: Иаженткомманд
description: Иаженткомманд
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7118fa06fc895729755a36872a6d092d962d2416f81ac50e5c528cf9d69f5312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477659"
---
# <a name="iagentcommandgetenabled"></a>Иаженткомманд:: enable

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md), [**Иаженткомманд:: сетвисибле**](iagentcommand--setvisible.md), [**иаженткомманд:: Сетвоице**](iagentcommand--setvoice.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)


 

 