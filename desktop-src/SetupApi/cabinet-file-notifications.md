---
description: Сетупитератекабинет отправляет следующие уведомления. Дополнительные сведения о форматировании и использовании уведомлений см. в разделе уведомления.
ms.assetid: 5a362a93-ebe8-4995-aacc-13ee10d3407a
title: Уведомления о CAB-файлах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3e4eb7645fc3603f026db6bde3ce92f2ed2ce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662335"
---
# <a name="cabinet-file-notifications"></a><span data-ttu-id="50454-104">Уведомления о CAB-файлах</span><span class="sxs-lookup"><span data-stu-id="50454-104">Cabinet File Notifications</span></span>

<span data-ttu-id="50454-105">[**Сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)отправляет следующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="50454-105">The following notifications are sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="50454-106">Дополнительные сведения о форматировании и использовании уведомлений см. в разделе [уведомления](notifications.md).</span><span class="sxs-lookup"><span data-stu-id="50454-106">For more information about the format and use of notifications, see [Notifications](notifications.md).</span></span>



| <span data-ttu-id="50454-107">Уведомление</span><span class="sxs-lookup"><span data-stu-id="50454-107">Notification</span></span>                                                        | <span data-ttu-id="50454-108">Описание</span><span class="sxs-lookup"><span data-stu-id="50454-108">Description</span></span>                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="50454-109">**СПФИЛЕНОТИФИ \_ филикстрактед**</span><span class="sxs-lookup"><span data-stu-id="50454-109">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="50454-110">Файл был извлечен из CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="50454-110">The file has been extracted from the cabinet.</span></span>                                  |
| [<span data-ttu-id="50454-111">**СПФИЛЕНОТИФИ \_ филеинкабинет**</span><span class="sxs-lookup"><span data-stu-id="50454-111">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="50454-112">Файл находится в CAB-файле, и приложение должно его извлечь?</span><span class="sxs-lookup"><span data-stu-id="50454-112">A file is encountered in the cabinet, does the application want to extract it?</span></span> |
| [<span data-ttu-id="50454-113">**СПФИЛЕНОТИФИ \_ нидневкабинет**</span><span class="sxs-lookup"><span data-stu-id="50454-113">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="50454-114">Текущий файл продолжает работу в следующем CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="50454-114">The current file is continued in the next cabinet.</span></span>                             |



 

 

 



