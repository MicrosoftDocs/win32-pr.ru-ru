---
description: Описание кодов ошибок 4000-5999, определенных в файле заголовка WinError. h и предназначенных для разработчиков.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Коды системных ошибок (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141614"
---
# <a name="system-error-codes-4000-5999"></a><span data-ttu-id="1472b-103">Коды системных ошибок (4000-5999)</span><span class="sxs-lookup"><span data-stu-id="1472b-103">System Error Codes (4000-5999)</span></span>

> [!NOTE]
> <span data-ttu-id="1472b-104">Эти сведения предназначены для разработчиков, которые отлаживать системные ошибки.</span><span class="sxs-lookup"><span data-stu-id="1472b-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="1472b-105">Для других ошибок, например проблем с Центр обновления Windows, на странице [коды ошибок](system-error-codes.md) содержится список ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1472b-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="1472b-106">В следующем списке приведены [коды системных ошибок](system-error-codes.md) для ошибок 4000 – 5999.</span><span class="sxs-lookup"><span data-stu-id="1472b-106">The following list describes [system error codes](system-error-codes.md) for errors 4000 to 5999.</span></span> <span data-ttu-id="1472b-107">Они возвращаются функцией [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) при сбое множества функций.</span><span class="sxs-lookup"><span data-stu-id="1472b-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="1472b-108">Чтобы получить текст описания ошибки в приложении, используйте функцию [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) с флагом **формата \_ Message \_ из \_ System** .</span><span class="sxs-lookup"><span data-stu-id="1472b-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="1472b-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**\_Внутренняя ошибка WINS \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR\_WINS\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-110">4000 (0xFA0)</span><span class="sxs-lookup"><span data-stu-id="1472b-110">4000 (0xFA0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-111">При обработке команды произошла ошибка WINS.</span><span class="sxs-lookup"><span data-stu-id="1472b-111">WINS encountered an error while processing the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**Ошибка \_ не может быть \_ \_ Del \_ локальную \_ службу WINS**</span><span class="sxs-lookup"><span data-stu-id="1472b-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR\_CAN\_NOT\_DEL\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-113">4001 (0xFA1)</span><span class="sxs-lookup"><span data-stu-id="1472b-113">4001 (0xFA1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-114">Невозможно удалить локальный WINS-сервер.</span><span class="sxs-lookup"><span data-stu-id="1472b-114">The local WINS cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**Ошибка при \_ статической \_ инициализации**</span><span class="sxs-lookup"><span data-stu-id="1472b-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR\_STATIC\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-116">4002 (0xFA2)</span><span class="sxs-lookup"><span data-stu-id="1472b-116">4002 (0xFA2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-117">Не удалось выполнить импорт из файла.</span><span class="sxs-lookup"><span data-stu-id="1472b-117">The importation from the file failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**\_Архив ошибок Inc \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR\_INC\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-119">4003 (0xFA3)</span><span class="sxs-lookup"><span data-stu-id="1472b-119">4003 (0xFA3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-120">Сбой резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="1472b-120">The backup failed.</span></span> <span data-ttu-id="1472b-121">Было ли выполнено полное резервное копирование ранее?</span><span class="sxs-lookup"><span data-stu-id="1472b-121">Was a full backup done before?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**Ошибка \_ полной \_ архивации**</span><span class="sxs-lookup"><span data-stu-id="1472b-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR\_FULL\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-123">4004 (0xFA4)</span><span class="sxs-lookup"><span data-stu-id="1472b-123">4004 (0xFA4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-124">Сбой резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="1472b-124">The backup failed.</span></span> <span data-ttu-id="1472b-125">Проверьте каталог, в котором выполняется резервное копирование базы данных.</span><span class="sxs-lookup"><span data-stu-id="1472b-125">Check the directory to which you are backing the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**Ошибка \_ REC \_ не \_ существует**</span><span class="sxs-lookup"><span data-stu-id="1472b-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR\_REC\_NON\_EXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-127">4005 (0xFA5)</span><span class="sxs-lookup"><span data-stu-id="1472b-127">4005 (0xFA5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-128">Имя не существует в базе данных WINS.</span><span class="sxs-lookup"><span data-stu-id="1472b-128">The name does not exist in the WINS database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**Ошибка \_ RPL \_ не \_ разрешена**</span><span class="sxs-lookup"><span data-stu-id="1472b-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERROR\_RPL\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-130">4006 (0xFA6)</span><span class="sxs-lookup"><span data-stu-id="1472b-130">4006 (0xFA6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-131">Репликация с ненастроенным партнером не разрешена.</span><span class="sxs-lookup"><span data-stu-id="1472b-131">Replication with a nonconfigured partner is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**\_Ошибка \_ контентинфо \_ версия \_ не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="1472b-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**PEERDIST\_ERROR\_CONTENTINFO\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-133">4050 (0xFD2)</span><span class="sxs-lookup"><span data-stu-id="1472b-133">4050 (0xFD2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-134">Версия предоставляемых сведений о содержимом не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1472b-134">The version of the supplied content information is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_Ошибка в \_ удалось \_ проанализировать \_ контентинфо**</span><span class="sxs-lookup"><span data-stu-id="1472b-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST\_ERROR\_CANNOT\_PARSE\_CONTENTINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-136">4051 (0xFD3)</span><span class="sxs-lookup"><span data-stu-id="1472b-136">4051 (0xFD3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-137">Указанная информация о содержимом неправильно сформирована.</span><span class="sxs-lookup"><span data-stu-id="1472b-137">The supplied content information is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**Ошибка в сведениях о том, что \_ \_ \_ данные отсутствуют**</span><span class="sxs-lookup"><span data-stu-id="1472b-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**PEERDIST\_ERROR\_MISSING\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-139">4052 (0xFD4)</span><span class="sxs-lookup"><span data-stu-id="1472b-139">4052 (0xFD4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-140">Запрошенные данные не могут быть найдены в локальных и одноранговых кэшах.</span><span class="sxs-lookup"><span data-stu-id="1472b-140">The requested data cannot be found in local or peer caches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**Ошибка в некотором сообщении о наличии \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST\_ERROR\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-142">4053 (0xFD5)</span><span class="sxs-lookup"><span data-stu-id="1472b-142">4053 (0xFD5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-143">Дополнительные данные недоступны или не требуются.</span><span class="sxs-lookup"><span data-stu-id="1472b-143">No more data is available or required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**ошибка, которая \_ \_ не была \_ инициализирована.**</span><span class="sxs-lookup"><span data-stu-id="1472b-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**PEERDIST\_ERROR\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-145">4054 (0xFD6)</span><span class="sxs-lookup"><span data-stu-id="1472b-145">4054 (0xFD6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-146">Предоставленный объект не был инициализирован.</span><span class="sxs-lookup"><span data-stu-id="1472b-146">The supplied object has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**ошибка, которая \_ \_ уже \_ инициализирована, не выполнена**</span><span class="sxs-lookup"><span data-stu-id="1472b-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**PEERDIST\_ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-148">4055 (0xFD7)</span><span class="sxs-lookup"><span data-stu-id="1472b-148">4055 (0xFD7)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-149">Предоставленный объект уже инициализирован.</span><span class="sxs-lookup"><span data-stu-id="1472b-149">The supplied object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_ \_ выполняется завершение работы \_ с ошибкой в списке \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST\_ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-151">4056 (0xFD8)</span><span class="sxs-lookup"><span data-stu-id="1472b-151">4056 (0xFD8)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-152">Операция завершения работы уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="1472b-152">A shutdown operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**ошибка, которая \_ \_ стала недействительной**</span><span class="sxs-lookup"><span data-stu-id="1472b-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**PEERDIST\_ERROR\_INVALIDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-154">4057 (0xFD9)</span><span class="sxs-lookup"><span data-stu-id="1472b-154">4057 (0xFD9)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-155">Предоставленный объект уже недействителен.</span><span class="sxs-lookup"><span data-stu-id="1472b-155">The supplied object has already been invalidated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**\_возникла ошибка, которая \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="1472b-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**PEERDIST\_ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-157">4058 (0xFDA)</span><span class="sxs-lookup"><span data-stu-id="1472b-157">4058 (0xFDA)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-158">Элемент уже существует и не был заменен.</span><span class="sxs-lookup"><span data-stu-id="1472b-158">An element already exists and was not replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**\_Ошибка \_ NotFound, операция \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST\_ERROR\_OPERATION\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-160">4059 (0xFDB)</span><span class="sxs-lookup"><span data-stu-id="1472b-160">4059 (0xFDB)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-161">Невозможно отменить запрошенную операцию, так как она уже завершена.</span><span class="sxs-lookup"><span data-stu-id="1472b-161">Can not cancel the requested operation as it has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**ошибка, которая \_ \_ уже \_ завершена**</span><span class="sxs-lookup"><span data-stu-id="1472b-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**PEERDIST\_ERROR\_ALREADY\_COMPLETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-163">4060 (0xFDC)</span><span class="sxs-lookup"><span data-stu-id="1472b-163">4060 (0xFDC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-164">Невозможно выполнить операцию запрошена, так как она уже была выполнена.</span><span class="sxs-lookup"><span data-stu-id="1472b-164">Can not perform the reqested operation because it has already been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_Ошибка \_ \_ , \_ связанная с нехваткой границ**</span><span class="sxs-lookup"><span data-stu-id="1472b-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST\_ERROR\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-166">4061 (0xFDD)</span><span class="sxs-lookup"><span data-stu-id="1472b-166">4061 (0xFDD)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-167">Операция обратилась к данным за границами допустимых данных.</span><span class="sxs-lookup"><span data-stu-id="1472b-167">An operation accessed data beyond the bounds of valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**\_версия ошибки, которую \_ \_ не поддерживает, не поддерживается**</span><span class="sxs-lookup"><span data-stu-id="1472b-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**PEERDIST\_ERROR\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-169">4062 (0xFDE)</span><span class="sxs-lookup"><span data-stu-id="1472b-169">4062 (0xFDE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-170">Запрошенная версия не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1472b-170">The requested version is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**ошибка, которая является \_ \_ недопустимой \_ конфигурацией**</span><span class="sxs-lookup"><span data-stu-id="1472b-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST\_ERROR\_INVALID\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-172">4063 (0xFDF)</span><span class="sxs-lookup"><span data-stu-id="1472b-172">4063 (0xFDF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-173">Недопустимое значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1472b-173">A configuration value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**Ошибка продукта, которая \_ \_ не \_ лицензирована**</span><span class="sxs-lookup"><span data-stu-id="1472b-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**PEERDIST\_ERROR\_NOT\_LICENSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-175">4064 (0xFE0)</span><span class="sxs-lookup"><span data-stu-id="1472b-175">4064 (0xFE0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-176">Номер SKU не лицензирован.</span><span class="sxs-lookup"><span data-stu-id="1472b-176">The SKU is not licensed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_Служба ошибок в \_ пакетах обновления \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="1472b-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**PEERDIST\_ERROR\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-178">4065 (0xFE1)</span><span class="sxs-lookup"><span data-stu-id="1472b-178">4065 (0xFE1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-179">Служба, которая по-прежнему инициализируется, будет доступна в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="1472b-179">PeerDist Service is still initializing and will be available shortly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**\_ \_ сбой при доверии для ошибки, \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST\_ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-181">4066 (0xFE2)</span><span class="sxs-lookup"><span data-stu-id="1472b-181">4066 (0xFE2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-182">Связь с одним или несколькими компьютерами будет временно заблокирована из-за последних ошибок.</span><span class="sxs-lookup"><span data-stu-id="1472b-182">Communication with one or more computers will be temporarily blocked due to recent errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**Ошибка \_ при \_ конфликте DHCP-адресов \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR\_DHCP\_ADDRESS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-184">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="1472b-184">4100 (0x1004)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-185">DHCP-клиент получил IP-адрес, который уже используется в сети.</span><span class="sxs-lookup"><span data-stu-id="1472b-185">The DHCP client has obtained an IP address that is already in use on the network.</span></span> <span data-ttu-id="1472b-186">Локальный интерфейс будет отключен до тех пор, пока DHCP-клиент не сможет получить новый адрес.</span><span class="sxs-lookup"><span data-stu-id="1472b-186">The local interface will be disabled until the DHCP client can obtain a new address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**Ошибка \_ \_ GUID WMI \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR\_WMI\_GUID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-188">4200 (0x1068)</span><span class="sxs-lookup"><span data-stu-id="1472b-188">4200 (0x1068)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-189">Переданный идентификатор GUID не распознан поставщиком данных WMI как допустимый.</span><span class="sxs-lookup"><span data-stu-id="1472b-189">The GUID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**экземпляр WMI об ОШИБКе \_ \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR\_WMI\_INSTANCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-191">4201 (0x1069)</span><span class="sxs-lookup"><span data-stu-id="1472b-191">4201 (0x1069)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-192">Переданное имя экземпляра не было распознано поставщиком данных WMI как допустимое.</span><span class="sxs-lookup"><span data-stu-id="1472b-192">The instance name passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ОШИБКА с \_ WMI \_ ITEMID \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR\_WMI\_ITEMID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-194">4202 (0x106A)</span><span class="sxs-lookup"><span data-stu-id="1472b-194">4202 (0x106A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-195">Переданный идентификатор элемента данных не распознан поставщиком данных WMI как допустимый.</span><span class="sxs-lookup"><span data-stu-id="1472b-195">The data item ID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**Ошибка \_ WMI \_ \_ Повторная попытка**</span><span class="sxs-lookup"><span data-stu-id="1472b-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR\_WMI\_TRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-197">4203 (0x106B)</span><span class="sxs-lookup"><span data-stu-id="1472b-197">4203 (0x106B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-198">Не удалось выполнить запрос WMI и повторить попытку.</span><span class="sxs-lookup"><span data-stu-id="1472b-198">The WMI request could not be completed and should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**Ошибка \_ " \_ точка распространения WMI \_ не \_ найдена"**</span><span class="sxs-lookup"><span data-stu-id="1472b-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR\_WMI\_DP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-200">4204 (0x106C)</span><span class="sxs-lookup"><span data-stu-id="1472b-200">4204 (0x106C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-201">Не удалось найти поставщик данных WMI.</span><span class="sxs-lookup"><span data-stu-id="1472b-201">The WMI data provider could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**Ошибка \_ \_ ссылки на неразрешенный \_ экземпляр WMI \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR\_WMI\_UNRESOLVED\_INSTANCE\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-203">4205 (0x106D)</span><span class="sxs-lookup"><span data-stu-id="1472b-203">4205 (0x106D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-204">Поставщик данных WMI ссылается на набор экземпляров, который не был зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="1472b-204">The WMI data provider references an instance set that has not been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**Ошибка \_ WMI \_ уже \_ включена**</span><span class="sxs-lookup"><span data-stu-id="1472b-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR\_WMI\_ALREADY\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-206">4206 (0x106E)</span><span class="sxs-lookup"><span data-stu-id="1472b-206">4206 (0x106E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-207">Блок данных WMI или уведомление о событии уже включены.</span><span class="sxs-lookup"><span data-stu-id="1472b-207">The WMI data block or event notification has already been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**Ошибка \_ при \_ \_ отключении GUID WMI**</span><span class="sxs-lookup"><span data-stu-id="1472b-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR\_WMI\_GUID\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-209">4207 (0x106F)</span><span class="sxs-lookup"><span data-stu-id="1472b-209">4207 (0x106F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-210">Блок данных WMI больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="1472b-210">The WMI data block is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**Ошибка \_ \_ Сервер WMI \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR\_WMI\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-212">4208 (0x1070)</span><span class="sxs-lookup"><span data-stu-id="1472b-212">4208 (0x1070)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-213">Служба данных WMI недоступна.</span><span class="sxs-lookup"><span data-stu-id="1472b-213">The WMI data service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**Ошибка \_ WMI \_ DP \_ при сбое**</span><span class="sxs-lookup"><span data-stu-id="1472b-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR\_WMI\_DP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-215">4209 (0x1071)</span><span class="sxs-lookup"><span data-stu-id="1472b-215">4209 (0x1071)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-216">Поставщику данных WMI не удалось выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="1472b-216">The WMI data provider failed to carry out the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**Ошибка \_ WMI- \_ Недопустимый \_ MOF**</span><span class="sxs-lookup"><span data-stu-id="1472b-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR\_WMI\_INVALID\_MOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-218">4210 (0x1072)</span><span class="sxs-lookup"><span data-stu-id="1472b-218">4210 (0x1072)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-219">Сведения об WMI MOF недопустимы.</span><span class="sxs-lookup"><span data-stu-id="1472b-219">The WMI MOF information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**Ошибка \_ WMI \_ Недопустимая \_ регинфо**</span><span class="sxs-lookup"><span data-stu-id="1472b-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR\_WMI\_INVALID\_REGINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-221">4211 (0x1073)</span><span class="sxs-lookup"><span data-stu-id="1472b-221">4211 (0x1073)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-222">Недопустимые сведения о регистрации WMI.</span><span class="sxs-lookup"><span data-stu-id="1472b-222">The WMI registration information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**Ошибка \_ WMI \_ уже \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="1472b-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR\_WMI\_ALREADY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-224">4212 (0x1074)</span><span class="sxs-lookup"><span data-stu-id="1472b-224">4212 (0x1074)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-225">Блок данных WMI или уведомление о событии уже отключены.</span><span class="sxs-lookup"><span data-stu-id="1472b-225">The WMI data block or event notification has already been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**Ошибка \_ \_ только для чтения WMI \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR\_WMI\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-227">4213 (0x1075)</span><span class="sxs-lookup"><span data-stu-id="1472b-227">4213 (0x1075)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-228">Элемент данных или блок данных WMI доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1472b-228">The WMI data item or data block is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**Ошибка \_ \_ при установке \_ WMI**</span><span class="sxs-lookup"><span data-stu-id="1472b-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR\_WMI\_SET\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-230">4214 (0x1076)</span><span class="sxs-lookup"><span data-stu-id="1472b-230">4214 (0x1076)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-231">Не удалось изменить элемент данных или блок данных WMI.</span><span class="sxs-lookup"><span data-stu-id="1472b-231">The WMI data item or data block could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**Ошибка \_ не является \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="1472b-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR\_NOT\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-233">4250 (0x109A)</span><span class="sxs-lookup"><span data-stu-id="1472b-233">4250 (0x109A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-234">Эта операция допустима только в контексте контейнера приложения.</span><span class="sxs-lookup"><span data-stu-id="1472b-234">This operation is only valid in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**\_требуется ошибка APPCONTAINER \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR\_APPCONTAINER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-236">4251 (0x109B)</span><span class="sxs-lookup"><span data-stu-id="1472b-236">4251 (0x109B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-237">Это приложение может выполняться только в контексте контейнера приложения.</span><span class="sxs-lookup"><span data-stu-id="1472b-237">This application can only run in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**Ошибка \_ не \_ поддерживается \_ в \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="1472b-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR\_NOT\_SUPPORTED\_IN\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-239">4252 (0x109C)</span><span class="sxs-lookup"><span data-stu-id="1472b-239">4252 (0x109C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-240">Эта функция не поддерживается в контексте контейнера приложения.</span><span class="sxs-lookup"><span data-stu-id="1472b-240">This functionality is not supported in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**Ошибка \_ Недопустимая \_ \_ Длина идентификатора безопасности пакета \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR\_INVALID\_PACKAGE\_SID\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-242">4253 (0x109D)</span><span class="sxs-lookup"><span data-stu-id="1472b-242">4253 (0x109D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-243">Длина переданного идентификатора SID не является допустимой для идентификаторов безопасности контейнера приложений.</span><span class="sxs-lookup"><span data-stu-id="1472b-243">The length of the SID supplied is not a valid length for app container SIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**Ошибка \_ недопустимого \_ носителя**</span><span class="sxs-lookup"><span data-stu-id="1472b-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR\_INVALID\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-245">4300 (0x10CC)</span><span class="sxs-lookup"><span data-stu-id="1472b-245">4300 (0x10CC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-246">Идентификатор носителя не представляет допустимый носитель.</span><span class="sxs-lookup"><span data-stu-id="1472b-246">The media identifier does not represent a valid medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**Ошибка \_ недопустимой \_ библиотеки**</span><span class="sxs-lookup"><span data-stu-id="1472b-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR\_INVALID\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-248">4301 (0x10CD)</span><span class="sxs-lookup"><span data-stu-id="1472b-248">4301 (0x10CD)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-249">Идентификатор библиотеки не представляет допустимую библиотеку.</span><span class="sxs-lookup"><span data-stu-id="1472b-249">The library identifier does not represent a valid library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**Ошибка \_ недопустимого \_ \_ пула носителей**</span><span class="sxs-lookup"><span data-stu-id="1472b-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR\_INVALID\_MEDIA\_POOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-251">4302 (0x10CE)</span><span class="sxs-lookup"><span data-stu-id="1472b-251">4302 (0x10CE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-252">Идентификатор пула носителей не представляет допустимый пул носителей.</span><span class="sxs-lookup"><span data-stu-id="1472b-252">The media pool identifier does not represent a valid media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии носителя**</span><span class="sxs-lookup"><span data-stu-id="1472b-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR\_DRIVE\_MEDIA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-254">4303 (0x10CF)</span><span class="sxs-lookup"><span data-stu-id="1472b-254">4303 (0x10CF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-255">Диск и носитель не совместимы или существуют в разных библиотеках.</span><span class="sxs-lookup"><span data-stu-id="1472b-255">The drive and medium are not compatible or exist in different libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**Ошибка \_ мультимедиа в \_ автономном режиме**</span><span class="sxs-lookup"><span data-stu-id="1472b-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**ERROR\_MEDIA\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-257">4304 (0x10D0)</span><span class="sxs-lookup"><span data-stu-id="1472b-257">4304 (0x10D0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-258">Носитель в данный момент находится в автономной библиотеке и должен быть подключен к сети для выполнения этой операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-258">The medium currently exists in an offline library and must be online to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**\_Библиотека ошибок \_ вне сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**ERROR\_LIBRARY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-260">4305 (0x10D1)</span><span class="sxs-lookup"><span data-stu-id="1472b-260">4305 (0x10D1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-261">Невозможно выполнить операцию для автономной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="1472b-261">The operation cannot be performed on an offline library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**Ошибка \_ пуста**</span><span class="sxs-lookup"><span data-stu-id="1472b-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-263">4306 (0x10D2)</span><span class="sxs-lookup"><span data-stu-id="1472b-263">4306 (0x10D2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-264">Библиотека, диск или пул носителей пусты.</span><span class="sxs-lookup"><span data-stu-id="1472b-264">The library, drive, or media pool is empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**Ошибка \_ не \_ пуста**</span><span class="sxs-lookup"><span data-stu-id="1472b-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-266">4307 (0x10D3)</span><span class="sxs-lookup"><span data-stu-id="1472b-266">4307 (0x10D3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-267">Для выполнения этой операции Библиотека, диск или пул носителей должны быть пустыми.</span><span class="sxs-lookup"><span data-stu-id="1472b-267">The library, drive, or media pool must be empty to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**\_носитель ошибок \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**ERROR\_MEDIA\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-269">4308 (0x10D4)</span><span class="sxs-lookup"><span data-stu-id="1472b-269">4308 (0x10D4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-270">В этом пуле носителей или библиотеке нет доступных носителей.</span><span class="sxs-lookup"><span data-stu-id="1472b-270">No media is currently available in this media pool or library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ресурс об ОШИБКе \_ \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="1472b-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ERROR\_RESOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-272">4309 (0x10D5)</span><span class="sxs-lookup"><span data-stu-id="1472b-272">4309 (0x10D5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-273">Ресурс, необходимый для этой операции, отключен.</span><span class="sxs-lookup"><span data-stu-id="1472b-273">A resource required for this operation is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**Ошибка \_ неправильной \_ очистки**</span><span class="sxs-lookup"><span data-stu-id="1472b-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR\_INVALID\_CLEANER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-275">4310 (0x10D6)</span><span class="sxs-lookup"><span data-stu-id="1472b-275">4310 (0x10D6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-276">Идентификатор носителя не представляет допустимый очиститель.</span><span class="sxs-lookup"><span data-stu-id="1472b-276">The media identifier does not represent a valid cleaner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**\_не удалось \_ \_ очистить**</span><span class="sxs-lookup"><span data-stu-id="1472b-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR\_UNABLE\_TO\_CLEAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-278">4311 (0x10D7)</span><span class="sxs-lookup"><span data-stu-id="1472b-278">4311 (0x10D7)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-279">Диск не может быть очищен или не поддерживает очистку.</span><span class="sxs-lookup"><span data-stu-id="1472b-279">The drive cannot be cleaned or does not support cleaning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_объект ошибки \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**ERROR\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-281">4312 (0x10D8)</span><span class="sxs-lookup"><span data-stu-id="1472b-281">4312 (0x10D8)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-282">Идентификатор объекта не представляет допустимый объект.</span><span class="sxs-lookup"><span data-stu-id="1472b-282">The object identifier does not represent a valid object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**Ошибка \_ базы данных при ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR\_DATABASE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-284">4313 (0x10D9)</span><span class="sxs-lookup"><span data-stu-id="1472b-284">4313 (0x10D9)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-285">Не удается выполнить чтение из базы данных или запись в нее.</span><span class="sxs-lookup"><span data-stu-id="1472b-285">Unable to read from or write to the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**\_база данных с ошибкой \_ заполнена**</span><span class="sxs-lookup"><span data-stu-id="1472b-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR\_DATABASE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-287">4314 (0x10DA)</span><span class="sxs-lookup"><span data-stu-id="1472b-287">4314 (0x10DA)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-288">База данных заполнена.</span><span class="sxs-lookup"><span data-stu-id="1472b-288">The database is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**несовместимость носителя с ОШИБКАми \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR\_MEDIA\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-290">4315 (0x10DB)</span><span class="sxs-lookup"><span data-stu-id="1472b-290">4315 (0x10DB)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-291">Носитель не совместим с устройством или пулом носителей.</span><span class="sxs-lookup"><span data-stu-id="1472b-291">The medium is not compatible with the device or media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**\_ресурс ошибки \_ отсутствует \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**ERROR\_RESOURCE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-293">4316 (0x10DC)</span><span class="sxs-lookup"><span data-stu-id="1472b-293">4316 (0x10DC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-294">Ресурс, необходимый для этой операции, не существует.</span><span class="sxs-lookup"><span data-stu-id="1472b-294">The resource required for this operation does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**Ошибка \_ недопустимой \_ операции**</span><span class="sxs-lookup"><span data-stu-id="1472b-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-296">4317 (0x10DD)</span><span class="sxs-lookup"><span data-stu-id="1472b-296">4317 (0x10DD)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-297">Недопустимый идентификатор операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-297">The operation identifier is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**\_носитель ошибок \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**ERROR\_MEDIA\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-299">4318 (0x10DE)</span><span class="sxs-lookup"><span data-stu-id="1472b-299">4318 (0x10DE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-300">Носитель не подключен или готов к использованию.</span><span class="sxs-lookup"><span data-stu-id="1472b-300">The media is not mounted or ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**устройство с ОШИБКАми \_ \_ \_ недоступно**</span><span class="sxs-lookup"><span data-stu-id="1472b-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR\_DEVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-302">4319 (0x10DF)</span><span class="sxs-lookup"><span data-stu-id="1472b-302">4319 (0x10DF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-303">Устройство не готово к использованию.</span><span class="sxs-lookup"><span data-stu-id="1472b-303">The device is not ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**запрос на ошибку \_ \_ отклонен**</span><span class="sxs-lookup"><span data-stu-id="1472b-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**ERROR\_REQUEST\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-305">4320 (0x10E0)</span><span class="sxs-lookup"><span data-stu-id="1472b-305">4320 (0x10E0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-306">Оператор или администратор отклонили запрос.</span><span class="sxs-lookup"><span data-stu-id="1472b-306">The operator or administrator has refused the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**Ошибка в \_ недопустимом \_ \_ объекте диска**</span><span class="sxs-lookup"><span data-stu-id="1472b-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR\_INVALID\_DRIVE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-308">4321 (0x10E1)</span><span class="sxs-lookup"><span data-stu-id="1472b-308">4321 (0x10E1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-309">Идентификатор диска не представляет допустимый диск.</span><span class="sxs-lookup"><span data-stu-id="1472b-309">The drive identifier does not represent a valid drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**\_Библиотека ошибок \_ заполнена**</span><span class="sxs-lookup"><span data-stu-id="1472b-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**ERROR\_LIBRARY\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-311">4322 (0x10E2)</span><span class="sxs-lookup"><span data-stu-id="1472b-311">4322 (0x10E2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-312">Библиотека заполнена.</span><span class="sxs-lookup"><span data-stu-id="1472b-312">Library is full.</span></span> <span data-ttu-id="1472b-313">Нет слота, доступной для использования.</span><span class="sxs-lookup"><span data-stu-id="1472b-313">No slot is available for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**Ошибка \_ : средний уровень \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR\_MEDIUM\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-315">4323 (0x10E3)</span><span class="sxs-lookup"><span data-stu-id="1472b-315">4323 (0x10E3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-316">Транспорту не удается получить доступ к носителю.</span><span class="sxs-lookup"><span data-stu-id="1472b-316">The transport cannot access the medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**\_не удалось \_ \_ загрузить \_ носитель**</span><span class="sxs-lookup"><span data-stu-id="1472b-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR\_UNABLE\_TO\_LOAD\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-318">4324 (0x10E4)</span><span class="sxs-lookup"><span data-stu-id="1472b-318">4324 (0x10E4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-319">Не удалось загрузить носитель в диск.</span><span class="sxs-lookup"><span data-stu-id="1472b-319">Unable to load the medium into the drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**Ошибка \_ при \_ \_ инвентаризации \_ диска**</span><span class="sxs-lookup"><span data-stu-id="1472b-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-321">4325 (0x10E5)</span><span class="sxs-lookup"><span data-stu-id="1472b-321">4325 (0x10E5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-322">Не удалось получить состояние диска.</span><span class="sxs-lookup"><span data-stu-id="1472b-322">Unable to retrieve the drive status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**Ошибка \_ не удалось выполнить \_ \_ инвентаризацию \_ слота**</span><span class="sxs-lookup"><span data-stu-id="1472b-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_SLOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-324">4326 (0x10E6)</span><span class="sxs-lookup"><span data-stu-id="1472b-324">4326 (0x10E6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-325">Не удалось получить состояние слота.</span><span class="sxs-lookup"><span data-stu-id="1472b-325">Unable to retrieve the slot status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**Ошибка \_ при \_ \_ инвентаризации \_ транспорта**</span><span class="sxs-lookup"><span data-stu-id="1472b-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_TRANSPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-327">4327 (0x10E7)</span><span class="sxs-lookup"><span data-stu-id="1472b-327">4327 (0x10E7)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-328">Не удалось получить сведения о состоянии транспорта.</span><span class="sxs-lookup"><span data-stu-id="1472b-328">Unable to retrieve status about the transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**\_полный транспорт \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR\_TRANSPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-330">4328 (0x10E8)</span><span class="sxs-lookup"><span data-stu-id="1472b-330">4328 (0x10E8)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-331">Невозможно использовать транспорт, так как он уже используется.</span><span class="sxs-lookup"><span data-stu-id="1472b-331">Cannot use the transport because it is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**Ошибка \_ управления \_ IEPORT**</span><span class="sxs-lookup"><span data-stu-id="1472b-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR\_CONTROLLING\_IEPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-333">4329 (0x10E9)</span><span class="sxs-lookup"><span data-stu-id="1472b-333">4329 (0x10E9)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-334">Не удается открыть или закрыть порт вставки и извлечения.</span><span class="sxs-lookup"><span data-stu-id="1472b-334">Unable to open or close the inject/eject port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**Ошибка \_ не \_ удалось \_ извлечь \_ подключенный \_ носитель**</span><span class="sxs-lookup"><span data-stu-id="1472b-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR\_UNABLE\_TO\_EJECT\_MOUNTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-336">4330 (0x10EA)</span><span class="sxs-lookup"><span data-stu-id="1472b-336">4330 (0x10EA)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-337">Не удалось извлечь носитель, так как он находится на диске.</span><span class="sxs-lookup"><span data-stu-id="1472b-337">Unable to eject the medium because it is in a drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**Ошибка \_ очистки \_ набора слотов \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**ERROR\_CLEANER\_SLOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-339">4331 (0x10EB)</span><span class="sxs-lookup"><span data-stu-id="1472b-339">4331 (0x10EB)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-340">Слот очистителя уже зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="1472b-340">A cleaner slot is already reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**Ошибка \_ очистки \_ слота \_ не \_ задана**</span><span class="sxs-lookup"><span data-stu-id="1472b-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR\_CLEANER\_SLOT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-342">4332 (0x10EC)</span><span class="sxs-lookup"><span data-stu-id="1472b-342">4332 (0x10EC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-343">Слот очистителя не зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="1472b-343">A cleaner slot is not reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**Ошибка \_ чистящего \_ картриджа очистки \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR\_CLEANER\_CARTRIDGE\_SPENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-345">4333 (0x10ED)</span><span class="sxs-lookup"><span data-stu-id="1472b-345">4333 (0x10ED)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-346">Чистящая кассета выполнила максимальное число чистых дисков.</span><span class="sxs-lookup"><span data-stu-id="1472b-346">The cleaner cartridge has performed the maximum number of drive cleanings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**произошла \_ непредвиденная ошибка \_ Omid**</span><span class="sxs-lookup"><span data-stu-id="1472b-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR\_UNEXPECTED\_OMID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-348">4334 (0x10EE)</span><span class="sxs-lookup"><span data-stu-id="1472b-348">4334 (0x10EE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-349">Непредвиденный идентификатор на носителе.</span><span class="sxs-lookup"><span data-stu-id="1472b-349">Unexpected on-medium identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ОШИБКА не \_ удается \_ удалить \_ последний \_ элемент**</span><span class="sxs-lookup"><span data-stu-id="1472b-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR\_CANT\_DELETE\_LAST\_ITEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-351">4335 (0x10EF)</span><span class="sxs-lookup"><span data-stu-id="1472b-351">4335 (0x10EF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-352">Не удается удалить последний оставшийся элемент в этой группе или ресурсе.</span><span class="sxs-lookup"><span data-stu-id="1472b-352">The last remaining item in this group or resource cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**сообщение об ОШИБКе \_ \_ превышает \_ максимальный \_ Размер**</span><span class="sxs-lookup"><span data-stu-id="1472b-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**ERROR\_MESSAGE\_EXCEEDS\_MAX\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-354">4336 (0x10F0)</span><span class="sxs-lookup"><span data-stu-id="1472b-354">4336 (0x10F0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-355">Указанное сообщение превышает максимальный размер, допустимый для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="1472b-355">The message provided exceeds the maximum size allowed for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**\_том ошибок \_ содержит \_ sys \_ файлов**</span><span class="sxs-lookup"><span data-stu-id="1472b-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**ERROR\_VOLUME\_CONTAINS\_SYS\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-357">4337 (0x10F1)</span><span class="sxs-lookup"><span data-stu-id="1472b-357">4337 (0x10F1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-358">Том содержит системные или файлы подкачки.</span><span class="sxs-lookup"><span data-stu-id="1472b-358">The volume contains system or paging files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**\_тип ошибки местных \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERROR\_INDIGENOUS\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-360">4338 (0x10F2)</span><span class="sxs-lookup"><span data-stu-id="1472b-360">4338 (0x10F2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-361">Невозможно удалить тип носителя из этой библиотеки, так как по крайней мере один диск в библиотеке сообщает, что он поддерживает этот тип носителя.</span><span class="sxs-lookup"><span data-stu-id="1472b-361">The media type cannot be removed from this library since at least one drive in the library reports it can support this media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**Ошибка \_ не \_ поддерживает \_ диски**</span><span class="sxs-lookup"><span data-stu-id="1472b-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR\_NO\_SUPPORTING\_DRIVES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-363">4339 (0x10F3)</span><span class="sxs-lookup"><span data-stu-id="1472b-363">4339 (0x10F3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-364">Этот автономный носитель не может быть подключен к этой системе, так как не существует включенных дисков, которые можно использовать.</span><span class="sxs-lookup"><span data-stu-id="1472b-364">This offline media cannot be mounted on this system since no enabled drives are present which can be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**Ошибка \_ при \_ установке чистящего картриджа \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**ERROR\_CLEANER\_CARTRIDGE\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-366">4340 (0x10F4)</span><span class="sxs-lookup"><span data-stu-id="1472b-366">4340 (0x10F4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-367">В ленточной библиотеке имеется чистящий картридж.</span><span class="sxs-lookup"><span data-stu-id="1472b-367">A cleaner cartridge is present in the tape library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**Ошибка \_ IEPORT \_ Full**</span><span class="sxs-lookup"><span data-stu-id="1472b-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR\_IEPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-369">4341 (0x10F5)</span><span class="sxs-lookup"><span data-stu-id="1472b-369">4341 (0x10F5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-370">Невозможно использовать порт вставки и извлечения, так как он не пуст.</span><span class="sxs-lookup"><span data-stu-id="1472b-370">Cannot use the inject/eject port because it is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**\_файл ошибок \_ вне сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ERROR\_FILE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-372">4350 (0x10FE)</span><span class="sxs-lookup"><span data-stu-id="1472b-372">4350 (0x10FE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-373">Этот файл сейчас недоступен для использования на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="1472b-373">This file is currently not available for use on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**Ошибка " \_ Удаленное \_ хранилище \_ не \_ активно"**</span><span class="sxs-lookup"><span data-stu-id="1472b-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR\_REMOTE\_STORAGE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-375">4351 (0x10FF)</span><span class="sxs-lookup"><span data-stu-id="1472b-375">4351 (0x10FF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-376">Служба внешнего хранилища в настоящее время неработоспособна.</span><span class="sxs-lookup"><span data-stu-id="1472b-376">The remote storage service is not operational at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**Ошибка \_ \_ носителя удаленного \_ хранилища \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR\_REMOTE\_STORAGE\_MEDIA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-378">4352 (0x1100)</span><span class="sxs-lookup"><span data-stu-id="1472b-378">4352 (0x1100)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-379">Служба внешнего хранилища обнаружила ошибку носителя.</span><span class="sxs-lookup"><span data-stu-id="1472b-379">The remote storage service encountered a media error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**Ошибка \_ не \_ является \_ точкой повторного \_ анализа**</span><span class="sxs-lookup"><span data-stu-id="1472b-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR\_NOT\_A\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-381">4390 (0x1126)</span><span class="sxs-lookup"><span data-stu-id="1472b-381">4390 (0x1126)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-382">Файл или каталог не является точкой повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="1472b-382">The file or directory is not a reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**Ошибка \_ при \_ конфликте атрибутов повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-384">4391 (0x1127)</span><span class="sxs-lookup"><span data-stu-id="1472b-384">4391 (0x1127)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-385">Невозможно задать атрибут точки повторной обработки, так как он конфликтует с существующим атрибутом.</span><span class="sxs-lookup"><span data-stu-id="1472b-385">The reparse point attribute cannot be set because it conflicts with an existing attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**Ошибка \_ недопустимых \_ данных повторного анализа \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR\_INVALID\_REPARSE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-387">4392 (0x1128)</span><span class="sxs-lookup"><span data-stu-id="1472b-387">4392 (0x1128)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-388">Данные в буфере точки повторной обработки недопустимы.</span><span class="sxs-lookup"><span data-stu-id="1472b-388">The data present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**\_Недопустимый тег повторного анализа ошибок \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR\_REPARSE\_TAG\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-390">4393 (0x1129)</span><span class="sxs-lookup"><span data-stu-id="1472b-390">4393 (0x1129)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-391">В буфере точки повторной обработки указан недопустимый тег.</span><span class="sxs-lookup"><span data-stu-id="1472b-391">The tag present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**Ошибка \_ при \_ несоответствии тегов при повторном анализе \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR\_REPARSE\_TAG\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-393">4394 (0x112A)</span><span class="sxs-lookup"><span data-stu-id="1472b-393">4394 (0x112A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-394">Обнаружено несоответствие между тегом, указанным в запросе, и тегом, который присутствует в точке повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="1472b-394">There is a mismatch between the tag specified in the request and the tag present in the reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**\_ \_ \_ не \_ найдены данные приложения об ошибках**</span><span class="sxs-lookup"><span data-stu-id="1472b-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR\_APP\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-396">4400 (0x1130)</span><span class="sxs-lookup"><span data-stu-id="1472b-396">4400 (0x1130)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-397">Не найдены данные быстрого кэширования.</span><span class="sxs-lookup"><span data-stu-id="1472b-397">Fast Cache data not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**Ошибка \_ при \_ \_ истечении срока действия данных приложения**</span><span class="sxs-lookup"><span data-stu-id="1472b-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR\_APP\_DATA\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-399">4401 (0x1131)</span><span class="sxs-lookup"><span data-stu-id="1472b-399">4401 (0x1131)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-400">Срок действия данных быстрого кэширования истек.</span><span class="sxs-lookup"><span data-stu-id="1472b-400">Fast Cache data expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ОШИБКИ \_ в \_ данных приложения \_ повреждены**</span><span class="sxs-lookup"><span data-stu-id="1472b-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROR\_APP\_DATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-402">4402 (0x1132)</span><span class="sxs-lookup"><span data-stu-id="1472b-402">4402 (0x1132)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-403">Данные быстрого кэширования повреждены.</span><span class="sxs-lookup"><span data-stu-id="1472b-403">Fast Cache data corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**\_ \_ \_ превышен предел данных приложения \_ об ошибках**</span><span class="sxs-lookup"><span data-stu-id="1472b-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERROR\_APP\_DATA\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-405">4403 (0x1133)</span><span class="sxs-lookup"><span data-stu-id="1472b-405">4403 (0x1133)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-406">Данные быстрого кэширования превысили максимальный размер и не могут быть обновлены.</span><span class="sxs-lookup"><span data-stu-id="1472b-406">Fast Cache data has exceeded its max size and cannot be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**Ошибка \_ при \_ \_ перезагрузке данных приложения \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR\_APP\_DATA\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-408">4404 (0x1134)</span><span class="sxs-lookup"><span data-stu-id="1472b-408">4404 (0x1134)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-409">Быстрый кэш был восстановлен и требует перезагрузки, пока его невозможно будет обновить.</span><span class="sxs-lookup"><span data-stu-id="1472b-409">Fast Cache has been ReArmed and requires a reboot until it can be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**\_ \_ обнаружена ошибка безопасной загрузки отката \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR\_SECUREBOOT\_ROLLBACK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-411">4420 (0x1144)</span><span class="sxs-lookup"><span data-stu-id="1472b-411">4420 (0x1144)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-412">При безопасной загрузке обнаружен откат защищенных данных.</span><span class="sxs-lookup"><span data-stu-id="1472b-412">Secure Boot detected that rollback of protected data has been attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**Ошибка \_ безопасной загрузки \_ \_ нарушение политики**</span><span class="sxs-lookup"><span data-stu-id="1472b-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR\_SECUREBOOT\_POLICY\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-414">4421 (0x1145)</span><span class="sxs-lookup"><span data-stu-id="1472b-414">4421 (0x1145)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-415">Значение защищено политикой безопасной загрузки и не может быть изменено или удалено.</span><span class="sxs-lookup"><span data-stu-id="1472b-415">The value is protected by Secure Boot policy and cannot be modified or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**Ошибка \_ безопасной загрузки \_ Недопустимая \_ Политика**</span><span class="sxs-lookup"><span data-stu-id="1472b-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR\_SECUREBOOT\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-417">4422 (0x1146)</span><span class="sxs-lookup"><span data-stu-id="1472b-417">4422 (0x1146)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-418">Недопустимая политика безопасной загрузки.</span><span class="sxs-lookup"><span data-stu-id="1472b-418">The Secure Boot policy is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**Ошибка \_ безопасной загрузки \_ политики \_ \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR\_SECUREBOOT\_POLICY\_PUBLISHER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-420">4423 (0x1147)</span><span class="sxs-lookup"><span data-stu-id="1472b-420">4423 (0x1147)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-421">Новая политика безопасной загрузки не содержала текущий издатель в списке обновлений.</span><span class="sxs-lookup"><span data-stu-id="1472b-421">A new Secure Boot policy did not contain the current publisher on its update list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**Ошибка \_ безопасной загрузки. \_ политика \_ не \_ подписана**</span><span class="sxs-lookup"><span data-stu-id="1472b-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR\_SECUREBOOT\_POLICY\_NOT\_SIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-423">4424 (0x1148)</span><span class="sxs-lookup"><span data-stu-id="1472b-423">4424 (0x1148)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-424">Политика безопасной загрузки либо не подписана, либо подписана недоверенным подписывающий.</span><span class="sxs-lookup"><span data-stu-id="1472b-424">The Secure Boot policy is either not signed or is signed by a non-trusted signer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**Ошибка \_ безопасной загрузки \_ не \_ включена**</span><span class="sxs-lookup"><span data-stu-id="1472b-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR\_SECUREBOOT\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-426">4425 (0x1149)</span><span class="sxs-lookup"><span data-stu-id="1472b-426">4425 (0x1149)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-427">Безопасная загрузка не включена на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="1472b-427">Secure Boot is not enabled on this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**Ошибка \_ при \_ \_ замене файла безопасной загрузки**</span><span class="sxs-lookup"><span data-stu-id="1472b-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR\_SECUREBOOT\_FILE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-429">4426 (0x114A)</span><span class="sxs-lookup"><span data-stu-id="1472b-429">4426 (0x114A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-430">Для безопасной загрузки необходимо, чтобы определенные файлы и драйверы не были заменены другими файлами или драйверами.</span><span class="sxs-lookup"><span data-stu-id="1472b-430">Secure Boot requires that certain files and drivers are not replaced by other files or drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**Ошибка \_ разгрузки \_ Read \_ ФЛТ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="1472b-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-432">4440 (0x1158)</span><span class="sxs-lookup"><span data-stu-id="1472b-432">4440 (0x1158)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-433">Операция чтения копии разгрузки не поддерживается фильтром.</span><span class="sxs-lookup"><span data-stu-id="1472b-433">The copy offload read operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**Ошибка \_ разгрузки \_ записи \_ ФЛТ \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="1472b-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-435">4441 (0x1159)</span><span class="sxs-lookup"><span data-stu-id="1472b-435">4441 (0x1159)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-436">Операция записи для разгрузки копий не поддерживается фильтром.</span><span class="sxs-lookup"><span data-stu-id="1472b-436">The copy offload write operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**Ошибка \_ разгрузки \_ чтения \_ файла \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="1472b-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-438">4442 (0x115A)</span><span class="sxs-lookup"><span data-stu-id="1472b-438">4442 (0x115A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-439">Операция чтения копии разгрузки для файла не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1472b-439">The copy offload read operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**Ошибка \_ разгрузки \_ \_ файла записи \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="1472b-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-441">4443 (0x115B)</span><span class="sxs-lookup"><span data-stu-id="1472b-441">4443 (0x115B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-442">Операция записи разгрузки копирования не поддерживается для этого файла.</span><span class="sxs-lookup"><span data-stu-id="1472b-442">The copy offload write operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**\_том ошибки \_ не \_ \_ включен SIS**</span><span class="sxs-lookup"><span data-stu-id="1472b-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**ERROR\_VOLUME\_NOT\_SIS\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-444">4500 (0x1194)</span><span class="sxs-lookup"><span data-stu-id="1472b-444">4500 (0x1194)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-445">Хранилище единственных экземпляров недоступно на этом томе.</span><span class="sxs-lookup"><span data-stu-id="1472b-445">Single Instance Storage is not available on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_существует ресурс, зависящий от ошибки \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**ERROR\_DEPENDENT\_RESOURCE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-447">5001 (0x1389)</span><span class="sxs-lookup"><span data-stu-id="1472b-447">5001 (0x1389)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-448">Операция не может быть завершена, так как другие ресурсы зависят от этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="1472b-448">The operation cannot be completed because other resources are dependent on this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_зависимость ошибок \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**ERROR\_DEPENDENCY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-450">5002 (0x138A)</span><span class="sxs-lookup"><span data-stu-id="1472b-450">5002 (0x138A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-451">Не удается найти зависимость ресурса кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-451">The cluster resource dependency cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**\_зависимость ошибок \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="1472b-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**ERROR\_DEPENDENCY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-453">5003 (0x138B)</span><span class="sxs-lookup"><span data-stu-id="1472b-453">5003 (0x138B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-454">Невозможно сделать ресурс кластера зависимым от указанного ресурса, так как он уже является зависимым.</span><span class="sxs-lookup"><span data-stu-id="1472b-454">The cluster resource cannot be made dependent on the specified resource because it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**\_ресурс ошибки \_ не в \_ сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**ERROR\_RESOURCE\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-456">5004 (0x138C)</span><span class="sxs-lookup"><span data-stu-id="1472b-456">5004 (0x138C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-457">Ресурс кластера находится вне сети.</span><span class="sxs-lookup"><span data-stu-id="1472b-457">The cluster resource is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**\_узел узла \_ ошибок \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**ERROR\_HOST\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-459">5005 (0x138D)</span><span class="sxs-lookup"><span data-stu-id="1472b-459">5005 (0x138D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-460">Узел кластера недоступен для этой операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-460">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**\_ресурс ошибки \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ERROR\_RESOURCE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-462">5006 (0x138E)</span><span class="sxs-lookup"><span data-stu-id="1472b-462">5006 (0x138E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-463">Ресурс кластера недоступен.</span><span class="sxs-lookup"><span data-stu-id="1472b-463">The cluster resource is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ресурс об ОШИБКе \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ERROR\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-465">5007 (0x138F)</span><span class="sxs-lookup"><span data-stu-id="1472b-465">5007 (0x138F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-466">Не удалось найти ресурс кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-466">The cluster resource could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**Ошибка при \_ завершении работы \_ кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR\_SHUTDOWN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-468">5008 (0x1390)</span><span class="sxs-lookup"><span data-stu-id="1472b-468">5008 (0x1390)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-469">Идет завершение работы кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-469">The cluster is being shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ОШИБКА не \_ удается \_ исключить \_ Активный \_ узел**</span><span class="sxs-lookup"><span data-stu-id="1472b-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR\_CANT\_EVICT\_ACTIVE\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-471">5009 (0x1391)</span><span class="sxs-lookup"><span data-stu-id="1472b-471">5009 (0x1391)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-472">Узел кластера не может быть удален из кластера, если узел не работает или является последним узлом.</span><span class="sxs-lookup"><span data-stu-id="1472b-472">A cluster node cannot be evicted from the cluster unless the node is down or it is the last node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**\_объект ошибки \_ уже \_ существует**</span><span class="sxs-lookup"><span data-stu-id="1472b-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**ERROR\_OBJECT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-474">5010 (0x1392)</span><span class="sxs-lookup"><span data-stu-id="1472b-474">5010 (0x1392)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-475">Объект уже существует.</span><span class="sxs-lookup"><span data-stu-id="1472b-475">The object already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_объект Error \_ в \_ списке**</span><span class="sxs-lookup"><span data-stu-id="1472b-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**ERROR\_OBJECT\_IN\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-477">5011 (0x1393)</span><span class="sxs-lookup"><span data-stu-id="1472b-477">5011 (0x1393)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-478">Объект уже находится в списке.</span><span class="sxs-lookup"><span data-stu-id="1472b-478">The object is already in the list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**\_Группа ошибок \_ \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="1472b-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**ERROR\_GROUP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-480">5012 (0x1394)</span><span class="sxs-lookup"><span data-stu-id="1472b-480">5012 (0x1394)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-481">Группа кластеров недоступна для новых запросов.</span><span class="sxs-lookup"><span data-stu-id="1472b-481">The cluster group is not available for any new requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_Группа ошибок \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**ERROR\_GROUP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-483">5013 (0x1395)</span><span class="sxs-lookup"><span data-stu-id="1472b-483">5013 (0x1395)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-484">Не удалось найти группу кластеров.</span><span class="sxs-lookup"><span data-stu-id="1472b-484">The cluster group could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**\_Группа ошибок \_ не в \_ сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**ERROR\_GROUP\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-486">5014 (0x1396)</span><span class="sxs-lookup"><span data-stu-id="1472b-486">5014 (0x1396)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-487">Не удалось выполнить операцию, так как кластерная группа не находится в режиме "в сети".</span><span class="sxs-lookup"><span data-stu-id="1472b-487">The operation could not be completed because the cluster group is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**Ошибка \_ " \_ узел узла \_ не является \_ \_ владельцем ресурса"**</span><span class="sxs-lookup"><span data-stu-id="1472b-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR\_HOST\_NODE\_NOT\_RESOURCE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-489">5015 (0x1397)</span><span class="sxs-lookup"><span data-stu-id="1472b-489">5015 (0x1397)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-490">Не удалось выполнить операцию, так как указанный узел кластера не является владельцем ресурса, или узел не является возможным владельцем ресурса.</span><span class="sxs-lookup"><span data-stu-id="1472b-490">The operation failed because either the specified cluster node is not the owner of the resource, or the node is not a possible owner of the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**Ошибка \_ " \_ узел узла \_ не является \_ \_ владельцем группы"**</span><span class="sxs-lookup"><span data-stu-id="1472b-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR\_HOST\_NODE\_NOT\_GROUP\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-492">5016 (0x1398)</span><span class="sxs-lookup"><span data-stu-id="1472b-492">5016 (0x1398)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-493">Не удалось выполнить операцию, так как указанный узел кластера не является и не может стать владельцем этой группы.</span><span class="sxs-lookup"><span data-stu-id="1472b-493">The operation failed because either the specified cluster node is not the owner of the group, or the node is not a possible owner of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**Ошибка \_ \_ при создании \_ ресмон**</span><span class="sxs-lookup"><span data-stu-id="1472b-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR\_RESMON\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-495">5017 (0x1399)</span><span class="sxs-lookup"><span data-stu-id="1472b-495">5017 (0x1399)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-496">Не удалось создать ресурс кластера в указанном мониторе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1472b-496">The cluster resource could not be created in the specified resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**Ошибка \_ ресмон в \_ сети \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR\_RESMON\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-498">5018 (0x139A)</span><span class="sxs-lookup"><span data-stu-id="1472b-498">5018 (0x139A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-499">Монитору ресурсов не удалось перевести ресурс кластера в режим "в сети".</span><span class="sxs-lookup"><span data-stu-id="1472b-499">The cluster resource could not be brought online by the resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ресурс ошибки в \_ \_ сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ERROR\_RESOURCE\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-501">5019 (0x139B)</span><span class="sxs-lookup"><span data-stu-id="1472b-501">5019 (0x139B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-502">Не удалось выполнить операцию, так как ресурс кластера находится в режиме "в сети".</span><span class="sxs-lookup"><span data-stu-id="1472b-502">The operation could not be completed because the cluster resource is online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ресурс с ошибкой \_ кворума \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERROR\_QUORUM\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-504">5020 (0x139C)</span><span class="sxs-lookup"><span data-stu-id="1472b-504">5020 (0x139C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-505">Ресурс кластера не может быть удален или переведен в автономный режим, так как он является ресурсом кворума.</span><span class="sxs-lookup"><span data-stu-id="1472b-505">The cluster resource could not be deleted or brought offline because it is the quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**Ошибка \_ не \_ \_ поддерживает кворум**</span><span class="sxs-lookup"><span data-stu-id="1472b-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR\_NOT\_QUORUM\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-507">5021 (0x139D)</span><span class="sxs-lookup"><span data-stu-id="1472b-507">5021 (0x139D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-508">Кластеру не удалось сделать указанный ресурс ресурсом кворума, так как он не может быть ресурсом кворума.</span><span class="sxs-lookup"><span data-stu-id="1472b-508">The cluster could not make the specified resource a quorum resource because it is not capable of being a quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**Ошибка \_ при \_ завершении работы кластера \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR\_CLUSTER\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-510">5022 (0x139E)</span><span class="sxs-lookup"><span data-stu-id="1472b-510">5022 (0x139E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-511">Завершается работа программного обеспечения кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-511">The cluster software is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**Ошибка \_ недопустимого \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="1472b-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-513">5023 (0x139F)</span><span class="sxs-lookup"><span data-stu-id="1472b-513">5023 (0x139F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-514">Группа или ресурс находятся в неправильном состоянии для выполнения запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-514">The group or resource is not in the correct state to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**\_свойства ресурса \_ ошибки \_ сохранены**</span><span class="sxs-lookup"><span data-stu-id="1472b-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**ERROR\_RESOURCE\_PROPERTIES\_STORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-516">5024 (0x13A0)</span><span class="sxs-lookup"><span data-stu-id="1472b-516">5024 (0x13A0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-517">Свойства были сохранены, но не все изменения вступят в силу до того, как ресурс вновь перейдет в оперативный режим.</span><span class="sxs-lookup"><span data-stu-id="1472b-517">The properties were stored but not all changes will take effect until the next time the resource is brought online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**Ошибка \_ не \_ является \_ классом кворума**</span><span class="sxs-lookup"><span data-stu-id="1472b-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR\_NOT\_QUORUM\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-519">5025 (0x13A1)</span><span class="sxs-lookup"><span data-stu-id="1472b-519">5025 (0x13A1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-520">Кластеру не удалось сделать указанный ресурс ресурсом кворума, так как он не принадлежит к общему классу хранилища.</span><span class="sxs-lookup"><span data-stu-id="1472b-520">The cluster could not make the specified resource a quorum resource because it does not belong to a shared storage class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**\_ресурс ядра \_ ошибки**</span><span class="sxs-lookup"><span data-stu-id="1472b-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR\_CORE\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-522">5026 (0x13A2)</span><span class="sxs-lookup"><span data-stu-id="1472b-522">5026 (0x13A2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-523">Не удалось удалить ресурс кластера, так как он является основным ресурсом.</span><span class="sxs-lookup"><span data-stu-id="1472b-523">The cluster resource could not be deleted since it is a core resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**\_сбой ресурса кворума "ошибка в \_ \_ сети \_ "**</span><span class="sxs-lookup"><span data-stu-id="1472b-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR\_QUORUM\_RESOURCE\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-525">5027 (0x13A3)</span><span class="sxs-lookup"><span data-stu-id="1472b-525">5027 (0x13A3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-526">Не удалось подключить ресурс кворума к сети.</span><span class="sxs-lookup"><span data-stu-id="1472b-526">The quorum resource failed to come online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**Ошибка \_ \_ при открытии \_ куорумлог**</span><span class="sxs-lookup"><span data-stu-id="1472b-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR\_QUORUMLOG\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-528">5028 (0x13A4)</span><span class="sxs-lookup"><span data-stu-id="1472b-528">5028 (0x13A4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-529">Не удалось успешно создать или присоединить журнал кворума.</span><span class="sxs-lookup"><span data-stu-id="1472b-529">The quorum log could not be created or mounted successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**Ошибка \_ CLUSTERLOG \_ повреждена**</span><span class="sxs-lookup"><span data-stu-id="1472b-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR\_CLUSTERLOG\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-531">5029 (0x13A5)</span><span class="sxs-lookup"><span data-stu-id="1472b-531">5029 (0x13A5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-532">Журнал кластера поврежден.</span><span class="sxs-lookup"><span data-stu-id="1472b-532">The cluster log is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**Ошибка \_ \_ записи CLUSTERLOG \_ превышает \_ MAXSIZE**</span><span class="sxs-lookup"><span data-stu-id="1472b-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_RECORD\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-534">5030 (0x13A6)</span><span class="sxs-lookup"><span data-stu-id="1472b-534">5030 (0x13A6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-535">Запись не может быть записана в журнал кластера, так как она превышает максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="1472b-535">The record could not be written to the cluster log since it exceeds the maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**Ошибка \_ CLUSTERLOG \_ превышает \_ MAXSIZE**</span><span class="sxs-lookup"><span data-stu-id="1472b-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-537">5031 (0x13A7)</span><span class="sxs-lookup"><span data-stu-id="1472b-537">5031 (0x13A7)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-538">Размер журнала кластера превышает максимальный.</span><span class="sxs-lookup"><span data-stu-id="1472b-538">The cluster log exceeds its maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**Ошибка \_ CLUSTERLOG \_ чкпоинт \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR\_CLUSTERLOG\_CHKPOINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-540">5032 (0x13A8)</span><span class="sxs-lookup"><span data-stu-id="1472b-540">5032 (0x13A8)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-541">В журнале кластера не найдена запись контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="1472b-541">No checkpoint record was found in the cluster log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**Ошибка \_ CLUSTERLOG \_ \_ недостаточно \_ места**</span><span class="sxs-lookup"><span data-stu-id="1472b-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR\_CLUSTERLOG\_NOT\_ENOUGH\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-543">5033 (0x13A9)</span><span class="sxs-lookup"><span data-stu-id="1472b-543">5033 (0x13A9)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-544">Минимально необходимое для ведения журнала место на диске недоступно.</span><span class="sxs-lookup"><span data-stu-id="1472b-544">The minimum required disk space needed for logging is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**Ошибка \_ в \_ активном владельце кворума \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR\_QUORUM\_OWNER\_ALIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-546">5034 (0x13AA)</span><span class="sxs-lookup"><span data-stu-id="1472b-546">5034 (0x13AA)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-547">Узлу кластера не удалось получить управление ресурсом кворума, так как владельцем ресурса является другой активный узел.</span><span class="sxs-lookup"><span data-stu-id="1472b-547">The cluster node failed to take control of the quorum resource because the resource is owned by another active node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**\_сеть ошибок \_ \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="1472b-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR\_NETWORK\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-549">5035 (0x13AB)</span><span class="sxs-lookup"><span data-stu-id="1472b-549">5035 (0x13AB)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-550">Сеть кластера недоступна для этой операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-550">A cluster network is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**\_узел ошибки \_ \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**ERROR\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-552">5036 (0x13AC)</span><span class="sxs-lookup"><span data-stu-id="1472b-552">5036 (0x13AC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-553">Узел кластера недоступен для этой операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-553">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**Ошибка \_ все \_ узлы \_ \_ недоступны**</span><span class="sxs-lookup"><span data-stu-id="1472b-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR\_ALL\_NODES\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-555">5037 (0x13AD)</span><span class="sxs-lookup"><span data-stu-id="1472b-555">5037 (0x13AD)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-556">Для выполнения этой операции должны быть установлены все узлы кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-556">All cluster nodes must be running to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**\_сбой ресурса "ошибка" \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR\_RESOURCE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-558">5038 (0x13AE)</span><span class="sxs-lookup"><span data-stu-id="1472b-558">5038 (0x13AE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-559">сбой ресурса кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-559">A cluster resource failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**\_ \_ Недопустимый \_ узел кластера ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR\_CLUSTER\_INVALID\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-561">5039 (0x13AF)</span><span class="sxs-lookup"><span data-stu-id="1472b-561">5039 (0x13AF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-562">Недопустимый узел кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-562">The cluster node is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**\_узел кластера \_ ошибок \_ существует**</span><span class="sxs-lookup"><span data-stu-id="1472b-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**ERROR\_CLUSTER\_NODE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-564">5040 (0x13B0)</span><span class="sxs-lookup"><span data-stu-id="1472b-564">5040 (0x13B0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-565">Узел кластера уже существует.</span><span class="sxs-lookup"><span data-stu-id="1472b-565">The cluster node already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**Ошибка \_ \_ при присоединении кластера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-567">5041 (0x13B1)</span><span class="sxs-lookup"><span data-stu-id="1472b-567">5041 (0x13B1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-568">Узел находится в процессе присоединения к кластеру.</span><span class="sxs-lookup"><span data-stu-id="1472b-568">A node is in the process of joining the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**\_узел кластера \_ ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR\_CLUSTER\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-570">5042 (0x13B2)</span><span class="sxs-lookup"><span data-stu-id="1472b-570">5042 (0x13B2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-571">Узел кластера не найден.</span><span class="sxs-lookup"><span data-stu-id="1472b-571">The cluster node was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_ \_ \_ \_ не найден локальный узел кластера \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR\_CLUSTER\_LOCAL\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-573">5043 (0x13B3)</span><span class="sxs-lookup"><span data-stu-id="1472b-573">5043 (0x13B3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-574">Сведения о локальном узле кластера не найдены.</span><span class="sxs-lookup"><span data-stu-id="1472b-574">The cluster local node information was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**\_существует ошибка \_ сети \_ кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR\_CLUSTER\_NETWORK\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-576">5044 (0x13B4)</span><span class="sxs-lookup"><span data-stu-id="1472b-576">5044 (0x13B4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-577">Сеть кластера уже существует.</span><span class="sxs-lookup"><span data-stu-id="1472b-577">The cluster network already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**Ошибка \_ \_ сети кластера \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-579">5045 (0x13B5)</span><span class="sxs-lookup"><span data-stu-id="1472b-579">5045 (0x13B5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-580">Сеть кластера не найдена.</span><span class="sxs-lookup"><span data-stu-id="1472b-580">The cluster network was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**\_нетинтерфаце кластера \_ ошибок \_ существует**</span><span class="sxs-lookup"><span data-stu-id="1472b-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR\_CLUSTER\_NETINTERFACE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-582">5046 (0x13B6)</span><span class="sxs-lookup"><span data-stu-id="1472b-582">5046 (0x13B6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-583">Сетевой интерфейс кластера уже существует.</span><span class="sxs-lookup"><span data-stu-id="1472b-583">The cluster network interface already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**Ошибка \_ кластера \_ нетинтерфаце \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR\_CLUSTER\_NETINTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-585">5047 (0x13B7)</span><span class="sxs-lookup"><span data-stu-id="1472b-585">5047 (0x13B7)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-586">Не удалось найти сетевой интерфейс кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-586">The cluster network interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**\_ \_ Недопустимый \_ запрос кластера ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR\_CLUSTER\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-588">5048 (0x13B8)</span><span class="sxs-lookup"><span data-stu-id="1472b-588">5048 (0x13B8)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-589">Запрос кластера недопустим для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="1472b-589">The cluster request is not valid for this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**кластер ошибок — \_ \_ Недопустимый \_ \_ поставщик сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-591">5049 (0x13B9)</span><span class="sxs-lookup"><span data-stu-id="1472b-591">5049 (0x13B9)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-592">Недопустимый поставщик сети кластеров.</span><span class="sxs-lookup"><span data-stu-id="1472b-592">The cluster network provider is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**Ошибка \_ \_ отключения узла \_ кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR\_CLUSTER\_NODE\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-594">5050 (0x13BA)</span><span class="sxs-lookup"><span data-stu-id="1472b-594">5050 (0x13BA)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-595">Узел кластера не работает.</span><span class="sxs-lookup"><span data-stu-id="1472b-595">The cluster node is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**\_узел кластера \_ ошибок \_ недоступен**</span><span class="sxs-lookup"><span data-stu-id="1472b-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR\_CLUSTER\_NODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-597">5051 (0x13BB)</span><span class="sxs-lookup"><span data-stu-id="1472b-597">5051 (0x13BB)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-598">Узел кластера недоступен.</span><span class="sxs-lookup"><span data-stu-id="1472b-598">The cluster node is not reachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**Ошибка \_ узла кластера, \_ \_ не \_ входящего в группу**</span><span class="sxs-lookup"><span data-stu-id="1472b-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR\_CLUSTER\_NODE\_NOT\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-600">5052 (0x13BC)</span><span class="sxs-lookup"><span data-stu-id="1472b-600">5052 (0x13BC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-601">Узел кластера не является членом кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-601">The cluster node is not a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**Ошибка \_ \_ Присоединение к кластеру \_ не \_ \_ выполняется**</span><span class="sxs-lookup"><span data-stu-id="1472b-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-603">5053 (0x13BD)</span><span class="sxs-lookup"><span data-stu-id="1472b-603">5053 (0x13BD)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-604">Операция присоединение к кластеру не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1472b-604">A cluster join operation is not in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**\_ \_ недействительная \_ сеть кластера ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-606">5054 (0x13BE)</span><span class="sxs-lookup"><span data-stu-id="1472b-606">5054 (0x13BE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-607">Недопустимая сеть кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-607">The cluster network is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**\_узел кластера \_ ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR\_CLUSTER\_NODE\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-609">5056 (0x13C0)</span><span class="sxs-lookup"><span data-stu-id="1472b-609">5056 (0x13C0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-610">Узел кластера работает.</span><span class="sxs-lookup"><span data-stu-id="1472b-610">The cluster node is up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**\_используется кластер \_ ошибок \_ reduce \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR\_CLUSTER\_IPADDR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-612">5057 (0x13C1)</span><span class="sxs-lookup"><span data-stu-id="1472b-612">5057 (0x13C1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-613">IP-адрес кластера уже используется.</span><span class="sxs-lookup"><span data-stu-id="1472b-613">The cluster IP address is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**\_узел кластера \_ ошибок \_ не \_ приостановлен**</span><span class="sxs-lookup"><span data-stu-id="1472b-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**ERROR\_CLUSTER\_NODE\_NOT\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-615">5058 (0x13C2)</span><span class="sxs-lookup"><span data-stu-id="1472b-615">5058 (0x13C2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-616">Узел кластера не приостановлен.</span><span class="sxs-lookup"><span data-stu-id="1472b-616">The cluster node is not paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**\_кластер ошибок \_ без \_ \_ контекста безопасности**</span><span class="sxs-lookup"><span data-stu-id="1472b-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR\_CLUSTER\_NO\_SECURITY\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-618">5059 (0x13C3)</span><span class="sxs-lookup"><span data-stu-id="1472b-618">5059 (0x13C3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-619">Контекст безопасности кластера недоступен.</span><span class="sxs-lookup"><span data-stu-id="1472b-619">No cluster security context is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**Ошибка \_ сети кластера, \_ \_ не \_ внутренней**</span><span class="sxs-lookup"><span data-stu-id="1472b-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-621">5060 (0x13C4)</span><span class="sxs-lookup"><span data-stu-id="1472b-621">5060 (0x13C4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-622">Сеть кластера не настроена для взаимодействия с внутренним кластером.</span><span class="sxs-lookup"><span data-stu-id="1472b-622">The cluster network is not configured for internal cluster communication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**\_узел кластера \_ ошибок \_ уже \_ включен**</span><span class="sxs-lookup"><span data-stu-id="1472b-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-624">5061 (0x13C5)</span><span class="sxs-lookup"><span data-stu-id="1472b-624">5061 (0x13C5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-625">Узел кластера уже включен.</span><span class="sxs-lookup"><span data-stu-id="1472b-625">The cluster node is already up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**\_узел кластера \_ ошибок \_ уже \_ отключен**</span><span class="sxs-lookup"><span data-stu-id="1472b-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-627">5062 (0x13C6)</span><span class="sxs-lookup"><span data-stu-id="1472b-627">5062 (0x13C6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-628">Узел кластера уже отключен.</span><span class="sxs-lookup"><span data-stu-id="1472b-628">The cluster node is already down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**Ошибка \_ \_ сети кластера \_ уже в \_ сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-630">5063 (0x13C7)</span><span class="sxs-lookup"><span data-stu-id="1472b-630">5063 (0x13C7)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-631">Сеть кластера уже подключена.</span><span class="sxs-lookup"><span data-stu-id="1472b-631">The cluster network is already online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**Ошибка \_ \_ сети кластера \_ уже \_ вне сети**</span><span class="sxs-lookup"><span data-stu-id="1472b-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-633">5064 (0x13C8)</span><span class="sxs-lookup"><span data-stu-id="1472b-633">5064 (0x13C8)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-634">Сеть кластера уже находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="1472b-634">The cluster network is already offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**\_узел кластера \_ ошибок \_ уже является \_ членом**</span><span class="sxs-lookup"><span data-stu-id="1472b-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-636">5065 (0x13C9)</span><span class="sxs-lookup"><span data-stu-id="1472b-636">5065 (0x13C9)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-637">Узел кластера уже является членом кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-637">The cluster node is already a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**\_ \_ Последняя \_ Внутренняя сеть кластера \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERROR\_CLUSTER\_LAST\_INTERNAL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-639">5066 (0x13CA)</span><span class="sxs-lookup"><span data-stu-id="1472b-639">5066 (0x13CA)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-640">Только сеть кластера настроена для внутреннего взаимодействия между двумя или более активными узлами кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-640">The cluster network is the only one configured for internal cluster communication between two or more active cluster nodes.</span></span> <span data-ttu-id="1472b-641">Возможность внутренней связи не может быть удалена из сети.</span><span class="sxs-lookup"><span data-stu-id="1472b-641">The internal communication capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**Ошибка \_ \_ сеть кластера \_ \_ зависит от**</span><span class="sxs-lookup"><span data-stu-id="1472b-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR\_CLUSTER\_NETWORK\_HAS\_DEPENDENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-643">5067 (0x13CB)</span><span class="sxs-lookup"><span data-stu-id="1472b-643">5067 (0x13CB)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-644">Один или несколько ресурсов кластера зависят от сети для предоставления клиентам услуг.</span><span class="sxs-lookup"><span data-stu-id="1472b-644">One or more cluster resources depend on the network to provide service to clients.</span></span> <span data-ttu-id="1472b-645">Возможность клиентского доступа не может быть удалена из сети.</span><span class="sxs-lookup"><span data-stu-id="1472b-645">The client access capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**Ошибка \_ недопустимой \_ операции \_ с \_ кворумом**</span><span class="sxs-lookup"><span data-stu-id="1472b-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR\_INVALID\_OPERATION\_ON\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-647">5068 (0x13CC)</span><span class="sxs-lookup"><span data-stu-id="1472b-647">5068 (0x13CC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-648">Эта операция не может быть выполнена для ресурса кластера, так как он является ресурсом кворума.</span><span class="sxs-lookup"><span data-stu-id="1472b-648">This operation cannot be performed on the cluster resource as it the quorum resource.</span></span> <span data-ttu-id="1472b-649">Вы не можете перевести ресурс кворума в автономный режим или изменить список возможных владельцев.</span><span class="sxs-lookup"><span data-stu-id="1472b-649">You may not bring the quorum resource offline or modify its possible owners list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**\_зависимость ошибок \_ не \_ разрешена**</span><span class="sxs-lookup"><span data-stu-id="1472b-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**ERROR\_DEPENDENCY\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-651">5069 (0x13CD)</span><span class="sxs-lookup"><span data-stu-id="1472b-651">5069 (0x13CD)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-652">Ресурс кворума кластера не может иметь никаких зависимостей.</span><span class="sxs-lookup"><span data-stu-id="1472b-652">The cluster quorum resource is not allowed to have any dependencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**Ошибка \_ при \_ \_ остановке узла кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR\_CLUSTER\_NODE\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-654">5070 (0x13CE)</span><span class="sxs-lookup"><span data-stu-id="1472b-654">5070 (0x13CE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-655">Узел кластера приостановлен.</span><span class="sxs-lookup"><span data-stu-id="1472b-655">The cluster node is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**узел ошибки не \_ \_ удается \_ разместить \_ ресурс**</span><span class="sxs-lookup"><span data-stu-id="1472b-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR\_NODE\_CANT\_HOST\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-657">5071 (0x13CF)</span><span class="sxs-lookup"><span data-stu-id="1472b-657">5071 (0x13CF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-658">Не удается перевести ресурс кластера в режим "в сети".</span><span class="sxs-lookup"><span data-stu-id="1472b-658">The cluster resource cannot be brought online.</span></span> <span data-ttu-id="1472b-659">Узлу владельца не удается запустить этот ресурс.</span><span class="sxs-lookup"><span data-stu-id="1472b-659">The owner node cannot run this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**\_узел кластера \_ ошибок \_ не \_ готов**</span><span class="sxs-lookup"><span data-stu-id="1472b-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR\_CLUSTER\_NODE\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-661">5072 (0x13D0)</span><span class="sxs-lookup"><span data-stu-id="1472b-661">5072 (0x13D0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-662">Узел кластера не готов к выполнению запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-662">The cluster node is not ready to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**Ошибка \_ при \_ \_ завершении работы узла кластера \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR\_CLUSTER\_NODE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-664">5073 (0x13D1)</span><span class="sxs-lookup"><span data-stu-id="1472b-664">5073 (0x13D1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-665">Узел кластера завершает работу.</span><span class="sxs-lookup"><span data-stu-id="1472b-665">The cluster node is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**Ошибка \_ при \_ присоединении к кластеру \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR\_CLUSTER\_JOIN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-667">5074 (0x13D2)</span><span class="sxs-lookup"><span data-stu-id="1472b-667">5074 (0x13D2)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-668">Операция присоединение к кластеру прервана.</span><span class="sxs-lookup"><span data-stu-id="1472b-668">The cluster join operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**\_ \_ несовместимые версии кластера с ошибками \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR\_CLUSTER\_INCOMPATIBLE\_VERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-670">5075 (0x13D3)</span><span class="sxs-lookup"><span data-stu-id="1472b-670">5075 (0x13D3)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-671">Сбой операции присоединения к кластеру из-за несовместимых версий программного обеспечения между соединяемым узлом и его спонсором.</span><span class="sxs-lookup"><span data-stu-id="1472b-671">The cluster join operation failed due to incompatible software versions between the joining node and its sponsor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**\_ \_ превышено МАКСНУМ кластера ошибок \_ для \_ ресурсов \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR\_CLUSTER\_MAXNUM\_OF\_RESOURCES\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-673">5076 (0x13D4)</span><span class="sxs-lookup"><span data-stu-id="1472b-673">5076 (0x13D4)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-674">Невозможно создать этот ресурс, так как в кластере достигнуто ограничение на количество ресурсов, которое он может отслеживать.</span><span class="sxs-lookup"><span data-stu-id="1472b-674">This resource cannot be created because the cluster has reached the limit on the number of resources it can monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**Ошибка \_ при \_ \_ изменении конфигурации \_ системы кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR\_CLUSTER\_SYSTEM\_CONFIG\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-676">5077 (0x13D5)</span><span class="sxs-lookup"><span data-stu-id="1472b-676">5077 (0x13D5)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-677">Конфигурация системы изменилась во время выполнения операции присоединением к кластеру или формой.</span><span class="sxs-lookup"><span data-stu-id="1472b-677">The system configuration changed during the cluster join or form operation.</span></span> <span data-ttu-id="1472b-678">Операция объединения или формы прервана.</span><span class="sxs-lookup"><span data-stu-id="1472b-678">The join or form operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**\_ \_ тип ресурса кластера \_ ошибок \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-680">5078 (0x13D6)</span><span class="sxs-lookup"><span data-stu-id="1472b-680">5078 (0x13D6)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-681">Указанный тип ресурса не найден.</span><span class="sxs-lookup"><span data-stu-id="1472b-681">The specified resource type was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**Ошибка \_ кластера \_ рестипе \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="1472b-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR\_CLUSTER\_RESTYPE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-683">5079 (0x13D7)</span><span class="sxs-lookup"><span data-stu-id="1472b-683">5079 (0x13D7)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-684">Указанный узел не поддерживает ресурс этого типа.</span><span class="sxs-lookup"><span data-stu-id="1472b-684">The specified node does not support a resource of this type.</span></span> <span data-ttu-id="1472b-685">Это может быть вызвано несоответствием версий или отсутствием DLL-библиотеки ресурсов на этом узле.</span><span class="sxs-lookup"><span data-stu-id="1472b-685">This may be due to version inconsistencies or due to the absence of the resource DLL on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**Ошибка \_ кластера \_ реснаме \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR\_CLUSTER\_RESNAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-687">5080 (0x13D8)</span><span class="sxs-lookup"><span data-stu-id="1472b-687">5080 (0x13D8)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-688">Указанное имя ресурса не поддерживается этой БИБЛИОТЕКой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1472b-688">The specified resource name is not supported by this resource DLL.</span></span> <span data-ttu-id="1472b-689">Это может быть вызвано неправильным (или измененным) именем, переданным в БИБЛИОТЕКУ ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1472b-689">This may be due to a bad (or changed) name supplied to the resource DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**\_кластер ошибок \_ не \_ \_ \_ зарегистрированы пакеты RPC**</span><span class="sxs-lookup"><span data-stu-id="1472b-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR\_CLUSTER\_NO\_RPC\_PACKAGES\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-691">5081 (0x13D9)</span><span class="sxs-lookup"><span data-stu-id="1472b-691">5081 (0x13D9)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-692">Не удалось зарегистрировать пакет проверки подлинности на сервере RPC.</span><span class="sxs-lookup"><span data-stu-id="1472b-692">No authentication package could be registered with the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**Ошибка \_ владельца кластера, \_ \_ не \_ \_ префлист**</span><span class="sxs-lookup"><span data-stu-id="1472b-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR\_CLUSTER\_OWNER\_NOT\_IN\_PREFLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-694">5082 (0x13DA)</span><span class="sxs-lookup"><span data-stu-id="1472b-694">5082 (0x13DA)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-695">Невозможно перевести группу в режим «в сети», так как владелец группы не находится в списке предпочтительных для группы.</span><span class="sxs-lookup"><span data-stu-id="1472b-695">You cannot bring the group online because the owner of the group is not in the preferred list for the group.</span></span> <span data-ttu-id="1472b-696">Чтобы изменить узел владельца для группы, переместите группу.</span><span class="sxs-lookup"><span data-stu-id="1472b-696">To change the owner node for the group, move the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**Ошибка \_ при \_ секмисматч базы данных кластера \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR\_CLUSTER\_DATABASE\_SEQMISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-698">5083 (0x13DB)</span><span class="sxs-lookup"><span data-stu-id="1472b-698">5083 (0x13DB)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-699">Не удалось выполнить операцию JOIN, так как порядковый номер базы данных кластера изменился или несовместим с узлом-блокировкой.</span><span class="sxs-lookup"><span data-stu-id="1472b-699">The join operation failed because the cluster database sequence number has changed or is incompatible with the locker node.</span></span> <span data-ttu-id="1472b-700">Это может произойти во время операции объединения, если база данных кластера была изменена во время объединения.</span><span class="sxs-lookup"><span data-stu-id="1472b-700">This may happen during a join operation if the cluster database was changing during the join.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**Ошибка \_ ресмон \_ недопустимое \_ состояние**</span><span class="sxs-lookup"><span data-stu-id="1472b-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR\_RESMON\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-702">5084 (0x13DC)</span><span class="sxs-lookup"><span data-stu-id="1472b-702">5084 (0x13DC)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-703">Монитор ресурсов не позволит выполнить операцию сбоя, пока ресурс находится в текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="1472b-703">The resource monitor will not allow the fail operation to be performed while the resource is in its current state.</span></span> <span data-ttu-id="1472b-704">Это может произойти, если ресурс находится в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="1472b-704">This may happen if the resource is in a pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**Ошибка \_ кластера \_ переполняется \_ не является \_ блокировкой**</span><span class="sxs-lookup"><span data-stu-id="1472b-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR\_CLUSTER\_GUM\_NOT\_LOCKER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-706">5085 (0x13DD)</span><span class="sxs-lookup"><span data-stu-id="1472b-706">5085 (0x13DD)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-707">Код, не являющийся блокировкой, получил запрос на резервирование блокировки для выполнения глобальных обновлений.</span><span class="sxs-lookup"><span data-stu-id="1472b-707">A non locker code got a request to reserve the lock for making global updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**\_диск кворума ошибок \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1472b-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERROR\_QUORUM\_DISK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-709">5086 (0x13DE)</span><span class="sxs-lookup"><span data-stu-id="1472b-709">5086 (0x13DE)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-710">Не удалось найти диск кворума службой кластеров.</span><span class="sxs-lookup"><span data-stu-id="1472b-710">The quorum disk could not be located by the cluster service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**Ошибка \_ \_ резервного копирования базы данных \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR\_DATABASE\_BACKUP\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-712">5087 (0x13DF)</span><span class="sxs-lookup"><span data-stu-id="1472b-712">5087 (0x13DF)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-713">Возможно, повреждена резервная копия базы данных кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-713">The backed up cluster database is possibly corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**\_узел кластера \_ ошибок \_ уже \_ имеет \_ \_ корень DFS**</span><span class="sxs-lookup"><span data-stu-id="1472b-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_HAS\_DFS\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-715">5088 (0x13E0)</span><span class="sxs-lookup"><span data-stu-id="1472b-715">5088 (0x13E0)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-716">Корень DFS уже существует на этом узле кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-716">A DFS root already exists in this cluster node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**\_ \_ неизменяемое свойство ресурса ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR\_RESOURCE\_PROPERTY\_UNCHANGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-718">5089 (0x13E1)</span><span class="sxs-lookup"><span data-stu-id="1472b-718">5089 (0x13E1)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-719">Сбой при изменении свойства ресурса, так как он конфликтует с другим существующим свойством.</span><span class="sxs-lookup"><span data-stu-id="1472b-719">An attempt to modify a resource property failed because it conflicts with another existing property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**Ошибка \_ " \_ \_ недопустимое \_ состояние членства в кластере"**</span><span class="sxs-lookup"><span data-stu-id="1472b-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-721">5890 (0x1702)</span><span class="sxs-lookup"><span data-stu-id="1472b-721">5890 (0x1702)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-722">Предпринята попытка выполнить операцию, которая несовместима с текущим состоянием членства узла.</span><span class="sxs-lookup"><span data-stu-id="1472b-722">An operation was attempted that is incompatible with the current membership state of the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**Ошибка \_ кластера \_ куорумлог \_ не \_ найдена**</span><span class="sxs-lookup"><span data-stu-id="1472b-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR\_CLUSTER\_QUORUMLOG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-724">5891 (0x1703)</span><span class="sxs-lookup"><span data-stu-id="1472b-724">5891 (0x1703)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-725">Ресурс кворума не содержит журнал кворума.</span><span class="sxs-lookup"><span data-stu-id="1472b-725">The quorum resource does not contain the quorum log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**Ошибка \_ при \_ остановке членства в кластере \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_HALT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-727">5892 (0x1704)</span><span class="sxs-lookup"><span data-stu-id="1472b-727">5892 (0x1704)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-728">Подсистема членства запросила завершение работы службы кластеров на этом узле.</span><span class="sxs-lookup"><span data-stu-id="1472b-728">The membership engine requested shutdown of the cluster service on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии идентификатора экземпляра кластера \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR\_CLUSTER\_INSTANCE\_ID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-730">5893 (0x1705)</span><span class="sxs-lookup"><span data-stu-id="1472b-730">5893 (0x1705)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-731">Не удалось выполнить операцию соединения, так как идентификатор экземпляра кластера присоединенного узла не совпадает с ИДЕНТИФИКАТОРом экземпляра кластера спонсорского узла.</span><span class="sxs-lookup"><span data-stu-id="1472b-731">The join operation failed because the cluster instance ID of the joining node does not match the cluster instance ID of the sponsor node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**\_ \_ \_ \_ \_ для \_ IP-адреса не найдена сеть кластера с ошибками**</span><span class="sxs-lookup"><span data-stu-id="1472b-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND\_FOR\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-733">5894 (0x1706)</span><span class="sxs-lookup"><span data-stu-id="1472b-733">5894 (0x1706)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-734">Не удалось найти соответствующую сеть кластера для указанного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="1472b-734">A matching cluster network for the specified IP address could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**\_несоответствие \_ \_ типов данных \_ свойства \_ кластера ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR\_CLUSTER\_PROPERTY\_DATA\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-736">5895 (0x1707)</span><span class="sxs-lookup"><span data-stu-id="1472b-736">5895 (0x1707)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-737">Фактический тип данных свойства не соответствует ожидаемому типу данных свойства.</span><span class="sxs-lookup"><span data-stu-id="1472b-737">The actual data type of the property did not match the expected data type of the property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**\_кластер ошибок \_ исключить \_ без \_ очистки**</span><span class="sxs-lookup"><span data-stu-id="1472b-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR\_CLUSTER\_EVICT\_WITHOUT\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-739">5896 (0x1708)</span><span class="sxs-lookup"><span data-stu-id="1472b-739">5896 (0x1708)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-740">Узел кластера успешно удален из кластера, но узел не был очищен.</span><span class="sxs-lookup"><span data-stu-id="1472b-740">The cluster node was evicted from the cluster successfully, but the node was not cleaned up.</span></span> <span data-ttu-id="1472b-741">Чтобы определить, какие шаги очистки завершились сбоем и как выполнить восстановление, просмотрите журнал событий приложения отказоустойчивой кластеризации с помощью Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="1472b-741">To determine what cleanup steps failed and how to recover, see the Failover Clustering application event log using Event Viewer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**Ошибка \_ при \_ \_ несоответствии параметров кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR\_CLUSTER\_PARAMETER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-743">5897 (0x1709)</span><span class="sxs-lookup"><span data-stu-id="1472b-743">5897 (0x1709)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-744">Два или более значений параметров, указанных для свойств ресурса, конфликтуют.</span><span class="sxs-lookup"><span data-stu-id="1472b-744">Two or more parameter values specified for a resource's properties are in conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**\_узел ошибки \_ не может \_ быть \_ кластеризованным**</span><span class="sxs-lookup"><span data-stu-id="1472b-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**ERROR\_NODE\_CANNOT\_BE\_CLUSTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-746">5898 (0x170A)</span><span class="sxs-lookup"><span data-stu-id="1472b-746">5898 (0x170A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-747">Этот компьютер невозможно сделать членом кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-747">This computer cannot be made a member of a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**Ошибка \_ кластера \_ неправильной \_ \_ версии ОС**</span><span class="sxs-lookup"><span data-stu-id="1472b-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR\_CLUSTER\_WRONG\_OS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-749">5899 (0x170B)</span><span class="sxs-lookup"><span data-stu-id="1472b-749">5899 (0x170B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-750">Этот компьютер невозможно сделать членом кластера, так как на нем не установлена правильная версия Windows.</span><span class="sxs-lookup"><span data-stu-id="1472b-750">This computer cannot be made a member of a cluster because it does not have the correct version of Windows installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**кластер ошибок не \_ \_ удается \_ создать \_ \_ имя кластера DUP \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR\_CLUSTER\_CANT\_CREATE\_DUP\_CLUSTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-752">5900 (0x170C)</span><span class="sxs-lookup"><span data-stu-id="1472b-752">5900 (0x170C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-753">Невозможно создать кластер с указанным именем кластера, так как это имя кластера уже используется.</span><span class="sxs-lookup"><span data-stu-id="1472b-753">A cluster cannot be created with the specified cluster name because that cluster name is already in use.</span></span> <span data-ttu-id="1472b-754">Укажите другое имя для кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-754">Specify a different name for the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**Ошибка \_ клускфг \_ уже \_ зафиксирована**</span><span class="sxs-lookup"><span data-stu-id="1472b-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR\_CLUSCFG\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-756">5901 (0x170D)</span><span class="sxs-lookup"><span data-stu-id="1472b-756">5901 (0x170D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-757">Действие конфигурации кластера уже зафиксировано.</span><span class="sxs-lookup"><span data-stu-id="1472b-757">The cluster configuration action has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**Ошибка \_ \_ при откате клускфг \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR\_CLUSCFG\_ROLLBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-759">5902 (0x170E)</span><span class="sxs-lookup"><span data-stu-id="1472b-759">5902 (0x170E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-760">Не удалось выполнить откат действия конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-760">The cluster configuration action could not be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**Ошибка \_ клускфг \_ . \_ \_ \_ \_ конфликт букв диска системного диска**</span><span class="sxs-lookup"><span data-stu-id="1472b-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR\_CLUSCFG\_SYSTEM\_DISK\_DRIVE\_LETTER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-762">5903 (0x170F)</span><span class="sxs-lookup"><span data-stu-id="1472b-762">5903 (0x170F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-763">Буква диска, назначенная системному диску на одном узле, конфликтует с буквой диска, назначенной диску на другом узле.</span><span class="sxs-lookup"><span data-stu-id="1472b-763">The drive letter assigned to a system disk on one node conflicted with the drive letter assigned to a disk on another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**\_ \_ старая версия кластера \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERROR\_CLUSTER\_OLD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-765">5904 (0x1710)</span><span class="sxs-lookup"><span data-stu-id="1472b-765">5904 (0x1710)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-766">Один или несколько узлов в кластере работают под управлением версии Windows, которая не поддерживает эту операцию.</span><span class="sxs-lookup"><span data-stu-id="1472b-766">One or more nodes in the cluster are running a version of Windows that does not support this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**Ошибка \_ \_ несоответствие \_ имени учетной ошибки компьютера кластера \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR\_CLUSTER\_MISMATCHED\_COMPUTER\_ACCT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-768">5905 (0x1711)</span><span class="sxs-lookup"><span data-stu-id="1472b-768">5905 (0x1711)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-769">Имя соответствующей учетной записи компьютера не соответствует сетевому имени для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="1472b-769">The name of the corresponding computer account doesn't match the Network Name for this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**\_кластер ошибок \_ нет \_ сетевых \_ адаптеров**</span><span class="sxs-lookup"><span data-stu-id="1472b-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR\_CLUSTER\_NO\_NET\_ADAPTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-771">5906 (0x1712)</span><span class="sxs-lookup"><span data-stu-id="1472b-771">5906 (0x1712)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-772">Нет доступных сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="1472b-772">No network adapters are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**\_кластер ошибок \_ поврежден**</span><span class="sxs-lookup"><span data-stu-id="1472b-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR\_CLUSTER\_POISONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-774">5907 (0x1713)</span><span class="sxs-lookup"><span data-stu-id="1472b-774">5907 (0x1713)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-775">Узел кластера поврежден.</span><span class="sxs-lookup"><span data-stu-id="1472b-775">The cluster node has been poisoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**Ошибка \_ при \_ перемещении группы кластеров \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR\_CLUSTER\_GROUP\_MOVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-777">5908 (0x1714)</span><span class="sxs-lookup"><span data-stu-id="1472b-777">5908 (0x1714)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-778">Группе не удалось принять запрос, так как он перемещается на другой узел.</span><span class="sxs-lookup"><span data-stu-id="1472b-778">The group is unable to accept the request since it is moving to another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**\_ \_ тип ресурса кластера \_ ошибок \_ занят**</span><span class="sxs-lookup"><span data-stu-id="1472b-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-780">5909 (0x1715)</span><span class="sxs-lookup"><span data-stu-id="1472b-780">5909 (0x1715)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-781">Тип ресурса не может принять запрос, так как он слишком занят выполнением другой операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-781">The resource type cannot accept the request since is too busy performing another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**\_ \_ \_ истекло время ожидания при ВЫЗОВЕ ресурса при ошибке \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**ERROR\_RESOURCE\_CALL\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-783">5910 (0x1716)</span><span class="sxs-lookup"><span data-stu-id="1472b-783">5910 (0x1716)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-784">Истекло время ожидания вызова библиотеки DLL ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-784">The call to the cluster resource DLL timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**Ошибка \_ недопустимого \_ \_ IPv6- \_ адреса кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR\_INVALID\_CLUSTER\_IPV6\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-786">5911 (0x1717)</span><span class="sxs-lookup"><span data-stu-id="1472b-786">5911 (0x1717)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-787">Недопустимый адрес для ресурса IPv6-адреса.</span><span class="sxs-lookup"><span data-stu-id="1472b-787">The address is not valid for an IPv6 Address resource.</span></span> <span data-ttu-id="1472b-788">Требуется глобальный IPv6-адрес, который должен соответствовать сети кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-788">A global IPv6 address is required, and it must match a cluster network.</span></span> <span data-ttu-id="1472b-789">Адреса совместимости запрещены.</span><span class="sxs-lookup"><span data-stu-id="1472b-789">Compatibility addresses are not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**Ошибка \_ при \_ внутренней \_ недопустимой \_ функции кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR\_CLUSTER\_INTERNAL\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-791">5912 (0x1718)</span><span class="sxs-lookup"><span data-stu-id="1472b-791">5912 (0x1718)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-792">Произошла внутренняя ошибка кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-792">An internal cluster error occurred.</span></span> <span data-ttu-id="1472b-793">Предпринята попытка вызова недопустимой функции.</span><span class="sxs-lookup"><span data-stu-id="1472b-793">A call to an invalid function was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**\_параметр кластера ошибок вне допустимых \_ \_ \_ \_ границ**</span><span class="sxs-lookup"><span data-stu-id="1472b-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERROR\_CLUSTER\_PARAMETER\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-795">5913 (0x1719)</span><span class="sxs-lookup"><span data-stu-id="1472b-795">5913 (0x1719)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-796">Значение параметра выходит за пределы допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="1472b-796">A parameter value is out of acceptable range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**Ошибка \_ \_ частичной \_ отправки кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR\_CLUSTER\_PARTIAL\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-798">5914 (0x171A)</span><span class="sxs-lookup"><span data-stu-id="1472b-798">5914 (0x171A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-799">Произошла сетевая ошибка при отправке данных на другой узел в кластере.</span><span class="sxs-lookup"><span data-stu-id="1472b-799">A network error occurred while sending data to another node in the cluster.</span></span> <span data-ttu-id="1472b-800">Количество переданных байтов было меньше, чем требовалось.</span><span class="sxs-lookup"><span data-stu-id="1472b-800">The number of bytes transmitted was less than required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**Ошибка \_ \_ \_ недопустимая функция реестра кластера \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR\_CLUSTER\_REGISTRY\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-802">5915 (0x171B)</span><span class="sxs-lookup"><span data-stu-id="1472b-802">5915 (0x171B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-803">Предпринята попытка выполнить недопустимую операцию реестра кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-803">An invalid cluster registry operation was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**кластер ошибок " \_ \_ недопустимое \_ \_ Завершение строки"**</span><span class="sxs-lookup"><span data-stu-id="1472b-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_TERMINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-805">5916 (0x171C)</span><span class="sxs-lookup"><span data-stu-id="1472b-805">5916 (0x171C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-806">Входная строка символов не завершена должным образом.</span><span class="sxs-lookup"><span data-stu-id="1472b-806">An input string of characters is not properly terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**\_ \_ Недопустимый \_ Формат строки кластера ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-808">5917 (0x171D)</span><span class="sxs-lookup"><span data-stu-id="1472b-808">5917 (0x171D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-809">Входная строка символов имеет недопустимый формат для данных, которые он представляет.</span><span class="sxs-lookup"><span data-stu-id="1472b-809">An input string of characters is not in a valid format for the data it represents.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**Ошибка \_ \_ \_ \_ при выполнении транзакции базы данных кластера \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-811">5918 (0x171E)</span><span class="sxs-lookup"><span data-stu-id="1472b-811">5918 (0x171E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-812">Произошла внутренняя ошибка кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-812">An internal cluster error occurred.</span></span> <span data-ttu-id="1472b-813">Предпринята попытка транзакции базы данных кластера, пока транзакция уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="1472b-813">A cluster database transaction was attempted while a transaction was already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**Ошибка \_ \_ \_ \_ \_ при \_ выполнении транзакции базы данных кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-815">5919 (0x171F)</span><span class="sxs-lookup"><span data-stu-id="1472b-815">5919 (0x171F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-816">Произошла внутренняя ошибка кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-816">An internal cluster error occurred.</span></span> <span data-ttu-id="1472b-817">Предпринята попытка зафиксировать транзакцию базы данных кластера, пока не выполнялась транзакция.</span><span class="sxs-lookup"><span data-stu-id="1472b-817">There was an attempt to commit a cluster database transaction while no transaction was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**Ошибка в \_ кластере \_ \_ данных null**</span><span class="sxs-lookup"><span data-stu-id="1472b-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR\_CLUSTER\_NULL\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-819">5920 (0x1720)</span><span class="sxs-lookup"><span data-stu-id="1472b-819">5920 (0x1720)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-820">Произошла внутренняя ошибка кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-820">An internal cluster error occurred.</span></span> <span data-ttu-id="1472b-821">Данные не были должным образом инициализированы.</span><span class="sxs-lookup"><span data-stu-id="1472b-821">Data was not properly initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**Ошибка \_ при \_ частичном \_ чтении кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR\_CLUSTER\_PARTIAL\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-823">5921 (0x1721)</span><span class="sxs-lookup"><span data-stu-id="1472b-823">5921 (0x1721)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-824">Произошла ошибка при чтении из потока данных.</span><span class="sxs-lookup"><span data-stu-id="1472b-824">An error occurred while reading from a stream of data.</span></span> <span data-ttu-id="1472b-825">Возвращено непредвиденное число байтов.</span><span class="sxs-lookup"><span data-stu-id="1472b-825">An unexpected number of bytes was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**Ошибка \_ \_ частичной записи в кластере \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR\_CLUSTER\_PARTIAL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-827">5922 (0x1722)</span><span class="sxs-lookup"><span data-stu-id="1472b-827">5922 (0x1722)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-828">Произошла ошибка при записи в поток данных.</span><span class="sxs-lookup"><span data-stu-id="1472b-828">An error occurred while writing to a stream of data.</span></span> <span data-ttu-id="1472b-829">Не удалось записать требуемое число байтов.</span><span class="sxs-lookup"><span data-stu-id="1472b-829">The required number of bytes could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**кластер ошибок не \_ \_ удается \_ десериализовать \_ данные**</span><span class="sxs-lookup"><span data-stu-id="1472b-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR\_CLUSTER\_CANT\_DESERIALIZE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-831">5923 (0x1723)</span><span class="sxs-lookup"><span data-stu-id="1472b-831">5923 (0x1723)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-832">Произошла ошибка при десериализации потока данных кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-832">An error occurred while deserializing a stream of cluster data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_ \_ \_ конфликт свойств ресурса, ЗАВИСИМого от ошибки \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR\_DEPENDENT\_RESOURCE\_PROPERTY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-834">5924 (0x1724)</span><span class="sxs-lookup"><span data-stu-id="1472b-834">5924 (0x1724)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-835">Одно или несколько значений свойств для этого ресурса конфликтуют с одним или несколькими значениями свойств, связанными с зависимыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="1472b-835">One or more property values for this resource are in conflict with one or more property values associated with its dependent resource(s).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**\_кластер ошибок \_ без \_ кворума**</span><span class="sxs-lookup"><span data-stu-id="1472b-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR\_CLUSTER\_NO\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-837">5925 (0x1725)</span><span class="sxs-lookup"><span data-stu-id="1472b-837">5925 (0x1725)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-838">Отсутствует кворум узлов кластера для формирования кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-838">A quorum of cluster nodes was not present to form a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**\_Кластер ошибок \_ -Недопустимая \_ \_ сеть IPv6**</span><span class="sxs-lookup"><span data-stu-id="1472b-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-840">5926 (0x1726)</span><span class="sxs-lookup"><span data-stu-id="1472b-840">5926 (0x1726)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-841">Сеть кластера недопустима для ресурса IPv6-адреса или не соответствует заданному адресу.</span><span class="sxs-lookup"><span data-stu-id="1472b-841">The cluster network is not valid for an IPv6 Address resource, or it does not match the configured address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**\_Кластер ошибок \_ Недопустимая \_ \_ туннельная \_ сеть IPv6**</span><span class="sxs-lookup"><span data-stu-id="1472b-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_TUNNEL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-843">5927 (0x1727)</span><span class="sxs-lookup"><span data-stu-id="1472b-843">5927 (0x1727)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-844">Сеть кластера недопустима для ресурса туннеля IPv6.</span><span class="sxs-lookup"><span data-stu-id="1472b-844">The cluster network is not valid for an IPv6 Tunnel resource.</span></span> <span data-ttu-id="1472b-845">Проверьте конфигурацию ресурса IP-адреса, от которого зависит туннельный ресурс IPv6.</span><span class="sxs-lookup"><span data-stu-id="1472b-845">Check the configuration of the IP Address resource on which the IPv6 Tunnel resource depends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_ \_ \_ \_ в \_ этой \_ группе не допускается использование кворума "ошибка"**</span><span class="sxs-lookup"><span data-stu-id="1472b-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**ERROR\_QUORUM\_NOT\_ALLOWED\_IN\_THIS\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-847">5928 (0x1728)</span><span class="sxs-lookup"><span data-stu-id="1472b-847">5928 (0x1728)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-848">Ресурс кворума не может находиться в доступной группе хранения.</span><span class="sxs-lookup"><span data-stu-id="1472b-848">Quorum resource cannot reside in the Available Storage group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**\_дерево зависимостей \_ ошибок \_ слишком \_ сложное**</span><span class="sxs-lookup"><span data-stu-id="1472b-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ERROR\_DEPENDENCY\_TREE\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-850">5929 (0x1729)</span><span class="sxs-lookup"><span data-stu-id="1472b-850">5929 (0x1729)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-851">Зависимости для этого ресурса имеют слишком глубокий уровень вложенности.</span><span class="sxs-lookup"><span data-stu-id="1472b-851">The dependencies for this resource are nested too deeply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**Ошибка \_ исключения \_ в \_ \_ вызове ресурса**</span><span class="sxs-lookup"><span data-stu-id="1472b-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**ERROR\_EXCEPTION\_IN\_RESOURCE\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-853">5930 (0x172A)</span><span class="sxs-lookup"><span data-stu-id="1472b-853">5930 (0x172A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-854">Вызов библиотеки DLL ресурсов вызвал необработанное исключение.</span><span class="sxs-lookup"><span data-stu-id="1472b-854">The call into the resource DLL raised an unhandled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**Ошибка \_ \_ \_ при инициализации "сбой кластера RHS" \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR\_CLUSTER\_RHS\_FAILED\_INITIALIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-856">5931 (0x172B)</span><span class="sxs-lookup"><span data-stu-id="1472b-856">5931 (0x172B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-857">Не удалось инициализировать процесс RHS.</span><span class="sxs-lookup"><span data-stu-id="1472b-857">The RHS process failed to initialize.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**\_кластер ошибок \_ не \_ установлен**</span><span class="sxs-lookup"><span data-stu-id="1472b-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERROR\_CLUSTER\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-859">5932 (0x172C)</span><span class="sxs-lookup"><span data-stu-id="1472b-859">5932 (0x172C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-860">Компонент отказоустойчивой кластеризации не установлен на этом узле.</span><span class="sxs-lookup"><span data-stu-id="1472b-860">The Failover Clustering feature is not installed on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ресурсы кластера \_ ошибок \_ должны \_ находиться \_ в \_ сети \_ на \_ одном \_ узле**</span><span class="sxs-lookup"><span data-stu-id="1472b-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**ERROR\_CLUSTER\_RESOURCES\_MUST\_BE\_ONLINE\_ON\_THE\_SAME\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-862">5933 (0x172D)</span><span class="sxs-lookup"><span data-stu-id="1472b-862">5933 (0x172D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-863">Для этой операции ресурсы должны находиться в сети на одном узле.</span><span class="sxs-lookup"><span data-stu-id="1472b-863">The resources must be online on the same node for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_ \_ Максимальное количество узлов кластера с ошибками \_ \_ в \_ кластере**</span><span class="sxs-lookup"><span data-stu-id="1472b-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR\_CLUSTER\_MAX\_NODES\_IN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-865">5934 (0x172E)</span><span class="sxs-lookup"><span data-stu-id="1472b-865">5934 (0x172E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-866">Невозможно добавить новый узел, так как этот кластер уже находится на максимальном количестве узлов.</span><span class="sxs-lookup"><span data-stu-id="1472b-866">A new node can not be added since this cluster is already at its maximum number of nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**Ошибка \_ кластера \_ слишком \_ большого количества \_ узлов**</span><span class="sxs-lookup"><span data-stu-id="1472b-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR\_CLUSTER\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-868">5935 (0x172F)</span><span class="sxs-lookup"><span data-stu-id="1472b-868">5935 (0x172F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-869">Невозможно создать этот кластер, так как указанное число узлов превышает максимально допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="1472b-869">This cluster can not be created since the specified number of nodes exceeds the maximum allowed limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**\_объект кластера \_ ошибок \_ уже \_ используется**</span><span class="sxs-lookup"><span data-stu-id="1472b-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERROR\_CLUSTER\_OBJECT\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-871">5936 (0x1730)</span><span class="sxs-lookup"><span data-stu-id="1472b-871">5936 (0x1730)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-872">Попытка использовать указанное имя кластера завершилась сбоем, так как в домене уже существует включенный объект компьютера с данным именем.</span><span class="sxs-lookup"><span data-stu-id="1472b-872">An attempt to use the specified cluster name failed because an enabled computer object with the given name already exists in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**\_ \_ обнаружены неключевые группы ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR\_NONCORE\_GROUPS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-874">5937 (0x1731)</span><span class="sxs-lookup"><span data-stu-id="1472b-874">5937 (0x1731)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-875">Этот кластер не может быть уничтожен.</span><span class="sxs-lookup"><span data-stu-id="1472b-875">This cluster cannot be destroyed.</span></span> <span data-ttu-id="1472b-876">Она содержит неосновные группы приложений, которые необходимо удалить перед уничтожением кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-876">It has non-core application groups which must be deleted before the cluster can be destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**Ошибка \_ при \_ \_ конфликте ресурсов общего файлового ресурса \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERROR\_FILE\_SHARE\_RESOURCE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-878">5938 (0x1732)</span><span class="sxs-lookup"><span data-stu-id="1472b-878">5938 (0x1732)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-879">Общая папка, связанная с ресурсом-свидетелем файлового ресурса, не может размещаться в этом кластере или на любом из его узлов.</span><span class="sxs-lookup"><span data-stu-id="1472b-879">File share associated with file share witness resource cannot be hosted by this cluster or any of its nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**кластер ошибок " \_ \_ исключить \_ Недопустимый \_ запрос"**</span><span class="sxs-lookup"><span data-stu-id="1472b-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR\_CLUSTER\_EVICT\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-881">5939 (0x1733)</span><span class="sxs-lookup"><span data-stu-id="1472b-881">5939 (0x1733)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-882">В данный момент вытеснение этого узла недопустимо.</span><span class="sxs-lookup"><span data-stu-id="1472b-882">Eviction of this node is invalid at this time.</span></span> <span data-ttu-id="1472b-883">Из-за превышения требований к кворуму операция вытеснения узла приведет к завершению работы кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-883">Due to quorum requirements node eviction will result in cluster shutdown.</span></span> <span data-ttu-id="1472b-884">Если это последний узел в кластере, следует использовать команду уничтожения кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-884">If it is the last node in the cluster, destroy cluster command should be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**Ошибка \_ \_ SINGLETON — \_ ресурс кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**ERROR\_CLUSTER\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-886">5940 (0x1734)</span><span class="sxs-lookup"><span data-stu-id="1472b-886">5940 (0x1734)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-887">В кластере допускается только один экземпляр этого типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1472b-887">Only one instance of this resource type is allowed in the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**Ошибка \_ \_ \_ одноэлементного \_ ресурса группы кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERROR\_CLUSTER\_GROUP\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-889">5941 (0x1735)</span><span class="sxs-lookup"><span data-stu-id="1472b-889">5941 (0x1735)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-890">Для каждой группы ресурсов допускается только один экземпляр этого типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="1472b-890">Only one instance of this resource type is allowed per resource group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**Ошибка \_ \_ \_ \_ при попытке поставщика ресурсов кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR\_CLUSTER\_RESOURCE\_PROVIDER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-892">5942 (0x1736)</span><span class="sxs-lookup"><span data-stu-id="1472b-892">5942 (0x1736)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-893">Не удалось перевести ресурс в режим "в сети" из-за сбоя одного или нескольких ресурсов поставщика.</span><span class="sxs-lookup"><span data-stu-id="1472b-893">The resource failed to come online due to the failure of one or more provider resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**Ошибка \_ \_ конфигурации ресурса \_ кластера \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR\_CLUSTER\_RESOURCE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-895">5943 (0x1737)</span><span class="sxs-lookup"><span data-stu-id="1472b-895">5943 (0x1737)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-896">Ресурс указал, что он не может быть подключен к сети на любом узле.</span><span class="sxs-lookup"><span data-stu-id="1472b-896">The resource has indicated that it cannot come online on any node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**Группа "ошибка \_ кластера \_ \_ занята"**</span><span class="sxs-lookup"><span data-stu-id="1472b-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERROR\_CLUSTER\_GROUP\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-898">5944 (0x1738)</span><span class="sxs-lookup"><span data-stu-id="1472b-898">5944 (0x1738)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-899">В настоящее время невозможно выполнить текущую операцию в этой группе.</span><span class="sxs-lookup"><span data-stu-id="1472b-899">The current operation cannot be performed on this group at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**\_кластер ошибок \_ не является \_ общим \_ томом**</span><span class="sxs-lookup"><span data-stu-id="1472b-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR\_CLUSTER\_NOT\_SHARED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-901">5945 (0x1739)</span><span class="sxs-lookup"><span data-stu-id="1472b-901">5945 (0x1739)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-902">Каталог или файл не расположены на общем томе кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-902">The directory or file is not located on a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**\_ \_ Недопустимый \_ дескриптор безопасности кластера ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR\_CLUSTER\_INVALID\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-904">5946 (0x173A)</span><span class="sxs-lookup"><span data-stu-id="1472b-904">5946 (0x173A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-905">Дескриптор безопасности не отвечает требованиям кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-905">The Security Descriptor does not meet the requirements for a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ Общие тома кластера \_ ошибок \_ \_ используются**</span><span class="sxs-lookup"><span data-stu-id="1472b-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR\_CLUSTER\_SHARED\_VOLUMES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-907">5947 (0x173B)</span><span class="sxs-lookup"><span data-stu-id="1472b-907">5947 (0x173B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-908">В кластере настроен один или несколько ресурсов общих томов.</span><span class="sxs-lookup"><span data-stu-id="1472b-908">There is one or more shared volumes resources configured in the cluster.</span></span> <span data-ttu-id="1472b-909">Эти ресурсы необходимо переместить в Доступное хранилище, чтобы обеспечить успешную работу.</span><span class="sxs-lookup"><span data-stu-id="1472b-909">Those resources must be moved to available storage in order for operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**\_ \_ использование \_ \_ API общих ТОМОВ \_ в кластере ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR\_CLUSTER\_USE\_SHARED\_VOLUMES\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-911">5948 (0x173C)</span><span class="sxs-lookup"><span data-stu-id="1472b-911">5948 (0x173C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-912">Этой группе или ресурсу нельзя управлять напрямую.</span><span class="sxs-lookup"><span data-stu-id="1472b-912">This group or resource cannot be directly manipulated.</span></span> <span data-ttu-id="1472b-913">Используйте интерфейсы API общего тома для выполнения требуемой операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-913">Use shared volume APIs to perform desired operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**\_ \_ выполняется резервное копирование кластера \_ ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR\_CLUSTER\_BACKUP\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-915">5949 (0x173D)</span><span class="sxs-lookup"><span data-stu-id="1472b-915">5949 (0x173D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-916">Выполняется резервное копирование.</span><span class="sxs-lookup"><span data-stu-id="1472b-916">Back up is in progress.</span></span> <span data-ttu-id="1472b-917">Перед повторным выполнением этой операции дождитесь завершения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="1472b-917">Please wait for backup completion before trying this operation again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**Ошибка \_ не \_ CSV- \_ путь**</span><span class="sxs-lookup"><span data-stu-id="1472b-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR\_NON\_CSV\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-919">5950 (0x173E)</span><span class="sxs-lookup"><span data-stu-id="1472b-919">5950 (0x173E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-920">Путь не принадлежит к общему тому кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-920">The path does not belong to a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**Ошибка \_ тома CSV, \_ \_ не \_ локального**</span><span class="sxs-lookup"><span data-stu-id="1472b-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR\_CSV\_VOLUME\_NOT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-922">5951 (0x173F)</span><span class="sxs-lookup"><span data-stu-id="1472b-922">5951 (0x173F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-923">Общий том кластера не подключен к этому узлу локально.</span><span class="sxs-lookup"><span data-stu-id="1472b-923">The cluster shared volume is not locally mounted on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**Ошибка \_ при \_ прерывании наблюдения за кластером \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR\_CLUSTER\_WATCHDOG\_TERMINATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-925">5952 (0x1740)</span><span class="sxs-lookup"><span data-stu-id="1472b-925">5952 (0x1740)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-926">Модуль наблюдения за кластером завершает работу.</span><span class="sxs-lookup"><span data-stu-id="1472b-926">The cluster watchdog is terminating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**Ошибка \_ ресурс кластера с \_ \_ ЗАПРЕТом \_ перемещения \_ несовместимые \_ узлы**</span><span class="sxs-lookup"><span data-stu-id="1472b-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_INCOMPATIBLE\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-928">5953 (0x1741)</span><span class="sxs-lookup"><span data-stu-id="1472b-928">5953 (0x1741)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-929">Ресурс запретил перемещение между двумя узлами, так как они несовместимы.</span><span class="sxs-lookup"><span data-stu-id="1472b-929">A resource vetoed a move between two nodes because they are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**\_ \_ Недопустимый \_ вес узла в кластере ошибок \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERROR\_CLUSTER\_INVALID\_NODE\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-931">5954 (0x1742)</span><span class="sxs-lookup"><span data-stu-id="1472b-931">5954 (0x1742)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-932">Запрос является недопустимым либо из-за того, что вес узла не может быть изменен, пока кластер находится в режиме кворума "только диск" или если изменение веса узла привело к нарушению минимальных требований кворума кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-932">The request is invalid either because node weight cannot be changed while the cluster is in disk-only quorum mode, or because changing the node weight would violate the minimum cluster quorum requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**Ошибка \_ при \_ \_ \_ вызове незаблокированного ресурса кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-934">5955 (0x1743)</span><span class="sxs-lookup"><span data-stu-id="1472b-934">5955 (0x1743)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-935">Ресурс запретил вызов.</span><span class="sxs-lookup"><span data-stu-id="1472b-935">The resource vetoed the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**Ошибка \_ ресмон \_ . \_ \_ нехватка системных ресурсов**</span><span class="sxs-lookup"><span data-stu-id="1472b-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR\_RESMON\_SYSTEM\_RESOURCES\_LACKING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-937">5956 (0x1744)</span><span class="sxs-lookup"><span data-stu-id="1472b-937">5956 (0x1744)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-938">Не удалось запустить или запустить ресурс, поскольку ему не удалось зарезервировать достаточные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="1472b-938">Resource could not start or run because it could not reserve sufficient system resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**Ошибка \_ " \_ ресурс кластера \_ запрещен" \_ Перемещение \_ не \_ хватает \_ ресурсов \_ в \_ месте назначения**</span><span class="sxs-lookup"><span data-stu-id="1472b-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_DESTINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-940">5957 (0x1745)</span><span class="sxs-lookup"><span data-stu-id="1472b-940">5957 (0x1745)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-941">Ресурс запретил перемещение между двумя узлами, так как в настоящее время в целевом объекте недостаточно ресурсов для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-941">A resource vetoed a move between two nodes because the destination currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**Ошибка \_ " \_ ресурс кластера \_ запрещен" \_ Перемещение \_ не \_ хватает \_ ресурсов \_ в \_ источнике**</span><span class="sxs-lookup"><span data-stu-id="1472b-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-943">5958 (0x1746)</span><span class="sxs-lookup"><span data-stu-id="1472b-943">5958 (0x1746)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-944">Ресурс запретил перемещение между двумя узлами, так как в настоящее время в источнике недостаточно ресурсов для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-944">A resource vetoed a move between two nodes because the source currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**\_Группа кластера \_ ошибок \_ в очереди**</span><span class="sxs-lookup"><span data-stu-id="1472b-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR\_CLUSTER\_GROUP\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-946">5959 (0x1747)</span><span class="sxs-lookup"><span data-stu-id="1472b-946">5959 (0x1747)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-947">Не удается выполнить запрошенную операцию, так как группа поставлена в очередь для операции.</span><span class="sxs-lookup"><span data-stu-id="1472b-947">The requested operation can not be completed because the group is queued for an operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**\_ \_ \_ состояние блокировки ресурса кластера \_ ошибок**</span><span class="sxs-lookup"><span data-stu-id="1472b-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR\_CLUSTER\_RESOURCE\_LOCKED\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-949">5960 (0x1748)</span><span class="sxs-lookup"><span data-stu-id="1472b-949">5960 (0x1748)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-950">Запрошенная операция не может быть завершена, так как ресурс заблокирован.</span><span class="sxs-lookup"><span data-stu-id="1472b-950">The requested operation can not be completed because a resource has locked status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**Ошибка \_ \_ \_ \_ отработки отказа общего тома кластера \_ не \_ разрешена**</span><span class="sxs-lookup"><span data-stu-id="1472b-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_FAILOVER\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-952">5961 (0x1749)</span><span class="sxs-lookup"><span data-stu-id="1472b-952">5961 (0x1749)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-953">Ресурс не может быть перемещен на другой узел, так как общий том кластера запретил операцию.</span><span class="sxs-lookup"><span data-stu-id="1472b-953">The resource cannot move to another node because a cluster shared volume vetoed the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**Ошибка \_ \_ \_ \_ при выполнении очистки узла \_ кластера**</span><span class="sxs-lookup"><span data-stu-id="1472b-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR\_CLUSTER\_NODE\_DRAIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-955">5962 (0x174A)</span><span class="sxs-lookup"><span data-stu-id="1472b-955">5962 (0x174A)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-956">Очистка узла уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="1472b-956">A node drain is already in progress.</span></span>

<span data-ttu-id="1472b-957">Это значение также называется " **Ошибка \_ \_ узла кластера \_ эвакуации \_ \_** "</span><span class="sxs-lookup"><span data-stu-id="1472b-957">This value was also named **ERROR\_CLUSTER\_NODE\_EVACUATION\_IN\_PROGRESS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**Ошибка \_ " \_ диск кластера \_ не \_ подключен"**</span><span class="sxs-lookup"><span data-stu-id="1472b-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR\_CLUSTER\_DISK\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-959">5963 (0x174B)</span><span class="sxs-lookup"><span data-stu-id="1472b-959">5963 (0x174B)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-960">Кластерное хранилище не подключено к узлу.</span><span class="sxs-lookup"><span data-stu-id="1472b-960">Clustered storage is not connected to the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**\_диск ошибок \_ не \_ \_ поддерживает CSV**</span><span class="sxs-lookup"><span data-stu-id="1472b-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR\_DISK\_NOT\_CSV\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-962">5964 (0x174C)</span><span class="sxs-lookup"><span data-stu-id="1472b-962">5964 (0x174C)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-963">Диск не настроен таким образом, чтобы его можно было использовать с CSV.</span><span class="sxs-lookup"><span data-stu-id="1472b-963">The disk is not configured in a way to be used with CSV.</span></span> <span data-ttu-id="1472b-964">Диски CSV должны иметь по крайней мере один раздел, отформатированный с помощью NTFS.</span><span class="sxs-lookup"><span data-stu-id="1472b-964">CSV disks must have at least one partition that is formatted with NTFS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**\_ресурс ошибки \_ не \_ в \_ доступном \_ хранилище**</span><span class="sxs-lookup"><span data-stu-id="1472b-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**ERROR\_RESOURCE\_NOT\_IN\_AVAILABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-966">5965 (0x174D)</span><span class="sxs-lookup"><span data-stu-id="1472b-966">5965 (0x174D)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-967">Для выполнения этого действия ресурс должен быть частью доступной группы хранения.</span><span class="sxs-lookup"><span data-stu-id="1472b-967">The resource must be part of the Available Storage group to complete this action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**\_ \_ общий том кластера \_ ошибок \_ перенаправлен**</span><span class="sxs-lookup"><span data-stu-id="1472b-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-969">5966 (0x174E)</span><span class="sxs-lookup"><span data-stu-id="1472b-969">5966 (0x174E)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-970">CSVFS не удалось выполнить операцию, так как том находится в перенаправленном режиме.</span><span class="sxs-lookup"><span data-stu-id="1472b-970">CSVFS failed operation as volume is in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**\_ \_ общий том кластера \_ ошибок \_ не \_ перенаправлен**</span><span class="sxs-lookup"><span data-stu-id="1472b-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-972">5967 (0x174F)</span><span class="sxs-lookup"><span data-stu-id="1472b-972">5967 (0x174F)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-973">CSVFS не удалось выполнить операцию, так как том не находится в перенаправленном режиме.</span><span class="sxs-lookup"><span data-stu-id="1472b-973">CSVFS failed operation as volume is not in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**\_кластер ошибок \_ не может \_ возвращать \_ Свойства**</span><span class="sxs-lookup"><span data-stu-id="1472b-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**ERROR\_CLUSTER\_CANNOT\_RETURN\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-975">5968 (0x1750)</span><span class="sxs-lookup"><span data-stu-id="1472b-975">5968 (0x1750)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-976">В настоящее время невозможно вернуть свойства кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-976">Cluster properties cannot be returned at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**\_ресурс кластера \_ ошибок \_ содержит \_ неподдерживаемую \_ \_ область копирования \_ для \_ общих \_ томов**</span><span class="sxs-lookup"><span data-stu-id="1472b-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERROR\_CLUSTER\_RESOURCE\_CONTAINS\_UNSUPPORTED\_DIFF\_AREA\_FOR\_SHARED\_VOLUMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-978">5969 (0x1751)</span><span class="sxs-lookup"><span data-stu-id="1472b-978">5969 (0x1751)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-979">Ресурс "кластерный диск" содержит область копирования моментальных снимков программного обеспечения, которая не поддерживается для общих томов кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-979">The clustered disk resource contains software snapshot diff area that are not supported for Cluster Shared Volumes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**Ошибка \_ \_ ресурса кластера \_ \_ в \_ режиме обслуживания \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_IN\_MAINTENANCE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-981">5970 (0x1752)</span><span class="sxs-lookup"><span data-stu-id="1472b-981">5970 (0x1752)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-982">Невозможно завершить операцию, так как ресурс находится в режиме обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1472b-982">The operation cannot be completed because the resource is in maintenance mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**Ошибка \_ при \_ конфликте сходства кластера \_**</span><span class="sxs-lookup"><span data-stu-id="1472b-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR\_CLUSTER\_AFFINITY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-984">5971 (0x1753)</span><span class="sxs-lookup"><span data-stu-id="1472b-984">5971 (0x1753)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-985">Не удается завершить операцию из-за конфликтов сходства кластера.</span><span class="sxs-lookup"><span data-stu-id="1472b-985">The operation cannot be completed because of cluster affinity conflicts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1472b-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**\_ресурс кластера \_ ошибок \_ — \_ реплика \_ виртуальной \_ машины**</span><span class="sxs-lookup"><span data-stu-id="1472b-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_REPLICA\_VIRTUAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1472b-987">5972 (0x1754)</span><span class="sxs-lookup"><span data-stu-id="1472b-987">5972 (0x1754)</span></span>
</dt> <dt>



<span data-ttu-id="1472b-988">Невозможно выполнить операцию, так как ресурс является репликой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1472b-988">The operation cannot be completed because the resource is a replica virtual machine.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="1472b-989">Требования</span><span class="sxs-lookup"><span data-stu-id="1472b-989">Requirements</span></span>



| <span data-ttu-id="1472b-990">Требование</span><span class="sxs-lookup"><span data-stu-id="1472b-990">Requirement</span></span> | <span data-ttu-id="1472b-991">Значение</span><span class="sxs-lookup"><span data-stu-id="1472b-991">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1472b-992">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1472b-992">Minimum supported client</span></span><br/> | <span data-ttu-id="1472b-993">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1472b-993">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1472b-994">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1472b-994">Minimum supported server</span></span><br/> | <span data-ttu-id="1472b-995">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1472b-995">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1472b-996">Header</span><span class="sxs-lookup"><span data-stu-id="1472b-996">Header</span></span><br/>                   | <dl> <span data-ttu-id="1472b-997"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="1472b-997"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1472b-998">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1472b-998">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1472b-999">Коды системных ошибок</span><span class="sxs-lookup"><span data-stu-id="1472b-999">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




