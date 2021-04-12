---
title: Иаженткоммандекс Жетвоицекаптион
description: Иаженткоммандекс Жетвоицекаптион
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f367a7956d1029eae47064a0778264e3b77f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336937"
---
# <a name="iagentcommandexgetvoicecaption"></a>Иаженткоммандекс:: Жетвоицекаптион

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Возвращает [**воицекаптион**](voicecaption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*пбсзвоицекаптион*
</dt> <dd>

Адрес строки BSTR, которая получает значение текста [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

[**Воицекаптион**](voicecaption-property.md) — это текст, отображаемый для [**командного**](/windows/desktop/lwef/the-command-object) объекта в окне "голосовые команды", если клиентское приложение является входным.

## <a name="see-also"></a>См. также:

[**Иаженткоммандекс:: сетвоицекаптион**](iagentcommandex--setvoicecaption.md), [**Иаженткомманд:: сетенаблед**](iagentcommand--setenabled.md), [**иаженткомманд:: Сетвисибле**](iagentcommand--setvisible.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)


 

 