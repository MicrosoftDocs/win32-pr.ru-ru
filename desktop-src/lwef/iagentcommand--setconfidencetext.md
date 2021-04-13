---
title: Иаженткомманд Сетконфиденцетекст
description: Иаженткомманд Сетконфиденцетекст
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cff1ae34c03f8ff67da61bea1834c25d6844ab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412800"
---
# <a name="iagentcommandsetconfidencetext"></a>Иаженткомманд:: Сетконфиденцетекст

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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

## <a name="see-also"></a>См. также:

[**Иаженткомманд:: сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md), [**Иаженткомманд:: жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md), [**иаженткомманд:: GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 