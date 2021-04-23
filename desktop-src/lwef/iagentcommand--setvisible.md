---
title: Иаженткомманд Сетвисибле
description: Иаженткомманд Сетвисибле
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691504"
---
# <a name="iagentcommandsetvisible"></a><span data-ttu-id="07b27-103">Иаженткомманд:: Сетвисибле</span><span class="sxs-lookup"><span data-stu-id="07b27-103">IAgentCommand::SetVisible</span></span>

<span data-ttu-id="07b27-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07b27-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

<span data-ttu-id="07b27-105">Задает значение свойства [**Visible**](visible-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="07b27-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="07b27-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="07b27-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="07b27-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*</span><span class="sxs-lookup"><span data-stu-id="07b27-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="07b27-108">Логическое значение, определяющее свойство [**Visible**](visible-property.md) [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="07b27-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="07b27-109">**Значение true** показывает **команду**; **Значение false** скрывает его.</span><span class="sxs-lookup"><span data-stu-id="07b27-109">**True** shows the **Command**; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="07b27-110">Свойству [**Visible**](visible-property.md) [**команды**](/windows/desktop/lwef/the-command-object) должно быть присвоено значение **true** , а свойство [**Caption**](caption-property.md) со значением отображается во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="07b27-110">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Visible**](visible-property.md) property set to **True** and its [**Caption**](caption-property.md) property set to appear in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="07b27-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="07b27-111">See Also</span></span>

<span data-ttu-id="07b27-112">[**Иаженткомманд::**](iagentcommand--getvisible.md), [**Иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="07b27-112">[**IAgentCommand::GetVisible**](iagentcommand--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 