---
title: Листенингтип, свойство
description: Листенингтип, свойство
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691352"
---
# <a name="listeningtip-property"></a><span data-ttu-id="052a9-103">Листенингтип, свойство</span><span class="sxs-lookup"><span data-stu-id="052a9-103">ListeningTip Property</span></span>

<span data-ttu-id="052a9-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="052a9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="052a9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="052a9-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="052a9-106">Возвращает логическое значение, указывающее текущий параметр пользователя для Совета прослушивания.</span><span class="sxs-lookup"><span data-stu-id="052a9-106">Returns a Boolean indicating the current user setting for the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="052a9-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="052a9-107"><span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Syntax**</span></span> 
</dt> <dd>

<span data-ttu-id="052a9-108">*агент \* \* *. Спичинпут. Листенингтип**</span><span class="sxs-lookup"><span data-stu-id="052a9-108">*agent\*\*\*.SpeechInput.ListeningTip*\*</span></span>



| <span data-ttu-id="052a9-109">Значение</span><span class="sxs-lookup"><span data-stu-id="052a9-109">Value</span></span>     | <span data-ttu-id="052a9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="052a9-110">Description</span></span>                    |
|-----------|--------------------------------|
| <span data-ttu-id="052a9-111">**True**</span><span class="sxs-lookup"><span data-stu-id="052a9-111">**True**</span></span>  | <span data-ttu-id="052a9-112">TIP Listening включен.</span><span class="sxs-lookup"><span data-stu-id="052a9-112">The Listening Tip is enabled.</span></span>  |
| <span data-ttu-id="052a9-113">**False**</span><span class="sxs-lookup"><span data-stu-id="052a9-113">**False**</span></span> | <span data-ttu-id="052a9-114">TIP Listen отключен.</span><span class="sxs-lookup"><span data-stu-id="052a9-114">The Listening Tip is disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="052a9-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="052a9-115">Remarks</span></span>

<span data-ttu-id="052a9-116">Свойство **листенингтип** указывает, включен ли параметр TIP Listening на вкладке свойств Microsoft Agent (дополнительные параметры символов).</span><span class="sxs-lookup"><span data-stu-id="052a9-116">The **ListeningTip** property indicates whether the Display Listening Tip option in the Microsoft Agent property sheet (Advanced Character Options) is enabled.</span></span> <span data-ttu-id="052a9-117">Если **листенингтип** возвращает **true** , а речевой ввод включен, сервер отображает окно подсказки, когда пользователь нажимает клавишу прослушивания.</span><span class="sxs-lookup"><span data-stu-id="052a9-117">When **ListeningTip** returns **True** and speech input is enabled, the server displays the tip window when the user presses the Listening key.</span></span>

## <a name="see-also"></a><span data-ttu-id="052a9-118">См. также:</span><span class="sxs-lookup"><span data-stu-id="052a9-118">See Also</span></span>

[<span data-ttu-id="052a9-119">**Событие Ажентпропертичанже**</span><span class="sxs-lookup"><span data-stu-id="052a9-119">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




