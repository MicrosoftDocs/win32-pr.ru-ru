---
title: Иажентнотифисинкекс Хелпкомплете
description: Иажентнотифисинкекс Хелпкомплете
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069876"
---
# <a name="iagentnotifysinkexhelpcomplete"></a><span data-ttu-id="468c5-103">Иажентнотифисинкекс:: Хелпкомплете</span><span class="sxs-lookup"><span data-stu-id="468c5-103">IAgentNotifySinkEx::HelpComplete</span></span>

<span data-ttu-id="468c5-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="468c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

<span data-ttu-id="468c5-105">Уведомляет клиентское приложение, когда пользователь выбирает команду или символ для завершения режима справки.</span><span class="sxs-lookup"><span data-stu-id="468c5-105">Notifies a client application when the user selects a command or character to complete Help mode.</span></span>

-   <span data-ttu-id="468c5-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="468c5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="468c5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="468c5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="468c5-108">Идентификатор символа, для которого был выполнен режим справки.</span><span class="sxs-lookup"><span data-stu-id="468c5-108">Identifier of the character for which Help mode completed.</span></span>

</dd> <dt>

<span data-ttu-id="468c5-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*двкоммандид*</span><span class="sxs-lookup"><span data-stu-id="468c5-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="468c5-110">Идентификатор команды, выбранной пользователем.</span><span class="sxs-lookup"><span data-stu-id="468c5-110">Identifier of the command the user selected.</span></span>

</dd> <dt>

<span data-ttu-id="468c5-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*двкаусе*</span><span class="sxs-lookup"><span data-stu-id="468c5-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="468c5-112">Причина события, которая может принимать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="468c5-112">The cause for the event, which may be the following values:</span></span>



| <span data-ttu-id="468c5-113">Значение</span><span class="sxs-lookup"><span data-stu-id="468c5-113">Value</span></span>                                                                         | <span data-ttu-id="468c5-114">Описание</span><span class="sxs-lookup"><span data-stu-id="468c5-114">Description</span></span>                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="468c5-115">**const неподписанная короткая** **\_ команда кшелпкаусе = 1;**</span><span class="sxs-lookup"><span data-stu-id="468c5-115">**const unsigned short** **CSHELPCAUSE\_COMMAND = 1;**</span></span><br/>             | <span data-ttu-id="468c5-116">Пользователь выбрал команду, предоставленную вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="468c5-116">The user selected a command supplied by your application.</span></span>                            |
| <span data-ttu-id="468c5-117">**const без знака Short** **кшелпкаусе \_ осерпрограм = 2;**</span><span class="sxs-lookup"><span data-stu-id="468c5-117">**const unsigned short** **CSHELPCAUSE\_OTHERPROGRAM = 2;**</span></span><br/>        | <span data-ttu-id="468c5-118">Пользователь выбрал объект [**Commands**](/windows/desktop/lwef/the-commands-collection-object) другого клиента.</span><span class="sxs-lookup"><span data-stu-id="468c5-118">The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span> |
| <span data-ttu-id="468c5-119">**const без знака Short** **кшелпкаусе \_ опенкоммандсвиндов = 3;**</span><span class="sxs-lookup"><span data-stu-id="468c5-119">**const unsigned short** **CSHELPCAUSE\_OPENCOMMANDSWINDOW = 3;**</span></span><br/>  | <span data-ttu-id="468c5-120">Пользователь выбрал команду "открыть голосовое меню".</span><span class="sxs-lookup"><span data-stu-id="468c5-120">The user selected the Open Voice Commands command.</span></span>                                   |
| <span data-ttu-id="468c5-121">**const без знака Short** **кшелпкаусе \_ клосекоммандсвиндов = 4;**</span><span class="sxs-lookup"><span data-stu-id="468c5-121">**const unsigned short** **CSHELPCAUSE\_CLOSECOMMANDSWINDOW = 4;**</span></span><br/> | <span data-ttu-id="468c5-122">Пользователь выбрал команду "закрыть голосовое меню".</span><span class="sxs-lookup"><span data-stu-id="468c5-122">The user selected the Close Voice Commands command.</span></span>                                  |
| <span data-ttu-id="468c5-123">**const без знака Short** **кшелпкаусе \_ шовчарактер = 5;**</span><span class="sxs-lookup"><span data-stu-id="468c5-123">**const unsigned short** **CSHELPCAUSE\_SHOWCHARACTER = 5;**</span></span><br/>       | <span data-ttu-id="468c5-124">Пользователь выбрал команду "показывать *чарактернаме* ".</span><span class="sxs-lookup"><span data-stu-id="468c5-124">The user selected the Show *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="468c5-125">**const без знака Short** **кшелпкаусе \_ хидечарактер = 6;**</span><span class="sxs-lookup"><span data-stu-id="468c5-125">**const unsigned short** **CSHELPCAUSE\_HIDECHARACTER = 6;**</span></span><br/>       | <span data-ttu-id="468c5-126">Пользователь выбрал команду Hide *чарактернаме* .</span><span class="sxs-lookup"><span data-stu-id="468c5-126">The user selected the Hide *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="468c5-127">**const неподписанный короткий** **кшелпкаусе \_ символ = 7;**</span><span class="sxs-lookup"><span data-stu-id="468c5-127">**const unsigned short** **CSHELPCAUSE\_CHARACTER = 7;**</span></span><br/>           | <span data-ttu-id="468c5-128">Пользователь выбрал (щелкнул.) символ.</span><span class="sxs-lookup"><span data-stu-id="468c5-128">The user selected (clicked) the character.</span></span>                                           |



 

