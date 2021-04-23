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
# <a name="iagentcommandgetconfidencethreshold"></a><span data-ttu-id="d35c8-103">Иаженткомманд:: Жетконфиденцесрешолд</span><span class="sxs-lookup"><span data-stu-id="d35c8-103">IAgentCommand::GetConfidenceThreshold</span></span>

<span data-ttu-id="d35c8-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d35c8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

<span data-ttu-id="d35c8-105">Возвращает значение свойства [**конфиденцесрешолд**](/windows/desktop/lwef/confidence-property) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="d35c8-105">Retrieves the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="d35c8-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d35c8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d35c8-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*плконфиденцесрешолд*</span><span class="sxs-lookup"><span data-stu-id="d35c8-107"><span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*</span></span>
</dt> <dd>

<span data-ttu-id="d35c8-108">Адрес переменной, получающей значение свойства [**конфиденцесрешолд**](/windows/desktop/lwef/confidence-property) для команды.</span><span class="sxs-lookup"><span data-stu-id="d35c8-108">The address of a variable that receives the value of the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property for a Command.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d35c8-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="d35c8-109">See Also</span></span>

<span data-ttu-id="d35c8-110">[**Иаженткомманд:: сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md), [**Иаженткомманд:: сетконфиденцетекст**](iagentcommand--setconfidencetext.md), [**иажентусеринпут:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="d35c8-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 