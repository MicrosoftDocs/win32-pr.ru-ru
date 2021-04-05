---
title: Событие Активатеинпут
description: Событие Активатеинпут
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068493"
---
# <a name="activateinput-event"></a><span data-ttu-id="40335-103">Событие Активатеинпут</span><span class="sxs-lookup"><span data-stu-id="40335-103">ActivateInput Event</span></span>

<span data-ttu-id="40335-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="40335-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="40335-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="40335-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="40335-106">Происходит, когда клиент получает входные данные.</span><span class="sxs-lookup"><span data-stu-id="40335-106">Occurs when a client becomes input-active.</span></span>

</dd> <dt>

<span data-ttu-id="40335-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="40335-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="40335-108"> *Подагент* \_ активатеинпут **(ByVal** *чарактерид\ * *)**</span><span class="sxs-lookup"><span data-stu-id="40335-108">**Sub** *agent*\_ActivateInput **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="40335-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="40335-109">Part</span></span>          | <span data-ttu-id="40335-110">Описание</span><span class="sxs-lookup"><span data-stu-id="40335-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="40335-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="40335-111">*CharacterID*</span></span> | <span data-ttu-id="40335-112">Возвращает идентификатор символа, через который клиент получает входные данные.</span><span class="sxs-lookup"><span data-stu-id="40335-112">Returns the ID of the character through which the client becomes input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="40335-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40335-113">Remarks</span></span>

<span data-ttu-id="40335-114">Входной — активный клиент получает события мыши и речевого ввода, предоставляемые сервером.</span><span class="sxs-lookup"><span data-stu-id="40335-114">The input-active client receives mouse and speech input events supplied by the server.</span></span> <span data-ttu-id="40335-115">Сервер отправляет это событие только клиенту, который получает входные данные.</span><span class="sxs-lookup"><span data-stu-id="40335-115">The server sends this event only to the client that becomes input-active.</span></span>

<span data-ttu-id="40335-116">Это событие может произойти, если пользователь переключается на объект [команды](the-command-object.md) , например, выбрав запись объекта команды в окне команды или во всплывающем меню для символа.</span><span class="sxs-lookup"><span data-stu-id="40335-116">This event can occur when the user switches to your [Command](the-command-object.md) object, for example, by choosing your Command object entry in the Commands Window or in the pop-up menu for a character.</span></span> <span data-ttu-id="40335-117">Это также может произойти, когда пользователь выбирает символ (щелчком мыши или говорите его именем), когда символ отображается и когда символ другого клиентского приложения станет скрытым.</span><span class="sxs-lookup"><span data-stu-id="40335-117">It can also occur when the user selects a character (by clicking or speaking its name), when a character becomes visible, and when the character of another client application becomes hidden.</span></span> <span data-ttu-id="40335-118">Можно также вызвать [метод Activate](activate-method.md) (с **состоянием** , равным 2), чтобы явно сделать символ самым верхним, что приведет к тому, что клиентское приложение станет активным входным и активирует это событие.</span><span class="sxs-lookup"><span data-stu-id="40335-118">You can also call the [Activate Method](activate-method.md) (with **State** set to 2) to explicitly make the character topmost, which results in your client application becoming input-active and triggers this event.</span></span> <span data-ttu-id="40335-119">Однако это событие не происходит при использовании метода Activate только для указания того, является ли клиент активным клиентом символа.</span><span class="sxs-lookup"><span data-stu-id="40335-119">However, this event does not occur if you use the Activate Method method only to specify whether your client is the active client of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="40335-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="40335-120">See Also</span></span>

<span data-ttu-id="40335-121">[Событие **деактиватеинпут**](deactivateinput-event.md), [метод **Activate**](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="40335-121">[**DeactivateInput** event](deactivateinput-event.md), [**Activate** method](activate-method.md)</span></span>


 

 




