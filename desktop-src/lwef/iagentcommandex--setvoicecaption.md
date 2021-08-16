---
title: Иаженткоммандекс Сетвоицекаптион
description: Иаженткоммандекс Сетвоицекаптион
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe76edb17c2b099db5e16e2b6160703c6b11e8a9f52bcbc24a9ca4bfcb7077c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477217"
---
# <a name="iagentcommandexsetvoicecaption"></a>Иаженткоммандекс:: Сетвоицекаптион

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Задает текст [**воицекаптион**](voicecaption-property.md) , отображаемый для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*бсзвоицекаптион*
</dt> <dd>

Значение типа BSTR, указывающее текст для свойства [**воицекаптион**](voicecaption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Если вы определяете объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) и устанавливаете его свойство [**Voice**](voice-property.md) , обычно также устанавливается свойство [**воицекаптион**](voicecaption-property.md) . Этот текст будет отображаться в окне "Voice Commands", если клиентское приложение является активным. Если это свойство не задано, параметр для свойства [**Caption**](caption-property.md) определяет отображаемый текст. Если ни одно свойство **воицекаптион** или не задано, команда не отображается в окне "Voice Commands".

[**Caption**](caption-property.md)

## <a name="see-also"></a>См. также

[**Иаженткомманд::**](iagentcommand--getcaption.md)иаженткомманд, [**:: сетенаблед**](iagentcommand--setenabled.md), [**иаженткомманд:: Сетвисибле**](iagentcommand--setvisible.md), [**иаженткомманд:: сетвоице**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)


 

 