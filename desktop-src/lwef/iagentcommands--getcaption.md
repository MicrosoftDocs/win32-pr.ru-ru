---
title: Иаженткоммандс субтитры
description: Иаженткоммандс субтитры
ms.assetid: bbaaaa20-c8c2-41af-a6fc-cf8849daa399
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f886413ae6bfbfe104306d7280d8c66b08bf311a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691484"
---
# <a name="iagentcommandsgetcaption"></a><span data-ttu-id="c3e3c-103">Иаженткоммандс:: oncaption</span><span class="sxs-lookup"><span data-stu-id="c3e3c-103">IAgentCommands::GetCaption</span></span>

<span data-ttu-id="c3e3c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3e3c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption text for Commands collection
);
```

<span data-ttu-id="c3e3c-105">Извлекает [**заголовок**](caption-property.md) коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c3e3c-105">Retrieves the [**Caption**](caption-property.md) for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="c3e3c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c3e3c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c3e3c-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*пбсзкаптион*</span><span class="sxs-lookup"><span data-stu-id="c3e3c-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="c3e3c-108">Адрес объекта BSTR, который получает значение параметра текста [**заголовка**](caption-property.md) , отображаемое для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c3e3c-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text setting displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c3e3c-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="c3e3c-109">See Also</span></span>

<span data-ttu-id="c3e3c-110">[**Иаженткоммандс:: сеткаптион**](iagentcommands--setcaption.md), [**иаженткоммандс::**](iagentcommands--getvisible.md), [**иаженткоммандс:: Voice**](iagentcommands--getvoice.md)</span><span class="sxs-lookup"><span data-stu-id="c3e3c-110">[**IAgentCommands::SetCaption**](iagentcommands--setcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommands::GetVoice**](iagentcommands--getvoice.md)</span></span>


 

 