---
title: Иаженткомманд Сетенаблед
description: Иаженткомманд Сетенаблед
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069878"
---
# <a name="iagentcommandsetenabled"></a><span data-ttu-id="3c2de-103">Иаженткомманд:: Сетенаблед</span><span class="sxs-lookup"><span data-stu-id="3c2de-103">IAgentCommand::SetEnabled</span></span>

<span data-ttu-id="3c2de-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3c2de-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

<span data-ttu-id="3c2de-105">Задает свойство [**Enabled**](enabled-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="3c2de-105">Sets the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="3c2de-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3c2de-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3c2de-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*бенаблед*</span><span class="sxs-lookup"><span data-stu-id="3c2de-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="3c2de-108">Логическое значение, которое задает значение параметра [**включения**](enabled-property.md) [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="3c2de-108">A Boolean value that sets the value of the [**Enabled**](enabled-property.md) setting of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="3c2de-109">**Значение true** включает **команду**; **Значение false** отключает его.</span><span class="sxs-lookup"><span data-stu-id="3c2de-109">**True** enables the **Command**; **False** disables it.</span></span> <span data-ttu-id="3c2de-110">Невозможно выбрать отключенную **команду** .</span><span class="sxs-lookup"><span data-stu-id="3c2de-110">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

<span data-ttu-id="3c2de-111">Для [**команды**](/windows/desktop/lwef/the-command-object) свойство Enabled должно иметь значение **true** , чтобы быть [**доступным**](enabled-property.md) для выбора.</span><span class="sxs-lookup"><span data-stu-id="3c2de-111">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Enabled**](enabled-property.md) property set to **True** to be selectable.</span></span> <span data-ttu-id="3c2de-112">Он также должен иметь набор свойств [**Caption**](caption-property.md) , а свойство [**Visible**](visible-property.md) — значение **true** , чтобы оно отображалось во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="3c2de-112">It also must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear in the character's pop-up menu.</span></span> <span data-ttu-id="3c2de-113">Чтобы **команда** отображалась в окне " **Voice Commands**", необходимо задать ее свойство [**Voice**](voice-property.md).</span><span class="sxs-lookup"><span data-stu-id="3c2de-113">To make the **Command** appear in the **Voice Commands Window**, you must set its [**Voice**](voice-property.md)property.</span></span>

## <a name="see-also"></a><span data-ttu-id="3c2de-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="3c2de-114">See Also</span></span>

<span data-ttu-id="3c2de-115">[**Иаженткомманд::**](iagentcommand--getcaption.md)иаженткомманд, [**:: сетвоице**](iagentcommand--setvoice.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**иаженткоммандс:: INSERT**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="3c2de-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 