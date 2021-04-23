---
title: Иаженткомманд Сеткаптион
description: Иаженткомманд Сеткаптион
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88453f54ffa59b413f30d27c58aa6cd2dcc6e12e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069925"
---
# <a name="iagentcommandsetcaption"></a><span data-ttu-id="4387d-103">Иаженткомманд:: Сеткаптион</span><span class="sxs-lookup"><span data-stu-id="4387d-103">IAgentCommand::SetCaption</span></span>

<span data-ttu-id="4387d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4387d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

<span data-ttu-id="4387d-105">Задает текст [**заголовка**](caption-property.md) , отображаемого для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="4387d-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="4387d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4387d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4387d-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*бсзкаптион*</span><span class="sxs-lookup"><span data-stu-id="4387d-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="4387d-108">Значение типа BSTR, указывающее текст для свойства [**Caption**](caption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="4387d-108">A BSTR that specifies the text for the [**Caption**](caption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="4387d-109">Установка свойства [**Caption**](caption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object) определяет, как она будет отображаться во всплывающем меню символа, если его свойство [**Visible**](visible-property.md) имеет значение **true** , а ваше приложение не является клиентом input-Active.</span><span class="sxs-lookup"><span data-stu-id="4387d-109">Setting the [**Caption**](caption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="4387d-110">Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.</span><span class="sxs-lookup"><span data-stu-id="4387d-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span> <span data-ttu-id="4387d-111">Чтобы сделать его доступным для выбора, его свойство [**Enabled**](enabled-property.md) должно иметь значение **true**.</span><span class="sxs-lookup"><span data-stu-id="4387d-111">To make it selectable, its [**Enabled**](enabled-property.md) property must be set to **True**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4387d-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="4387d-112">See Also</span></span>

<span data-ttu-id="4387d-113">[**Иаженткомманд::**](iagentcommand--getcaption.md)иаженткомманд, [**:: сетенаблед**](iagentcommand--setenabled.md), [**иаженткомманд:: Сетвисибле**](iagentcommand--setvisible.md), [**иаженткомманд:: сетвоице**](iagentcommand--setvoice.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="4387d-113">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 