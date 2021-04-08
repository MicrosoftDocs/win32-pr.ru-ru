---
title: Иажентчарактерекс
description: Иажентчарактерекс
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888892"
---
# <a name="iagentcharacterexgetactive"></a><span data-ttu-id="7490e-103">Иажентчарактерекс:: onactive</span><span class="sxs-lookup"><span data-stu-id="7490e-103">IAgentCharacterEx::GetActive</span></span>

<span data-ttu-id="7490e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7490e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

<span data-ttu-id="7490e-105">Получает значение, указывающее, является ли клиентское приложение активным клиентом символа и является ли этот символ верхним.</span><span class="sxs-lookup"><span data-stu-id="7490e-105">Retrieves whether your client application is the active client of the character and whether the character is topmost.</span></span>

-   <span data-ttu-id="7490e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7490e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="7490e-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*псстате*</span><span class="sxs-lookup"><span data-stu-id="7490e-107"><span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*</span></span>
</dt> <dd>

<span data-ttu-id="7490e-108">Адрес переменной, принимающей одно из следующих значений параметра State:</span><span class="sxs-lookup"><span data-stu-id="7490e-108">Address of a variable that receives one of the following values for the state setting:</span></span>



| <span data-ttu-id="7490e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="7490e-109">Value</span></span>                                                              | <span data-ttu-id="7490e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7490e-110">Description</span></span>                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="7490e-111">**const без знака Short** **\_ ненулевое значение = 0;**</span><span class="sxs-lookup"><span data-stu-id="7490e-111">**const unsigned short** **ACTIVATE\_NOTACTIVE = 0;**</span></span><br/>   | <span data-ttu-id="7490e-112">Клиент не является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="7490e-112">Your client is not the active client of the character.</span></span>                |
| <span data-ttu-id="7490e-113">**const неподписанных коротких** **активных активаций \_ = 1;**</span><span class="sxs-lookup"><span data-stu-id="7490e-113">**const unsigned short** **ACTIVATE\_ACTIVE = 1;**</span></span><br/>      | <span data-ttu-id="7490e-114">Клиент является активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="7490e-114">Your client is the active client of the character.</span></span>                    |
| <span data-ttu-id="7490e-115">**const неподписанного короткого** **ключа \_ инпутактиве = 2;**</span><span class="sxs-lookup"><span data-stu-id="7490e-115">**const unsigned short** **ACTIVATE\_INPUTACTIVE = 2;**</span></span><br/> | <span data-ttu-id="7490e-116">Клиент имеет входные данные (активный клиент верхнего символа).</span><span class="sxs-lookup"><span data-stu-id="7490e-116">Your client is input-active (active client of the topmost character).</span></span> |



 

</dd> </dl>

<span data-ttu-id="7490e-117">Этот параметр позволяет определить, является ли вы активным клиентом символа или является ли ваш символ активным входным символом.</span><span class="sxs-lookup"><span data-stu-id="7490e-117">This setting lets you know whether you are the active client of the character or whether your character is the input active character.</span></span> <span data-ttu-id="7490e-118">Если несколько клиентских приложений совместно используют один и тот же символ, то активный клиент символа получает ввод с помощью мыши (например, элемент управления агента Microsoft Agent щелкнул или перетаскивает события).</span><span class="sxs-lookup"><span data-stu-id="7490e-118">When multiple client applications share the same character, the active client of the character receives mouse input (for example, Microsoft Agent control click or drag events).</span></span> <span data-ttu-id="7490e-119">Аналогично, когда отображается несколько символов, активный клиент самого верхнего символа (также известный как клиент ввода) получает события [**иажентнотифисинк:: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="7490e-119">Similarly, when multiple characters are displayed, the active client of the topmost character (also known as the input-active client) receives [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events.</span></span>

<span data-ttu-id="7490e-120">Используйте метод [**Activate**](iagentcharacter--activate.md) , чтобы задать, является ли ваше приложение активным клиентом символа, или сделайте так, чтобы приложение использовало входной активный клиент (который также делает символ самым верхним).</span><span class="sxs-lookup"><span data-stu-id="7490e-120">Use the [**Activate**](iagentcharacter--activate.md) method to set whether your application is the active client of the character or to make your application the input active client (which also makes the character topmost).</span></span>

## <a name="see-also"></a><span data-ttu-id="7490e-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="7490e-121">See Also</span></span>

<span data-ttu-id="7490e-122">[**Иажентчарактер:: Activate**](iagentcharacter--activate.md), [ **иажентнотифисинкекс:: активеклиентчанже**](iagentnotifysinkex--activeclientchange.md)</span><span class="sxs-lookup"><span data-stu-id="7490e-122">[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)</span></span>


 

 





