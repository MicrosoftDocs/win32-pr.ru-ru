---
title: Иаженткомманд
description: Иаженткомманд
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487628"
---
# <a name="iagentcommandgetenabled"></a><span data-ttu-id="6d62f-103">Иаженткомманд:: enable</span><span class="sxs-lookup"><span data-stu-id="6d62f-103">IAgentCommand::GetEnabled</span></span>

<span data-ttu-id="6d62f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6d62f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

<span data-ttu-id="6d62f-105">Извлекает значение свойства [**Enabled**](enabled-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="6d62f-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="6d62f-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6d62f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="6d62f-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*пбенаблед*</span><span class="sxs-lookup"><span data-stu-id="6d62f-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="6d62f-108">Адрес переменной, принимающей **значение true** , если [**команда**](/windows/desktop/lwef/the-command-object) включена, или **значение false** , если она отключена.</span><span class="sxs-lookup"><span data-stu-id="6d62f-108">The address of a variable that receives **True** if the [**Command**](/windows/desktop/lwef/the-command-object) is enabled, or **False** if it is disabled.</span></span> <span data-ttu-id="6d62f-109">Невозможно выбрать отключенную **команду** .</span><span class="sxs-lookup"><span data-stu-id="6d62f-109">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="6d62f-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="6d62f-110">See Also</span></span>

<span data-ttu-id="6d62f-111">[**Иаженткомманд:: сеткаптион**](iagentcommand--setcaption.md), [**Иаженткомманд:: сетвисибле**](iagentcommand--setvisible.md), [**иаженткомманд:: Сетвоице**](iagentcommand--setvoice.md), [**иаженткоммандс:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="6d62f-111">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 