---
title: Иаженткоммандс Сетвисибле
description: Иаженткоммандс Сетвисибле
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105710259"
---
# <a name="iagentcommandssetvisible"></a><span data-ttu-id="212fa-103">Иаженткоммандс:: Сетвисибле</span><span class="sxs-lookup"><span data-stu-id="212fa-103">IAgentCommands::SetVisible</span></span>

<span data-ttu-id="212fa-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="212fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

<span data-ttu-id="212fa-105">Задает значение свойства [**Visible**](visible-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="212fa-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="212fa-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="212fa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="212fa-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*</span><span class="sxs-lookup"><span data-stu-id="212fa-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="212fa-108">Логическое значение, определяющее свойство [**Visible**](visible-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="212fa-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="212fa-109">**Значение true** задает отображение [**заголовка**](caption-property.md) коллекции **команд** при отображении всплывающего меню символа; *Значение false* не отображает.</span><span class="sxs-lookup"><span data-stu-id="212fa-109">**True** sets the **Commands** collection's [**Caption**](caption-property.md) to be visible when the character's pop-up menu is displayed; *False* does not display it.</span></span>

</dd> </dl>

<span data-ttu-id="212fa-110">Для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) необходимо установить свойство [**Caption**](caption-property.md) , а для свойства [**Visible**](visible-property.md) — значение **true** , чтобы оно отображалось во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="212fa-110">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span> <span data-ttu-id="212fa-111">Свойству **Visible** также должно быть присвоено значение **true** , чтобы команды в коллекции отображались, когда клиентское приложение является входным.</span><span class="sxs-lookup"><span data-stu-id="212fa-111">The **Visible** property must also be set to **True** for commands in the collection to appear when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="212fa-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="212fa-112">See Also</span></span>

<span data-ttu-id="212fa-113">[**Иаженткоммандс:: OnVisible**](iagentcommands--getvisible.md), [ **иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="212fa-113">[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md)</span></span>


 

 