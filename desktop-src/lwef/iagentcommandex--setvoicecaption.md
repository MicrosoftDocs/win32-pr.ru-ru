---
title: Иаженткоммандекс Сетвоицекаптион
description: Иаженткоммандекс Сетвоицекаптион
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069838"
---
# <a name="iagentcommandexsetvoicecaption"></a><span data-ttu-id="793ac-103">Иаженткоммандекс:: Сетвоицекаптион</span><span class="sxs-lookup"><span data-stu-id="793ac-103">IAgentCommandEx::SetVoiceCaption</span></span>

<span data-ttu-id="793ac-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="793ac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="793ac-105">Задает текст [**воицекаптион**](voicecaption-property.md) , отображаемый для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="793ac-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="793ac-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="793ac-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="793ac-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*бсзвоицекаптион*</span><span class="sxs-lookup"><span data-stu-id="793ac-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="793ac-108">Значение типа BSTR, указывающее текст для свойства [**воицекаптион**](voicecaption-property.md) для [**команды**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="793ac-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="793ac-109">Если вы определяете объект [**Command**](/windows/desktop/lwef/the-command-object) в коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) и устанавливаете его свойство [**Voice**](voice-property.md) , обычно также устанавливается свойство [**воицекаптион**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="793ac-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="793ac-110">Этот текст будет отображаться в окне "Voice Commands", если клиентское приложение является активным.</span><span class="sxs-lookup"><span data-stu-id="793ac-110">This text will appear in the Voice Commands Window when your client application is input active.</span></span> <span data-ttu-id="793ac-111">Если это свойство не задано, параметр для свойства [**Caption**](caption-property.md) определяет отображаемый текст.</span><span class="sxs-lookup"><span data-stu-id="793ac-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="793ac-112">Если ни одно свойство **воицекаптион** или не задано, команда не отображается в окне "Voice Commands".</span><span class="sxs-lookup"><span data-stu-id="793ac-112">When neither the **VoiceCaption** or property is set, the command does not appear in the Voice Commands Window.</span></span>

[<span data-ttu-id="793ac-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="793ac-113">**Caption**</span></span>](caption-property.md)

## <a name="see-also"></a><span data-ttu-id="793ac-114">См. также:</span><span class="sxs-lookup"><span data-stu-id="793ac-114">See Also</span></span>

<span data-ttu-id="793ac-115">[**Иаженткомманд::**](iagentcommand--getcaption.md)иаженткомманд, [**:: сетенаблед**](iagentcommand--setenabled.md), [**иаженткомманд:: Сетвисибле**](iagentcommand--setvisible.md), [**иаженткомманд:: сетвоице**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: INSERT**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="793ac-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 