---
description: Представляет сведения, поддерживаемые диспетчером секций, о диске, входящем в состав кластера.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: Структура DISK_CLUSTER_INFO (Нтдддиск. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663391"
---
# <a name="disk_cluster_info-structure"></a><span data-ttu-id="7810e-103">\_ \_ Структура сведений о КЛАСТЕРе диска</span><span class="sxs-lookup"><span data-stu-id="7810e-103">DISK\_CLUSTER\_INFO structure</span></span>

<span data-ttu-id="7810e-104">Представляет сведения, поддерживаемые диспетчером секций, о диске, входящем в состав кластера.</span><span class="sxs-lookup"><span data-stu-id="7810e-104">Represents information maintained on the partition manager about a disk that is part of a cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="7810e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7810e-105">Syntax</span></span>


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a><span data-ttu-id="7810e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="7810e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7810e-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="7810e-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="7810e-108">Номер версии.</span><span class="sxs-lookup"><span data-stu-id="7810e-108">The version number.</span></span> <span data-ttu-id="7810e-109">Это значение должно быть равно размеру этой структуры.</span><span class="sxs-lookup"><span data-stu-id="7810e-109">This value must be set to the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="7810e-110">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="7810e-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7810e-111">Сочетание флагов, связанных с дисками и кластерами.</span><span class="sxs-lookup"><span data-stu-id="7810e-111">A combination of flags related to disks and clusters.</span></span>



| <span data-ttu-id="7810e-112">Значение</span><span class="sxs-lookup"><span data-stu-id="7810e-112">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="7810e-113">Значение</span><span class="sxs-lookup"><span data-stu-id="7810e-113">Meaning</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <span data-ttu-id="7810e-114"><dt>**Диск \_ \_Флаг кластера \_ включен**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7810e-114"><dt>**DISK\_CLUSTER\_FLAG\_ENABLED**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="7810e-115">Диск используется как часть службы кластеров.</span><span class="sxs-lookup"><span data-stu-id="7810e-115">The disk is used as part of the cluster service.</span></span><br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <span data-ttu-id="7810e-116"><dt>**Диск \_ \_Флаг кластера \_ CSV**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7810e-116"><dt>**DISK\_CLUSTER\_FLAG\_CSV**</dt> <dt>2</dt></span></span> </dl>                                                      | <span data-ttu-id="7810e-117">Тома на диске публикуются CSVFS на всех узлах кластера.</span><span class="sxs-lookup"><span data-stu-id="7810e-117">Volumes on the disk are exposed by CSVFS on all nodes of the cluster.</span></span><br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <span data-ttu-id="7810e-118"><dt>**Диск \_ \_Флаг кластера \_ в \_ обслуживании**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7810e-118"><dt>**DISK\_CLUSTER\_FLAG\_IN\_MAINTENANCE**</dt> <dt>4</dt></span></span> </dl>                    | <span data-ttu-id="7810e-119">Ресурс кластера, связанный с этим диском, находится в режиме обслуживания.</span><span class="sxs-lookup"><span data-stu-id="7810e-119">The cluster resource associated with this disk is in maintenance mode.</span></span><br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <span data-ttu-id="7810e-120"><dt>**Диск \_ Установка \_ флага кластера о \_ \_ получении PnP \_ завершена**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="7810e-120"><dt>**DISK\_CLUSTER\_FLAG\_PNP\_ARRIVAL\_COMPLETE**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="7810e-121">Драйвер диска кластера для режима ядра (Clusdisk) получил уведомление PnP о поступлении диска.</span><span class="sxs-lookup"><span data-stu-id="7810e-121">The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the disk.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7810e-122">**флагсмаск**</span><span class="sxs-lookup"><span data-stu-id="7810e-122">**FlagsMask**</span></span>
</dt> <dd>

<span data-ttu-id="7810e-123">Флаги, изменяемые в элементе **flags** .</span><span class="sxs-lookup"><span data-stu-id="7810e-123">The flags that are being modified in the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="7810e-124">**Уведомление**</span><span class="sxs-lookup"><span data-stu-id="7810e-124">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="7810e-125">**Значение true** , чтобы отправить уведомление об изменении макета; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="7810e-125">**TRUE** to send a layout change notification; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7810e-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7810e-126">Requirements</span></span>



| <span data-ttu-id="7810e-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7810e-127">Requirement</span></span> | <span data-ttu-id="7810e-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7810e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7810e-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7810e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7810e-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7810e-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="7810e-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7810e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7810e-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7810e-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7810e-133">Header</span><span class="sxs-lookup"><span data-stu-id="7810e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7810e-134"><dt>Нтдддиск. h</dt></span><span class="sxs-lookup"><span data-stu-id="7810e-134"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7810e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7810e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7810e-136">Структуры управления дисками</span><span class="sxs-lookup"><span data-stu-id="7810e-136">Disk Management Structures</span></span>](disk-management-structures.md)
</dt> <dt>

[<span data-ttu-id="7810e-137">**IOCTL \_ Disk \_ Получение \_ \_ сведений о кластере**</span><span class="sxs-lookup"><span data-stu-id="7810e-137">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="7810e-138">**\_ \_ сведения о наборе дисков для \_ кластера ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="7810e-138">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




