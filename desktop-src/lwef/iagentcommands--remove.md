---
title: Иаженткоммандс удалить
description: Иаженткоммандс удалить
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104260603"
---
# <a name="iagentcommandsremove"></a><span data-ttu-id="f3df0-103">Иаженткоммандс:: Remove</span><span class="sxs-lookup"><span data-stu-id="f3df0-103">IAgentCommands::Remove</span></span>

<span data-ttu-id="f3df0-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3df0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

<span data-ttu-id="f3df0-105">Удаляет указанную [**команду**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f3df0-105">Removes the specified [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="f3df0-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f3df0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f3df0-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*двид*</span><span class="sxs-lookup"><span data-stu-id="f3df0-107"><span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*</span></span>
</dt> <dd>

<span data-ttu-id="f3df0-108">Идентификатор [**команды**](/windows/desktop/lwef/the-command-object) , удаляемой из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f3df0-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) to remove from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="f3df0-109">При удалении [**команды**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) она также удаляется из всплывающего меню и из окна " **голосовые команды** ", если приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="f3df0-109">Removing a [**Command**](/windows/desktop/lwef/the-command-object) from a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection also removes it from the pop-up menu and the **Voice Commands Window** when your application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3df0-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="f3df0-110">See Also</span></span>

<span data-ttu-id="f3df0-111">[**Иаженткоммандс:: Add**](iagentcommands--add.md), [**Иаженткоммандс:: INSERT**](iagentcommands--insert.md), [**иаженткоммандс:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="f3df0-111">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 