---
description: Интерфейсы, используемые в управлении дисками.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Интерфейсы управления дисками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266135"
---
# <a name="disk-management-interfaces"></a><span data-ttu-id="057ae-103">Интерфейсы управления дисками</span><span class="sxs-lookup"><span data-stu-id="057ae-103">Disk Management Interfaces</span></span>

<span data-ttu-id="057ae-104">В оснастке «Управление дисками» используются следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="057ae-104">The following interfaces are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="057ae-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="057ae-105">In this section</span></span>



| <span data-ttu-id="057ae-106">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="057ae-106">Interface</span></span>                                                     | <span data-ttu-id="057ae-107">Описание</span><span class="sxs-lookup"><span data-stu-id="057ae-107">Description</span></span>                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="057ae-108">**идисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="057ae-108">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | <span data-ttu-id="057ae-109">Управляет дисковыми квотами для одного тома файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="057ae-109">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="057ae-110">**идисккуотаевентс**</span><span class="sxs-lookup"><span data-stu-id="057ae-110">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | <span data-ttu-id="057ae-111">Получает уведомления о событиях, связанных с квотами.</span><span class="sxs-lookup"><span data-stu-id="057ae-111">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="057ae-112">**идисккуотаусер**</span><span class="sxs-lookup"><span data-stu-id="057ae-112">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | <span data-ttu-id="057ae-113">Представляет одну запись пользовательской квоты в файле сведений о квотах тома.</span><span class="sxs-lookup"><span data-stu-id="057ae-113">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="057ae-114">**идисккуотаусербатч**</span><span class="sxs-lookup"><span data-stu-id="057ae-114">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | <span data-ttu-id="057ae-115">Добавляет несколько пользовательских объектов квоты в контейнер, который затем отправляется для обновления в одном вызове.</span><span class="sxs-lookup"><span data-stu-id="057ae-115">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="057ae-116">**иенумдисккуотаусерс**</span><span class="sxs-lookup"><span data-stu-id="057ae-116">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | <span data-ttu-id="057ae-117">Перечисляет записи квоты пользователя на томе.</span><span class="sxs-lookup"><span data-stu-id="057ae-117">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

