---
title: Иаженткоммандсекс Аддекс
description: Иаженткоммандсекс Аддекс
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790602"
---
# <a name="iagentcommandsexaddex"></a><span data-ttu-id="bc8f1-103">Иаженткоммандсекс:: Аддекс</span><span class="sxs-lookup"><span data-stu-id="bc8f1-103">IAgentCommandsEx::AddEx</span></span>

<span data-ttu-id="bc8f1-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bc8f1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

<span data-ttu-id="bc8f1-105">Добавляет [**команду**](/windows/desktop/lwef/the-command-object) в коллекцию [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bc8f1-105">Adds a [**Command**](/windows/desktop/lwef/the-command-object) to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="bc8f1-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bc8f1-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*бсзкаптион*</span><span class="sxs-lookup"><span data-stu-id="bc8f1-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="bc8f1-108">Объект BSTR, указывающий значение текста [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bc8f1-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="bc8f1-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*бсзвоице*</span><span class="sxs-lookup"><span data-stu-id="bc8f1-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="bc8f1-110">Объект BSTR, указывающий значение параметра текста [**голоса**](voice-property.md) для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bc8f1-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="bc8f1-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*бсзвоицекаптион*</span><span class="sxs-lookup"><span data-stu-id="bc8f1-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="bc8f1-112">Объект BSTR, указывающий значение [**воицекаптион**](voicecaption-property.md) текста, отображаемого для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bc8f1-112">A BSTR that specifies the value of the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="bc8f1-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*бенаблед*</span><span class="sxs-lookup"><span data-stu-id="bc8f1-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="bc8f1-114">Логическое выражение, задающее параметр [**Enabled**](enabled-property.md) для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bc8f1-114">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="bc8f1-115">Если параметр имеет **значение true**, **команда** включена и может быть выбрана. Если задано **значение false**, **команда** отключена.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-115">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="bc8f1-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*</span><span class="sxs-lookup"><span data-stu-id="bc8f1-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="bc8f1-117">Логическое выражение, указывающее [**видимый**](visible-property.md) параметр для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="bc8f1-117">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="bc8f1-118">Если параметр имеет **значение true**, **команда** будет видна во всплывающем меню символа (если также задано свойство [**Caption**](caption-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="bc8f1-118">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="bc8f1-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*улхелпид*</span><span class="sxs-lookup"><span data-stu-id="bc8f1-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="bc8f1-120">Контекстный номер раздела справки, связанного с объектом [**Command**](/windows/desktop/lwef/the-command-object) ; используется для предоставления контекстной справки для команды.</span><span class="sxs-lookup"><span data-stu-id="bc8f1-120">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> <dt>

<span data-ttu-id="bc8f1-121"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*пдвид*</span><span class="sxs-lookup"><span data-stu-id="bc8f1-121"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="bc8f1-122">Адрес переменной, которая получает идентификатор для добавленной [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="bc8f1-122">Address of a variable that receives the ID for the added [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="bc8f1-123">[**Иаженткоммандсекс:: аддекс**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) расширяет [**Иаженткоммандс:: Add**](iagentcommands--add.md) , включая свойство [**хелпконтекстид**](helpcontextid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="bc8f1-123">[**IAgentCommandsEx::AddEx**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) extends [**IAgentCommands::Add**](iagentcommands--add.md) by including the [**HelpContextID**](helpcontextid-property.md) property.</span></span> <span data-ttu-id="bc8f1-124">Свойство также можно задать с помощью [ **иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="bc8f1-124">You can also set the property using [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="bc8f1-125">См. также:</span><span class="sxs-lookup"><span data-stu-id="bc8f1-125">See Also</span></span>

<span data-ttu-id="bc8f1-126">[**Иаженткоммандс:: Add**](iagentcommands--add.md), [**Иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md), [**иаженткомманд:: Сеткаптион**](iagentcommand--setcaption.md), [**иаженткомманд:: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand:: SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="bc8f1-126">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 