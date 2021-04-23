---
title: Иаженткоммандсекс Инсертекс
description: Иаженткоммандсекс Инсертекс
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d59b504cfa475c3ac63888796d7df8d800bfd72
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069921"
---
# <a name="iagentcommandsexinsertex"></a><span data-ttu-id="c62e2-103">Иаженткоммандсекс:: Инсертекс</span><span class="sxs-lookup"><span data-stu-id="c62e2-103">IAgentCommandsEx::InsertEx</span></span>

<span data-ttu-id="c62e2-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c62e2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

<span data-ttu-id="c62e2-105">Вставляет объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекцию [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c62e2-105">Inserts a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="c62e2-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c62e2-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c62e2-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*бсзкаптион*</span><span class="sxs-lookup"><span data-stu-id="c62e2-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-108">Объект BSTR, указывающий значение текста [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c62e2-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*бсзвоице*</span><span class="sxs-lookup"><span data-stu-id="c62e2-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-110">Объект BSTR, указывающий значение параметра текста [**голоса**](voice-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c62e2-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*бсзвоицекаптион*</span><span class="sxs-lookup"><span data-stu-id="c62e2-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-112">Объект BSTR, указывающий значение [**воицекаптион**](voicecaption-property.md) текста, отображаемого для [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c62e2-112">A BSTR that specifies the value of the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*бенаблед*</span><span class="sxs-lookup"><span data-stu-id="c62e2-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-114">Логическое выражение, задающее параметр [**Enabled**](enabled-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c62e2-114">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="c62e2-115">Если параметр имеет **значение true**, **команда** включена и может быть выбрана. Если задано **значение false**, **команда** отключена.</span><span class="sxs-lookup"><span data-stu-id="c62e2-115">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*</span><span class="sxs-lookup"><span data-stu-id="c62e2-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-117">Логическое выражение, указывающее [**видимый**](visible-property.md) параметр для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c62e2-117">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="c62e2-118">Если параметр имеет **значение true**, **команда** будет видна во всплывающем меню символа (если также задано свойство [**Caption**](caption-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="c62e2-118">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*улхелпид*</span><span class="sxs-lookup"><span data-stu-id="c62e2-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-120">Контекстный номер раздела справки, связанного с объектом [**Command**](/windows/desktop/lwef/the-command-object) ; используется для предоставления контекстной справки для команды.</span><span class="sxs-lookup"><span data-stu-id="c62e2-120">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*дврефид*</span><span class="sxs-lookup"><span data-stu-id="c62e2-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-122">Идентификатор [**команды**](/windows/desktop/lwef/the-command-object) , используемой в качестве ссылки относительной вставки новой **команды**.</span><span class="sxs-lookup"><span data-stu-id="c62e2-122">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) used as a reference for the relative insertion of the new **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*дбефоре*</span><span class="sxs-lookup"><span data-stu-id="c62e2-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span></span>
</dt> <dd>

<span data-ttu-id="c62e2-124">Логическое выражение, указывающее место размещения [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c62e2-124">A Boolean expression that specifies where to place the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="c62e2-125">Если этот параметр имеет **значение true**, то новая **команда** вставляется перед указанной **командой**. Если **значение равно false**, то новая **команда** помещается после указанной **команды**.</span><span class="sxs-lookup"><span data-stu-id="c62e2-125">If this parameter is **True**, the new **Command** is inserted before the referenced **Command**; if **False**, the new **Command** is placed after the referenced **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="c62e2-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*пдвид*</span><span class="sxs-lookup"><span data-stu-id="c62e2-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="c62e2-127">Адрес переменной, которая получает идентификатор для вставленной [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c62e2-127">Address of a variable that receives the ID for the inserted [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="c62e2-128">[**Иаженткоммандсекс:: инсертекс**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) расширяет [**Иаженткоммандс:: INSERT**](iagentcommands--insert.md) , включая свойство [**хелпконтекстид**](helpcontextid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c62e2-128">[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) extends [**IAgentCommands::Insert**](iagentcommands--insert.md) by including the [**HelpContextID**](helpcontextid-property.md) property.</span></span> <span data-ttu-id="c62e2-129">Свойство также можно задать с помощью [ **иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="c62e2-129">You can also set the property using [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="c62e2-130">См. также:</span><span class="sxs-lookup"><span data-stu-id="c62e2-130">See Also</span></span>

<span data-ttu-id="c62e2-131">[**Иаженткоммандсекс:: аддекс**](iagentcommandsex--addex.md), [**Иаженткоммандсекс:: сеселпконтекстид**](iagentcommandsex--sethelpcontextid.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="c62e2-131">[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 