---
title: Событие Листенстарт
description: Событие Листенстарт
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889024"
---
# <a name="listenstart-event"></a><span data-ttu-id="ef14f-103">Событие Листенстарт</span><span class="sxs-lookup"><span data-stu-id="ef14f-103">ListenStart Event</span></span>

<span data-ttu-id="ef14f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef14f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ef14f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="ef14f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ef14f-106">Происходит при запуске режима прослушивания (распознавание речи).</span><span class="sxs-lookup"><span data-stu-id="ef14f-106">Occurs when Listening mode (speech recognition) begins.</span></span>

</dd> <dt>

<span data-ttu-id="ef14f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="ef14f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ef14f-108"> *Подагент.\ *\ *\ * листенстарт (ByVal*\ *  *чарактерид\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="ef14f-108">**Sub** *agent.\*\*\*ListenStart (ByVal*\* *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="ef14f-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="ef14f-109">Part</span></span>          | <span data-ttu-id="ef14f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ef14f-110">Description</span></span>                                            |
|---------------|--------------------------------------------------------|
| <span data-ttu-id="ef14f-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="ef14f-111">*CharacterID*</span></span> | <span data-ttu-id="ef14f-112">Возвращает идентификатор прослушивающего символа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="ef14f-112">Returns the ID of the listening character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="ef14f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef14f-113">Remarks</span></span>

<span data-ttu-id="ef14f-114">Это событие отправляется всем клиентам, когда запускается режим прослушивания, так как пользователь нажал на ключ прослушивания или клиент ввода-клиента, который называется методом [**Listen**](listen-method.md) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="ef14f-114">This event is sent to all clients when Listening mode begins because the user pressed the Listening key or the input-active client called the [**Listen**](listen-method.md) method with **True**.</span></span> <span data-ttu-id="ef14f-115">Это событие можно использовать, чтобы избежать диктовки символа при включенном режиме прослушивания.</span><span class="sxs-lookup"><span data-stu-id="ef14f-115">You can use this event to avoid having your character speak while the Listening mode is on.</span></span>

<span data-ttu-id="ef14f-116">Если включить режим прослушивания с помощью метода [**Listen**](listen-method.md) , а затем пользователь нажмет клавишу прослушивания, режим прослушивания сбрасывается и продолжит работу до завершения времени ожидания ключа прослушивания, отпускания клавишу прослушивания, или пользователь завершает говорить, в зависимости от того, что происходит позже.</span><span class="sxs-lookup"><span data-stu-id="ef14f-116">If you turn on Listening mode with the [**Listen**](listen-method.md) method and then the user presses the Listening key, the Listening mode resets and continues until the Listening key time-out completes, the Listening key is released, or the user finishes speaking, whichever is later.</span></span> <span data-ttu-id="ef14f-117">В этом случае, когда режим прослушивания уже включен, вы не получаете дополнительное событие **листенстарт** , когда пользователь нажимает клавишу прослушивания.</span><span class="sxs-lookup"><span data-stu-id="ef14f-117">In this situation, when Listening mode is already on, you will not get an additional **ListenStart** event when the user presses the Listening key.</span></span>

<span data-ttu-id="ef14f-118">Событие возвращает символ для клиентов, которые в настоящий момент загрузили этот символ.</span><span class="sxs-lookup"><span data-stu-id="ef14f-118">The event returns the character to the clients that currently have this character loaded.</span></span> <span data-ttu-id="ef14f-119">Все остальные клиенты получают символ null (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="ef14f-119">All other clients receive a null character (empty string).</span></span>

### <a name="see-also"></a><span data-ttu-id="ef14f-120">См. также:</span><span class="sxs-lookup"><span data-stu-id="ef14f-120">See Also</span></span>

<span data-ttu-id="ef14f-121">[**Событие листенкомплете**](listencomplete-event.md), [ **метод Listen**](listen-method.md)</span><span class="sxs-lookup"><span data-stu-id="ef14f-121">[**ListenComplete event**](listencomplete-event.md), [**Listen method**](listen-method.md)</span></span>


 

 




