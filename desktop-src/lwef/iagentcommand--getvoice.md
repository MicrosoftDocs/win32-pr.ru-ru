---
title: Иаженткомманд Voice
description: Иаженткомманд Voice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700847"
---
# <a name="iagentcommandgetvoice"></a>Иаженткомманд:: Voice

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Возвращает значение свойства "текст [**голоса**](voice-property.md) " для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*пбсзвоице*
</dt> <dd>

Адрес строки BSTR, которая получает свойство текста [**голоса**](voice-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

[**Команда**](/windows/desktop/lwef/the-command-object) со своим набором свойств [**Voice**](voice-property.md) и [**включенным**](enabled-property.md) свойством со значением **true** будет иметь доступ к голосовым данным. Если свойство [**Caption**](caption-property.md) также задано, оно отображается в окне "Voice Commands". Если его свойство [**Visible**](visible-property.md) имеет значение **true**, оно отображается во всплывающем меню символа.

## <a name="see-also"></a>См. также:

[**Иаженткомманд:: сетвоице**](iagentcommand--setvoice.md), [**Иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)


 

 