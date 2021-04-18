---
title: Иажентнотифисинк Висиблестате
description: Иажентнотифисинк Висиблестате
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700667"
---
# <a name="iagentnotifysinkvisiblestate"></a><span data-ttu-id="10380-103">Иажентнотифисинк:: Висиблестате</span><span class="sxs-lookup"><span data-stu-id="10380-103">IAgentNotifySink::VisibleState</span></span>

<span data-ttu-id="10380-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="10380-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

<span data-ttu-id="10380-105">Уведомляет клиентское приложение об изменении состояния видимости символа.</span><span class="sxs-lookup"><span data-stu-id="10380-105">Notifies a client application when the visibility state of the character changes.</span></span>

-   <span data-ttu-id="10380-106">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="10380-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="10380-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*двчарид*</span><span class="sxs-lookup"><span data-stu-id="10380-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="10380-108">Идентификатор символа, состояние видимости которого изменяется.</span><span class="sxs-lookup"><span data-stu-id="10380-108">Identifier of the character whose visibility state is changed.</span></span>

</dd> <dt>

<span data-ttu-id="10380-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*бвисибле*</span><span class="sxs-lookup"><span data-stu-id="10380-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="10380-110">Флаг видимости.</span><span class="sxs-lookup"><span data-stu-id="10380-110">Visibility flag.</span></span> <span data-ttu-id="10380-111">Это логическое значение имеет **значение true** , когда символ становится видимым, и **false** , если символ становится скрытым.</span><span class="sxs-lookup"><span data-stu-id="10380-111">This Boolean value is **True** when character becomes visible and **False** when the character becomes hidden.</span></span>

</dd> <dt>

<span data-ttu-id="10380-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*двкаусе*</span><span class="sxs-lookup"><span data-stu-id="10380-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="10380-113">Причина последнего изменения состояния видимости символа.</span><span class="sxs-lookup"><span data-stu-id="10380-113">Cause of last change to the character's visibility state.</span></span> <span data-ttu-id="10380-114">Параметр может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="10380-114">The parameter may be one of the following:</span></span>



| <span data-ttu-id="10380-115">Значение</span><span class="sxs-lookup"><span data-stu-id="10380-115">Value</span></span>                                                                   | <span data-ttu-id="10380-116">Описание</span><span class="sxs-lookup"><span data-stu-id="10380-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="10380-117">**const без знака Short** **невершовн = 0;**</span><span class="sxs-lookup"><span data-stu-id="10380-117">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="10380-118">Символ не показан.</span><span class="sxs-lookup"><span data-stu-id="10380-118">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="10380-119">**const без знака Short** **усерхид = 1;**</span><span class="sxs-lookup"><span data-stu-id="10380-119">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="10380-120">Пользователь скрыл символ во всплывающем меню со значком символа на панели задач или с голосовым входом.</span><span class="sxs-lookup"><span data-stu-id="10380-120">User hid the character with the character's taskbar icon pop-up menu or with speech input..</span></span> |
| <span data-ttu-id="10380-121">**const без знака Short** **усершовед = 2;**</span><span class="sxs-lookup"><span data-stu-id="10380-121">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="10380-122">Пользователь показал символ.</span><span class="sxs-lookup"><span data-stu-id="10380-122">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="10380-123">**const без знака Short** **програмхид = 3;**</span><span class="sxs-lookup"><span data-stu-id="10380-123">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="10380-124">Приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="10380-124">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="10380-125">**const без знака Short** **програмшовед = 4;**</span><span class="sxs-lookup"><span data-stu-id="10380-125">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="10380-126">Приложение показало этот символ.</span><span class="sxs-lookup"><span data-stu-id="10380-126">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="10380-127">**const без знака Short** **осерпрограмхид = 5;**</span><span class="sxs-lookup"><span data-stu-id="10380-127">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="10380-128">Другое приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="10380-128">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="10380-129">**const без знака Short** **осерпрограмшовед = 6;**</span><span class="sxs-lookup"><span data-stu-id="10380-129">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="10380-130">Этот символ был продемонстрирован другим приложением.</span><span class="sxs-lookup"><span data-stu-id="10380-130">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="10380-131">**const без знака Short** **усерхидвиачарактермену = 7**</span><span class="sxs-lookup"><span data-stu-id="10380-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="10380-132">Пользователь скрыл символ во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="10380-132">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="10380-133">**const без знака Short** **усерхидвиатаскбарикон = усерхид**</span><span class="sxs-lookup"><span data-stu-id="10380-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="10380-134">Пользователь скрыл символ во всплывающем меню со значком символа на панели задач или с помощью речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="10380-134">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="10380-135">См. также:</span><span class="sxs-lookup"><span data-stu-id="10380-135">See Also</span></span>

<span data-ttu-id="10380-136">[**Иажентчарактер:: OnVisible**](iagentcharacter--getvisible.md), [ **иажентчарактер:: жетвисибилитикаусе**](iagentcharacter--getvisibilitycause.md)</span><span class="sxs-lookup"><span data-stu-id="10380-136">[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [**IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span></span>


 

 





