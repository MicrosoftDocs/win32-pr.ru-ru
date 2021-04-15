---
description: '\_ \_ Мьютекс мсипромптфоркд существует, когда установщик предлагает пользователю вставить компакт-диск.'
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD мьютекс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662991"
---
# <a name="__msipromptforcd-mutex"></a><span data-ttu-id="4c8b8-103">\_\_Мьютекс Мсипромптфоркд</span><span class="sxs-lookup"><span data-stu-id="4c8b8-103">\_\_MsiPromptForCD Mutex</span></span>

<span data-ttu-id="4c8b8-104">\_ \_ Мьютекс мсипромптфоркд существует, когда установщик предлагает пользователю вставить компакт-диск.</span><span class="sxs-lookup"><span data-stu-id="4c8b8-104">The \_\_MsiPromptForCD Mutex exists when the installer prompts the user to insert a CD-ROM.</span></span> <span data-ttu-id="4c8b8-105">Программы автозапуска должны проверять, \_ \_ не задан ли в данный момент мьютекс мсипромптфоркд перед запуском.</span><span class="sxs-lookup"><span data-stu-id="4c8b8-105">Autoplay programs should check that the \_\_MsiPromptForCD mutex is not currently set before starting.</span></span> <span data-ttu-id="4c8b8-106">Обратите внимание, что можно выполнить запрос к дисководу компакт-дисков перед тем, как будет существовать ключ выполнения или \_ мьютекс мсиексекуте.</span><span class="sxs-lookup"><span data-stu-id="4c8b8-106">Note that it is possible for a CD-ROM prompt to occur before either the InProgress key or the \_MSIExecute Mutex exist.</span></span>

 

 



