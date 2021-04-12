---
title: Создание настройки распространения
description: Создание настройки распространения
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media Format SDK, повторное распространение программного обеспечения
- Расширенный формат систем (ASF), повторное распространение программного обеспечения
- ASF (Расширенный системный формат), повторное распространение программного обеспечения
- Пакет SDK для Windows Media Format, повторное распространение
- Расширенный формат систем (ASF), распространение
- ASF (Расширенный системный формат), повторное распространение
- повторное распространение программного обеспечения, создание
- распространение программного обеспечения, WMFDist.exe
- повторное распространение, создание
- распространение, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253203"
---
# <a name="to-create-a-redistribution-setup"></a><span data-ttu-id="4a75c-114">Создание настройки распространения</span><span class="sxs-lookup"><span data-stu-id="4a75c-114">To Create a Redistribution Setup</span></span>

1.  <span data-ttu-id="4a75c-115">Перед вызовом пакета распространения необходимо установить файлы приложения и выполнить необходимые настройки.</span><span class="sxs-lookup"><span data-stu-id="4a75c-115">Have your setup routine install your application files and make required settings before invoking the redistribution package.</span></span>
2.  <span data-ttu-id="4a75c-116">Установите WMFDist.exe.</span><span class="sxs-lookup"><span data-stu-id="4a75c-116">Install WMFDist.exe.</span></span> <span data-ttu-id="4a75c-117">Вы можете использовать флаг/Q: A для автоматической установки и подавления пользовательского интерфейса настройки распространения во время установки приложения.</span><span class="sxs-lookup"><span data-stu-id="4a75c-117">You can use the /Q:A flag to do a quiet, unattended installation and suppress the user interface of the redistribution setup during the installation of your application.</span></span> <span data-ttu-id="4a75c-118">Ваша подпрограммы должна определить, требуется ли перезагрузка в конце.</span><span class="sxs-lookup"><span data-stu-id="4a75c-118">Your routine must then detect whether restarting is needed at the end.</span></span>

    <span data-ttu-id="4a75c-119">Пример:</span><span class="sxs-lookup"><span data-stu-id="4a75c-119">For example:</span></span>

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4a75c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="4a75c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a75c-121">**Повторное распространение программного обеспечения**</span><span class="sxs-lookup"><span data-stu-id="4a75c-121">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




