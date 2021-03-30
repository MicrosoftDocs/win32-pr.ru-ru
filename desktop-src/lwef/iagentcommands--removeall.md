---
title: Иаженткоммандс RemoveAll
description: Иаженткоммандс RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791430"
---
# <a name="iagentcommandsremoveall"></a><span data-ttu-id="410b5-103">Иаженткоммандс:: RemoveAll</span><span class="sxs-lookup"><span data-stu-id="410b5-103">IAgentCommands::RemoveAll</span></span>

<span data-ttu-id="410b5-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="410b5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove();
```

<span data-ttu-id="410b5-105">Удаляет все [**команды**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="410b5-105">Removes all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="410b5-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="410b5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="410b5-107">Удаление всех [**команд**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) также приводит к их удалению из всплывающего меню и **окна «Voice Commands»** , если приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="410b5-107">Removing all [**Commands**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes them from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span> <span data-ttu-id="410b5-108">**RemoveAll** не удаляет записи сервера или другого клиента.</span><span class="sxs-lookup"><span data-stu-id="410b5-108">**RemoveAll** does not remove server or other client's entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="410b5-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="410b5-109">See Also</span></span>

<span data-ttu-id="410b5-110">[**Иаженткоммандс:: Add**](iagentcommands--add.md), [**Иаженткоммандс:: INSERT**](iagentcommands--insert.md), [**иаженткоммандс:: Remove**](iagentcommands--remove.md)</span><span class="sxs-lookup"><span data-stu-id="410b5-110">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md)</span></span>


 

 