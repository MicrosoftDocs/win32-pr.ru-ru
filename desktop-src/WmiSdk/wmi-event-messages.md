---
description: В следующем списке перечислены события, поддерживаемые журналами WMI в Windows Vista и более поздних операционных системах.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Сообщения о событиях WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711733"
---
# <a name="wmi-event-messages"></a><span data-ttu-id="1c35c-103">Сообщения о событиях WMI</span><span class="sxs-lookup"><span data-stu-id="1c35c-103">WMI Event Messages</span></span>

<span data-ttu-id="1c35c-104">В следующем списке перечислены события, поддерживаемые журналами WMI в Windows Vista и более поздних операционных системах.</span><span class="sxs-lookup"><span data-stu-id="1c35c-104">The following list lists events supported by WMI logs in Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="1c35c-105">Следующая документация предназначена для разработчиков и ИТ-администраторов.</span><span class="sxs-lookup"><span data-stu-id="1c35c-105">The following documentation is designed for developers and IT administrators.</span></span> <span data-ttu-id="1c35c-106">Если вы пытаетесь разрешить сообщение об ошибке WMI в домашней системе, обратитесь к веб-сайту [Служба поддержки Майкрософт](https://support.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="1c35c-106">If you are attempting to resolve a WMI error message on your home system, please refer to the [Microsoft Support](https://support.microsoft.com/) website.</span></span>

 

<dl> <dt>

<span data-ttu-id="1c35c-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_репозиторий WBEM MC не \_ \_ согласован**</span><span class="sxs-lookup"><span data-stu-id="1c35c-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM\_MC\_REPOSITORY\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-108">1073747424 (0x400015E0)</span><span class="sxs-lookup"><span data-stu-id="1c35c-108">1073747424 (0x400015E0)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-109">Служба инструментарий управления Windows (WMI) обнаружила несогласованность с репозиторием WMI в *\\ \\ \\ репозитории каталога% WINDIR% system32* и не смог восстановить его.</span><span class="sxs-lookup"><span data-stu-id="1c35c-109">The Windows Management Instrumentation Service detected an inconsistency with the WMI repository in the directory *%windir%\\system32\\wbem\\repository* and was not able to recover it.</span></span> <span data-ttu-id="1c35c-110">Репозиторий WMI теперь будет удален, и на основе механизма автоматического восстановления будет создан новый репозиторий.</span><span class="sxs-lookup"><span data-stu-id="1c35c-110">The WMI repository will now be deleted, A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**\_ \_ \_ \_ \_ Загрузка поставщика системных LocalSystem \_ для поставщика WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="1c35c-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM\_MC\_PROVIDER\_SUBSYSTEM\_LOCALSYSTEM\_PROVIDER\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-112">2147483711 (0x8000003F)</span><span class="sxs-lookup"><span data-stu-id="1c35c-112">2147483711 (0x8000003F)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-113">Поставщик %1 зарегистрирован в инструментарий управления Windows (WMI) пространстве имен %2 для использования учетной записи LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="1c35c-113">A provider, %1, has been registered in the Windows Management Instrumentation namespace %2 to use the LocalSystem account.</span></span> <span data-ttu-id="1c35c-114">Эта учетная запись является привилегированной, и поставщик может вызвать нарушение безопасности, если он неправильно олицетворяет запросы пользователей.</span><span class="sxs-lookup"><span data-stu-id="1c35c-114">This account is privileged and the provider may cause a security violation if it does not correctly impersonate user requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_ \_ \_ \_ \_ при \_ восстановлении не загружен MOF-файла WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="1c35c-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM\_MC\_MOF\_NOT\_LOADED\_AT\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-116">3221225476 (0xC0000004)</span><span class="sxs-lookup"><span data-stu-id="1c35c-116">3221225476 (0xC0000004)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-117">Произошла ошибка %1 при попытке загрузить MOF %2 при восстановлении. MOF-файл, помеченный автовосстановлением.</span><span class="sxs-lookup"><span data-stu-id="1c35c-117">Error %1 encountered when trying to load MOF %2 while recovering .MOF file marked with autorecover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ не удается \_ активировать \_ Фильтр**</span><span class="sxs-lookup"><span data-stu-id="1c35c-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM\_MC\_CANNOT\_ACTIVATE\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-119">3221225482 (0xC000000A)</span><span class="sxs-lookup"><span data-stu-id="1c35c-119">3221225482 (0xC000000A)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-120">Не удалось повторно активировать фильтр событий с запросом "%2" в пространстве имен "%1" из-за ошибки %3.</span><span class="sxs-lookup"><span data-stu-id="1c35c-120">Event filter with query "%2" could not be reactivated in namespace "%1" because of error %3.</span></span> <span data-ttu-id="1c35c-121">События не могут быть доставлены через этот фильтр, пока проблема не будет устранена.</span><span class="sxs-lookup"><span data-stu-id="1c35c-121">Events cannot be delivered through this filter until the problem is corrected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_ \_ Недопустимый \_ \_ запрос поставщика \_ событий WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="1c35c-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-123">3221225493 (0xC0000015)</span><span class="sxs-lookup"><span data-stu-id="1c35c-123">3221225493 (0xC0000015)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-124">Поставщик событий %1 попытался зарегистрировать синтаксически недопустимый запрос "%2".</span><span class="sxs-lookup"><span data-stu-id="1c35c-124">Event provider %1 attempted to register a syntactically invalid query "%2".</span></span> <span data-ttu-id="1c35c-125">Запрос будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="1c35c-125">The query will be ignored.</span></span> <span data-ttu-id="1c35c-126">Запрос можно исправить, изучив репозиторий WMI в CIM Studio и обновив постоянные подписки для указанного поставщика и запроса.</span><span class="sxs-lookup"><span data-stu-id="1c35c-126">The query can be corrected by examining the WMI repository with CIM studio and updating the permanent subscriptions for the listed provider and query.</span></span> <span data-ttu-id="1c35c-127">Если постоянная подписка создана с помощью MOF-файла, поступающего с установленным продуктом, необходимо обратиться к поставщику приложения, чтобы исправить неудачную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="1c35c-127">If the permanent subscription is created with MOF file coming with an installed product, the application vendor must be contacted to correct the faulty registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ Недопустимый \_ \_ \_ внутренний запрос поставщика \_ событий WBEM**</span><span class="sxs-lookup"><span data-stu-id="1c35c-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_INTRINSIC\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-129">3221225494 (0xC0000016)</span><span class="sxs-lookup"><span data-stu-id="1c35c-129">3221225494 (0xC0000016)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-130">Поставщик событий %1 попытался зарегистрировать внутренний запрос события "%2" в пространстве имен "%3", для которого не удалось определить набор целевых классов объектов.</span><span class="sxs-lookup"><span data-stu-id="1c35c-130">Event provider %1 attempted to register an intrinsic event query "%2" in %3 namespace for which the set of target object classes could not be determined.</span></span> <span data-ttu-id="1c35c-131">Запрос будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="1c35c-131">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_ \_ \_ \_ \_ слишком \_ широкий запрос поставщика событий WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="1c35c-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-133">3221225495 (0xC0000017)</span><span class="sxs-lookup"><span data-stu-id="1c35c-133">3221225495 (0xC0000017)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-134">Поставщик событий %1 попытался зарегистрировать запрос "%2" в пространстве имен "%3", которое слишком большое.</span><span class="sxs-lookup"><span data-stu-id="1c35c-134">Event provider %1 attempted to register query "%2" in %3 namespace which is too broad.</span></span> <span data-ttu-id="1c35c-135">Поставщики событий не могут предоставлять события, предоставляемые системой.</span><span class="sxs-lookup"><span data-stu-id="1c35c-135">Event providers cannot provide events that are provided by the system.</span></span> <span data-ttu-id="1c35c-136">Запрос будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="1c35c-136">The query will be ignored.</span></span> <span data-ttu-id="1c35c-137">Обратитесь к поставщику приложения.</span><span class="sxs-lookup"><span data-stu-id="1c35c-137">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_ \_ запрос поставщика событий WBEM MC \_ \_ \_ не \_ найден**</span><span class="sxs-lookup"><span data-stu-id="1c35c-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-139">3221225496 (0xC0000018)</span><span class="sxs-lookup"><span data-stu-id="1c35c-139">3221225496 (0xC0000018)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-140">Поставщик событий %1 попытался зарегистрировать запрос "%2", целевой класс "%3" которого в пространстве имен %4 не существует.</span><span class="sxs-lookup"><span data-stu-id="1c35c-140">Event provider %1 attempted to register query "%2" whose target class "%3" in %4 namespace does not exist.</span></span> <span data-ttu-id="1c35c-141">Запрос будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="1c35c-141">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_несобытие \_ \_ запроса поставщика \_ событий \_ WBEM \_ MC**</span><span class="sxs-lookup"><span data-stu-id="1c35c-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-143">3221225497 (0xC0000019)</span><span class="sxs-lookup"><span data-stu-id="1c35c-143">3221225497 (0xC0000019)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-144">Поставщик событий %1 попытался зарегистрировать запрос &quot; %2 &quot; , целевой класс &quot; %3 которого &quot; не является классом событий.</span><span class="sxs-lookup"><span data-stu-id="1c35c-144">Event provider %1 attempted to register query &quot;%2&quot; whose target class &quot;%3&quot; is not an event class.</span></span> <span data-ttu-id="1c35c-145">Запрос будет проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="1c35c-145">The query will be ignored.</span></span> <span data-ttu-id="1c35c-146">Обратитесь к поставщику приложения.</span><span class="sxs-lookup"><span data-stu-id="1c35c-146">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**\_ \_ \_ сбой ядра WBEM MC \_**</span><span class="sxs-lookup"><span data-stu-id="1c35c-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM\_MC\_WBEM\_CORE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-148">3221225500 (0xC000001C)</span><span class="sxs-lookup"><span data-stu-id="1c35c-148">3221225500 (0xC000001C)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-149">Не удалось инициализировать ядро WMI или подсистему поставщика или подсистему событий, номер ошибки: %1.</span><span class="sxs-lookup"><span data-stu-id="1c35c-149">Failed to Initialize WMI Core or Provider SubSystem or Event SubSystem with error number %1.</span></span> <span data-ttu-id="1c35c-150">Это может быть вызвано неправильной установленной версией WMI, сбоем обновления репозитория WMI, недостатком места на диске или недостатком памяти.</span><span class="sxs-lookup"><span data-stu-id="1c35c-150">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**\_ \_ \_ сбой подключения ADAP MC \_ (WBEM)**</span><span class="sxs-lookup"><span data-stu-id="1c35c-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM\_MC\_ADAP\_CONNECTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-152">3221225515 (0xC000002B)</span><span class="sxs-lookup"><span data-stu-id="1c35c-152">3221225515 (0xC000002B)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-153">Инструментарий управления Windows (WMI) ADAP не удалось подключиться к пространству имен %1 из следующей ошибки: %2.</span><span class="sxs-lookup"><span data-stu-id="1c35c-153">Windows Management Instrumentation ADAP failed to connect to namespace %1 with the following error %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**\_сбой путкласс (WBEM MC \_ ADAP \_ PERFLIB \_ \_ )**</span><span class="sxs-lookup"><span data-stu-id="1c35c-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM\_MC\_ADAP\_PERFLIB\_PUTCLASS\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-155">3221225520 (0xC0000030)</span><span class="sxs-lookup"><span data-stu-id="1c35c-155">3221225520 (0xC0000030)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-156">Инструментарий управления Windows (WMI) ADAP не удалось сохранить объект %1 в пространстве имен %2 из-за следующей ошибки %3.</span><span class="sxs-lookup"><span data-stu-id="1c35c-156">Windows Management Instrumentation ADAP was unable to save object %1 in namespace %2 because of the following error %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ не \_ удалось \_ Добавить \_ WIN32PERF**</span><span class="sxs-lookup"><span data-stu-id="1c35c-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-158">3221225530 (0xC000003A)</span><span class="sxs-lookup"><span data-stu-id="1c35c-158">3221225530 (0xC000003A)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-159">Инструментарий управления Windows (WMI) ADAP не удалось создать \_ базовый класс производительности Win32 в %1: result = %2.</span><span class="sxs-lookup"><span data-stu-id="1c35c-159">Windows Management Instrumentation ADAP was unable to create the Win32\_Perf base class in %1:Result=%2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ не \_ удалось \_ Добавить \_ WIN32PERFRAWDATA**</span><span class="sxs-lookup"><span data-stu-id="1c35c-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERFRAWDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-161">3221225531 (0xC000003B)</span><span class="sxs-lookup"><span data-stu-id="1c35c-161">3221225531 (0xC000003B)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-162">Инструментарий управления Windows (WMI) ADAP не удалось создать \_ базовый класс Win32 перфравдата %1.</span><span class="sxs-lookup"><span data-stu-id="1c35c-162">Windows Management Instrumentation ADAP was unable to create the Win32\_PerfRawData base class %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ не удалось \_ запустить репозиторий WBEM MC \_**</span><span class="sxs-lookup"><span data-stu-id="1c35c-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM\_MC\_REPOSITORY\_FAILED\_TO\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-164">3221231073 (0xC00015E1)</span><span class="sxs-lookup"><span data-stu-id="1c35c-164">3221231073 (0xC00015E1)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-165">Службе инструментарий управления Windows (WMI) не удалось загрузить файлы репозитория в *\\ \\ \\ репозиторий% WINDIR% system32 WBEM*.</span><span class="sxs-lookup"><span data-stu-id="1c35c-165">The Windows Management Instrumentation Service failed to load the repository files under the directory *%windir%\\system32\\wbem\\repository*.</span></span> <span data-ttu-id="1c35c-166">Это может быть вызвано повреждением файлов репозитория, параметрами безопасности в этом каталоге, недостатком места на диске или другими проблемами системных ресурсов, например нехваткой памяти.</span><span class="sxs-lookup"><span data-stu-id="1c35c-166">This can be caused by a corruption in the repository files, security settings on this directory, lack of disk space, or other system resource issues such as lack of memory.</span></span> <span data-ttu-id="1c35c-167">Если эта ошибка возникает при каждом перезапуске компьютера, администратору этого компьютера может потребоваться отключить службу WMI, проверить параметры безопасности для этой папки и файлов в этой папке и запустить служебную wmidiag для проверки работоспособности инструментарий управления Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1c35c-167">If this error occurs each time the computer is restarted then the administrator on this computer may need to stop WMI Service, review the security setting on this folder and files under this folder, and run WMIDiag to validate the health of Windows Management Instrumentation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**для WBEM \_ MC для \_ WBEM \_ требуется \_ Шифрование \_ отклонено**</span><span class="sxs-lookup"><span data-stu-id="1c35c-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-169">3221231077 (0xC00015E5)</span><span class="sxs-lookup"><span data-stu-id="1c35c-169">3221231077 (0xC00015E5)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-170">Отказано в доступе к пространству имен %1, так как оно помечено Рекуиресенкриптион, но скрипт или приложение попытались подключиться к этому пространству имен с уровнем проверки подлинности ниже " **PKT \_ Privacy**".</span><span class="sxs-lookup"><span data-stu-id="1c35c-170">Access to the %1 namespace was denied because the namespace is marked with RequiresEncryption but the script or application attempted to connect to this namespace with an authentication level below **Pkt\_Privacy**.</span></span> <span data-ttu-id="1c35c-171">Измените уровень проверки подлинности на **\_ общепринятое** и повторно запустите сценарий или приложение.</span><span class="sxs-lookup"><span data-stu-id="1c35c-171">Change the authentication level to **Pkt\_Privacy** and run the script or application again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC для \_ WBEM \_ требуется шифрование с \_ \_ асинхронным \_ отклонением**</span><span class="sxs-lookup"><span data-stu-id="1c35c-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_ASYNC\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-173">3221231078 (0xC00015E6)</span><span class="sxs-lookup"><span data-stu-id="1c35c-173">3221231078 (0xC00015E6)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-174">Службе инструментарий управления Windows (WMI) не удалось асинхронно доставить результаты для пространства имен %1.</span><span class="sxs-lookup"><span data-stu-id="1c35c-174">Windows Management Instrumentation Service could not deliver results asynchronously for %1 namespace.</span></span> <span data-ttu-id="1c35c-175">Пространство имен помечено как Рекуиресенкриптион, но WinMgmt не удалось установить безопасное подключение к клиентскому компьютеру.</span><span class="sxs-lookup"><span data-stu-id="1c35c-175">The namespace is marked with RequiresEncryption but WinMgmt could not establish a secure connection back to the client computer.</span></span> <span data-ttu-id="1c35c-176">Убедитесь в наличии отношений доверия между клиентскими и серверными компьютерами, чтобы клиент распознавал учетную запись компьютера сервера.</span><span class="sxs-lookup"><span data-stu-id="1c35c-176">Ensure there is a trust relationship between the client and server computers so that the client recognizes the server computer account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**\_узел WBEM \_ с \_ ведущим адаптером WBEM \_ уничтожен**</span><span class="sxs-lookup"><span data-stu-id="1c35c-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM\_MC\_WBEM\_HOST\_KILLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-178">3221231084 (0xC00015EC)</span><span class="sxs-lookup"><span data-stu-id="1c35c-178">3221231084 (0xC00015EC)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-179">Инструментарий управления Windows (WMI) остановлен WMIPRVSE.EXE, так как квота достигла значения предупреждения.</span><span class="sxs-lookup"><span data-stu-id="1c35c-179">Windows Management Instrumentation has stopped WMIPRVSE.EXE because a quota reached a warning value.</span></span> <span data-ttu-id="1c35c-180">Квота: %1 значение: %2, максимальное значение: %3, PID WMIPRVSE: %4.</span><span class="sxs-lookup"><span data-stu-id="1c35c-180">Quota: %1 Value: %2 Maximum value: %3 WMIPRVSE PID: %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ репфилеснотфаунд**</span><span class="sxs-lookup"><span data-stu-id="1c35c-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM\_MC\_WBEM\_REPFILESNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-182">3221231086 (0xC00015EE)</span><span class="sxs-lookup"><span data-stu-id="1c35c-182">3221231086 (0xC00015EE)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-183">Во время запуска службы службе инструментарий управления Windows (WMI) не удалось разместить файлы репозитория.</span><span class="sxs-lookup"><span data-stu-id="1c35c-183">During the service startup, the Windows Management Instrumentation service was unable to locate the repository files.</span></span> <span data-ttu-id="1c35c-184">Новый репозиторий будет создан на основе механизма автоматического восстановления.</span><span class="sxs-lookup"><span data-stu-id="1c35c-184">A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ , \_ Запуск WBEM, \_ \_ успешно запущен**</span><span class="sxs-lookup"><span data-stu-id="1c35c-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM\_MC\_WBEM\_STARTED\_SUCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-186">3221231087 (0xC00015EF)</span><span class="sxs-lookup"><span data-stu-id="1c35c-186">3221231087 (0xC00015EF)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-187">Служба инструментарий управления Windows (WMI) успешно запущена.</span><span class="sxs-lookup"><span data-stu-id="1c35c-187">Windows Management Instrumentation Service started successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**\_ \_ \_ инициализация ядра WBEM, основная \_ Техническая поддержка \_ ESS \_**</span><span class="sxs-lookup"><span data-stu-id="1c35c-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM\_MC\_WBEM\_CORE\_PSS\_ESS\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-189">3221231089 (0xC00015F1)</span><span class="sxs-lookup"><span data-stu-id="1c35c-189">3221231089 (0xC00015F1)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-190">Инструментарий управления Windows (WMI)ные подсистемы службы успешно инициализированы.</span><span class="sxs-lookup"><span data-stu-id="1c35c-190">Windows Management Instrumentation Service subsystems initialized successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_ \_ \_ \_ сбой инициализации службы WBEM MC \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="1c35c-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM\_MC\_WBEM\_SERVICE\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-192">3221225501 (0xC000001D)</span><span class="sxs-lookup"><span data-stu-id="1c35c-192">3221225501 (0xC000001D)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-193">При попытке инициализации службы инструментарий управления Windows (WMI) был возвращен номер ошибки %1.</span><span class="sxs-lookup"><span data-stu-id="1c35c-193">Error number %1 was returned in trying to initialize Windows Management Instrumentation Service.</span></span> <span data-ttu-id="1c35c-194">Это может быть вызвано неправильной установленной версией WMI, сбоем обновления репозитория WMI, недостатком места на диске или недостатком памяти.</span><span class="sxs-lookup"><span data-stu-id="1c35c-194">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1c35c-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**\_ \_ репозиторий WBEM MC WBEM \_ \_ создан повторно**</span><span class="sxs-lookup"><span data-stu-id="1c35c-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM\_MC\_WBEM\_REPOSITORY\_RECREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c35c-196">3221231088 (0xC00015F0)</span><span class="sxs-lookup"><span data-stu-id="1c35c-196">3221231088 (0xC00015F0)</span></span>
</dt> <dt>



<span data-ttu-id="1c35c-197">Репозиторий инструментарий управления Windows (WMI) успешно воссоздан повторно с помощью механизма восстановления.</span><span class="sxs-lookup"><span data-stu-id="1c35c-197">Windows Management Instrumentation Repository successfully recreated using Autorecovery mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c35c-198">Требования</span><span class="sxs-lookup"><span data-stu-id="1c35c-198">Requirements</span></span>



| <span data-ttu-id="1c35c-199">Требование</span><span class="sxs-lookup"><span data-stu-id="1c35c-199">Requirement</span></span> | <span data-ttu-id="1c35c-200">Значение</span><span class="sxs-lookup"><span data-stu-id="1c35c-200">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1c35c-201">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c35c-201">Minimum supported client</span></span><br/> | <span data-ttu-id="1c35c-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c35c-202">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1c35c-203">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c35c-203">Minimum supported server</span></span><br/> | <span data-ttu-id="1c35c-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c35c-204">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c35c-205">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c35c-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c35c-206">События WMI</span><span class="sxs-lookup"><span data-stu-id="1c35c-206">WMI Events</span></span>](wmi-events.md)
</dt> <dt>

<span data-ttu-id="1c35c-207">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="1c35c-207">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> </dl>

 

 




