---
title: Константы прав
description: Константы прав
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- Windows Media Format SDK, константы
- Управление цифровыми правами (DRM), константы
- DRM (Управление цифровыми правами), константы
- Расширенные API клиента DRM, константы
- Расширенные API клиента, константы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1349da53b63b1b7df59c13e0e69f7fdbf47ee3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104133014"
---
# <a name="rights-constants"></a><span data-ttu-id="af64e-108">Константы прав</span><span class="sxs-lookup"><span data-stu-id="af64e-108">Rights Constants</span></span>

<span data-ttu-id="af64e-109">Константы, перечисленные в следующей таблице, используются для обнаружения действий DRM и построения списков действий.</span><span class="sxs-lookup"><span data-stu-id="af64e-109">The constants listed in the following table are used to identify DRM actions and to build lists of actions.</span></span>



| <span data-ttu-id="af64e-110">Константа</span><span class="sxs-lookup"><span data-stu-id="af64e-110">Constant</span></span>                                        | <span data-ttu-id="af64e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="af64e-111">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af64e-112">\_тег g всзвмдрм \_ актионлист \_</span><span class="sxs-lookup"><span data-stu-id="af64e-112">g\_wszWMDRM\_ACTIONLIST\_TAG</span></span>                    | <span data-ttu-id="af64e-113">Определяет имя XML-элемента для списка действий.</span><span class="sxs-lookup"><span data-stu-id="af64e-113">Defines the XML element name for an action list.</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="af64e-114">\_ \_ тег действия g \_ всзвмдрм</span><span class="sxs-lookup"><span data-stu-id="af64e-114">g\_wszWMDRM\_ACTION\_TAG</span></span>                        | <span data-ttu-id="af64e-115">Определяет имя XML-элемента для записи в списке действий.</span><span class="sxs-lookup"><span data-stu-id="af64e-115">Defines the XML element name for an entry in an action list.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="af64e-116">g \_ всзвмдрм \_ правое \_ Воспроизведение</span><span class="sxs-lookup"><span data-stu-id="af64e-116">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="af64e-117">Определяет строку справа для воспроизведения содержимого.</span><span class="sxs-lookup"><span data-stu-id="af64e-117">Defines the string for the right to play content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="af64e-118">g \_ всзвмдрм \_ , \_ копия справа</span><span class="sxs-lookup"><span data-stu-id="af64e-118">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="af64e-119">Определяет строку справа для копирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="af64e-119">Defines the string for the right to copy content.</span></span>                                                                                                                                                                                                              |
| <span data-ttu-id="af64e-120">\_всзвмдрм \_ правой \_ записи списка воспроизведения \_</span><span class="sxs-lookup"><span data-stu-id="af64e-120">g\_wszWMDRM\_RIGHT\_PLAYLIST\_BURN</span></span>              | <span data-ttu-id="af64e-121">Определяет строку право на запись содержимого на компакт-диск в составе списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="af64e-121">Defines the string for the right to burn content to CD as part of a playlist.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="af64e-122">g \_ всзвмдрм \_ справа \_ Создание \_ эскиза \_ изображения</span><span class="sxs-lookup"><span data-stu-id="af64e-122">g\_wszWMDRM\_RIGHT\_CREATE\_THUMBNAIL\_IMAGE</span></span>    | <span data-ttu-id="af64e-123">Определяет строку справа для создания эскиза изображения из видеосодержимого.</span><span class="sxs-lookup"><span data-stu-id="af64e-123">Defines the string for the right to create a thumbnail image from video content.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="af64e-124">g \_ всзвмдрм \_ право \_ Копировать \_ на \_ компакт-диск</span><span class="sxs-lookup"><span data-stu-id="af64e-124">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="af64e-125">Определяет строку справа для копирования содержимого на компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="af64e-125">Defines the string for the right to copy content to a CD.</span></span> <span data-ttu-id="af64e-126">Новые лицензии не должны использовать это право.</span><span class="sxs-lookup"><span data-stu-id="af64e-126">New licenses should not use this right.</span></span> <span data-ttu-id="af64e-127">Вместо этого все права, предоставляющие разрешение на копирование содержимого, должны быть охвачены правом копирования и правым списком воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="af64e-127">Instead, all rights granting permission to copy content should be covered by the copy right and the playlist burn right.</span></span>                                     |
| <span data-ttu-id="af64e-128">g \_ всзвмдрм \_ право \_ Копировать \_ на \_ \_ устройство SDMI</span><span class="sxs-lookup"><span data-stu-id="af64e-128">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="af64e-129">Определяет строку, которая подходит для копирования содержимого на устройство, соответствующее инициативе защиты цифровой музыки (SDMI).</span><span class="sxs-lookup"><span data-stu-id="af64e-129">Defines the string for the right to copy content to a device that conforms to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="af64e-130">Новые лицензии не должны использовать это право.</span><span class="sxs-lookup"><span data-stu-id="af64e-130">New licenses should not use this right.</span></span> <span data-ttu-id="af64e-131">Вместо этого все права, предоставляющие разрешение на копирование содержимого, должны быть охвачены правом копирования.</span><span class="sxs-lookup"><span data-stu-id="af64e-131">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="af64e-132">g \_ всзвмдрм \_ right \_ Копировать \_ на \_ устройство, отличное от \_ SDMI \_</span><span class="sxs-lookup"><span data-stu-id="af64e-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="af64e-133">Определяет строку, которая подходит для копирования на устройство, которое не соответствует инициативе для защиты цифровой музыки (SDMI).</span><span class="sxs-lookup"><span data-stu-id="af64e-133">Defines the string for the right to copy to a device that does not conform to the Secure Digital Music Initiative (SDMI).</span></span> <span data-ttu-id="af64e-134">Новые лицензии не должны использовать это право.</span><span class="sxs-lookup"><span data-stu-id="af64e-134">New licenses should not use this right.</span></span> <span data-ttu-id="af64e-135">Вместо этого все права, предоставляющие разрешение на копирование содержимого, должны быть охвачены правом копирования.</span><span class="sxs-lookup"><span data-stu-id="af64e-135">Instead, all rights granting permission to copy content should be covered by the copy right.</span></span> |
| <span data-ttu-id="af64e-136">g \_ всзвмдрм, \_ правое \_ резервное копирование</span><span class="sxs-lookup"><span data-stu-id="af64e-136">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="af64e-137">Определяет строку справа для резервного копирования лицензии.</span><span class="sxs-lookup"><span data-stu-id="af64e-137">Defines the string for the right to backup the license.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="af64e-138">g \_ всзвмдрм \_ право на \_ сотрудничество \_</span><span class="sxs-lookup"><span data-stu-id="af64e-138">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="af64e-139">Определяет строку, которая подходит для воспроизведения содержимого по сети в составе общего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="af64e-139">Defines the string for the right to play content over a network as part of a shared playlist.</span></span>                                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="af64e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="af64e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af64e-141">**Константы**</span><span class="sxs-lookup"><span data-stu-id="af64e-141">**Constants**</span></span>](constants.md)
</dt> </dl>

 

 




