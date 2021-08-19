---
title: Иаженткомманд Сетенаблед
description: Иаженткомманд Сетенаблед
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da164b6603d93496e3381ccc6938a3b6d8f520bcea887cfd11f031cec7d845a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976314"
---
# <a name="iagentcommandsetenabled"></a>Иаженткомманд:: Сетенаблед

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Задает свойство [**Enabled**](enabled-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*бенаблед*
</dt> <dd>

Логическое значение, которое задает значение параметра [**включения**](enabled-property.md) [**команды**](/windows/desktop/lwef/the-command-object). **Значение true** включает **команду**; **Значение false** отключает его. Невозможно выбрать отключенную **команду** .

</dd> </dl>

Для [**команды**](/windows/desktop/lwef/the-command-object) свойство Enabled должно иметь значение **true** , чтобы быть [**доступным**](enabled-property.md) для выбора. Он также должен иметь набор свойств [**Caption**](caption-property.md) , а свойство [**Visible**](visible-property.md) — значение **true** , чтобы оно отображалось во всплывающем меню символа. Чтобы **команда** отображалась в окне " **Voice Commands**", необходимо задать ее свойство [**Voice**](voice-property.md).

## <a name="see-also"></a>См. также:

[**Иаженткомманд::**](iagentcommand--getcaption.md)иаженткомманд, [**:: сетвоице**](iagentcommand--setvoice.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)


 

 