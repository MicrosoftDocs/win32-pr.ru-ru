---
description: Описывает два типа ограничений дисковой квоты и способ измерения дисковой квоты.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Ограничения дисковой квоты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663606"
---
# <a name="disk-quota-limits"></a><span data-ttu-id="1c72d-103">Ограничения дисковой квоты</span><span class="sxs-lookup"><span data-stu-id="1c72d-103">Disk Quota Limits</span></span>

<span data-ttu-id="1c72d-104">Место на диске, используемое каждым файлом, наследуется непосредственно пользователю, владеющему файлом.</span><span class="sxs-lookup"><span data-stu-id="1c72d-104">The disk space that each file uses is charged directly to the user who owns the file.</span></span> <span data-ttu-id="1c72d-105">Владелец файла определяется идентификатором безопасности (SID) в сведениях о безопасности для файла.</span><span class="sxs-lookup"><span data-stu-id="1c72d-105">The owner of a file is identified by the security identifier (SID) in the security information for the file.</span></span> <span data-ttu-id="1c72d-106">Общим объемом дискового пространства, выданного пользователю, является сумма длины всех потоков данных.</span><span class="sxs-lookup"><span data-stu-id="1c72d-106">The total disk space charged to a user is the sum of the length of all data streams.</span></span> <span data-ttu-id="1c72d-107">Иными словами, потоки набора свойств и потоки данных резидентных пользователей влияют на квоту пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c72d-107">In other words, property set streams and resident user data streams affect the user's quota.</span></span>

<span data-ttu-id="1c72d-108">Квота не насчитывается за точки повторного синтаксического анализа, дескрипторы безопасности или другие метаданные, связанные с файлами.</span><span class="sxs-lookup"><span data-stu-id="1c72d-108">Quota is not charged for re-parse points, security descriptors, or other metadata that is associated with the files.</span></span> <span data-ttu-id="1c72d-109">Сжатие или распаковка файлов не влияет на дисковое пространство, сообщаемое для файлов.</span><span class="sxs-lookup"><span data-stu-id="1c72d-109">Compressing or decompressing files does not affect the disk space reported for the files.</span></span> <span data-ttu-id="1c72d-110">Поэтому параметры квот на одном томе можно сравнить с параметрами на другом томе.</span><span class="sxs-lookup"><span data-stu-id="1c72d-110">Therefore, quota settings on one volume can be compared to settings on another volume.</span></span>

<span data-ttu-id="1c72d-111">Существует два типа ограничения дисковой квоты, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1c72d-111">There are two types of disk quota limits, as shown in the following table.</span></span>



| <span data-ttu-id="1c72d-112">Ограничение</span><span class="sxs-lookup"><span data-stu-id="1c72d-112">Limit</span></span>                        | <span data-ttu-id="1c72d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1c72d-113">Description</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c72d-114">Пороговое значение предупреждения</span><span class="sxs-lookup"><span data-stu-id="1c72d-114">Warning threshold</span></span><br/> | <span data-ttu-id="1c72d-115">Можно настроить систему для создания записи системного журнала, если объем дискового пространства, заданный пользователю, превысит это значение.</span><span class="sxs-lookup"><span data-stu-id="1c72d-115">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="1c72d-116">Жесткая квота</span><span class="sxs-lookup"><span data-stu-id="1c72d-116">Hard quota</span></span><br/>        | <span data-ttu-id="1c72d-117">Можно настроить систему для создания записи системного журнала, если объем дискового пространства, заданный пользователю, превысит это значение.</span><span class="sxs-lookup"><span data-stu-id="1c72d-117">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span> <span data-ttu-id="1c72d-118">Кроме того, можно настроить систему на запрет дополнительного места на диске при превышении этого значения дискового пространства, установленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="1c72d-118">You can also configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.</span></span><br/> |



 

<span data-ttu-id="1c72d-119">При первой записи пользователя в том файловая система NTFS автоматически создает запись квоты пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c72d-119">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="1c72d-120">Создаваемым записям автоматически присваиваются пороговые значения предупреждения по умолчанию и фиксированная квота для тома.</span><span class="sxs-lookup"><span data-stu-id="1c72d-120">Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume.</span></span>

 

 




