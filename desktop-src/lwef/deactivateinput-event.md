---
title: Событие Деактиватеинпут
description: Событие Деактиватеинпут
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986598"
---
# <a name="deactivateinput-event"></a><span data-ttu-id="e73c6-103">Событие Деактиватеинпут</span><span class="sxs-lookup"><span data-stu-id="e73c6-103">DeactivateInput Event</span></span>

<span data-ttu-id="e73c6-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e73c6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e73c6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="e73c6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e73c6-106">Происходит, когда клиент переходит в неактивный поток ввода.</span><span class="sxs-lookup"><span data-stu-id="e73c6-106">Occurs when a client becomes non-input-active.</span></span>

</dd> <dt>

<span data-ttu-id="e73c6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e73c6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e73c6-108"> *Подагент\ *\ *\ * \_ деактиватеинпут*\ *  **(ByVal** *чарактерид\ * *)**</span><span class="sxs-lookup"><span data-stu-id="e73c6-108">**Sub** *agent\*\*\*\_DeactivateInput*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="e73c6-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="e73c6-109">Part</span></span>          | <span data-ttu-id="e73c6-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e73c6-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e73c6-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="e73c6-111">*CharacterID*</span></span> | <span data-ttu-id="e73c6-112">Возвращает идентификатор символа, который делает клиент невходным: активным.</span><span class="sxs-lookup"><span data-stu-id="e73c6-112">Returns the ID of the character that makes the client become non-input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="e73c6-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e73c6-113">Remarks</span></span>

<span data-ttu-id="e73c6-114">Клиент, не входящий в ввод, больше не получает события мыши или речи от сервера (за исключением того, что он снова станет входным).</span><span class="sxs-lookup"><span data-stu-id="e73c6-114">A non-input-active client no longer receives mouse or speech events from the server (unless it becomes input-active again).</span></span> <span data-ttu-id="e73c6-115">Сервер отправляет это событие только клиенту, который не является входным.</span><span class="sxs-lookup"><span data-stu-id="e73c6-115">The server sends this event only to the client that becomes non-input-active.</span></span>

<span data-ttu-id="e73c6-116">Это событие возникает, когда клиентское приложение находится в состоянии input-Active и пользователь выбирает заголовок другого клиента во всплывающем меню символа или в окне "Voice Commands" или вызывает метод [**Activate**](activate-method.md) и устанавливает для параметра **State** значение 0.</span><span class="sxs-lookup"><span data-stu-id="e73c6-116">This event occurs when your client application is input-active and the user chooses the caption of another client in a character's pop-up menu or the Voice Commands Window or you call the [**Activate**](activate-method.md) method and set the **State** parameter to 0.</span></span> <span data-ttu-id="e73c6-117">Это также может произойти, когда пользователь выбирает имя другого символа, нажимая или говорите.</span><span class="sxs-lookup"><span data-stu-id="e73c6-117">It may also occur when the user selects the name of another character by clicking or speaking.</span></span> <span data-ttu-id="e73c6-118">Это событие также появляется, когда ваш символ скрыт или виден другой символ.</span><span class="sxs-lookup"><span data-stu-id="e73c6-118">You also get this event when your character is hidden or another character becomes visible.</span></span>

### <a name="see-also"></a><span data-ttu-id="e73c6-119">См. также:</span><span class="sxs-lookup"><span data-stu-id="e73c6-119">See Also</span></span>

[<span data-ttu-id="e73c6-120">**Событие Активатеинпут**</span><span class="sxs-lookup"><span data-stu-id="e73c6-120">**ActivateInput event**</span></span>](activateinput-event.md)


 

 




