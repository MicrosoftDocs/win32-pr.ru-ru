---
title: Иаженткоммандс, команда
description: Иаженткоммандс, команда
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e81043bb8dbe8a6d050f226d09f03b396d0f8f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069995"
---
# <a name="iagentcommandsgetcommand"></a><span data-ttu-id="6ea91-103">Иаженткоммандс:: Command</span><span class="sxs-lookup"><span data-stu-id="6ea91-103">IAgentCommands::GetCommand</span></span>

<span data-ttu-id="6ea91-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6ea91-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

<span data-ttu-id="6ea91-105">Извлекает объект [**команды**](/windows/desktop/lwef/the-command-object) из коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="6ea91-105">Retrieves a [**Command**](/windows/desktop/lwef/the-command-object) object from the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="6ea91-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6ea91-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6ea91-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*двкоммандид*</span><span class="sxs-lookup"><span data-stu-id="6ea91-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="6ea91-108">Идентификатор объекта [**команды**](/windows/desktop/lwef/the-command-object) в коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="6ea91-108">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) object in the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="6ea91-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="6ea91-109"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="6ea91-110">Адрес интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) для объекта [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="6ea91-110">The address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6ea91-111">См. также:</span><span class="sxs-lookup"><span data-stu-id="6ea91-111">See Also</span></span>

[<span data-ttu-id="6ea91-112">**иаженткомманд**</span><span class="sxs-lookup"><span data-stu-id="6ea91-112">**IAgentCommand**</span></span>](iagentcommand.md)


 

 