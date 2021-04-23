---
title: Иаженткоммандс
description: Иаженткоммандс
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691506"
---
# <a name="iagentcommandsgetvisible"></a><span data-ttu-id="bd81c-103">Иаженткоммандс:: Visible</span><span class="sxs-lookup"><span data-stu-id="bd81c-103">IAgentCommands::GetVisible</span></span>

<span data-ttu-id="bd81c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bd81c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

<span data-ttu-id="bd81c-105">Извлекает значение свойства [**Visible**](visible-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bd81c-105">Retrieves the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="bd81c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bd81c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bd81c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*пбвисибле*</span><span class="sxs-lookup"><span data-stu-id="bd81c-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="bd81c-108">Адрес переменной, получающей значение [**видимого**](visible-property.md) свойства для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bd81c-108">The address of a variable that receives the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="bd81c-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="bd81c-109">See Also</span></span>

<span data-ttu-id="bd81c-110">[**Иаженткоммандс:: сетвисибле**](iagentcommands--setvisible.md), [ **иаженткоммандс:: сеткаптион**](iagentcommands--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="bd81c-110">[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md)</span></span>


 

 