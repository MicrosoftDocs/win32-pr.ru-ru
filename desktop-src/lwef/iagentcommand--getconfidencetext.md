---
title: Иаженткомманд Жетконфиденцетекст
description: Иаженткомманд Жетконфиденцетекст
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d1d5894a04eeb09289e98db42362acbc43d587e5ac680b98276260ba9c323b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961934"
---
# <a name="iagentcommandgetconfidencetext"></a>Иаженткомманд:: Жетконфиденцетекст

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также

[**Иаженткомманд:: сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md), [**Иаженткомманд:: жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md), [**иаженткомманд:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 