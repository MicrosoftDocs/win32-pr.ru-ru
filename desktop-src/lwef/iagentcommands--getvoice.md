---
title: Иаженткоммандс Voice
description: Иаженткоммандс Voice
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412962"
---
# <a name="iagentcommandsgetvoice"></a><span data-ttu-id="7dbf6-103">Иаженткоммандс:: Voice</span><span class="sxs-lookup"><span data-stu-id="7dbf6-103">IAgentCommands::GetVoice</span></span>

<span data-ttu-id="7dbf6-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7dbf6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

<span data-ttu-id="7dbf6-105">Возвращает значение свойства [**Voice**](voice-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="7dbf6-105">Retrieves the value of the [**Voice**](voice-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="7dbf6-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7dbf6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7dbf6-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*пбсзвоице*</span><span class="sxs-lookup"><span data-stu-id="7dbf6-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="7dbf6-108">Адрес объекта BSTR, который получает значение параметра текста [**голоса**](voice-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="7dbf6-108">The address of a BSTR that receives the value of the [**Voice**](voice-property.md) text setting for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="7dbf6-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="7dbf6-109">See Also</span></span>

<span data-ttu-id="7dbf6-110">[**Иаженткоммандс:: сетвоице**](iagentcommands--setvoice.md), [**иаженткоммандс:: oncaption**](iagentcommands--getcaption.md), [**иаженткоммандс::**](iagentcommands--getvisible.md)</span><span class="sxs-lookup"><span data-stu-id="7dbf6-110">[**IAgentCommands::SetVoice**](iagentcommands--setvoice.md), [**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::GetVisible**](iagentcommands--getvisible.md)</span></span>


 

 