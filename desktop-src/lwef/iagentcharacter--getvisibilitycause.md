---
title: Иажентчарактер Жетвисибилитикаусе
description: Иажентчарактер Жетвисибилитикаусе
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411450"
---
# <a name="iagentcharactergetvisibilitycause"></a><span data-ttu-id="8927c-103">Иажентчарактер:: Жетвисибилитикаусе</span><span class="sxs-lookup"><span data-stu-id="8927c-103">IAgentCharacter::GetVisibilityCause</span></span>

<span data-ttu-id="8927c-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8927c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

<span data-ttu-id="8927c-105">Извлекает причину видимого состояния символа.</span><span class="sxs-lookup"><span data-stu-id="8927c-105">Retrieves the cause of the character's visible state.</span></span>

-   <span data-ttu-id="8927c-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8927c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8927c-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*пдвкаусе*</span><span class="sxs-lookup"><span data-stu-id="8927c-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="8927c-108">Адрес переменной, которая получает причину последнего изменения состояния видимости символа и будет одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="8927c-108">Address of a variable that receives the cause of the character's last visibility state change and will be one of the following:</span></span>



| <span data-ttu-id="8927c-109">Значение</span><span class="sxs-lookup"><span data-stu-id="8927c-109">Value</span></span>                                                                   | <span data-ttu-id="8927c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8927c-110">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8927c-111">**const без знака Short** **невершовн = 0;**</span><span class="sxs-lookup"><span data-stu-id="8927c-111">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="8927c-112">Символ не показан.</span><span class="sxs-lookup"><span data-stu-id="8927c-112">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="8927c-113">**const без знака Short** **усерхид = 1;**</span><span class="sxs-lookup"><span data-stu-id="8927c-113">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="8927c-114">Пользователь скрыл символ во всплывающем меню со значком символа на панели задач или с помощью речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="8927c-114">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |
| <span data-ttu-id="8927c-115">**const без знака Short** **усершовед = 2;**</span><span class="sxs-lookup"><span data-stu-id="8927c-115">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="8927c-116">Пользователь показал символ.</span><span class="sxs-lookup"><span data-stu-id="8927c-116">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="8927c-117">**const без знака Short** **програмхид = 3;**</span><span class="sxs-lookup"><span data-stu-id="8927c-117">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="8927c-118">Приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="8927c-118">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="8927c-119">**const без знака Short** **програмшовед = 4;**</span><span class="sxs-lookup"><span data-stu-id="8927c-119">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="8927c-120">Приложение показало этот символ.</span><span class="sxs-lookup"><span data-stu-id="8927c-120">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="8927c-121">**const без знака Short** **осерпрограмхид = 5;**</span><span class="sxs-lookup"><span data-stu-id="8927c-121">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="8927c-122">Другое приложение скрыло символ.</span><span class="sxs-lookup"><span data-stu-id="8927c-122">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="8927c-123">**const без знака Short** **осерпрограмшовед = 6;**</span><span class="sxs-lookup"><span data-stu-id="8927c-123">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="8927c-124">Этот символ был продемонстрирован другим приложением.</span><span class="sxs-lookup"><span data-stu-id="8927c-124">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="8927c-125">**const без знака Short** **усерхидвиачарактермену = 7**</span><span class="sxs-lookup"><span data-stu-id="8927c-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="8927c-126">Пользователь скрыл символ во всплывающем меню символа.</span><span class="sxs-lookup"><span data-stu-id="8927c-126">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="8927c-127">**const без знака Short** **усерхидвиатаскбарикон = усерхид**</span><span class="sxs-lookup"><span data-stu-id="8927c-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="8927c-128">Пользователь скрыл символ во всплывающем меню со значком символа на панели задач или с помощью речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="8927c-128">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8927c-129">См. также:</span><span class="sxs-lookup"><span data-stu-id="8927c-129">See Also</span></span>

[<span data-ttu-id="8927c-130">**Иажентнотифисинк:: Висиблестате**</span><span class="sxs-lookup"><span data-stu-id="8927c-130">**IAgentNotifySink::VisibleState**</span></span>](iagentnotifysink--visiblestate.md)


 

 





