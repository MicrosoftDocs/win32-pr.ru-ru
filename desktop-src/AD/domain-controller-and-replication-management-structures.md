---
title: Структуры управления репликацией и контроллером домена
description: В контроллерах домена и функциях управления репликацией используются следующие структуры.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afe084e4285f4851457f9a519e747952e3bbd67
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890436"
---
# <a name="domain-controller-and-replication-management-structures"></a><span data-ttu-id="ed39b-103">Структуры управления репликацией и контроллером домена</span><span class="sxs-lookup"><span data-stu-id="ed39b-103">Domain Controller and Replication Management Structures</span></span>

<span data-ttu-id="ed39b-104">Контроллеры домена и функции управления репликацией используют следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="ed39b-104">The domain controller and replication management functions use the following structures:</span></span>

-   [<span data-ttu-id="ed39b-105">**\_ \_ Сведения об контроллере домена DS \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ed39b-105">**DS\_DOMAIN\_CONTROLLER\_INFO\_1**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [<span data-ttu-id="ed39b-106">**\_ \_ Сведения о контроллере домена DS \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed39b-106">**DS\_DOMAIN\_CONTROLLER\_INFO\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [<span data-ttu-id="ed39b-107">**\_ \_ Сведения об контроллере домена DS \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ed39b-107">**DS\_DOMAIN\_CONTROLLER\_INFO\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [<span data-ttu-id="ed39b-108">**\_результат имени \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-108">**DS\_NAME\_RESULT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [<span data-ttu-id="ed39b-109">**\_ \_ элемент результата имени \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-109">**DS\_NAME\_RESULT\_ITEM**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [<span data-ttu-id="ed39b-110">**\_ \_ метаданные attr для DS REPL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-110">**DS\_REPL\_ATTR\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [<span data-ttu-id="ed39b-111">**Службы DS \_ REPL, \_ \_ метаданные \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed39b-111">**DS\_REPL\_ATTR\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [<span data-ttu-id="ed39b-112">**\_BLOB- \_ \_ \_ объект метаданных attr \_ для DS REPL**</span><span class="sxs-lookup"><span data-stu-id="ed39b-112">**DS\_REPL\_ATTR\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [<span data-ttu-id="ed39b-113">**\_ \_ \_ метаданные значения attr \_ \_ для DS REPL**</span><span class="sxs-lookup"><span data-stu-id="ed39b-113">**DS\_REPL\_ATTR\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [<span data-ttu-id="ed39b-114">**\_Метаданные для \_ значения attr для DS REPL \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed39b-114">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [<span data-ttu-id="ed39b-115">**\_ \_ \_ \_ расширение МЕТАДАННЫХ значения \_ attr \_ для DS REPL**</span><span class="sxs-lookup"><span data-stu-id="ed39b-115">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [<span data-ttu-id="ed39b-116">**\_курсор REPL в DS \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-116">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [<span data-ttu-id="ed39b-117">**DS \_ REPL, \_ курсор \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed39b-117">**DS\_REPL\_CURSOR\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [<span data-ttu-id="ed39b-118">**\_Курсор репликации \_ DS \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ed39b-118">**DS\_REPL\_CURSOR\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [<span data-ttu-id="ed39b-119">**\_BLOB- \_ объект курсора REPL DS \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-119">**DS\_REPL\_CURSOR\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [<span data-ttu-id="ed39b-120">**\_курсоры REPL в DS \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-120">**DS\_REPL\_CURSORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [<span data-ttu-id="ed39b-121">**DS \_ REPL, \_ курсоры \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed39b-121">**DS\_REPL\_CURSORS\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [<span data-ttu-id="ed39b-122">**\_Курсоры REPL в DS \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ed39b-122">**DS\_REPL\_CURSORS\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [<span data-ttu-id="ed39b-123">**\_сбой проверки \_ согласованности DS \_ DSA \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-123">**DS\_REPL\_KCC\_DSA\_FAILURE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [<span data-ttu-id="ed39b-124">**\_сбои проверки \_ согласованности DS \_ DSA \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-124">**DS\_REPL\_KCC\_DSA\_FAILURES**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [<span data-ttu-id="ed39b-125">**DS \_ REPL \_ KCC \_ DSA \_ фаилурев \_ BLOB**</span><span class="sxs-lookup"><span data-stu-id="ed39b-125">**DS\_REPL\_KCC\_DSA\_FAILUREW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [<span data-ttu-id="ed39b-126">**\_сосед DS REPL \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-126">**DS\_REPL\_NEIGHBOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [<span data-ttu-id="ed39b-127">**\_соседи DS REPL \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-127">**DS\_REPL\_NEIGHBORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [<span data-ttu-id="ed39b-128">**DS \_ REPL \_ неигхборв, \_ большой двоичный объект**</span><span class="sxs-lookup"><span data-stu-id="ed39b-128">**DS\_REPL\_NEIGHBORW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [<span data-ttu-id="ed39b-129">**\_ \_ метаданные obj- \_ \_ данных DS REPL**</span><span class="sxs-lookup"><span data-stu-id="ed39b-129">**DS\_REPL\_OBJ\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [<span data-ttu-id="ed39b-130">**DS \_ REPL \_ , \_ метаданные obj- \_ данных \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed39b-130">**DS\_REPL\_OBJ\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [<span data-ttu-id="ed39b-131">**DS \_ REPL, \_ операция**</span><span class="sxs-lookup"><span data-stu-id="ed39b-131">**DS\_REPL\_OP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [<span data-ttu-id="ed39b-132">**\_ \_ \_ большой двоичный объект для печати DS REPL**</span><span class="sxs-lookup"><span data-stu-id="ed39b-132">**DS\_REPL\_OPW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [<span data-ttu-id="ed39b-133">**\_ \_ ожидающих операций DS REPL \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-133">**DS\_REPL\_PENDING\_OPS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [<span data-ttu-id="ed39b-134">**DS \_ REPL \_ очереди \_ статистиксв**</span><span class="sxs-lookup"><span data-stu-id="ed39b-134">**DS\_REPL\_QUEUE\_STATISTICSW**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   <span data-ttu-id="ed39b-135">[**\_BLOB- \_ \_ объект статистиксв очереди DS REPL \_**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed39b-135">[**DS\_REPL\_QUEUE\_STATISTICSW\_BLOB**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span></span>
-   [<span data-ttu-id="ed39b-136">**\_ \_ метаданные значения REPL \_ для \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-136">**DS\_REPL\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [<span data-ttu-id="ed39b-137">**\_Метаданные для значения репликации DS REPL \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ed39b-137">**DS\_REPL\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [<span data-ttu-id="ed39b-138">**\_ \_ \_ расширение МЕТАДАННЫХ значения \_ \_ репликации DS REPL**</span><span class="sxs-lookup"><span data-stu-id="ed39b-138">**DS\_REPL\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [<span data-ttu-id="ed39b-139">**\_BLOB- \_ \_ \_ \_ объект метаданных значения REPL для DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-139">**DS\_REPL\_VALUE\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [<span data-ttu-id="ed39b-140">**\_ \_ \_ \_ \_ ext BLOB-объектов метаданных значения \_ репликации DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-140">**DS\_REPL\_VALUE\_META\_DATA\_BLOB\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [<span data-ttu-id="ed39b-141">**DS \_ репсинкалл \_ ерринфо**</span><span class="sxs-lookup"><span data-stu-id="ed39b-141">**DS\_REPSYNCALL\_ERRINFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [<span data-ttu-id="ed39b-142">**\_Синхронизация РЕПСИНКАЛЛ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-142">**DS\_REPSYNCALL\_SYNC**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [<span data-ttu-id="ed39b-143">**\_Обновление РЕПСИНКАЛЛ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-143">**DS\_REPSYNCALL\_UPDATE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [<span data-ttu-id="ed39b-144">**\_ \_ Таблица GUID схемы \_ DS**</span><span class="sxs-lookup"><span data-stu-id="ed39b-144">**DS\_SCHEMA\_GUID\_MAP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [<span data-ttu-id="ed39b-145">**\_ \_ сведения о стоимости сайта DS \_**</span><span class="sxs-lookup"><span data-stu-id="ed39b-145">**DS\_SITE\_COST\_INFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [<span data-ttu-id="ed39b-146">**Расписание**</span><span class="sxs-lookup"><span data-stu-id="ed39b-146">**SCHEDULE**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [<span data-ttu-id="ed39b-147">**\_заголовок расписания**</span><span class="sxs-lookup"><span data-stu-id="ed39b-147">**SCHEDULE\_HEADER**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a><span data-ttu-id="ed39b-148">См. также</span><span class="sxs-lookup"><span data-stu-id="ed39b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed39b-149">Структуры в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="ed39b-149">Structures in Active Directory Domain Services</span></span>](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 