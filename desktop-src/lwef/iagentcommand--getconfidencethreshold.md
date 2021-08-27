---
title: Иаженткомманд Жетконфиденцесрешолд
description: Иаженткомманд Жетконфиденцесрешолд
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e4297012db2118da2fe5db79dbe8e969d9b4006b4078198a0d384898fc9fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976384"
---
# <a name="iagentcommandgetconfidencethreshold"></a>Иаженткомманд:: Жетконфиденцесрешолд

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 