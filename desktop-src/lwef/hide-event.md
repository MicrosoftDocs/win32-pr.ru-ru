---
title: Скрыть событие
description: Скрыть событие
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888464"
---
# <a name="hide-event"></a><span data-ttu-id="bbc7a-103">Скрыть событие</span><span class="sxs-lookup"><span data-stu-id="bbc7a-103">Hide Event</span></span>

<span data-ttu-id="bbc7a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bbc7a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bbc7a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="bbc7a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bbc7a-106">Происходит при скрытии символа.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-106">Occurs when a character is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="bbc7a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="bbc7a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bbc7a-108"> *Подагент\ *\ *\ * \_ Hide (*\ *  **ByVal** *чарактерид*, **ByVal** , *Причина\ *\ * *)**</span><span class="sxs-lookup"><span data-stu-id="bbc7a-108">**Sub** *agent\*\*\*\_Hide(*\* **ByVal** *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="bbc7a-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="bbc7a-109">Part</span></span>          | <span data-ttu-id="bbc7a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bbc7a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc7a-111">*чарактерид*</span><span class="sxs-lookup"><span data-stu-id="bbc7a-111">*CharacterID*</span></span> | <span data-ttu-id="bbc7a-112">Возвращает идентификатор скрытого символа в виде строки.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-112">Returns the ID of the hidden character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="bbc7a-113">*Причина*</span><span class="sxs-lookup"><span data-stu-id="bbc7a-113">*Cause*</span></span>       | <span data-ttu-id="bbc7a-114">Возвращает значение, указывающее, что привело к скрытию символа.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-114">Returns a value that indicates what caused the character to hide.</span></span> <span data-ttu-id="bbc7a-115">1 пользователь скрыл символ, выбирая команду во всплывающем меню значка символа на панели задач или используя речевой ввод.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-115">1 User hid the character by selecting the command on the character's taskbar icon pop-up menu or using speech input.</span></span><br/> <span data-ttu-id="bbc7a-116">3 клиентское приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-116">3 Your client application hid the character.</span></span><br/> <span data-ttu-id="bbc7a-117">5 другое клиентское приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-117">5 Another client application hid the character.</span></span><br/> <span data-ttu-id="bbc7a-118">7. пользователь скрыл символ, выбрав команду во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-118">7 User hid the character by selecting the command on the character's pop-up menu.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="bbc7a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbc7a-119">Remarks</span></span>

<span data-ttu-id="bbc7a-120">Сервер отправляет это событие всем клиентам символа.</span><span class="sxs-lookup"><span data-stu-id="bbc7a-120">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="bbc7a-121">Чтобы запросить текущее состояние символа, используйте свойство [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc7a-121">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="bbc7a-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="bbc7a-122">See Also</span></span>

<span data-ttu-id="bbc7a-123">[**Показывать событие**](show-event.md), [ **висибилитикаусе**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="bbc7a-123">[**Show event**](show-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





