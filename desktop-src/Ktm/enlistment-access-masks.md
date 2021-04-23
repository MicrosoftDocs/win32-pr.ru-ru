---
description: KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии зачислений.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Маски доступа прикрепления (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684454"
---
# <a name="enlistment-access-masks"></a><span data-ttu-id="d758b-103">Маски доступа прикрепления</span><span class="sxs-lookup"><span data-stu-id="d758b-103">Enlistment Access Masks</span></span>

<span data-ttu-id="d758b-104">KTM определяет следующие маски доступа прикрепления, которые будут использоваться при открытии зачислений.</span><span class="sxs-lookup"><span data-stu-id="d758b-104">KTM defines the following enlistment access masks to be used when opening enlistments.</span></span>

<dl> <dt>

<span data-ttu-id="d758b-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_сведения о запросе ПРИкрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**ENLISTMENT\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-106">Номера 0x00001</span><span class="sxs-lookup"><span data-stu-id="d758b-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="d758b-107">Вызывающий объект может запросить в KTM сведения о зачислении.</span><span class="sxs-lookup"><span data-stu-id="d758b-107">The caller can query KTM for information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_сведения о наборе ЗАчислений \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**ENLISTMENT\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="d758b-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="d758b-110">Вызывающий объект может задавать сведения о зачислении.</span><span class="sxs-lookup"><span data-stu-id="d758b-110">The caller can set information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**Восстановление прикрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="d758b-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="d758b-113">Вызывающий объект может восстановить зачисление.</span><span class="sxs-lookup"><span data-stu-id="d758b-113">The caller can recover an enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**\_подчиненные права ПРИкрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**ENLISTMENT\_SUBORDINATE\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="d758b-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="d758b-116">Вызывающий объект может выполнять действия, выполняемые диспетчером ресурсов от имени транзакции.</span><span class="sxs-lookup"><span data-stu-id="d758b-116">The caller can complete actions that a resource manager does on behalf of the transaction.</span></span> <span data-ttu-id="d758b-117">Ниже приведен список действий.</span><span class="sxs-lookup"><span data-stu-id="d758b-117">The following is a list of actions:</span></span>

-   [<span data-ttu-id="d758b-118">**коммиткомплете**</span><span class="sxs-lookup"><span data-stu-id="d758b-118">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="d758b-119">**препарекомплете**</span><span class="sxs-lookup"><span data-stu-id="d758b-119">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="d758b-120">**препрепарекомплете**</span><span class="sxs-lookup"><span data-stu-id="d758b-120">**PrePrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [<span data-ttu-id="d758b-121">**роллбакккомплете**</span><span class="sxs-lookup"><span data-stu-id="d758b-121">**RollbackComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [<span data-ttu-id="d758b-122">**реадонленлистмент**</span><span class="sxs-lookup"><span data-stu-id="d758b-122">**ReadOnlyEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [<span data-ttu-id="d758b-123">**роллбаккенлистмент**</span><span class="sxs-lookup"><span data-stu-id="d758b-123">**RollbackEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [<span data-ttu-id="d758b-124">**синглефасережект**</span><span class="sxs-lookup"><span data-stu-id="d758b-124">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**\_старшие права ПРИкрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ENLISTMENT\_SUPERIOR\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-126">0x00010</span><span class="sxs-lookup"><span data-stu-id="d758b-126">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="d758b-127">Вызывающий объект может быть прикреплен в транзакции в качестве старшего диспетчера транзакций.</span><span class="sxs-lookup"><span data-stu-id="d758b-127">The caller can enlist in the transaction as a superior transaction manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_универсальное чтение ПРИкрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-129">0x20001</span><span class="sxs-lookup"><span data-stu-id="d758b-129">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="d758b-130">Вызывающий объект имеет следующие привилегии: **стандартные \_ права на \_ Чтение** и **Прикрепление \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="d758b-130">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **ENLISTMENT\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_Универсальная запись ПРИкрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**ENLISTMENT\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-132">0x2001E</span><span class="sxs-lookup"><span data-stu-id="d758b-132">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="d758b-133">Вызывающий объект имеет следующие привилегии: **стандартные \_ права на \_ запись**, **\_ \_ сведения о наборе зачислений** и **Прикрепление к \_ восстановлению**.</span><span class="sxs-lookup"><span data-stu-id="d758b-133">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **ENLISTMENT\_SET\_INFORMATION**, and **ENLISTMENT\_RECOVER**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_универсальное выполнение ПРИкрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-135">0x2001C</span><span class="sxs-lookup"><span data-stu-id="d758b-135">0x2001C</span></span>
</dt> <dt>



<span data-ttu-id="d758b-136">Вызывающий объект имеет следующие привилегии **: \_ \_ выполнение стандартных прав**, **\_ Восстановление прикрепления** и **\_ подчиненные \_ права прикрепления**.</span><span class="sxs-lookup"><span data-stu-id="d758b-136">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **ENLISTMENT\_RECOVER**, and **ENLISTMENT\_SUBORDINATE\_RIGHTS**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d758b-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**\_доступ ко всем операциям ПРИкрепления \_**</span><span class="sxs-lookup"><span data-stu-id="d758b-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ENLISTMENT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d758b-138">0xF001F</span><span class="sxs-lookup"><span data-stu-id="d758b-138">0xF001F</span></span>
</dt> <dt>



<span data-ttu-id="d758b-139">Это значение задает все допустимые биты для значения доступа к зачислению.</span><span class="sxs-lookup"><span data-stu-id="d758b-139">This value sets all valid bits for an enlistment access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d758b-140">Требования</span><span class="sxs-lookup"><span data-stu-id="d758b-140">Requirements</span></span>



| <span data-ttu-id="d758b-141">Требование</span><span class="sxs-lookup"><span data-stu-id="d758b-141">Requirement</span></span> | <span data-ttu-id="d758b-142">Значение</span><span class="sxs-lookup"><span data-stu-id="d758b-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d758b-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d758b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d758b-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d758b-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="d758b-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d758b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d758b-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d758b-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="d758b-147">Header</span><span class="sxs-lookup"><span data-stu-id="d758b-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d758b-148"><dt>Файл WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d758b-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




