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
# <a name="iagentcommandgetconfidencetext"></a><span data-ttu-id="444ff-103">Иаженткомманд:: Жетконфиденцетекст</span><span class="sxs-lookup"><span data-stu-id="444ff-103">IAgentCommand::GetConfidenceText</span></span>

<span data-ttu-id="444ff-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="444ff-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

<span data-ttu-id="444ff-105">Извлекает текст подсказки для прослушивания, ранее заданный для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="444ff-105">Retrieves the Listening Tip text previously set for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="444ff-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="444ff-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="444ff-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*пбсзтиптекст*</span><span class="sxs-lookup"><span data-stu-id="444ff-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="444ff-108">Адрес строки BSTR, которая получает значение текста подсказки прослушивания для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="444ff-108">The address of a BSTR that receives the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="444ff-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="444ff-109">See Also</span></span>

<span data-ttu-id="444ff-110">[**Иаженткомманд:: сетконфиденцесрешолд**](iagentcommand--setconfidencethreshold.md), [**Иаженткомманд:: жетконфиденцесрешолд**](iagentcommand--getconfidencethreshold.md), [**иаженткомманд:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="444ff-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 