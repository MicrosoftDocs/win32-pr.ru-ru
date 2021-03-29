---
title: Хелпмодеон, свойство
description: Хелпмодеон, свойство
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776460"
---
# <a name="helpmodeon-property"></a><span data-ttu-id="dd4ed-103">Хелпмодеон, свойство</span><span class="sxs-lookup"><span data-stu-id="dd4ed-103">HelpModeOn Property</span></span>

<span data-ttu-id="dd4ed-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dd4ed-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="dd4ed-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="dd4ed-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="dd4ed-106">Возвращает или задает значение, указывающее, включен ли контекстно-зависимый режим справки для символа.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-106">Returns or sets whether context-sensitive Help mode is on for the character.</span></span>

</dd> <dt>

<span data-ttu-id="dd4ed-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="dd4ed-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="dd4ed-108">\*агент. ***Символы ("*** чарактерид \* \* *"). Хелпмодеон* \*  \[  =  *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="dd4ed-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").HelpModeOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="dd4ed-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="dd4ed-109">Part</span></span>      | <span data-ttu-id="dd4ed-110">Описание</span><span class="sxs-lookup"><span data-stu-id="dd4ed-110">Description</span></span>                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4ed-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="dd4ed-111">*boolean*</span></span> | <span data-ttu-id="dd4ed-112">Логическое выражение, указывающее, включен ли контекстно-зависимый режим справки.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-112">A Boolean expression specifying whether context-sensitive Help mode is on.</span></span> <span data-ttu-id="dd4ed-113">**Значение true** Режим справки включен.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-113">**True** Help mode is on.</span></span> <br/> <span data-ttu-id="dd4ed-114">**False** (по умолчанию) режим справки отключен.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-114">**False** (Default) Help mode is off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd4ed-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd4ed-115">Remarks</span></span>

<span data-ttu-id="dd4ed-116">Если для этого свойства задано **значение true**, то при перемещении по символу или во всплывающем меню для символа указатель мыши превращается в контекстно-зависимый рисунок справки.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-116">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="dd4ed-117">Когда пользователь щелкает или перетаскивает символ или щелкает элемент во всплывающем меню символа, сервер запускает событие [**хелпкомплете**](helpcomplete-event.md) и выходит из режима справки.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-117">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**HelpComplete**](helpcomplete-event.md) event and exits Help mode.</span></span>

<span data-ttu-id="dd4ed-118">В режиме справки сервер не отправляет события [**Click**](click-event.md), [**драгстарт**](dragstart-event.md), [**драгкомплете**](dragcomplete-event.md)и [**Command**](command-event.md) , если для свойства [**аутопопупмену**](autopopupmenu-property.md) не задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-118">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md), and [**Command**](command-event.md) events, unless you set the [**AutoPopupMenu**](autopopupmenu-property.md) property to **True**.</span></span> <span data-ttu-id="dd4ed-119">В этом случае сервер будет отсылать событие **щелчка** (не выходя из режима справки), но только при нажатии правой кнопки мыши для отображения всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-119">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="dd4ed-120">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="dd4ed-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd4ed-121">См. также:</span><span class="sxs-lookup"><span data-stu-id="dd4ed-121">See Also</span></span>

[<span data-ttu-id="dd4ed-122">**Событие Хелпкомплете**</span><span class="sxs-lookup"><span data-stu-id="dd4ed-122">**HelpComplete event**</span></span>](helpcomplete-event.md)


 

 





