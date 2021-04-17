---
description: Администраторы могут управлять объемом данных, которые каждый пользователь может хранить на томе файловой системы NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Управление квотами на диск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684362"
---
# <a name="managing-disk-quotas"></a><span data-ttu-id="12995-103">Управление квотами на диск</span><span class="sxs-lookup"><span data-stu-id="12995-103">Managing Disk Quotas</span></span>

<span data-ttu-id="12995-104">Файловая система NTFS поддерживает *дисковые квоты*, которые позволяют администраторам управлять объемом данных, которые каждый пользователь может хранить на томе файловой системы NTFS.</span><span class="sxs-lookup"><span data-stu-id="12995-104">The NTFS file system supports *disk quotas*, which allow administrators to control the amount of data that each user can store on an NTFS file system volume.</span></span> <span data-ttu-id="12995-105">Администраторы могут при необходимости настроить систему для регистрации событий, когда пользователи близки к своей квоте, а также отклонять дополнительное место на диске для пользователей, которые превышают их квоты.</span><span class="sxs-lookup"><span data-stu-id="12995-105">Administrators can optionally configure the system to log an event when users are near their quota, and to deny further disk space to users who exceed their quota.</span></span> <span data-ttu-id="12995-106">Администраторы также могут создавать отчеты и использовать монитор событий для отслеживания проблем с квотами.</span><span class="sxs-lookup"><span data-stu-id="12995-106">Administrators can also generate reports, and use the event monitor to track quota issues.</span></span>

<span data-ttu-id="12995-107">Определить, поддерживает ли файловая система квоты диска, можно путем вызова функции [**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) и проверки флага bit для **файловой системы \_ \_ квот** .</span><span class="sxs-lookup"><span data-stu-id="12995-107">You can determine whether a file system supports disk quotas by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_VOLUME\_QUOTAS** bit flag.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12995-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="12995-108">In this section</span></span>



| <span data-ttu-id="12995-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="12995-109">Topic</span></span>                                                                                                   | <span data-ttu-id="12995-110">Описание</span><span class="sxs-lookup"><span data-stu-id="12995-110">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12995-111">Администрирование дисковых квот на уровне пользователя</span><span class="sxs-lookup"><span data-stu-id="12995-111">User-level Administration of Disk Quotas</span></span>](user-level-administration-of-disk-quotas.md)<br/>     | <span data-ttu-id="12995-112">Как получить больше свободного места на диске после превышения квоты.</span><span class="sxs-lookup"><span data-stu-id="12995-112">How to get more free disk space after exceeding the quota allowance.</span></span><br/>                                                                  |
| [<span data-ttu-id="12995-113">Администрирование дисковых квот на уровне системы</span><span class="sxs-lookup"><span data-stu-id="12995-113">System-level Administration of Disk Quotas</span></span>](system-level-administration-of-disk-quotas.md)<br/> | <span data-ttu-id="12995-114">Системный администратор может устанавливать квоты для конкретных пользователей на томе.</span><span class="sxs-lookup"><span data-stu-id="12995-114">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="12995-115">Администратор также может задать квоты по умолчанию для тома.</span><span class="sxs-lookup"><span data-stu-id="12995-115">The administrator can also set default quotas for the volume.</span></span><br/> |
| [<span data-ttu-id="12995-116">Ограничения дисковой квоты</span><span class="sxs-lookup"><span data-stu-id="12995-116">Disk Quota Limits</span></span>](disk-quota-limits.md)<br/>                                                   | <span data-ttu-id="12995-117">Описывает два типа ограничений дисковой квоты и способ измерения дисковой квоты.</span><span class="sxs-lookup"><span data-stu-id="12995-117">Describes two types of disk quota limits and how disk quota limits are measured.</span></span><br/>                                                      |
| [<span data-ttu-id="12995-118">Интерфейсы дисковой квоты</span><span class="sxs-lookup"><span data-stu-id="12995-118">Disk Quota Interfaces</span></span>](disk-quota-interfaces.md)<br/>                                           | <span data-ttu-id="12995-119">Интерфейсы, используемые с квотами диска.</span><span class="sxs-lookup"><span data-stu-id="12995-119">Interfaces used with disk quotas.</span></span><br/>                                                                                                     |



 

 

 




