---
title: Иаженткомманд Сеткаптион
description: Иаженткомманд Сеткаптион
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88453f54ffa59b413f30d27c58aa6cd2dcc6e12e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069925"
---
# <a name="iagentcommandsetcaption"></a>Иаженткомманд:: Сеткаптион

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Задает текст [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*бсзкаптион*
</dt> <dd>

Значение типа BSTR, указывающее текст для свойства [**Caption**](caption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Установка свойства [**Caption**](caption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object) определяет, как она будет отображаться во всплывающем меню символа, если его свойство [**Visible**](visible-property.md) имеет значение **true** , а ваше приложение не является клиентом input-Active. Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом. Чтобы сделать его доступным для выбора, его свойство [**Enabled**](enabled-property.md) должно иметь значение **true**.

## <a name="see-also"></a>См. также:

[**Иаженткомманд::**](iagentcommand--getcaption.md)иаженткомманд, [**:: сетенаблед**](iagentcommand--setenabled.md), [**иаженткомманд:: Сетвисибле**](iagentcommand--setvisible.md), [**иаженткомманд:: сетвоице**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)


 

 