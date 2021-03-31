---
title: Повторное распространение программного обеспечения
description: Повторное распространение программного обеспечения
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media Format SDK, повторное распространение программного обеспечения
- Расширенный формат систем (ASF), повторное распространение программного обеспечения
- ASF (Расширенный системный формат), повторное распространение программного обеспечения
- Пакет SDK для Windows Media Format, повторное распространение
- Расширенный формат систем (ASF), распространение
- ASF (Расширенный системный формат), повторное распространение
- распространение программного обеспечения, о
- повторное распространение, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775011"
---
# <a name="software-redistribution"></a><span data-ttu-id="f6975-111">Повторное распространение программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="f6975-111">Software Redistribution</span></span>

<span data-ttu-id="f6975-112">Включение программного обеспечения формата Windows Media в программу установки приложения называется перераспределением.</span><span class="sxs-lookup"><span data-stu-id="f6975-112">The inclusion of Windows Media Format software in an application setup is known as redistribution.</span></span> <span data-ttu-id="f6975-113">Пакет SDK для формата Windows Media включает установочные пакеты, которые можно добавить в программу установки приложения.</span><span class="sxs-lookup"><span data-stu-id="f6975-113">The Windows Media Format SDK includes an installation package which can be included with your application setup.</span></span> <span data-ttu-id="f6975-114">Пакет установки — это исполняемый файл с именем wmfdist95.exe.</span><span class="sxs-lookup"><span data-stu-id="f6975-114">The installation package is an executable file named wmfdist95.exe.</span></span> <span data-ttu-id="f6975-115">При установке пакета SDK для формата Windows Media пакет установки копируется в \\ папку Redist каталога установки (c: \\ вмсдк \\ вмфсдк по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="f6975-115">When you install the Windows Media Format SDK, the installation package is copied to the \\Redist folder of the install directory (c:\\wmsdk\\wmfsdk by default).</span></span>

<span data-ttu-id="f6975-116">В следующих разделах приводятся процедуры и другие сведения о настройке распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="f6975-116">The following sections provide procedures and other information for software redistribution setup.</span></span>



| <span data-ttu-id="f6975-117">Section</span><span class="sxs-lookup"><span data-stu-id="f6975-117">Section</span></span>                                                                            | <span data-ttu-id="f6975-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f6975-118">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6975-119">Создание настройки распространения</span><span class="sxs-lookup"><span data-stu-id="f6975-119">To Create a Redistribution Setup</span></span>](to-create-a-redistribution-setup.md)           | <span data-ttu-id="f6975-120">Описание процедуры создания программы установки приложения.</span><span class="sxs-lookup"><span data-stu-id="f6975-120">Describes the procedure for creating an application setup.</span></span>                                                                                                                       |
| [<span data-ttu-id="f6975-121">Определение состояния установки</span><span class="sxs-lookup"><span data-stu-id="f6975-121">Detecting Setup Status</span></span>](detecting-setup-status.md)                               | <span data-ttu-id="f6975-122">Содержит пример кода, который проверяет наличие состояния установки в реестре, чтобы определить, нужно ли установить пакет распространения.</span><span class="sxs-lookup"><span data-stu-id="f6975-122">Provides example code that checks the registry for installation status to determine whether the redistribution package needs to be installed.</span></span>                                    |
| [<span data-ttu-id="f6975-123">Пример кода для настройки распространения</span><span class="sxs-lookup"><span data-stu-id="f6975-123">Example Code for Redistribution Setup</span></span>](example-code-for-redistribution-setup.md) | <span data-ttu-id="f6975-124">Содержит пример кода, который можно использовать в подпрограмме установки для запуска пакетов распространения в тихом режиме, и уведомлять программу установки о необходимости перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="f6975-124">Provides example code that can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f6975-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f6975-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6975-126">**Рекомендации по проекту**</span><span class="sxs-lookup"><span data-stu-id="f6975-126">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




