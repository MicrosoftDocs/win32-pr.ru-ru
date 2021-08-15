---
title: Иаженткомманд Сетконфиденцетекст
description: Иаженткомманд Сетконфиденцетекст
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8889c8c8c52f392a368c38a91510e112adbeeca42c611cdc0adcadad94f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976344"
---
# <a name="iagentcommandsetconfidencetext"></a>Иаженткомманд:: Сетконфиденцетекст

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

Задает значение текста подсказки прослушивания для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*бсзтиптекст*
</dt> <dd>

Значение типа BSTR, указывающее текст для свойства [**Конфиденцетекст**](confidencetext-property.md) [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Если значение достоверность, возвращенное в [**командном**](/windows/desktop/lwef/the-command-object) событии, не превышает значение, заданное для свойства [**конфиденцесрешолд**](/windows/desktop/lwef/confidence-property) , то текст, указанный в *Бсзтиптекст* , отображается в Tip прослушивания.

## <a name="see-also"></a>См. также

[**Иаженткомманд:: сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md), [**Иаженткомманд:: жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md), [**иаженткомманд:: GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 