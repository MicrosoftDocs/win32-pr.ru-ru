---
title: Иаженткомманд Жетконфиденцесрешолд
description: Иаженткомманд Жетконфиденцесрешолд
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6557ad4e6831734106ee2c2e8021f923ef8806
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790609"
---
# <a name="iagentcommandgetconfidencethreshold"></a>Иаженткомманд:: Жетконфиденцесрешолд

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

Возвращает значение свойства [**конфиденцесрешолд**](/windows/desktop/lwef/confidence-property) для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*плконфиденцесрешолд*
</dt> <dd>

Адрес переменной, получающей значение свойства [**конфиденцесрешолд**](/windows/desktop/lwef/confidence-property) для команды.

</dd> </dl>

## <a name="see-also"></a>См. также:

[**Иаженткомманд:: сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md), [**Иаженткомманд:: сетконфиденцетекст**](iagentcommand--setconfidencetext.md), [**иажентусеринпут:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 