</dd> </dl>

<span data-ttu-id="468c5-129">Обычно режим справки завершается, когда пользователь щелкает или перетаскивает символ или выбирает команду из всплывающего меню символа.</span><span class="sxs-lookup"><span data-stu-id="468c5-129">Typically Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="468c5-130">Щелчок на другом символе или в другом расположении на экране не приводит к отмене режима справки.</span><span class="sxs-lookup"><span data-stu-id="468c5-130">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="468c5-131">Клиент, который устанавливает режим справки для символа, может отменить режим справки, установив [**иажентчарактер:: хелпмодеон**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) в **значение false**.</span><span class="sxs-lookup"><span data-stu-id="468c5-131">The client that set Help mode for the character can cancel Help mode by setting [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) to **False**.</span></span> <span data-ttu-id="468c5-132">(Это не вызывает событие **иажентнотифисинкекс:: хелпкомплете** .)</span><span class="sxs-lookup"><span data-stu-id="468c5-132">(This does not trigger the **IAgentNotifySinkEx::HelpComplete** event.)</span></span>

<span data-ttu-id="468c5-133">Когда пользователь выбирает команду из всплывающего меню символа в режиме справки, сервер удаляет меню, вызывает справку с заданной командой [**хелпконтекстид**](helpcontextid-property.md)и отправляет это событие.</span><span class="sxs-lookup"><span data-stu-id="468c5-133">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="468c5-134">С учетом контекста (также называется тем, что это такое?) Окно справки отображается в положении указателя.</span><span class="sxs-lookup"><span data-stu-id="468c5-134">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="468c5-135">Если пользователь выберет команду по голосовому вводу, окно справки будет отображено над символом.</span><span class="sxs-lookup"><span data-stu-id="468c5-135">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="468c5-136">Если символ находится за пределами экрана, окно отображается на экране ближе к текущему положению символа.</span><span class="sxs-lookup"><span data-stu-id="468c5-136">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="468c5-137">Если сервер возвращает *двкоммандид* как пустую строку (""), он указывает, что пользователь выбрал команду, предоставляемую сервером.</span><span class="sxs-lookup"><span data-stu-id="468c5-137">If the server returns *dwCommandID* as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="468c5-138">Это событие отправляется только клиентскому приложению, которое помещает символ в режим справки.</span><span class="sxs-lookup"><span data-stu-id="468c5-138">This event is sent only to the client application that places the character into Help mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="468c5-139">См. также:</span><span class="sxs-lookup"><span data-stu-id="468c5-139">See Also</span></span>

<span data-ttu-id="468c5-140">[**Иажентчарактерекс:: сеселпмодеон**](iagentcharacterex--sethelpmodeon.md), [**Иажентчарактерекс:: сеселпфиленаме**](iagentcharacterex--sethelpfilename.md), [**иажентчарактерекс:: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="468c5-140">[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>


 

