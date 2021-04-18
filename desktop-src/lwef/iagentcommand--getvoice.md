---
title: Иаженткомманд Voice
description: Иаженткомманд Voice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105700847"
---
# <a name="iagentcommandgetvoice"></a><span data-ttu-id="57b8e-103">Иаженткомманд:: Voice</span><span class="sxs-lookup"><span data-stu-id="57b8e-103">IAgentCommand::GetVoice</span></span>

<span data-ttu-id="57b8e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="57b8e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

<span data-ttu-id="57b8e-105">Возвращает значение свойства "текст [**голоса**](voice-property.md) " для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="57b8e-105">Retrieves the value of the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="57b8e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="57b8e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="57b8e-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*пбсзвоице*</span><span class="sxs-lookup"><span data-stu-id="57b8e-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="57b8e-108">Адрес строки BSTR, которая получает свойство текста [**голоса**](voice-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="57b8e-108">The address of a BSTR that receives the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="57b8e-109">[**Команда**](/windows/desktop/lwef/the-command-object) со своим набором свойств [**Voice**](voice-property.md) и [**включенным**](enabled-property.md) свойством со значением **true** будет иметь доступ к голосовым данным.</span><span class="sxs-lookup"><span data-stu-id="57b8e-109">A [**Command**](/windows/desktop/lwef/the-command-object) with its [**Voice**](voice-property.md) property set and its [**Enabled**](enabled-property.md) property set to **True** will be voice-accessible.</span></span> <span data-ttu-id="57b8e-110">Если свойство [**Caption**](caption-property.md) также задано, оно отображается в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="57b8e-110">If its [**Caption**](caption-property.md) property is also set it appears in the Voice Commands Window.</span></span> <span data-ttu-id="57b8e-111">Если его свойство [**Visible**](visible-property.md) имеет значение **true**, оно отображается во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="57b8e-111">If its [**Visible**](visible-property.md) property is set to **True**, it appears in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="57b8e-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="57b8e-112">See Also</span></span>

<span data-ttu-id="57b8e-113">[**Иаженткомманд:: сетвоице**](iagentcommand--setvoice.md), [**Иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="57b8e-113">[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 