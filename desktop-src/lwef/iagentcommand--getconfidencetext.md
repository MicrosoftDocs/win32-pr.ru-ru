---
title: Иаженткомманд Жетконфиденцетекст
description: Иаженткомманд Жетконфиденцетекст
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987dca39016a20d185fbd4b8fd2b554c8bec02f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336841"
---
# <a name="iagentcommandgetconfidencetext"></a>Иаженткомманд:: Жетконфиденцетекст

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

Извлекает текст подсказки для прослушивания, ранее заданный для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*пбсзтиптекст*
</dt> <dd>

Адрес строки BSTR, которая получает значение текста подсказки прослушивания для [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткомманд:: сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md), [**Иаженткомманд:: жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md), [**иаженткомманд:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 