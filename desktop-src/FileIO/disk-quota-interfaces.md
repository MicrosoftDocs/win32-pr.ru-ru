---
description: Интерфейсы, используемые с квотами диска.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Интерфейсы дисковой квоты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497970"
---
# <a name="disk-quota-interfaces"></a><span data-ttu-id="6b664-103">Интерфейсы дисковой квоты</span><span class="sxs-lookup"><span data-stu-id="6b664-103">Disk Quota Interfaces</span></span>

<span data-ttu-id="6b664-104">С дисковой квотой используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="6b664-104">The following interfaces are used with disk quotas.</span></span>



| <span data-ttu-id="6b664-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="6b664-105">Interface</span></span>                                          | <span data-ttu-id="6b664-106">Описание</span><span class="sxs-lookup"><span data-stu-id="6b664-106">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b664-107">**идисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="6b664-107">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | <span data-ttu-id="6b664-108">Управляет дисковыми квотами для одного тома файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="6b664-108">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="6b664-109">**идисккуотаевентс**</span><span class="sxs-lookup"><span data-stu-id="6b664-109">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | <span data-ttu-id="6b664-110">Получает уведомления о событиях, связанных с квотами.</span><span class="sxs-lookup"><span data-stu-id="6b664-110">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="6b664-111">**идисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="6b664-111">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | <span data-ttu-id="6b664-112">Представляет одну запись пользовательской квоты в файле сведений о квотах тома.</span><span class="sxs-lookup"><span data-stu-id="6b664-112">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="6b664-113">**идисккуотаусербатч**</span><span class="sxs-lookup"><span data-stu-id="6b664-113">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | <span data-ttu-id="6b664-114">Добавляет несколько пользовательских объектов квоты в контейнер, который затем отправляется для обновления в одном вызове.</span><span class="sxs-lookup"><span data-stu-id="6b664-114">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="6b664-115">**иенумдисккуотаусерс**</span><span class="sxs-lookup"><span data-stu-id="6b664-115">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | <span data-ttu-id="6b664-116">Перечисляет записи квоты пользователя на томе.</span><span class="sxs-lookup"><span data-stu-id="6b664-116">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

