---
title: Иаженткоммандс Сеткаптион
description: Иаженткоммандс Сеткаптион
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412822"
---
# <a name="iagentcommandssetcaption"></a><span data-ttu-id="20e85-103">Иаженткоммандс:: Сеткаптион</span><span class="sxs-lookup"><span data-stu-id="20e85-103">IAgentCommands::SetCaption</span></span>

<span data-ttu-id="20e85-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="20e85-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

<span data-ttu-id="20e85-105">Задает текст [**заголовка**](caption-property.md) , отображаемого для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="20e85-105">Sets the [**Caption**](caption-property.md) text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="20e85-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="20e85-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="20e85-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*бсзкаптион*</span><span class="sxs-lookup"><span data-stu-id="20e85-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="20e85-108">Объект BSTR, указывающий значение для свойства [**Caption**](caption-property.md) коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="20e85-108">A BSTR that specifies the value for the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

<span data-ttu-id="20e85-109">Установка свойства [**Caption**](caption-property.md) для коллекции [**команд**](/windows/desktop/lwef/the-commands-collection-object) определяет, как она будет отображаться во всплывающем меню символа, если его свойство [**Visible**](visible-property.md) имеет значение **true** , а приложение не является клиентом ввода-активного.</span><span class="sxs-lookup"><span data-stu-id="20e85-109">Setting the [**Caption**](caption-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to **True** and your application is not the input-active client.</span></span> <span data-ttu-id="20e85-110">Чтобы указать клавишу доступа (нелинованной) для **заголовка**, добавьте символ амперсанда (&) перед этим символом.</span><span class="sxs-lookup"><span data-stu-id="20e85-110">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="20e85-111">При определении команд для коллекции [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , для которой задан [**заголовок**](caption-property.md) , обычно также определяется **заголовок** для коллекции **Commands** .</span><span class="sxs-lookup"><span data-stu-id="20e85-111">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has its [**Caption**](caption-property.md) set, you typically also define a **Caption** for its **Commands** collection.</span></span>

## <a name="see-also"></a><span data-ttu-id="20e85-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="20e85-112">See Also</span></span>

<span data-ttu-id="20e85-113">[**Иаженткоммандс:: oncaption**](iagentcommands--getcaption.md), [**Иаженткоммандс:: сетвисибле**](iagentcommands--setvisible.md), [**иаженткоммандс:: сетвоице**](iagentcommands--setvoice.md)</span><span class="sxs-lookup"><span data-stu-id="20e85-113">[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)</span></span>


 

 