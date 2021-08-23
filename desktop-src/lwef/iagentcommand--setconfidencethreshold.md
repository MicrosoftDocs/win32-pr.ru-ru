---
title: Иаженткомманд Сетконфиденцесрешолд
description: Иаженткомманд Сетконфиденцесрешолд
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 244f181fb4d9e706271440797e1261fd381897e00a5a216d681e0f3984d24a6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976304"
---
# <a name="iagentcommandsetconfidencethreshold"></a>Иаженткомманд:: Сетконфиденцесрешолд

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Задает значение свойства [**достоверности**](confidence-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*лконфиденце*
</dt> <dd>

Значение для свойства [**достоверности**](confidence-property.md) [**команды**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Если значение достоверность, возвращенное в [**командном**](/windows/desktop/lwef/the-command-object) событии, не превышает значение, заданное для свойства [**конфиденцесрешолд**](/windows/desktop/lwef/confidence-property) , то текст, указанный в [**Сетконфиденцетекст**](iagentcommand--setconfidencetext.md) , отображается в Tip прослушивания.

## <a name="see-also"></a>См. также:

[**Иаженткомманд:: жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md), [**Иаженткомманд:: сетконфиденцетекст**](iagentcommand--setconfidencetext.md), [**иажентусеринпут:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 