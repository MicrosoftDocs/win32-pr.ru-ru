---
description: KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера ресурсов.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Маски доступа диспетчер ресурсов (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156363"
---
# <a name="resource-manager-access-masks"></a><span data-ttu-id="dba45-103">Маски доступа диспетчер ресурсов</span><span class="sxs-lookup"><span data-stu-id="dba45-103">Resource Manager Access Masks</span></span>

<span data-ttu-id="dba45-104">KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии диспетчера ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dba45-104">KTM defines the following enlistment access masks to be used when opening a resource manager.</span></span>

<dl> <dt>

<span data-ttu-id="dba45-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_ \_ сведения о запросе RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="dba45-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-106">Вызывающий объект может запрашивать сведения об Resource Manager (RM).</span><span class="sxs-lookup"><span data-stu-id="dba45-106">The caller can query for the resource manager (RM) information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_сведения о наборе RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="dba45-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-108">Вызывающий объект может задать сведения об RM.</span><span class="sxs-lookup"><span data-stu-id="dba45-108">The caller can set the RM information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**\_Восстановление RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="dba45-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-110">Вызывающий объект может восстановить указанное RM.</span><span class="sxs-lookup"><span data-stu-id="dba45-110">The caller can recover the specified RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**Прикрепление RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="dba45-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-112">Вызывающий объект может прикрепить RM в транзакции.</span><span class="sxs-lookup"><span data-stu-id="dba45-112">The caller can enlist an RM in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_ \_ уведомление о получении RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="dba45-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER\_GET\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-114">Вызывающий объект может получить уведомление для RM.</span><span class="sxs-lookup"><span data-stu-id="dba45-114">The caller can receive a notification for an RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_универсальное \_ Чтение RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="dba45-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-116">Вызывающий объект имеет следующие привилегии: стандартные \_ права на \_ Чтение \_ , \_ сведения о запросе ResourceManager и \_ Восстановление ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="dba45-116">The caller has the following privileges: STANDARD\_RIGHTS\_READ, RESOURCEMANAGER\_QUERY\_INFORMATION, and RESOURCEMANAGER\_RECOVER.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_Универсальная \_ запись RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="dba45-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-118">Вызывающий объект имеет следующие привилегии: \_ запись стандартных прав \_ , \_ сведения о наборе ResourceManager, \_ \_ Прикрепление RESOURCEMANAGER и \_ \_ уведомление о получении ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="dba45-118">The caller has the following privileges: STANDARD\_RIGHTS\_WRITE, RESOURCEMANAGER\_SET\_INFORMATION, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_универсальный \_ Запуск RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="dba45-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-120">Вызывающий объект имеет следующие привилегии: \_ выполнение стандартных прав \_ , \_ Прикрепление диспетчера ресурсов \_ и \_ уведомление о получении ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="dba45-120">The caller has the following privileges: STANDARD\_RIGHTS\_EXECUTE, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dba45-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_все \_ доступ RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="dba45-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="dba45-122">У вызывающего объекта есть следующие права: \_ требуются стандартные права \_ .</span><span class="sxs-lookup"><span data-stu-id="dba45-122">The caller has the following privilege: STANDARD\_RIGHTS\_REQUIRED.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dba45-123">Требования</span><span class="sxs-lookup"><span data-stu-id="dba45-123">Requirements</span></span>



| <span data-ttu-id="dba45-124">Требование</span><span class="sxs-lookup"><span data-stu-id="dba45-124">Requirement</span></span> | <span data-ttu-id="dba45-125">Значение</span><span class="sxs-lookup"><span data-stu-id="dba45-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dba45-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dba45-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dba45-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dba45-127">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="dba45-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dba45-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dba45-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dba45-129">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="dba45-130">Header</span><span class="sxs-lookup"><span data-stu-id="dba45-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dba45-131"><dt>Файл WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="dba45-131"><dt>WinNT.h</dt></span></span> </dl> |



 

 




