---
title: Событие Хелпкомплете
description: Событие Хелпкомплете
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105691499"
---
# <a name="helpcomplete-event"></a><span data-ttu-id="9205f-103">Событие Хелпкомплете</span><span class="sxs-lookup"><span data-stu-id="9205f-103">HelpComplete Event</span></span>

<span data-ttu-id="9205f-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9205f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9205f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="9205f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9205f-106">Указывает, что контекстно-зависимый режим справки был завершен.</span><span class="sxs-lookup"><span data-stu-id="9205f-106">Indicates that context-sensitive Help mode has been exited.</span></span>

</dd> <dt>

<span data-ttu-id="9205f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="9205f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9205f-108"> *Подагент.\ *\ *\ * (ByVal*\ * \ *чарактерид\ *\ * *, ByVal*\ * \ *Name\ *\ * *, ByVal,*\ *  *Причина\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="9205f-108">**Sub** *agent.\*\*\*(ByVal*\* *CharacterID\*\*\*, ByVal*\* *Name\*\*\*, ByVal*\* *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="9205f-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="9205f-109">Part</span></span>          | <span data-ttu-id="9205f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9205f-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9205f-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="9205f-111">*CharacterID*</span></span> | <span data-ttu-id="9205f-112">Возвращает идентификатор нажатого символа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="9205f-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9205f-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="9205f-113">*Name*</span></span>        | <span data-ttu-id="9205f-114">Возвращает строковое значение, идентифицирующее имя (идентификатор) команды.</span><span class="sxs-lookup"><span data-stu-id="9205f-114">Returns a string value identifying the name (ID) of the command.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="9205f-115">*Причина*</span><span class="sxs-lookup"><span data-stu-id="9205f-115">*Cause*</span></span>       | <span data-ttu-id="9205f-116">Возвращает значение, указывающее, что привело к завершению режима справки.</span><span class="sxs-lookup"><span data-stu-id="9205f-116">Returns a value that indicates what caused the Help mode to complete.</span></span> <span data-ttu-id="9205f-117">1 пользователь выбрал команду, предоставленную вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="9205f-117">1 The user selected a command supplied by your application.</span></span><br/> <span data-ttu-id="9205f-118">2 пользователь выбрал объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) другого клиента.</span><span class="sxs-lookup"><span data-stu-id="9205f-118">2 The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span><br/> <span data-ttu-id="9205f-119">3 пользователь выбрал команду "открыть голосовое меню".</span><span class="sxs-lookup"><span data-stu-id="9205f-119">3 The user selected the Open Voice Commands command.</span></span><br/> <span data-ttu-id="9205f-120">4 пользователь выбрал команду "закрыть голосовое меню".</span><span class="sxs-lookup"><span data-stu-id="9205f-120">4 The user selected the Close Voice Commands command.</span></span><br/> <span data-ttu-id="9205f-121">5 пользователь выбрал команду "показывать *чарактернаме* ".</span><span class="sxs-lookup"><span data-stu-id="9205f-121">5 The user selected the Show *CharacterName* command.</span></span><br/> <span data-ttu-id="9205f-122">6 пользователь выбрал команду Скрыть *чарактернаме* .</span><span class="sxs-lookup"><span data-stu-id="9205f-122">6 The user selected the Hide *CharacterName* command.</span></span><br/> <span data-ttu-id="9205f-123">7 пользователь выбрал (щелкнул.) символ.</span><span class="sxs-lookup"><span data-stu-id="9205f-123">7 The user selected (clicked) the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="9205f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9205f-124">Remarks</span></span>

<span data-ttu-id="9205f-125">Как правило, режим справки завершается, когда пользователь щелкает или перетаскивает символ или выбирает команду из всплывающего меню символа.</span><span class="sxs-lookup"><span data-stu-id="9205f-125">Typically, Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="9205f-126">Щелчок на другом символе или в другом расположении на экране не приводит к отмене режима справки.</span><span class="sxs-lookup"><span data-stu-id="9205f-126">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="9205f-127">Клиент, который устанавливает режим справки для символа, может отменить режим справки, установив [](helpmodeon-property.md) для Хелпмодеон **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9205f-127">The client that set Help mode for the character can cancel Help mode by setting [**HelpModeOn**](helpmodeon-property.md) to **False**.</span></span> <span data-ttu-id="9205f-128">(Это не вызывает событие **хелпкомплете** .)</span><span class="sxs-lookup"><span data-stu-id="9205f-128">(This does not trigger the **HelpComplete** event.)</span></span>

<span data-ttu-id="9205f-129">Когда пользователь выбирает команду из всплывающего меню символа в режиме справки, сервер удаляет меню, вызывает справку с заданной командой [**хелпконтекстид**](helpcontextid-property.md)и отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="9205f-129">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="9205f-130">С учетом контекста (также называется тем, что это такое?) Окно справки отображается в положении указателя.</span><span class="sxs-lookup"><span data-stu-id="9205f-130">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="9205f-131">Если пользователь выберет команду по голосовому вводу, окно справки будет отображено над символом.</span><span class="sxs-lookup"><span data-stu-id="9205f-131">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="9205f-132">Если символ находится за пределами экрана, окно отображается на экране ближе к текущему положению символа.</span><span class="sxs-lookup"><span data-stu-id="9205f-132">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="9205f-133">Если сервер возвращает имя как пустую строку (""), он указывает, что пользователь выбрал команду, предоставляемую сервером.</span><span class="sxs-lookup"><span data-stu-id="9205f-133">If the server returns Name as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="9205f-134">Это событие отправляется только клиентскому приложению, которое помещает символ в режим справки.</span><span class="sxs-lookup"><span data-stu-id="9205f-134">This event is sent only to the client application that places the character in Help mode.</span></span>

### <a name="see-also"></a><span data-ttu-id="9205f-135">См. также:</span><span class="sxs-lookup"><span data-stu-id="9205f-135">See Also</span></span>

<span data-ttu-id="9205f-136">[**Свойство хелпмодеон**](helpmodeon-property.md), [ **свойство хелпконтекстид**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="9205f-136">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

