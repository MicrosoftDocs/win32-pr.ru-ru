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
# <a name="iagentcommandsetconfidencethreshold"></a><span data-ttu-id="96753-103">Иаженткомманд:: Сетконфиденцесрешолд</span><span class="sxs-lookup"><span data-stu-id="96753-103">IAgentCommand::SetConfidenceThreshold</span></span>

<span data-ttu-id="96753-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96753-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

<span data-ttu-id="96753-105">Задает значение свойства [**достоверности**](confidence-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="96753-105">Sets the value of the [**Confidence**](confidence-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="96753-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="96753-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="96753-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*лконфиденце*</span><span class="sxs-lookup"><span data-stu-id="96753-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="96753-108">Значение для свойства [**достоверности**](confidence-property.md) [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="96753-108">The value for the [**Confidence**](confidence-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="96753-109">Если значение достоверность, возвращенное в [**командном**](/windows/desktop/lwef/the-command-object) событии, не превышает значение, заданное для свойства [**конфиденцесрешолд**](/windows/desktop/lwef/confidence-property) , то текст, указанный в [**Сетконфиденцетекст**](iagentcommand--setconfidencetext.md) , отображается в Tip прослушивания.</span><span class="sxs-lookup"><span data-stu-id="96753-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="96753-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="96753-110">See Also</span></span>

<span data-ttu-id="96753-111">[**Иаженткомманд:: жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md), [**Иаженткомманд:: сетконфиденцетекст**](iagentcommand--setconfidencetext.md), [**иажентусеринпут:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="96753-111">[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 