---
title: Иаженткомманд Сетенаблед
description: Иаженткомманд Сетенаблед
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069878"
---
# <a name="iagentcommandsetenabled"></a>Иаженткомманд:: Сетенаблед

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 