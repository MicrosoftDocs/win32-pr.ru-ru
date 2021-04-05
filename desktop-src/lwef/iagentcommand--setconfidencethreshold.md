---
title: Иаженткомманд Сетконфиденцесрешолд
description: Иаженткомманд Сетконфиденцесрешолд
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a6ba352f9385c57d0f3d1f01070f4b46e147d3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133850"
---
# <a name="iagentcommandsetconfidencethreshold"></a>Иаженткомманд:: Сетконфиденцесрешолд

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 