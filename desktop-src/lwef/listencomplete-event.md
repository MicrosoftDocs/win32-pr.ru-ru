---
title: Событие Листенкомплете
description: Событие Листенкомплете
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dbfe0fac272b50af3f82efdc8a422bebddbf786
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411308"
---
# <a name="listencomplete-event"></a><span data-ttu-id="937ee-103">Событие Листенкомплете</span><span class="sxs-lookup"><span data-stu-id="937ee-103">ListenComplete Event</span></span>

<span data-ttu-id="937ee-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="937ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="937ee-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="937ee-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="937ee-106">Происходит при завершении режима прослушивания (распознавание речи).</span><span class="sxs-lookup"><span data-stu-id="937ee-106">Occurs when Listening mode (speech recognition) has ended.</span></span>

</dd> <dt>

<span data-ttu-id="937ee-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="937ee-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="937ee-108"> *Подагент.\ *\ *\ * листенкомплете (ByVal*\ *  *чарактерид*, **ByVal** , *Причина\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="937ee-108">**Sub** *agent.\*\*\*ListenComplete (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="937ee-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="937ee-109">Part</span></span>          | <span data-ttu-id="937ee-110">Описание</span><span class="sxs-lookup"><span data-stu-id="937ee-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="937ee-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="937ee-111">*CharacterID*</span></span> | <span data-ttu-id="937ee-112">Возвращает идентификатор прослушивающего символа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="937ee-112">Returns the ID of the listening character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="937ee-113">*Причина*</span><span class="sxs-lookup"><span data-stu-id="937ee-113">*Cause*</span></span>       | <span data-ttu-id="937ee-114">Возвращает причину завершения события как целое число, которое может быть одним из следующих: 1 режим прослушивания был отключен программным кодом.</span><span class="sxs-lookup"><span data-stu-id="937ee-114">Returns the cause of the complete event as an integer that may be one of the following: 1 Listening mode was turned off by program code.</span></span><br/> <span data-ttu-id="937ee-115">истекло время ожидания 2 режима прослушивания (включенного программным кодом).</span><span class="sxs-lookup"><span data-stu-id="937ee-115">2 Listening mode (turned on by program code) timed out.</span></span><br/> <span data-ttu-id="937ee-116">истекло время ожидания 3 режима прослушивания (включенного с помощью ключа прослушивания).</span><span class="sxs-lookup"><span data-stu-id="937ee-116">3 Listening mode (turned on by the Listening key) timed out.</span></span><br/> <span data-ttu-id="937ee-117">4 режим прослушивания отключен, так как пользователь освободил ключ прослушивания.</span><span class="sxs-lookup"><span data-stu-id="937ee-117">4 Listening mode was turned off because the user released the Listening key.</span></span><br/> <span data-ttu-id="937ee-118">5 режим прослушивания завершен, так как пользователь завершил говорить.</span><span class="sxs-lookup"><span data-stu-id="937ee-118">5 Listening mode ended because the user finished speaking.</span></span><br/> <span data-ttu-id="937ee-119">6 режим прослушивания завершен, так как клиент ввода был деактивирован.</span><span class="sxs-lookup"><span data-stu-id="937ee-119">6 Listening mode ended because the input-active client was deactivated.</span></span><br/> <span data-ttu-id="937ee-120">7 режим прослушивания завершен, так как был изменен символ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="937ee-120">7 Listening mode ended because the default character was changed.</span></span><br/> <span data-ttu-id="937ee-121">8 режим прослушивания завершен, так как пользователь отключил речевой ввод.</span><span class="sxs-lookup"><span data-stu-id="937ee-121">8 Listening mode ended because the user disabled speech input.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="937ee-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="937ee-122">Remarks</span></span>

<span data-ttu-id="937ee-123">Это событие отправляется всем клиентам, когда заканчивается время ожидания в режиме прослушивания, после освобождения пользователем ключа прослушивания, когда входной активный клиент вызывает метод [**Listen**](listen-method.md) со значением **false** или пользователь завершил говорить.</span><span class="sxs-lookup"><span data-stu-id="937ee-123">This event is sent to all clients when the Listening mode time-out ends, after the user releases the Listening key, when the input active client calls the [**Listen**](listen-method.md) method with **False**, or the user finished speaking.</span></span> <span data-ttu-id="937ee-124">С помощью этого события можно определить, когда следует возобновлять речевой вывод (звук).</span><span class="sxs-lookup"><span data-stu-id="937ee-124">You can use this event to determine when to resume character spoken (audio) output.</span></span>

<span data-ttu-id="937ee-125">Если включить режим прослушивания с помощью метода [**Listen**](listen-method.md) , а затем пользователь нажмет клавишу прослушивания, режим прослушивания сбрасывается и сохраняется до завершения тайм-аута ключа прослушивания, отменяется ключ прослушивания или пользователь завершает диктовку, в зависимости от того, что происходит позже.</span><span class="sxs-lookup"><span data-stu-id="937ee-125">If you turn on Listening mode using the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="937ee-126">В этом случае вы не получите событие **листенкомплете** , пока не завершится режим прослушивания ключа.</span><span class="sxs-lookup"><span data-stu-id="937ee-126">In this situation, you will not receive a **ListenComplete** event until the listening key's mode completes.</span></span>

<span data-ttu-id="937ee-127">Событие возвращает символ для клиентов, которые в настоящий момент загрузили этот символ.</span><span class="sxs-lookup"><span data-stu-id="937ee-127">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="937ee-128">Все остальные клиенты получают символ null (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="937ee-128">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="937ee-129">См. также:</span><span class="sxs-lookup"><span data-stu-id="937ee-129">See Also</span></span>

<span data-ttu-id="937ee-130">[**Событие листенстарт**](listenstart-event.md), [ **метод Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="937ee-130">[**ListenStart event**](listenstart-event.md), [**Listen method**](listen-method.md)</span></span>


 

 





