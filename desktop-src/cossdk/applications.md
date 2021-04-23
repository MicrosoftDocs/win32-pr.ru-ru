---
description: Содержит объект для каждого приложения COM+, установленного на локальном компьютере. Свойства, предоставляемые этими объектами, содержат все параметры, сделанные на уровне приложения.
ms.assetid: c0c46592-5282-412d-8f54-67637be8218a
title: Коллекция Applications
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Applications
api_type:
- COM
api_location: ''
ms.openlocfilehash: 54f286ae393e67d9732e21bc40cbb0f9c46d8c63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142034"
---
# <a name="applications-collection"></a><span data-ttu-id="3e422-104">Коллекция Applications</span><span class="sxs-lookup"><span data-stu-id="3e422-104">Applications collection</span></span>

<span data-ttu-id="3e422-105">Содержит объект для каждого приложения COM+, установленного на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3e422-105">Contains an object for each COM+ application installed on the local computer.</span></span> <span data-ttu-id="3e422-106">Свойства, предоставляемые этими объектами, содержат все параметры, сделанные на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-106">The properties exposed by these objects hold all settings made at the application level.</span></span>

<span data-ttu-id="3e422-107">Свойства для компонентов в приложении задаются с помощью коллекции связанных [**компонентов**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="3e422-107">You set properties for components within an application by using the related [**Components**](components.md) collection.</span></span> <span data-ttu-id="3e422-108">Роли назначаются приложению с помощью коллекции связанных [**ролей**](roles.md) .</span><span class="sxs-lookup"><span data-stu-id="3e422-108">You assign roles to an application by using the related [**Roles**](roles.md) collection.</span></span>

<span data-ttu-id="3e422-109">Чтобы установить компоненты в приложение, используйте методы для объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="3e422-109">To install components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="3e422-110">Чтобы установить приложение из файла или завершить работу или экспортировать приложение, также используйте методы для объекта **комадминкаталог** .</span><span class="sxs-lookup"><span data-stu-id="3e422-110">To install an application from a file or to shut down or export an application, also use methods on the **COMAdminCatalog** object.</span></span> <span data-ttu-id="3e422-111">В противном случае, чтобы создать новое приложение, можно добавить объект в коллекцию **приложений** .</span><span class="sxs-lookup"><span data-stu-id="3e422-111">Otherwise, to create a new application, you can add an object to the **Applications** collection.</span></span>

<span data-ttu-id="3e422-112">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="3e422-112">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="3e422-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="3e422-113">Members</span></span>

<span data-ttu-id="3e422-114">Коллекция **приложений** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="3e422-114">The **Applications** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="3e422-115">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="3e422-115">Related Collections</span></span>

<span data-ttu-id="3e422-116">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="3e422-116">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="3e422-117">**аппликатионинстанцес**</span><span class="sxs-lookup"><span data-stu-id="3e422-117">**ApplicationInstances**</span></span>](applicationinstances.md)
-   [<span data-ttu-id="3e422-118">**Компоненты**</span><span class="sxs-lookup"><span data-stu-id="3e422-118">**Components**</span></span>](components.md)
-   [<span data-ttu-id="3e422-119">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="3e422-119">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="3e422-120">**легацикомпонентс**</span><span class="sxs-lookup"><span data-stu-id="3e422-120">**LegacyComponents**</span></span>](legacycomponents.md)
-   [<span data-ttu-id="3e422-121">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="3e422-121">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="3e422-122">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="3e422-122">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="3e422-123">**Роли**</span><span class="sxs-lookup"><span data-stu-id="3e422-123">**Roles**</span></span>](roles.md)

<span data-ttu-id="3e422-124">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="3e422-124">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="3e422-125">**Секции**</span><span class="sxs-lookup"><span data-stu-id="3e422-125">**Partitions**</span></span>](partitions.md)
-   [<span data-ttu-id="3e422-126">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="3e422-126">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="3e422-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e422-127">Properties</span></span>

<span data-ttu-id="3e422-128">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="3e422-128">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="3e422-129">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="3e422-129">3GigSupportEnabled</span></span>](#3gigsupportenabled)
-   [<span data-ttu-id="3e422-130">акцессчеккслевел</span><span class="sxs-lookup"><span data-stu-id="3e422-130">AccessChecksLevel</span></span>](#accesscheckslevel)
-   [<span data-ttu-id="3e422-131">Активация</span><span class="sxs-lookup"><span data-stu-id="3e422-131">Activation</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="3e422-132">аппликатионакцессчекксенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-132">ApplicationAccessChecksEnabled</span></span>](#applicationaccesschecksenabled)
-   [<span data-ttu-id="3e422-133">аппликатиондиректори</span><span class="sxs-lookup"><span data-stu-id="3e422-133">ApplicationDirectory</span></span>](#applicationdirectory)
-   [<span data-ttu-id="3e422-134">аппликатионпрокси</span><span class="sxs-lookup"><span data-stu-id="3e422-134">ApplicationProxy</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="3e422-135">аппликатионпроксисервернаме</span><span class="sxs-lookup"><span data-stu-id="3e422-135">ApplicationProxyServerName</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="3e422-136">апппартитионид</span><span class="sxs-lookup"><span data-stu-id="3e422-136">AppPartitionID</span></span>](#apppartitionid)
-   [<span data-ttu-id="3e422-137">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="3e422-137">Authentication</span></span>](#authenticationcapability)
-   [<span data-ttu-id="3e422-138">аусентикатионкапабилити</span><span class="sxs-lookup"><span data-stu-id="3e422-138">AuthenticationCapability</span></span>](#authenticationcapability)
-   [<span data-ttu-id="3e422-139">Изменить</span><span class="sxs-lookup"><span data-stu-id="3e422-139">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="3e422-140">CommandLine</span><span class="sxs-lookup"><span data-stu-id="3e422-140">CommandLine</span></span>](#commandline)
-   [<span data-ttu-id="3e422-141">конкуррентаппс</span><span class="sxs-lookup"><span data-stu-id="3e422-141">ConcurrentApps</span></span>](#concurrentapps)
-   [<span data-ttu-id="3e422-142">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="3e422-142">CreatedBy</span></span>](#createdby)
-   [<span data-ttu-id="3e422-143">крменаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-143">CRMEnabled</span></span>](#crmenabled)
-   [<span data-ttu-id="3e422-144">крмлогфиле</span><span class="sxs-lookup"><span data-stu-id="3e422-144">CRMLogFile</span></span>](#crmlogfile)
-   [<span data-ttu-id="3e422-145">Предусмотрено</span><span class="sxs-lookup"><span data-stu-id="3e422-145">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="3e422-146">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-146">Description</span></span>](#description)
-   [<span data-ttu-id="3e422-147">думпенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-147">DumpEnabled</span></span>](#dumpenabled)
-   [<span data-ttu-id="3e422-148">думпонексцептион</span><span class="sxs-lookup"><span data-stu-id="3e422-148">DumpOnException</span></span>](#dumponexception)
-   [<span data-ttu-id="3e422-149">думпонфаилфаст</span><span class="sxs-lookup"><span data-stu-id="3e422-149">DumpOnFailfast</span></span>](#dumponfailfast)
-   [<span data-ttu-id="3e422-150">DumpPath</span><span class="sxs-lookup"><span data-stu-id="3e422-150">DumpPath</span></span>](#dumppath)
-   [<span data-ttu-id="3e422-151">евентсенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-151">EventsEnabled</span></span>](#eventsenabled)
-   [<span data-ttu-id="3e422-152">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="3e422-152">ID</span></span>](#applications-collection)
-   [<span data-ttu-id="3e422-153">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="3e422-153">Identity</span></span>](#identity)
-   [<span data-ttu-id="3e422-154">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="3e422-154">ImpersonationLevel</span></span>](#impersonationlevel)
-   [<span data-ttu-id="3e422-155">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="3e422-155">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="3e422-156">IsSystem</span><span class="sxs-lookup"><span data-stu-id="3e422-156">IsSystem</span></span>](#issystem)
-   [<span data-ttu-id="3e422-157">максдумпкаунт</span><span class="sxs-lookup"><span data-stu-id="3e422-157">MaxDumpCount</span></span>](#maxdumpcount)
-   [<span data-ttu-id="3e422-158">Name</span><span class="sxs-lookup"><span data-stu-id="3e422-158">Name</span></span>](#applicationproxyservername)
-   [<span data-ttu-id="3e422-159">Пароль</span><span class="sxs-lookup"><span data-stu-id="3e422-159">Password</span></span>](#password)
-   [<span data-ttu-id="3e422-160">ккаусентикатемсгс</span><span class="sxs-lookup"><span data-stu-id="3e422-160">QCAuthenticateMsgs</span></span>](#qcauthenticatemsgs)
-   [<span data-ttu-id="3e422-161">кклистенермакссреадс</span><span class="sxs-lookup"><span data-stu-id="3e422-161">QCListenerMaxThreads</span></span>](#qclistenermaxthreads)
-   [<span data-ttu-id="3e422-162">куеуелистенеренаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-162">QueueListenerEnabled</span></span>](#queuelistenerenabled)
-   [<span data-ttu-id="3e422-163">куеуинженаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-163">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="3e422-164">рециклеактиватионлимит</span><span class="sxs-lookup"><span data-stu-id="3e422-164">RecycleActivationLimit</span></span>](#recycleactivationlimit)
-   [<span data-ttu-id="3e422-165">рециклекалллимит</span><span class="sxs-lookup"><span data-stu-id="3e422-165">RecycleCallLimit</span></span>](#recyclecalllimit)
-   [<span data-ttu-id="3e422-166">рецикликспиратионтимеаут</span><span class="sxs-lookup"><span data-stu-id="3e422-166">RecycleExpirationTimeout</span></span>](#recycleexpirationtimeout)
-   [<span data-ttu-id="3e422-167">рециклелифетимелимит</span><span class="sxs-lookup"><span data-stu-id="3e422-167">RecycleLifetimeLimit</span></span>](#recyclelifetimelimit)
-   [<span data-ttu-id="3e422-168">рециклемеморилимит</span><span class="sxs-lookup"><span data-stu-id="3e422-168">RecycleMemoryLimit</span></span>](#recyclememorylimit)
-   [<span data-ttu-id="3e422-169">Репликаци</span><span class="sxs-lookup"><span data-stu-id="3e422-169">Replicable</span></span>](#replicable)
-   [<span data-ttu-id="3e422-170">рунфоревер</span><span class="sxs-lookup"><span data-stu-id="3e422-170">RunForever</span></span>](#runforever)
-   [<span data-ttu-id="3e422-171">Служба</span><span class="sxs-lookup"><span data-stu-id="3e422-171">ServiceName</span></span>](#servicename)
-   [<span data-ttu-id="3e422-172">шутдовнафтер</span><span class="sxs-lookup"><span data-stu-id="3e422-172">ShutdownAfter</span></span>](#shutdownafter)
-   [<span data-ttu-id="3e422-173">соапактиватед</span><span class="sxs-lookup"><span data-stu-id="3e422-173">SoapActivated</span></span>](#soapactivated)
-   [<span data-ttu-id="3e422-174">соапбасеурл</span><span class="sxs-lookup"><span data-stu-id="3e422-174">SoapBaseUrl</span></span>](#soapbaseurl)
-   [<span data-ttu-id="3e422-175">соапмаилто</span><span class="sxs-lookup"><span data-stu-id="3e422-175">SoapMailTo</span></span>](#soapmailto)
-   [<span data-ttu-id="3e422-176">соапврут</span><span class="sxs-lookup"><span data-stu-id="3e422-176">SoapVRoot</span></span>](#soapvroot)
-   [<span data-ttu-id="3e422-177">српенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-177">SRPEnabled</span></span>](#srpenabled)
-   [<span data-ttu-id="3e422-178">срптрустлевел</span><span class="sxs-lookup"><span data-stu-id="3e422-178">SRPTrustLevel</span></span>](#srptrustlevel)

### <a name="3gigsupportenabled"></a><span data-ttu-id="3e422-179">3GigSupportEnabled</span><span class="sxs-lookup"><span data-stu-id="3e422-179">3GigSupportEnabled</span></span>



| <span data-ttu-id="3e422-180">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-180">Entry</span></span> | <span data-ttu-id="3e422-181">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-181">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-182">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-182">Description</span></span>    | <span data-ttu-id="3e422-183">Указывает, может ли приложение использовать 3 ГБ памяти в процессе.</span><span class="sxs-lookup"><span data-stu-id="3e422-183">Indicates whether the application can use 3 GB of memory in its process.</span></span> <span data-ttu-id="3e422-184">Если этот параметр не включен, приложение может использовать только 2 ГБ памяти.</span><span class="sxs-lookup"><span data-stu-id="3e422-184">If this is not enabled, the application can use only 2 GB of memory.</span></span> |
| <span data-ttu-id="3e422-185">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-185">Access</span></span>         | <span data-ttu-id="3e422-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-186">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="3e422-187">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-187">Type</span></span>           | <span data-ttu-id="3e422-188">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-188">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="3e422-189">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-189">Default</span></span>        | <span data-ttu-id="3e422-190">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-190">False</span></span>                                                                                                                                         |
| <span data-ttu-id="3e422-191">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-191">Minimum system</span></span> | <span data-ttu-id="3e422-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-192">Windows 2000</span></span>                                                                                                                                  |



 

### <a name="accesscheckslevel"></a><span data-ttu-id="3e422-193">акцессчеккслевел</span><span class="sxs-lookup"><span data-stu-id="3e422-193">AccessChecksLevel</span></span>



| <span data-ttu-id="3e422-194">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-194">Entry</span></span> | <span data-ttu-id="3e422-195">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-195">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-196">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-196">Description</span></span>    | <span data-ttu-id="3e422-197">Указывает, выполняются ли проверки доступа только на уровне процесса или на уровне процесса и компонента.</span><span class="sxs-lookup"><span data-stu-id="3e422-197">Indicates whether access checks are performed at only the process level or at both the process and component level.</span></span> <span data-ttu-id="3e422-198">Рекомендуется использовать константы в перечислении, а не числовые значения.</span><span class="sxs-lookup"><span data-stu-id="3e422-198">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="3e422-199">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-199">Access</span></span>         | <span data-ttu-id="3e422-200">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-200">ReadWrite</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="3e422-201">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-201">Type</span></span>           | <span data-ttu-id="3e422-202">Длинные возможные значения: Комадминакцессчекксаппликатионлевел (0) Комадминакцессчекксаппликатионкомпонентлевел (1)</span><span class="sxs-lookup"><span data-stu-id="3e422-202">Long Possible values: COMAdminAccessChecksApplicationLevel (0) COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                |
| <span data-ttu-id="3e422-203">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-203">Default</span></span>        | <span data-ttu-id="3e422-204">Комадминакцессчекксаппликатионкомпонентлевел (1)</span><span class="sxs-lookup"><span data-stu-id="3e422-204">COMAdminAccessChecksApplicationComponentLevel (1)</span></span>                                                                                                                                                               |
| <span data-ttu-id="3e422-205">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-205">Minimum system</span></span> | <span data-ttu-id="3e422-206">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-206">Windows 2000</span></span>                                                                                                                                                                                                    |



 

### <a name="activation"></a><span data-ttu-id="3e422-207">Активация</span><span class="sxs-lookup"><span data-stu-id="3e422-207">Activation</span></span>



| <span data-ttu-id="3e422-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-208">Entry</span></span> | <span data-ttu-id="3e422-209">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-209">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-210">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-210">Description</span></span>    | <span data-ttu-id="3e422-211">Локальная активация указывает, что объекты в приложении выполняются в рамках выделенного процесса локального сервера (серверное приложение).</span><span class="sxs-lookup"><span data-stu-id="3e422-211">Local activation indicates that objects within the application run within a dedicated local server process (server application).</span></span> <span data-ttu-id="3e422-212">Внутрипроцессный процесс указывает, что объекты выполняются в процессе создателя (приложение библиотеки).</span><span class="sxs-lookup"><span data-stu-id="3e422-212">In-process activation indicates that objects run in their creator's process (library application).</span></span> |
| <span data-ttu-id="3e422-213">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-213">Access</span></span>         | <span data-ttu-id="3e422-214">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-214">ReadWrite</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="3e422-215">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-215">Type</span></span>           | <span data-ttu-id="3e422-216">Длинные возможные значения: Комадминактиватионинпрок (0) Комадминактиватионлокал (1)</span><span class="sxs-lookup"><span data-stu-id="3e422-216">Long Possible values:COMAdminActivationInproc (0)COMAdminActivationLocal (1)</span></span>                                                                                                                                                        |
| <span data-ttu-id="3e422-217">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-217">Default</span></span>        | <span data-ttu-id="3e422-218">Комадминактиватионлокал (1)</span><span class="sxs-lookup"><span data-stu-id="3e422-218">COMAdminActivationLocal (1)</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="3e422-219">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-219">Minimum system</span></span> | <span data-ttu-id="3e422-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-220">Windows 2000</span></span>                                                                                                                                                                                                                        |



 

### <a name="applicationaccesschecksenabled"></a><span data-ttu-id="3e422-221">аппликатионакцессчекксенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-221">ApplicationAccessChecksEnabled</span></span>



| <span data-ttu-id="3e422-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-222">Entry</span></span> | <span data-ttu-id="3e422-223">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-223">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-224">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-224">Description</span></span>    | <span data-ttu-id="3e422-225">Указывает, выполняются ли проверки доступа для приложения, когда клиенты выполняют вызовы.</span><span class="sxs-lookup"><span data-stu-id="3e422-225">Indicates whether access checks are performed for the application when clients make calls into it.</span></span> |
| <span data-ttu-id="3e422-226">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-226">Access</span></span>         | <span data-ttu-id="3e422-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-227">ReadWrite</span></span>                                                                                          |
| <span data-ttu-id="3e422-228">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-228">Type</span></span>           | <span data-ttu-id="3e422-229">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-229">Bool</span></span>                                                                                               |
| <span data-ttu-id="3e422-230">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-230">Default</span></span>        | <span data-ttu-id="3e422-231">True</span><span class="sxs-lookup"><span data-stu-id="3e422-231">True</span></span>                                                                                               |
| <span data-ttu-id="3e422-232">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-232">Minimum system</span></span> | <span data-ttu-id="3e422-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-233">Windows 2000</span></span>                                                                                       |



 

### <a name="applicationdirectory"></a><span data-ttu-id="3e422-234">аппликатиондиректори</span><span class="sxs-lookup"><span data-stu-id="3e422-234">ApplicationDirectory</span></span>



| <span data-ttu-id="3e422-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-235">Entry</span></span> | <span data-ttu-id="3e422-236">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-236">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-237">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-237">Description</span></span>    | <span data-ttu-id="3e422-238">Полный путь к приложению.</span><span class="sxs-lookup"><span data-stu-id="3e422-238">The full path to the application.</span></span> <span data-ttu-id="3e422-239">Эти сведения необходимы при настройке параллельных сборок (SxS).</span><span class="sxs-lookup"><span data-stu-id="3e422-239">This information is needed when you configure Side-by-Side (SxS) assemblies.</span></span> <span data-ttu-id="3e422-240">Параллельные сборки (SxS) позволяют приложениям ASP указывать, какую версию системной библиотеки, поддерживаемой SxS, можно использовать, например MSVCRT, MSXML, КОМКТЛ, GDIPLUS и т. д.</span><span class="sxs-lookup"><span data-stu-id="3e422-240">Side-by-side (SxS) assemblies allow ASP applications to specify which version of an SxS-supported system DLL to use, such as MSVCRT, MSXML, COMCTL, GDIPLUS, and so on.</span></span> <span data-ttu-id="3e422-241">Например, если приложение ASP использует MSVCRT версии 2,0, можно гарантировать, что приложение по-прежнему использует MSVCRT версии 2,0 даже после применения пакетов обновления к серверу.</span><span class="sxs-lookup"><span data-stu-id="3e422-241">For example, if your ASP application relies on MSVCRT version 2.0, you can ensure that your application still uses MSVCRT version 2.0 even after service packs are applied to the server.</span></span> <span data-ttu-id="3e422-242">Все новые версии MSVCRT по-прежнему устанавливаются на компьютере, но версия 2,0 остается и используется приложением.</span><span class="sxs-lookup"><span data-stu-id="3e422-242">Any new version of MSVCRT is still installed on the computer, but version 2.0 remains and is used by your application.</span></span> <span data-ttu-id="3e422-243">Файлы DLL, поддерживаемые SxS, хранятся в библиотеке% WINDIR% \\ WinSxS.</span><span class="sxs-lookup"><span data-stu-id="3e422-243">SxS-supported DLLs are stored in %WINDIR%\\WinSxS.</span></span> |
| <span data-ttu-id="3e422-244">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-244">Access</span></span>         | <span data-ttu-id="3e422-245">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-245">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3e422-246">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-246">Type</span></span>           | <span data-ttu-id="3e422-247">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-247">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3e422-248">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-248">Default</span></span>        | <span data-ttu-id="3e422-249">""</span><span class="sxs-lookup"><span data-stu-id="3e422-249">""</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e422-250">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-250">Minimum system</span></span> | <span data-ttu-id="3e422-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-251">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="3e422-252">В любом пуле приложений может использоваться только одна версия системной библиотеки DLL, хотя эта функция настраивается на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-252">Only one version of a system DLL can be used in any application pool, even though this feature is configurable at the application level.</span></span> <span data-ttu-id="3e422-253">Например, если приложение app1 использует библиотеки MSVCRT, версии 2,5 и приложения, то приложение, использующее библиотеки MSVCRT, версии 2,4, не должно находиться в одном пуле приложений.</span><span class="sxs-lookup"><span data-stu-id="3e422-253">For example, if application App1 uses MSVCRT, version 2.5 and application App2 uses MSVCRT, version 2.4, then App1 and App2 should not be in the same application pool.</span></span> <span data-ttu-id="3e422-254">Если это так, то приложение, которое загружается первым, имеет загруженную версию MSVCRT, а другое приложение принудительно использует его до тех пор, пока не будут выгружены приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-254">If they are, the application that is loaded first has its version of MSVCRT loaded, and the other application is forced to use it until the applications are unloaded.</span></span>

 

<span data-ttu-id="3e422-255">Дополнительные сведения см. в разделе "параллельные сборки" статьи [изменения в службах com+ в IIS 6,0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="3e422-255">For more information, see "Side-by-Side Assemblies" in [Changes in COM+ Services in IIS 6.0](/previous-versions/iis/6.0-sdk/ms526018(v=vs.90)).</span></span>

### <a name="applicationproxy"></a><span data-ttu-id="3e422-256">аппликатионпрокси</span><span class="sxs-lookup"><span data-stu-id="3e422-256">ApplicationProxy</span></span>



| <span data-ttu-id="3e422-257">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-257">Entry</span></span> | <span data-ttu-id="3e422-258">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-258">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="3e422-259">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-259">Description</span></span>    | <span data-ttu-id="3e422-260">Указывает, является ли приложение прокси-сервером приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-260">Indicates whether the application is an application proxy.</span></span> |
| <span data-ttu-id="3e422-261">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-261">Access</span></span>         | <span data-ttu-id="3e422-262">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e422-262">ReadOnly</span></span>                                                   |
| <span data-ttu-id="3e422-263">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-263">Type</span></span>           | <span data-ttu-id="3e422-264">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-264">Bool</span></span>                                                       |
| <span data-ttu-id="3e422-265">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-265">Default</span></span>        | <span data-ttu-id="3e422-266">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-266">False</span></span>                                                      |
| <span data-ttu-id="3e422-267">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-267">Minimum system</span></span> | <span data-ttu-id="3e422-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-268">Windows 2000</span></span>                                               |



 

### <a name="applicationproxyservername"></a><span data-ttu-id="3e422-269">аппликатионпроксисервернаме</span><span class="sxs-lookup"><span data-stu-id="3e422-269">ApplicationProxyServerName</span></span>



| <span data-ttu-id="3e422-270">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-270">Entry</span></span> | <span data-ttu-id="3e422-271">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-271">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-272">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-272">Description</span></span>    | <span data-ttu-id="3e422-273">Имя удаленного сервера, используемое при экспорте прокси приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-273">A remote server name used when exporting the application proxy.</span></span> <span data-ttu-id="3e422-274">Это имя сервера, на которое указывает прокси приложения при установке на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="3e422-274">It is this server name that the application proxy points to when it is installed on a client computer.</span></span> |
| <span data-ttu-id="3e422-275">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-275">Access</span></span>         | <span data-ttu-id="3e422-276">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-276">ReadWrite</span></span>                                                                                                                                                              |
| <span data-ttu-id="3e422-277">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-277">Type</span></span>           | <span data-ttu-id="3e422-278">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-278">String</span></span>                                                                                                                                                                 |
| <span data-ttu-id="3e422-279">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-279">Default</span></span>        | <span data-ttu-id="3e422-280">""</span><span class="sxs-lookup"><span data-stu-id="3e422-280">""</span></span>                                                                                                                                                                     |
| <span data-ttu-id="3e422-281">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-281">Minimum system</span></span> | <span data-ttu-id="3e422-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-282">Windows 2000</span></span>                                                                                                                                                           |



 

### <a name="apppartitionid"></a><span data-ttu-id="3e422-283">апппартитионид</span><span class="sxs-lookup"><span data-stu-id="3e422-283">AppPartitionID</span></span>



| <span data-ttu-id="3e422-284">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-284">Entry</span></span> | <span data-ttu-id="3e422-285">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-285">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="3e422-286">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-286">Description</span></span>    | <span data-ttu-id="3e422-287">Идентификатор GUID, представляющий идентификатор раздела приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-287">A GUID representing the application partition ID.</span></span> |
| <span data-ttu-id="3e422-288">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-288">Access</span></span>         | <span data-ttu-id="3e422-289">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e422-289">ReadOnly</span></span>                                          |
| <span data-ttu-id="3e422-290">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-290">Type</span></span>           | <span data-ttu-id="3e422-291">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-291">String</span></span>                                            |
| <span data-ttu-id="3e422-292">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-292">Default</span></span>        | <Generated>                                 |
| <span data-ttu-id="3e422-293">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-293">Minimum system</span></span> | <span data-ttu-id="3e422-294">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e422-294">Windows Server 2003</span></span>                               |



 

### <a name="authentication"></a><span data-ttu-id="3e422-295">Аутентификация</span><span class="sxs-lookup"><span data-stu-id="3e422-295">Authentication</span></span>



| <span data-ttu-id="3e422-296">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-296">Entry</span></span> | <span data-ttu-id="3e422-297">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-297">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-298">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-298">Description</span></span>    | <span data-ttu-id="3e422-299">Задает уровень проверки подлинности для вызовов со значениями, соответствующими параметрам проверки подлинности удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="3e422-299">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="3e422-300">При выборе Комадминаусентикатиондефаулт используется параметр в свойстве Дефаултаусентикатионлевел в коллекции [**локалкомпутер**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="3e422-300">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="3e422-301">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-301">Access</span></span>         | <span data-ttu-id="3e422-302">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-302">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3e422-303">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-303">Type</span></span>           | <span data-ttu-id="3e422-304">Длинные возможные значения: Комадминаусентикатиондефаулт (0) Комадминаусентикатионноне (1) Комадминаусентикатионконнект (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="3e422-304">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="3e422-305">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-305">Default</span></span>        | <span data-ttu-id="3e422-306">Комадминаусентикатионпаккет (4)</span><span class="sxs-lookup"><span data-stu-id="3e422-306">COMAdminAuthenticationPacket (4)</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3e422-307">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-307">Minimum system</span></span> | <span data-ttu-id="3e422-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-308">Windows 2000</span></span>                                                                                                                                                                                                                                                                                          |



 

> [!Note]  
> <span data-ttu-id="3e422-309">Для приложений библиотеки (внутрипроцессного) единственными допустимыми параметрами являются Комадминаусентикатиондефаулт и Комадминаусентикатионноне.</span><span class="sxs-lookup"><span data-stu-id="3e422-309">For library (in-process) applications, the only valid settings here are COMAdminAuthenticationDefault and COMAdminAuthenticationNone .</span></span> <span data-ttu-id="3e422-310">Рекомендуется использовать константы в перечислении, а не числовые значения.</span><span class="sxs-lookup"><span data-stu-id="3e422-310">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="authenticationcapability"></a><span data-ttu-id="3e422-311">аусентикатионкапабилити</span><span class="sxs-lookup"><span data-stu-id="3e422-311">AuthenticationCapability</span></span>



| <span data-ttu-id="3e422-312">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-312">Entry</span></span> | <span data-ttu-id="3e422-313">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-313">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-314">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-314">Description</span></span>    | <span data-ttu-id="3e422-315">Определяет, какое удостоверение отображается при олицетворении вызовов.</span><span class="sxs-lookup"><span data-stu-id="3e422-315">Determines what identity is presented when calls are impersonated.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="3e422-316">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-316">Access</span></span>         | <span data-ttu-id="3e422-317">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-317">ReadWrite</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3e422-318">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-318">Type</span></span>           | <span data-ttu-id="3e422-319">Длинные возможные значения: Комадминаусентикатионкапабилитиесноне (0x0) Комадминаусентикатионкапабилитиессекуререференце (0x2) COMAdminAuthenticationCapabilitiesStaticCloaking (0x20) COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span><span class="sxs-lookup"><span data-stu-id="3e422-319">Long Possible values:COMAdminAuthenticationCapabilitiesNone (0x0)COMAdminAuthenticationCapabilitiesSecureReference (0x2)COMAdminAuthenticationCapabilitiesStaticCloaking (0x20)COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span> |
| <span data-ttu-id="3e422-320">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-320">Default</span></span>        | <span data-ttu-id="3e422-321">Комадминаусентикатионкапабилитиесдинамикклоакинг (0x40)</span><span class="sxs-lookup"><span data-stu-id="3e422-321">COMAdminAuthenticationCapabilitiesDynamicCloaking (0x40)</span></span>                                                                                                                                                                                |
| <span data-ttu-id="3e422-322">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-322">Minimum system</span></span> | <span data-ttu-id="3e422-323">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-323">Windows 2000</span></span>                                                                                                                                                                                                                            |



 

### <a name="changeable"></a><span data-ttu-id="3e422-324">Изменить</span><span class="sxs-lookup"><span data-stu-id="3e422-324">Changeable</span></span>



| <span data-ttu-id="3e422-325">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-325">Entry</span></span> | <span data-ttu-id="3e422-326">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-326">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-327">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-327">Description</span></span>    | <span data-ttu-id="3e422-328">Определяет, разрешены ли изменения параметров приложения или их компонентов программным путем или с помощью средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="3e422-328">Determines whether changes to the application settings or those of its components are allowed, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="3e422-329">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-329">Access</span></span>         | <span data-ttu-id="3e422-330">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-330">ReadWrite</span></span>                                                                                                                                                                     |
| <span data-ttu-id="3e422-331">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-331">Type</span></span>           | <span data-ttu-id="3e422-332">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-332">Bool</span></span>                                                                                                                                                                          |
| <span data-ttu-id="3e422-333">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-333">Default</span></span>        | <span data-ttu-id="3e422-334">True</span><span class="sxs-lookup"><span data-stu-id="3e422-334">True</span></span>                                                                                                                                                                          |
| <span data-ttu-id="3e422-335">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-335">Minimum system</span></span> | <span data-ttu-id="3e422-336">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-336">Windows 2000</span></span>                                                                                                                                                                  |



 

### <a name="commandline"></a><span data-ttu-id="3e422-337">Командная строка</span><span class="sxs-lookup"><span data-stu-id="3e422-337">CommandLine</span></span>



| <span data-ttu-id="3e422-338">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-338">Entry</span></span> | <span data-ttu-id="3e422-339">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-339">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-340">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-340">Description</span></span>    | <span data-ttu-id="3e422-341">Строка командной строки для использования при отладке.</span><span class="sxs-lookup"><span data-stu-id="3e422-341">A command-line string for use in debugging.</span></span> <span data-ttu-id="3e422-342">Приложение может быть запущено в отладчике с указанной командной строкой.</span><span class="sxs-lookup"><span data-stu-id="3e422-342">The application can be launched in a debugger with the specified command line.</span></span> |
| <span data-ttu-id="3e422-343">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-343">Access</span></span>         | <span data-ttu-id="3e422-344">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-344">ReadWrite</span></span>                                                                                                                  |
| <span data-ttu-id="3e422-345">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-345">Type</span></span>           | <span data-ttu-id="3e422-346">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-346">String</span></span>                                                                                                                     |
| <span data-ttu-id="3e422-347">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-347">Default</span></span>        | <span data-ttu-id="3e422-348">""</span><span class="sxs-lookup"><span data-stu-id="3e422-348">""</span></span>                                                                                                                         |
| <span data-ttu-id="3e422-349">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-349">Minimum system</span></span> | <span data-ttu-id="3e422-350">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-350">Windows 2000</span></span>                                                                                                               |



 

### <a name="concurrentapps"></a><span data-ttu-id="3e422-351">конкуррентаппс</span><span class="sxs-lookup"><span data-stu-id="3e422-351">ConcurrentApps</span></span>



| <span data-ttu-id="3e422-352">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-352">Entry</span></span> | <span data-ttu-id="3e422-353">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-353">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-354">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-354">Description</span></span>    | <span data-ttu-id="3e422-355">Указывает максимальное количество приложений в составе пула, которые могут выполняться одновременно.</span><span class="sxs-lookup"><span data-stu-id="3e422-355">Specifies the maximum number of poolable applications that can run concurrently.</span></span> |
| <span data-ttu-id="3e422-356">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-356">Access</span></span>         | <span data-ttu-id="3e422-357">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-357">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="3e422-358">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-358">Type</span></span>           | <span data-ttu-id="3e422-359">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="3e422-359">Long (1-1048576)</span></span>                                                                 |
| <span data-ttu-id="3e422-360">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-360">Default</span></span>        | <span data-ttu-id="3e422-361">1</span><span class="sxs-lookup"><span data-stu-id="3e422-361">1</span></span>                                                                                |
| <span data-ttu-id="3e422-362">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-362">Minimum system</span></span> | <span data-ttu-id="3e422-363">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-363">Windows XP</span></span>                                                                       |



 

### <a name="createdby"></a><span data-ttu-id="3e422-364">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="3e422-364">CreatedBy</span></span>



| <span data-ttu-id="3e422-365">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-365">Entry</span></span> | <span data-ttu-id="3e422-366">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-366">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="3e422-367">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-367">Description</span></span>    | <span data-ttu-id="3e422-368">Информационная строка, описывающая, кто создал приложение.</span><span class="sxs-lookup"><span data-stu-id="3e422-368">Informational string to describe who created the application.</span></span> |
| <span data-ttu-id="3e422-369">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-369">Access</span></span>         | <span data-ttu-id="3e422-370">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-370">ReadWrite</span></span>                                                     |
| <span data-ttu-id="3e422-371">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-371">Type</span></span>           | <span data-ttu-id="3e422-372">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-372">String</span></span>                                                        |
| <span data-ttu-id="3e422-373">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-373">Default</span></span>        | <span data-ttu-id="3e422-374">""</span><span class="sxs-lookup"><span data-stu-id="3e422-374">""</span></span>                                                            |
| <span data-ttu-id="3e422-375">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-375">Minimum system</span></span> | <span data-ttu-id="3e422-376">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-376">Windows 2000</span></span>                                                  |



 

### <a name="crmenabled"></a><span data-ttu-id="3e422-377">крменаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-377">CRMEnabled</span></span>



| <span data-ttu-id="3e422-378">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-378">Entry</span></span> | <span data-ttu-id="3e422-379">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-379">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="3e422-380">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-380">Description</span></span>    | <span data-ttu-id="3e422-381">Определяет, включено ли компенсирующий диспетчер ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e422-381">Determines whether the Compensating Resource Manager is enabled.</span></span> |
| <span data-ttu-id="3e422-382">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-382">Access</span></span>         | <span data-ttu-id="3e422-383">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-383">ReadWrite</span></span>                                                        |
| <span data-ttu-id="3e422-384">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-384">Type</span></span>           | <span data-ttu-id="3e422-385">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-385">Bool</span></span>                                                             |
| <span data-ttu-id="3e422-386">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-386">Default</span></span>        | <span data-ttu-id="3e422-387">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-387">False</span></span>                                                            |
| <span data-ttu-id="3e422-388">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-388">Minimum system</span></span> | <span data-ttu-id="3e422-389">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-389">Windows 2000</span></span>                                                     |



 

### <a name="crmlogfile"></a><span data-ttu-id="3e422-390">крмлогфиле</span><span class="sxs-lookup"><span data-stu-id="3e422-390">CRMLogFile</span></span>



| <span data-ttu-id="3e422-391">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-391">Entry</span></span> | <span data-ttu-id="3e422-392">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-392">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-393">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-393">Description</span></span>    | <span data-ttu-id="3e422-394">Имя и путь к файлу для хранения журнала диспетчера компенсирующих ресурсов (CRM).</span><span class="sxs-lookup"><span data-stu-id="3e422-394">Name and path of file for keeping the log for the compensating resource manager (CRM).</span></span> |
| <span data-ttu-id="3e422-395">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-395">Access</span></span>         | <span data-ttu-id="3e422-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-396">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="3e422-397">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-397">Type</span></span>           | <span data-ttu-id="3e422-398">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-398">String</span></span>                                                                                 |
| <span data-ttu-id="3e422-399">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-399">Default</span></span>        | <span data-ttu-id="3e422-400">""</span><span class="sxs-lookup"><span data-stu-id="3e422-400">""</span></span>                                                                                     |
| <span data-ttu-id="3e422-401">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-401">Minimum system</span></span> | <span data-ttu-id="3e422-402">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-402">Windows 2000</span></span>                                                                           |



 

### <a name="deleteable"></a><span data-ttu-id="3e422-403">Предусмотрено</span><span class="sxs-lookup"><span data-stu-id="3e422-403">Deleteable</span></span>



| <span data-ttu-id="3e422-404">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-404">Entry</span></span> | <span data-ttu-id="3e422-405">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-405">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-406">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-406">Description</span></span>    | <span data-ttu-id="3e422-407">Определяет, можно ли удалить приложение либо программно, либо с помощью средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="3e422-407">Sets whether the application can be deleted, either programmatically or through the Component Services administration tool.</span></span> |
| <span data-ttu-id="3e422-408">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-408">Access</span></span>         | <span data-ttu-id="3e422-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-409">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="3e422-410">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-410">Type</span></span>           | <span data-ttu-id="3e422-411">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-411">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="3e422-412">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-412">Default</span></span>        | <span data-ttu-id="3e422-413">True</span><span class="sxs-lookup"><span data-stu-id="3e422-413">True</span></span>                                                                                                                        |
| <span data-ttu-id="3e422-414">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-414">Minimum system</span></span> | <span data-ttu-id="3e422-415">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-415">Windows 2000</span></span>                                                                                                                |



 

### <a name="description"></a><span data-ttu-id="3e422-416">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-416">Description</span></span>



| <span data-ttu-id="3e422-417">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-417">Entry</span></span> | <span data-ttu-id="3e422-418">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-418">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="3e422-419">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-419">Description</span></span>    | <span data-ttu-id="3e422-420">Описывает приложение.</span><span class="sxs-lookup"><span data-stu-id="3e422-420">Describes the application.</span></span> |
| <span data-ttu-id="3e422-421">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-421">Access</span></span>         | <span data-ttu-id="3e422-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-422">ReadWrite</span></span>                  |
| <span data-ttu-id="3e422-423">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-423">Type</span></span>           | <span data-ttu-id="3e422-424">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-424">String</span></span>                     |
| <span data-ttu-id="3e422-425">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-425">Default</span></span>        | <span data-ttu-id="3e422-426">""</span><span class="sxs-lookup"><span data-stu-id="3e422-426">""</span></span>                         |
| <span data-ttu-id="3e422-427">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-427">Minimum system</span></span> | <span data-ttu-id="3e422-428">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-428">Windows 2000</span></span>               |



 

### <a name="dumpenabled"></a><span data-ttu-id="3e422-429">думпенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-429">DumpEnabled</span></span>



| <span data-ttu-id="3e422-430">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-430">Entry</span></span> | <span data-ttu-id="3e422-431">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-431">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-432">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-432">Description</span></span>    | <span data-ttu-id="3e422-433">Включает дамп состояния приложения COM+ во время сбоя в указанном каталоге.</span><span class="sxs-lookup"><span data-stu-id="3e422-433">Enables the dump of the state of a COM+ application at the time of failure to a designated directory.</span></span> |
| <span data-ttu-id="3e422-434">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-434">Access</span></span>         | <span data-ttu-id="3e422-435">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-435">ReadWrite</span></span>                                                                                             |
| <span data-ttu-id="3e422-436">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-436">Type</span></span>           | <span data-ttu-id="3e422-437">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-437">Bool</span></span>                                                                                                  |
| <span data-ttu-id="3e422-438">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-438">Default</span></span>        | <span data-ttu-id="3e422-439">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-439">False</span></span>                                                                                                 |
| <span data-ttu-id="3e422-440">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-440">Minimum system</span></span> | <span data-ttu-id="3e422-441">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-441">Windows XP</span></span>                                                                                            |



 

> [!Note]  
> <span data-ttu-id="3e422-442">Начиная с Windows Server 2003, только администраторы имеют права доступа на чтение файлов дампа COM+.</span><span class="sxs-lookup"><span data-stu-id="3e422-442">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="dumponexception"></a><span data-ttu-id="3e422-443">думпонексцептион</span><span class="sxs-lookup"><span data-stu-id="3e422-443">DumpOnException</span></span>



| <span data-ttu-id="3e422-444">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-444">Entry</span></span> | <span data-ttu-id="3e422-445">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-445">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-446">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-446">Description</span></span>    | <span data-ttu-id="3e422-447">Включает дамп состояния приложения COM+, когда приложение вызывает необработанное исключение и завершается средой выполнения COM+.</span><span class="sxs-lookup"><span data-stu-id="3e422-447">Enables the dump of the state of a COM+ application when the application causes an unhandled exception and is terminated by the COM+ runtime.</span></span> |
| <span data-ttu-id="3e422-448">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-448">Access</span></span>         | <span data-ttu-id="3e422-449">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-449">ReadWrite</span></span>                                                                                                                                     |
| <span data-ttu-id="3e422-450">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-450">Type</span></span>           | <span data-ttu-id="3e422-451">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-451">Bool</span></span>                                                                                                                                          |
| <span data-ttu-id="3e422-452">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-452">Default</span></span>        | <span data-ttu-id="3e422-453">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-453">False</span></span>                                                                                                                                         |
| <span data-ttu-id="3e422-454">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-454">Minimum system</span></span> | <span data-ttu-id="3e422-455">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-455">Windows XP</span></span>                                                                                                                                    |



 

### <a name="dumponfailfast"></a><span data-ttu-id="3e422-456">думпонфаилфаст</span><span class="sxs-lookup"><span data-stu-id="3e422-456">DumpOnFailfast</span></span>



| <span data-ttu-id="3e422-457">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-457">Entry</span></span> | <span data-ttu-id="3e422-458">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-458">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-459">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-459">Description</span></span>    | <span data-ttu-id="3e422-460">Включает дамп состояния приложения COM+ при сбое приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-460">Enables the dump of the state of a COM+ application when the application fails.</span></span> |
| <span data-ttu-id="3e422-461">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-461">Access</span></span>         | <span data-ttu-id="3e422-462">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-462">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="3e422-463">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-463">Type</span></span>           | <span data-ttu-id="3e422-464">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-464">Bool</span></span>                                                                            |
| <span data-ttu-id="3e422-465">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-465">Default</span></span>        | <span data-ttu-id="3e422-466">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-466">False</span></span>                                                                           |
| <span data-ttu-id="3e422-467">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-467">Minimum system</span></span> | <span data-ttu-id="3e422-468">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-468">Windows XP</span></span>                                                                      |



 

### <a name="dumppath"></a><span data-ttu-id="3e422-469">DumpPath</span><span class="sxs-lookup"><span data-stu-id="3e422-469">DumpPath</span></span>



| <span data-ttu-id="3e422-470">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-470">Entry</span></span> | <span data-ttu-id="3e422-471">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-471">Value</span></span> |
|----------------|--------------------------------------------------------------|
| <span data-ttu-id="3e422-472">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-472">Description</span></span>    | <span data-ttu-id="3e422-473">Путь к каталогу, в котором сохраняются файлы дампа.</span><span class="sxs-lookup"><span data-stu-id="3e422-473">The path of the directory in which the dump files are saved.</span></span> |
| <span data-ttu-id="3e422-474">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-474">Access</span></span>         | <span data-ttu-id="3e422-475">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-475">ReadWrite</span></span>                                                    |
| <span data-ttu-id="3e422-476">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-476">Type</span></span>           | <span data-ttu-id="3e422-477">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-477">String</span></span>                                                       |
| <span data-ttu-id="3e422-478">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-478">Default</span></span>        | <span data-ttu-id="3e422-479">"% SystemRoot% \\ system32 \\ COM \\ DMP"</span><span class="sxs-lookup"><span data-stu-id="3e422-479">"%systemroot%\\system32\\com\\dmp"</span></span>                           |
| <span data-ttu-id="3e422-480">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-480">Minimum system</span></span> | <span data-ttu-id="3e422-481">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-481">Windows XP</span></span>                                                   |



 

> [!Note]  
> <span data-ttu-id="3e422-482">Начиная с Windows Server 2003, только администраторы имеют права доступа на чтение файлов дампа COM+.</span><span class="sxs-lookup"><span data-stu-id="3e422-482">As of Windows Server 2003, only administrators have read access privileges to the COM+ dump files.</span></span>

 

### <a name="eventsenabled"></a><span data-ttu-id="3e422-483">евентсенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-483">EventsEnabled</span></span>



| <span data-ttu-id="3e422-484">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-484">Entry</span></span> | <span data-ttu-id="3e422-485">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-485">Value</span></span> |
|----------------|-----------------------------------------------------------|
| <span data-ttu-id="3e422-486">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-486">Description</span></span>    | <span data-ttu-id="3e422-487">Указывает, включены ли события для приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-487">Indicates whether events are enabled for the application.</span></span> |
| <span data-ttu-id="3e422-488">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-488">Access</span></span>         | <span data-ttu-id="3e422-489">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-489">ReadWrite</span></span>                                                 |
| <span data-ttu-id="3e422-490">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-490">Type</span></span>           | <span data-ttu-id="3e422-491">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-491">Bool</span></span>                                                      |
| <span data-ttu-id="3e422-492">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-492">Default</span></span>        | <span data-ttu-id="3e422-493">True</span><span class="sxs-lookup"><span data-stu-id="3e422-493">True</span></span>                                                      |
| <span data-ttu-id="3e422-494">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-494">Minimum system</span></span> | <span data-ttu-id="3e422-495">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-495">Windows 2000</span></span>                                              |



 

### <a name="id"></a><span data-ttu-id="3e422-496">ID</span><span class="sxs-lookup"><span data-stu-id="3e422-496">ID</span></span>



| <span data-ttu-id="3e422-497">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-497">Entry</span></span> | <span data-ttu-id="3e422-498">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-498">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-499">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-499">Description</span></span>    | <span data-ttu-id="3e422-500">Идентификатор GUID, представляющий приложение.</span><span class="sxs-lookup"><span data-stu-id="3e422-500">A GUID representing the application.</span></span> <span data-ttu-id="3e422-501">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="3e422-501">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3e422-502">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-502">Access</span></span>         | <span data-ttu-id="3e422-503">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="3e422-503">WriteOnce</span></span>                                                                                                                                                            |
| <span data-ttu-id="3e422-504">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-504">Type</span></span>           | <span data-ttu-id="3e422-505">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-505">String</span></span>                                                                                                                                                               |
| <span data-ttu-id="3e422-506">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-506">Default</span></span>        | <Generated>                                                                                                                                                    |
| <span data-ttu-id="3e422-507">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-507">Minimum system</span></span> | <span data-ttu-id="3e422-508">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-508">Windows 2000</span></span>                                                                                                                                                         |



 

### <a name="identity"></a><span data-ttu-id="3e422-509">Идентификация</span><span class="sxs-lookup"><span data-stu-id="3e422-509">Identity</span></span>



| <span data-ttu-id="3e422-510">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-510">Entry</span></span> | <span data-ttu-id="3e422-511">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-511">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-512">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-512">Description</span></span>    | <span data-ttu-id="3e422-513">Задает удостоверение процесса сервера для приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-513">Sets the server process identity for the application.</span></span> <span data-ttu-id="3e422-514">Укажите допустимую учетную запись пользователя или "Интерактивный пользователь", чтобы приложение предполагало удостоверение текущего вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e422-514">Specify a valid user account or "Interactive User" to have the application assume the identity of the current logged-on user.</span></span> <span data-ttu-id="3e422-515">Можно также указать строки «NT Authority \\ LocalService», «NT Authority \\ NetworkService» и «NT Authority \\ System».</span><span class="sxs-lookup"><span data-stu-id="3e422-515">You can also specify the strings "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system".</span></span> <span data-ttu-id="3e422-516">Пароль по умолчанию для этих трех учетных записей — "" (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="3e422-516">The default password for these three accounts is "" (empty string).</span></span> |
| <span data-ttu-id="3e422-517">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-517">Access</span></span>         |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e422-518">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-518">Type</span></span>           |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e422-519">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-519">Default</span></span>        |                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e422-520">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-520">Minimum system</span></span> | <span data-ttu-id="3e422-521">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-521">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="3e422-522">Свойство Identity не включено для библиотечных приложений, которые выполняются в клиентском процессе.</span><span class="sxs-lookup"><span data-stu-id="3e422-522">The Identity property is not enabled for library applications, which run in the client process.</span></span>

<span data-ttu-id="3e422-523">Свойство Password должно быть задано одновременно с удостоверением, прежде чем использовать [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), так как пароль и удостоверение проверяются перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="3e422-523">The Password property should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="3e422-524">Если пароль и удостоверение не будут синхронизированы, приложение не сможет быть запущено, пока администратор не запустит их.</span><span class="sxs-lookup"><span data-stu-id="3e422-524">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="impersonationlevel"></a><span data-ttu-id="3e422-525">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="3e422-525">ImpersonationLevel</span></span>



| <span data-ttu-id="3e422-526">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-526">Entry</span></span> | <span data-ttu-id="3e422-527">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-527">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-528">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-528">Description</span></span>    | <span data-ttu-id="3e422-529">Задает уровень олицетворения, используемый для вызовов других приложений.</span><span class="sxs-lookup"><span data-stu-id="3e422-529">Sets impersonation level used for calls made to other applications.</span></span>                                                                                           |
| <span data-ttu-id="3e422-530">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-530">Access</span></span>         | <span data-ttu-id="3e422-531">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-531">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="3e422-532">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-532">Type</span></span>           | <span data-ttu-id="3e422-533">Длинные возможные значения: Комадминимперсонатионанонимаус (1) Комадминимперсонатионидентифи (2) Комадминимперсонатионимперсонате (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="3e422-533">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="3e422-534">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-534">Default</span></span>        | <span data-ttu-id="3e422-535">Комадминимперсонатионимперсонате (3)</span><span class="sxs-lookup"><span data-stu-id="3e422-535">COMAdminImpersonationImpersonate (3)</span></span>                                                                                                                          |
| <span data-ttu-id="3e422-536">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-536">Minimum system</span></span> | <span data-ttu-id="3e422-537">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-537">Windows 2000</span></span>                                                                                                                                                  |



 

### <a name="isenabled"></a><span data-ttu-id="3e422-538">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="3e422-538">IsEnabled</span></span>



| <span data-ttu-id="3e422-539">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-539">Entry</span></span> | <span data-ttu-id="3e422-540">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-540">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-541">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-541">Description</span></span>    | <span data-ttu-id="3e422-542">Если приложение или компонент COM+ отключены, параметр Enable имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="3e422-542">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="3e422-543">Если приложение или компонент COM+ включен, то параметр Enabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="3e422-543">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="3e422-544">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-544">Access</span></span>         | <span data-ttu-id="3e422-545">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-545">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="3e422-546">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-546">Type</span></span>           | <span data-ttu-id="3e422-547">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-547">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="3e422-548">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-548">Default</span></span>        | <span data-ttu-id="3e422-549">True</span><span class="sxs-lookup"><span data-stu-id="3e422-549">True</span></span>                                                                                                                                      |
| <span data-ttu-id="3e422-550">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-550">Minimum system</span></span> | <span data-ttu-id="3e422-551">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-551">Windows XP</span></span>                                                                                                                                |



 

### <a name="issystem"></a><span data-ttu-id="3e422-552">IsSystem</span><span class="sxs-lookup"><span data-stu-id="3e422-552">IsSystem</span></span>



| <span data-ttu-id="3e422-553">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-553">Entry</span></span> | <span data-ttu-id="3e422-554">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-554">Value</span></span> |
|----------------|--------------------------------------|
| <span data-ttu-id="3e422-555">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-555">Description</span></span>    | <span data-ttu-id="3e422-556">Определяет системные приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="3e422-556">Identifies COM+ system applications.</span></span> |
| <span data-ttu-id="3e422-557">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-557">Access</span></span>         | <span data-ttu-id="3e422-558">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e422-558">ReadOnly</span></span>                             |
| <span data-ttu-id="3e422-559">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-559">Type</span></span>           | <span data-ttu-id="3e422-560">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-560">Bool</span></span>                                 |
| <span data-ttu-id="3e422-561">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-561">Default</span></span>        | <span data-ttu-id="3e422-562">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-562">False</span></span>                                |
| <span data-ttu-id="3e422-563">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-563">Minimum system</span></span> | <span data-ttu-id="3e422-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-564">Windows 2000</span></span>                         |



 

### <a name="maxdumpcount"></a><span data-ttu-id="3e422-565">максдумпкаунт</span><span class="sxs-lookup"><span data-stu-id="3e422-565">MaxDumpCount</span></span>



| <span data-ttu-id="3e422-566">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-566">Entry</span></span> | <span data-ttu-id="3e422-567">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-567">Value</span></span> |
|----------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-568">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-568">Description</span></span>    | <span data-ttu-id="3e422-569">Указывает максимальное число файлов, создаваемых до перезаписи.</span><span class="sxs-lookup"><span data-stu-id="3e422-569">Indicates the maximum number of files to be generated before overwriting occurs.</span></span> |
| <span data-ttu-id="3e422-570">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-570">Access</span></span>         | <span data-ttu-id="3e422-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-571">ReadWrite</span></span>                                                                        |
| <span data-ttu-id="3e422-572">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-572">Type</span></span>           | <span data-ttu-id="3e422-573">Long (1-200)</span><span class="sxs-lookup"><span data-stu-id="3e422-573">Long (1-200)</span></span>                                                                     |
| <span data-ttu-id="3e422-574">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-574">Default</span></span>        | <span data-ttu-id="3e422-575">5</span><span class="sxs-lookup"><span data-stu-id="3e422-575">5</span></span>                                                                                |
| <span data-ttu-id="3e422-576">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-576">Minimum system</span></span> | <span data-ttu-id="3e422-577">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-577">Windows XP</span></span>                                                                       |



 

### <a name="name"></a><span data-ttu-id="3e422-578">Имя</span><span class="sxs-lookup"><span data-stu-id="3e422-578">Name</span></span>



| <span data-ttu-id="3e422-579">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-579">Entry</span></span> | <span data-ttu-id="3e422-580">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-580">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-581">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-581">Description</span></span>    | <span data-ttu-id="3e422-582">Имя приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-582">The name of the application.</span></span> <span data-ttu-id="3e422-583">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="3e422-583">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="3e422-584">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-584">Access</span></span>         | <span data-ttu-id="3e422-585">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-585">ReadWrite</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="3e422-586">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-586">Type</span></span>           | <span data-ttu-id="3e422-587">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-587">String</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="3e422-588">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-588">Default</span></span>        | <span data-ttu-id="3e422-589">"Новое приложение"</span><span class="sxs-lookup"><span data-stu-id="3e422-589">"New Application"</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="3e422-590">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-590">Minimum system</span></span> | <span data-ttu-id="3e422-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-591">Windows 2000</span></span>                                                                                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="3e422-592">Для приложений следует выбрать уникальные имена.</span><span class="sxs-lookup"><span data-stu-id="3e422-592">Unique names should be chosen for applications.</span></span> <span data-ttu-id="3e422-593">Если создано несколько приложений с одним и тем же именем, оно может мешать сослаться на эти приложения по имени, что приведет к непредсказуемому поведению.</span><span class="sxs-lookup"><span data-stu-id="3e422-593">If multiple applications are created with the same name, it can interfere with referencing the applications by name, resulting in unpredictable behavior.</span></span>

 

### <a name="password"></a><span data-ttu-id="3e422-594">Пароль</span><span class="sxs-lookup"><span data-stu-id="3e422-594">Password</span></span>



| <span data-ttu-id="3e422-595">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-595">Entry</span></span> | <span data-ttu-id="3e422-596">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-596">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="3e422-597">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-597">Description</span></span>    | <span data-ttu-id="3e422-598">Задает пароль, используемый серверным процессом для входа в систему под удостоверением.</span><span class="sxs-lookup"><span data-stu-id="3e422-598">Sets the password used by the server process to log on under the identity.</span></span> |
| <span data-ttu-id="3e422-599">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-599">Access</span></span>         | <span data-ttu-id="3e422-600">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="3e422-600">WriteOnly</span></span>                                                                  |
| <span data-ttu-id="3e422-601">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-601">Type</span></span>           | <span data-ttu-id="3e422-602">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-602">String</span></span>                                                                     |
| <span data-ttu-id="3e422-603">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-603">Default</span></span>        | <span data-ttu-id="3e422-604">""</span><span class="sxs-lookup"><span data-stu-id="3e422-604">""</span></span>                                                                         |
| <span data-ttu-id="3e422-605">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-605">Minimum system</span></span> | <span data-ttu-id="3e422-606">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-606">Windows 2000</span></span>                                                               |



 

<span data-ttu-id="3e422-607">Пароль должен быть задан в то же время, что и удостоверение, перед использованием [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), так как пароль и удостоверение проверяются перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="3e422-607">Password should be set at the same time as Identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="3e422-608">Если пароль и удостоверение не будут синхронизированы, приложение не сможет быть запущено, пока администратор не запустит их.</span><span class="sxs-lookup"><span data-stu-id="3e422-608">If the password and identity get out of sync, the application cannot be launched until they are reset by an administrator.</span></span>

### <a name="qcauthenticatemsgs"></a><span data-ttu-id="3e422-609">ккаусентикатемсгс</span><span class="sxs-lookup"><span data-stu-id="3e422-609">QCAuthenticateMsgs</span></span>



| <span data-ttu-id="3e422-610">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-610">Entry</span></span> | <span data-ttu-id="3e422-611">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-611">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-612">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-612">Description</span></span>    | <span data-ttu-id="3e422-613">Указывает, при каких обстоятельствах проверка подлинности запросов к приложению выполняется в очереди.</span><span class="sxs-lookup"><span data-stu-id="3e422-613">Indicates under what circumstances queued requests to an application are authenticated.</span></span>                                                 |
| <span data-ttu-id="3e422-614">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-614">Access</span></span>         | <span data-ttu-id="3e422-615">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-615">ReadWrite</span></span>                                                                                                                               |
| <span data-ttu-id="3e422-616">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-616">Type</span></span>           | <span data-ttu-id="3e422-617">Длинные возможные значения: Комадминккмессажеаусентикатесекуреаппс (0) Комадминккмессажеаусентикатеофф (1) Комадминккмессажеаусентикатеон (2)</span><span class="sxs-lookup"><span data-stu-id="3e422-617">Long Possible values:COMAdminQCMessageAuthenticateSecureApps (0)COMAdminQCMessageAuthenticateOff (1)COMAdminQCMessageAuthenticateOn (2)</span></span> |
| <span data-ttu-id="3e422-618">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-618">Default</span></span>        | <span data-ttu-id="3e422-619">Комадминккмессажеаусентикатесекуреаппс (0)</span><span class="sxs-lookup"><span data-stu-id="3e422-619">COMAdminQCMessageAuthenticateSecureApps (0)</span></span>                                                                                             |
| <span data-ttu-id="3e422-620">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-620">Minimum system</span></span> | <span data-ttu-id="3e422-621">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-621">Windows XP</span></span>                                                                                                                              |



 

### <a name="qclistenermaxthreads"></a><span data-ttu-id="3e422-622">кклистенермакссреадс</span><span class="sxs-lookup"><span data-stu-id="3e422-622">QCListenerMaxThreads</span></span>



| <span data-ttu-id="3e422-623">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-623">Entry</span></span> | <span data-ttu-id="3e422-624">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-624">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-625">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-625">Description</span></span>    | <span data-ttu-id="3e422-626">Указывает максимальное число параллельных потоков прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="3e422-626">Indicates the maximum number of concurrent listener threads.</span></span> <span data-ttu-id="3e422-627">Допустимый диапазон для этого свойства — от 0 до 1000.</span><span class="sxs-lookup"><span data-stu-id="3e422-627">The valid range for this property is 0 to 1000.</span></span> <span data-ttu-id="3e422-628">Для вновь созданного приложения этот параметр является производным от алгоритма, который в настоящее время используется для определения количества потоков прослушивателя по умолчанию: в 16 раз больше количества процессоров на сервере.</span><span class="sxs-lookup"><span data-stu-id="3e422-628">For a newly created application, the setting is derived from the algorithm currently used for determining the default number of listener threads: 16 times the number of CPUs in the server.</span></span> |
| <span data-ttu-id="3e422-629">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-629">Access</span></span>         | <span data-ttu-id="3e422-630">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-630">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3e422-631">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-631">Type</span></span>           | <span data-ttu-id="3e422-632">Long (0-1000)</span><span class="sxs-lookup"><span data-stu-id="3e422-632">Long (0-1000)</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3e422-633">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-633">Default</span></span>        | <span data-ttu-id="3e422-634">0</span><span class="sxs-lookup"><span data-stu-id="3e422-634">0</span></span>                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e422-635">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-635">Minimum system</span></span> | <span data-ttu-id="3e422-636">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-636">Windows XP</span></span>                                                                                                                                                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="3e422-637">Это свойство также доступно с возможностью чтения и записи на вкладке " **очередь** " средства администрирования "службы компонентов".</span><span class="sxs-lookup"><span data-stu-id="3e422-637">This property is also available with read/write capability from the **Queuing** tab of the Component Services administrative tool.</span></span>

 

### <a name="queuelistenerenabled"></a><span data-ttu-id="3e422-638">куеуелистенеренаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-638">QueueListenerEnabled</span></span>



| <span data-ttu-id="3e422-639">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-639">Entry</span></span> | <span data-ttu-id="3e422-640">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-640">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-641">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-641">Description</span></span>    | <span data-ttu-id="3e422-642">Указывает, включен ли прослушиватель очередей компонентов для приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-642">Indicates whether the queued components listener is enabled for the application.</span></span> <span data-ttu-id="3e422-643">Если параметр включен, прослушиватель запускается при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-643">If enabled, the listener is launched when the application starts.</span></span> <span data-ttu-id="3e422-644">Это свойство вступает в силу, только если для Куеуинженаблед задано значение true.</span><span class="sxs-lookup"><span data-stu-id="3e422-644">This property takes effect only if QueuingEnabled is set to True.</span></span> |
| <span data-ttu-id="3e422-645">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-645">Access</span></span>         | <span data-ttu-id="3e422-646">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-646">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="3e422-647">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-647">Type</span></span>           | <span data-ttu-id="3e422-648">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-648">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="3e422-649">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-649">Default</span></span>        | <span data-ttu-id="3e422-650">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-650">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="3e422-651">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-651">Minimum system</span></span> | <span data-ttu-id="3e422-652">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-652">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="queuingenabled"></a><span data-ttu-id="3e422-653">куеуинженаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-653">QueuingEnabled</span></span>



| <span data-ttu-id="3e422-654">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-654">Entry</span></span> | <span data-ttu-id="3e422-655">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-655">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-656">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-656">Description</span></span>    | <span data-ttu-id="3e422-657">Указывает, включена ли для приложения служба очередей компонентов COM+.</span><span class="sxs-lookup"><span data-stu-id="3e422-657">Indicates whether the COM+ Queued Components service is enabled for the application.</span></span> |
| <span data-ttu-id="3e422-658">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-658">Access</span></span>         | <span data-ttu-id="3e422-659">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-659">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="3e422-660">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-660">Type</span></span>           | <span data-ttu-id="3e422-661">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-661">Bool</span></span>                                                                                 |
| <span data-ttu-id="3e422-662">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-662">Default</span></span>        | <span data-ttu-id="3e422-663">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-663">False</span></span>                                                                                |
| <span data-ttu-id="3e422-664">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-664">Minimum system</span></span> | <span data-ttu-id="3e422-665">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-665">Windows 2000</span></span>                                                                         |



 

### <a name="recycleactivationlimit"></a><span data-ttu-id="3e422-666">рециклеактиватионлимит</span><span class="sxs-lookup"><span data-stu-id="3e422-666">RecycleActivationLimit</span></span>



| <span data-ttu-id="3e422-667">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-667">Entry</span></span> | <span data-ttu-id="3e422-668">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-668">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-669">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-669">Description</span></span>    | <span data-ttu-id="3e422-670">Указывает максимальное количество активаций настроенных объектов в приложении, которое следует принять перед повторным запуском процесса.</span><span class="sxs-lookup"><span data-stu-id="3e422-670">Indicates the maximum number of activations of configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="3e422-671">По умолчанию число активаций равно 0.</span><span class="sxs-lookup"><span data-stu-id="3e422-671">The default number of activations is 0.</span></span> |
| <span data-ttu-id="3e422-672">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-672">Access</span></span>         | <span data-ttu-id="3e422-673">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-673">ReadWrite</span></span>                                                                                                                                                            |
| <span data-ttu-id="3e422-674">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-674">Type</span></span>           | <span data-ttu-id="3e422-675">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="3e422-675">Long (0-1048576)</span></span>                                                                                                                                                     |
| <span data-ttu-id="3e422-676">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-676">Default</span></span>        | <span data-ttu-id="3e422-677">0</span><span class="sxs-lookup"><span data-stu-id="3e422-677">0</span></span>                                                                                                                                                                    |
| <span data-ttu-id="3e422-678">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-678">Minimum system</span></span> | <span data-ttu-id="3e422-679">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-679">Windows XP</span></span>                                                                                                                                                           |



 

### <a name="recyclecalllimit"></a><span data-ttu-id="3e422-680">рециклекалллимит</span><span class="sxs-lookup"><span data-stu-id="3e422-680">RecycleCallLimit</span></span>



| <span data-ttu-id="3e422-681">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-681">Entry</span></span> | <span data-ttu-id="3e422-682">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-682">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-683">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-683">Description</span></span>    | <span data-ttu-id="3e422-684">Указывает максимальное число вызовов, которое разрешает принимать настроенные объекты в приложении перед перезапуском процесса.</span><span class="sxs-lookup"><span data-stu-id="3e422-684">Indicates the maximum number of calls to allow configured objects in the application to accept before recycling the process.</span></span> <span data-ttu-id="3e422-685">По умолчанию число вызовов равно 0.</span><span class="sxs-lookup"><span data-stu-id="3e422-685">The default number of calls is 0.</span></span> |
| <span data-ttu-id="3e422-686">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-686">Access</span></span>         | <span data-ttu-id="3e422-687">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-687">ReadWrite</span></span>                                                                                                                                                      |
| <span data-ttu-id="3e422-688">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-688">Type</span></span>           | <span data-ttu-id="3e422-689">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="3e422-689">Long (0-1048576)</span></span>                                                                                                                                               |
| <span data-ttu-id="3e422-690">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-690">Default</span></span>        | <span data-ttu-id="3e422-691">0</span><span class="sxs-lookup"><span data-stu-id="3e422-691">0</span></span>                                                                                                                                                              |
| <span data-ttu-id="3e422-692">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-692">Minimum system</span></span> | <span data-ttu-id="3e422-693">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-693">Windows XP</span></span>                                                                                                                                                     |



 

### <a name="recycleexpirationtimeout"></a><span data-ttu-id="3e422-694">рецикликспиратионтимеаут</span><span class="sxs-lookup"><span data-stu-id="3e422-694">RecycleExpirationTimeout</span></span>



| <span data-ttu-id="3e422-695">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-695">Entry</span></span> | <span data-ttu-id="3e422-696">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-696">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-697">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-697">Description</span></span>    | <span data-ttu-id="3e422-698">Указывает период времени (в минутах), в течение которого должен выполняться перезапущенный процесс, прежде чем завершить его работу.</span><span class="sxs-lookup"><span data-stu-id="3e422-698">Indicates the amount of time (in minutes) to allow a recycled process to run before shutting it down.</span></span> <span data-ttu-id="3e422-699">Отсчет начинается сразу же после перезапуска процесса.</span><span class="sxs-lookup"><span data-stu-id="3e422-699">The countdown begins immediately after the process is recycled.</span></span> <span data-ttu-id="3e422-700">Максимальное время ожидания истечения срока действия составляет 1440 минут (24 часа), а значение по умолчанию — 15 минут.</span><span class="sxs-lookup"><span data-stu-id="3e422-700">The maximum expiration time-out is 1440 minutes (24 hours), and the default is 15 minutes.</span></span> |
| <span data-ttu-id="3e422-701">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-701">Access</span></span>         | <span data-ttu-id="3e422-702">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-702">ReadWrite</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="3e422-703">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-703">Type</span></span>           | <span data-ttu-id="3e422-704">Long (1-1440)</span><span class="sxs-lookup"><span data-stu-id="3e422-704">Long (1-1440)</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e422-705">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-705">Default</span></span>        | <span data-ttu-id="3e422-706">15</span><span class="sxs-lookup"><span data-stu-id="3e422-706">15</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3e422-707">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-707">Minimum system</span></span> | <span data-ttu-id="3e422-708">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-708">Windows XP</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="recyclelifetimelimit"></a><span data-ttu-id="3e422-709">рециклелифетимелимит</span><span class="sxs-lookup"><span data-stu-id="3e422-709">RecycleLifetimeLimit</span></span>



| <span data-ttu-id="3e422-710">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-710">Entry</span></span> | <span data-ttu-id="3e422-711">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-711">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-712">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-712">Description</span></span>    | <span data-ttu-id="3e422-713">Указывает максимальное количество минут, в течение которых можно запустить процесс перед его повторным запуском.</span><span class="sxs-lookup"><span data-stu-id="3e422-713">Indicates the maximum number of minutes to allow a process to run before recycling it.</span></span> <span data-ttu-id="3e422-714">Максимальный срок жизни составляет 30240 минут (21 день), а значение по умолчанию — 0 минут.</span><span class="sxs-lookup"><span data-stu-id="3e422-714">The maximum lifetime limit is 30240 minutes (21 days), and the default is 0 minutes.</span></span> |
| <span data-ttu-id="3e422-715">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-715">Access</span></span>         | <span data-ttu-id="3e422-716">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-716">ReadWrite</span></span>                                                                                                                                                                   |
| <span data-ttu-id="3e422-717">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-717">Type</span></span>           | <span data-ttu-id="3e422-718">Long (0-30240)</span><span class="sxs-lookup"><span data-stu-id="3e422-718">Long (0-30240)</span></span>                                                                                                                                                              |
| <span data-ttu-id="3e422-719">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-719">Default</span></span>        | <span data-ttu-id="3e422-720">0</span><span class="sxs-lookup"><span data-stu-id="3e422-720">0</span></span>                                                                                                                                                                           |
| <span data-ttu-id="3e422-721">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-721">Minimum system</span></span> | <span data-ttu-id="3e422-722">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-722">Windows XP</span></span>                                                                                                                                                                  |



 

### <a name="recyclememorylimit"></a><span data-ttu-id="3e422-723">рециклемеморилимит</span><span class="sxs-lookup"><span data-stu-id="3e422-723">RecycleMemoryLimit</span></span>



| <span data-ttu-id="3e422-724">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-724">Entry</span></span> | <span data-ttu-id="3e422-725">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-725">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-726">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-726">Description</span></span>    | <span data-ttu-id="3e422-727">Указывает максимальный объем использования памяти (в килобайтах), который может быть использован перед повторным запуском процесса.</span><span class="sxs-lookup"><span data-stu-id="3e422-727">Indicates the maximum amount of memory usage (in kilobytes) allowed a process before it's recycled.</span></span> <span data-ttu-id="3e422-728">Если использование памяти процесса превышает указанное число в течение более одной минуты, процесс будет перезапущен.</span><span class="sxs-lookup"><span data-stu-id="3e422-728">If the process memory usage exceeds the specified number for a period longer than one minute, the process is recycled.</span></span> <span data-ttu-id="3e422-729">По умолчанию объем используемой памяти составляет 0 КБ.</span><span class="sxs-lookup"><span data-stu-id="3e422-729">The default amount of memory usage is 0 KB.</span></span> |
| <span data-ttu-id="3e422-730">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-730">Access</span></span>         | <span data-ttu-id="3e422-731">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-731">ReadWrite</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="3e422-732">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-732">Type</span></span>           | <span data-ttu-id="3e422-733">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="3e422-733">Long (0-1048576)</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3e422-734">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-734">Default</span></span>        | <span data-ttu-id="3e422-735">0</span><span class="sxs-lookup"><span data-stu-id="3e422-735">0</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3e422-736">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-736">Minimum system</span></span> | <span data-ttu-id="3e422-737">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-737">Windows XP</span></span>                                                                                                                                                                                                                                                             |



 

### <a name="replicable"></a><span data-ttu-id="3e422-738">Репликаци</span><span class="sxs-lookup"><span data-stu-id="3e422-738">Replicable</span></span>



| <span data-ttu-id="3e422-739">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-739">Entry</span></span> | <span data-ttu-id="3e422-740">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-740">Value</span></span> |
|----------------|------------------------------------------------------|
| <span data-ttu-id="3e422-741">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-741">Description</span></span>    | <span data-ttu-id="3e422-742">Указывает, можно ли реплицировать приложение.</span><span class="sxs-lookup"><span data-stu-id="3e422-742">Indicates whether the application can be replicated.</span></span> |
| <span data-ttu-id="3e422-743">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-743">Access</span></span>         | <span data-ttu-id="3e422-744">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-744">ReadWrite</span></span>                                            |
| <span data-ttu-id="3e422-745">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-745">Type</span></span>           | <span data-ttu-id="3e422-746">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-746">Bool</span></span>                                                 |
| <span data-ttu-id="3e422-747">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-747">Default</span></span>        | <span data-ttu-id="3e422-748">True</span><span class="sxs-lookup"><span data-stu-id="3e422-748">True</span></span>                                                 |
| <span data-ttu-id="3e422-749">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-749">Minimum system</span></span> | <span data-ttu-id="3e422-750">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-750">Windows XP</span></span>                                           |



 

### <a name="runforever"></a><span data-ttu-id="3e422-751">рунфоревер</span><span class="sxs-lookup"><span data-stu-id="3e422-751">RunForever</span></span>



| <span data-ttu-id="3e422-752">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-752">Entry</span></span> | <span data-ttu-id="3e422-753">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-753">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-754">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-754">Description</span></span>    | <span data-ttu-id="3e422-755">Позволяет серверному процессу продолжать работу в случае бездействия приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-755">Enables a server process to continue if an application is idle.</span></span> <span data-ttu-id="3e422-756">Если задано значение true, серверный процесс не завершает работу при неактивности.</span><span class="sxs-lookup"><span data-stu-id="3e422-756">If set to True, the server process does not shut down when left idle.</span></span> <span data-ttu-id="3e422-757">Если задано значение false, процесс завершается в соответствии со значением, заданным свойством Шутдовнафтер.</span><span class="sxs-lookup"><span data-stu-id="3e422-757">If set to False, the process shuts down according to the value set by the ShutdownAfter property.</span></span> <span data-ttu-id="3e422-758">Рунфоревер не включен для приложений библиотеки (внутрипроцессного приложения).</span><span class="sxs-lookup"><span data-stu-id="3e422-758">RunForever is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="3e422-759">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-759">Access</span></span>         | <span data-ttu-id="3e422-760">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-760">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="3e422-761">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-761">Type</span></span>           | <span data-ttu-id="3e422-762">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-762">Bool</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="3e422-763">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-763">Default</span></span>        | <span data-ttu-id="3e422-764">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-764">False</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e422-765">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-765">Minimum system</span></span> | <span data-ttu-id="3e422-766">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-766">Windows 2000</span></span>                                                                                                                                                                                                                                                                                             |



 

### <a name="servicename"></a><span data-ttu-id="3e422-767">ServiceName</span><span class="sxs-lookup"><span data-stu-id="3e422-767">ServiceName</span></span>



| <span data-ttu-id="3e422-768">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-768">Entry</span></span> | <span data-ttu-id="3e422-769">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-769">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-770">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-770">Description</span></span>    | <span data-ttu-id="3e422-771">Имя службы, соответствующее приложению, настроенному для запуска в качестве приложения службы.</span><span class="sxs-lookup"><span data-stu-id="3e422-771">The service name corresponding to the application configured to run as a service application.</span></span> <span data-ttu-id="3e422-772">Если это значение равно **null**, приложение не будет настроено для запуска в качестве службы.</span><span class="sxs-lookup"><span data-stu-id="3e422-772">If this value is **NULL**, the application is not configured to run as a service.</span></span> <span data-ttu-id="3e422-773">В противном случае сведения о конфигурации для службы можно найти с помощью имени службы.</span><span class="sxs-lookup"><span data-stu-id="3e422-773">Otherwise, the configuration information for the service can be found by using the service name.</span></span> |
| <span data-ttu-id="3e422-774">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-774">Access</span></span>         | <span data-ttu-id="3e422-775">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="3e422-775">ReadOnly</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e422-776">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-776">Type</span></span>           | <span data-ttu-id="3e422-777">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-777">String</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="3e422-778">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-778">Default</span></span>        | <span data-ttu-id="3e422-779">""</span><span class="sxs-lookup"><span data-stu-id="3e422-779">""</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="3e422-780">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-780">Minimum system</span></span> | <span data-ttu-id="3e422-781">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-781">Windows XP</span></span>                                                                                                                                                                                                                                                                       |



 

### <a name="shutdownafter"></a><span data-ttu-id="3e422-782">шутдовнафтер</span><span class="sxs-lookup"><span data-stu-id="3e422-782">ShutdownAfter</span></span>



| <span data-ttu-id="3e422-783">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-783">Entry</span></span> | <span data-ttu-id="3e422-784">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-784">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-785">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-785">Description</span></span>    | <span data-ttu-id="3e422-786">Устанавливает задержку перед завершением процесса сервера после его простоя.</span><span class="sxs-lookup"><span data-stu-id="3e422-786">Sets the delay before shutting down a server process after it becomes idle.</span></span> <span data-ttu-id="3e422-787">Задержка завершения работы в диапазоне от 0 до 1440 минут (24 часа).</span><span class="sxs-lookup"><span data-stu-id="3e422-787">Shutdown latency ranges from 0 to 1440 minutes (24 hours).</span></span> <span data-ttu-id="3e422-788">Если Рунфоревер имеет значение true, это свойство игнорируется.</span><span class="sxs-lookup"><span data-stu-id="3e422-788">If RunForever is set to True, this property is ignored.</span></span> <span data-ttu-id="3e422-789">Шутдовнафтер не включен для приложений библиотеки (внутрипроцессного приложения).</span><span class="sxs-lookup"><span data-stu-id="3e422-789">ShutdownAfter is not enabled for library (in-process) applications.</span></span> |
| <span data-ttu-id="3e422-790">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-790">Access</span></span>         | <span data-ttu-id="3e422-791">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-791">ReadWrite</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3e422-792">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-792">Type</span></span>           | <span data-ttu-id="3e422-793">Long (0-1440)</span><span class="sxs-lookup"><span data-stu-id="3e422-793">Long (0-1440)</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3e422-794">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-794">Default</span></span>        | <span data-ttu-id="3e422-795">3</span><span class="sxs-lookup"><span data-stu-id="3e422-795">3</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3e422-796">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-796">Minimum system</span></span> | <span data-ttu-id="3e422-797">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="3e422-797">Windows 2000</span></span>                                                                                                                                                                                                                                                       |



 

### <a name="soapactivated"></a><span data-ttu-id="3e422-798">соапактиватед</span><span class="sxs-lookup"><span data-stu-id="3e422-798">SoapActivated</span></span>



| <span data-ttu-id="3e422-799">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-799">Entry</span></span> | <span data-ttu-id="3e422-800">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-800">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-801">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-801">Description</span></span>    | <span data-ttu-id="3e422-802">Указывает, доступно ли это приложение для использования через протокол SOAP.</span><span class="sxs-lookup"><span data-stu-id="3e422-802">Indicates whether this application is exposed for consumption via the SOAP protocol.</span></span> |
| <span data-ttu-id="3e422-803">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-803">Access</span></span>         | <span data-ttu-id="3e422-804">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-804">ReadWrite</span></span>                                                                            |
| <span data-ttu-id="3e422-805">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-805">Type</span></span>           | <span data-ttu-id="3e422-806">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-806">Bool</span></span>                                                                                 |
| <span data-ttu-id="3e422-807">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-807">Default</span></span>        | <span data-ttu-id="3e422-808">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-808">False</span></span>                                                                                |
| <span data-ttu-id="3e422-809">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-809">Minimum system</span></span> | <span data-ttu-id="3e422-810">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e422-810">Windows Server 2003</span></span>                                                                  |



 

### <a name="soapbaseurl"></a><span data-ttu-id="3e422-811">соапбасеурл</span><span class="sxs-lookup"><span data-stu-id="3e422-811">SoapBaseUrl</span></span>



| <span data-ttu-id="3e422-812">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-812">Entry</span></span> | <span data-ttu-id="3e422-813">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-813">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-814">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-814">Description</span></span>    | <span data-ttu-id="3e422-815">Конечная точка URL-адреса, в которой это приложение предоставляется через протокол SOAP.</span><span class="sxs-lookup"><span data-stu-id="3e422-815">The URL endpoint at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="3e422-816">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-816">Access</span></span>         | <span data-ttu-id="3e422-817">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-817">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="3e422-818">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-818">Type</span></span>           | <span data-ttu-id="3e422-819">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-819">String</span></span>                                                                       |
| <span data-ttu-id="3e422-820">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-820">Default</span></span>        | <span data-ttu-id="3e422-821">""</span><span class="sxs-lookup"><span data-stu-id="3e422-821">""</span></span>                                                                           |
| <span data-ttu-id="3e422-822">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-822">Minimum system</span></span> | <span data-ttu-id="3e422-823">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e422-823">Windows Server 2003</span></span>                                                          |



 

### <a name="soapmailto"></a><span data-ttu-id="3e422-824">соапмаилто</span><span class="sxs-lookup"><span data-stu-id="3e422-824">SoapMailTo</span></span>



| <span data-ttu-id="3e422-825">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-825">Entry</span></span> | <span data-ttu-id="3e422-826">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-826">Value</span></span> |
|----------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-827">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-827">Description</span></span>    | <span data-ttu-id="3e422-828">Адрес электронной почты, по которому приложение предоставляется через протокол SOAP.</span><span class="sxs-lookup"><span data-stu-id="3e422-828">The email address at which this application is exposed via the SOAP protocol.</span></span> |
| <span data-ttu-id="3e422-829">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-829">Access</span></span>         | <span data-ttu-id="3e422-830">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-830">ReadWrite</span></span>                                                                     |
| <span data-ttu-id="3e422-831">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-831">Type</span></span>           | <span data-ttu-id="3e422-832">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-832">String</span></span>                                                                        |
| <span data-ttu-id="3e422-833">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-833">Default</span></span>        | <span data-ttu-id="3e422-834">""</span><span class="sxs-lookup"><span data-stu-id="3e422-834">""</span></span>                                                                            |
| <span data-ttu-id="3e422-835">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-835">Minimum system</span></span> | <span data-ttu-id="3e422-836">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e422-836">Windows Server 2003</span></span>                                                           |



 

### <a name="soapvroot"></a><span data-ttu-id="3e422-837">соапврут</span><span class="sxs-lookup"><span data-stu-id="3e422-837">SoapVRoot</span></span>



| <span data-ttu-id="3e422-838">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-838">Entry</span></span> | <span data-ttu-id="3e422-839">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-839">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-840">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-840">Description</span></span>    | <span data-ttu-id="3e422-841">Виртуальный корневой каталог IIS, в котором находятся сценарии доступа, предоставляющие приложение через протокол SOAP.</span><span class="sxs-lookup"><span data-stu-id="3e422-841">The IIS virtual root directory in which the access scripts that expose the application via the SOAP protocol reside.</span></span> |
| <span data-ttu-id="3e422-842">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-842">Access</span></span>         | <span data-ttu-id="3e422-843">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-843">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="3e422-844">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-844">Type</span></span>           | <span data-ttu-id="3e422-845">Строка</span><span class="sxs-lookup"><span data-stu-id="3e422-845">String</span></span>                                                                                                               |
| <span data-ttu-id="3e422-846">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-846">Default</span></span>        | <span data-ttu-id="3e422-847">""</span><span class="sxs-lookup"><span data-stu-id="3e422-847">""</span></span>                                                                                                                   |
| <span data-ttu-id="3e422-848">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-848">Minimum system</span></span> | <span data-ttu-id="3e422-849">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e422-849">Windows Server 2003</span></span>                                                                                                  |



 

### <a name="srpenabled"></a><span data-ttu-id="3e422-850">српенаблед</span><span class="sxs-lookup"><span data-stu-id="3e422-850">SRPEnabled</span></span>



| <span data-ttu-id="3e422-851">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-851">Entry</span></span> | <span data-ttu-id="3e422-852">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-852">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-853">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-853">Description</span></span>    | <span data-ttu-id="3e422-854">Определяет политику ограниченного использования программ (SRP) для приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-854">Determines the software restriction policy (SRP) for the application.</span></span> <span data-ttu-id="3e422-855">Если задано значение true, используется свойство Срптрустлевел для приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-855">If set to True, the SRPTrustLevel property for the application is used.</span></span> <span data-ttu-id="3e422-856">Если задано значение false, используются политики ограниченного использования программ из локальных параметров безопасности.</span><span class="sxs-lookup"><span data-stu-id="3e422-856">If set to False, the software restriction policies from the local security settings are used.</span></span> <span data-ttu-id="3e422-857">Локальными параметрами безопасности управляет оснастка «Локальная политика безопасности» консоли управления (MMC).</span><span class="sxs-lookup"><span data-stu-id="3e422-857">The local security settings are controlled through the Local Security Policy snap-in of the Microsoft Management Console.</span></span> |
| <span data-ttu-id="3e422-858">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-858">Access</span></span>         | <span data-ttu-id="3e422-859">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-859">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="3e422-860">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-860">Type</span></span>           | <span data-ttu-id="3e422-861">Bool</span><span class="sxs-lookup"><span data-stu-id="3e422-861">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="3e422-862">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-862">Default</span></span>        | <span data-ttu-id="3e422-863">Неверно</span><span class="sxs-lookup"><span data-stu-id="3e422-863">False</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="3e422-864">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-864">Minimum system</span></span> | <span data-ttu-id="3e422-865">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-865">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                            |



 

### <a name="srptrustlevel"></a><span data-ttu-id="3e422-866">срптрустлевел</span><span class="sxs-lookup"><span data-stu-id="3e422-866">SRPTrustLevel</span></span>



| <span data-ttu-id="3e422-867">Ввод</span><span class="sxs-lookup"><span data-stu-id="3e422-867">Entry</span></span> | <span data-ttu-id="3e422-868">Значение</span><span class="sxs-lookup"><span data-stu-id="3e422-868">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e422-869">Описание</span><span class="sxs-lookup"><span data-stu-id="3e422-869">Description</span></span>    | <span data-ttu-id="3e422-870">Указывает уровень доверия для политики ограниченного использования программ (SRP) приложения.</span><span class="sxs-lookup"><span data-stu-id="3e422-870">Indicates the software restriction policy (SRP) trust level of the application.</span></span> <span data-ttu-id="3e422-871">Это свойство используется только в том случае, если свойство Српенаблед имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="3e422-871">This property is used only if the SRPEnabled property is set to True.</span></span> <span data-ttu-id="3e422-872">Уровень доверия SRP относится к уровню доверия, который вы хотите предоставить приложению.</span><span class="sxs-lookup"><span data-stu-id="3e422-872">The SRP trust level refers to the level of trust that you are willing to give to an application.</span></span> <span data-ttu-id="3e422-873">Неограниченный уровень доверия SRP соответствует более безопасному \_ \_ значению перечисления LEVELID фуллитрустед, а недопустимый уровень доверия SRP соответствует более безопасному \_ \_ неразрешенному значению LEVELID.</span><span class="sxs-lookup"><span data-stu-id="3e422-873">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="3e422-874">Перечисление уровней доверия определяется в Винсафер. h.</span><span class="sxs-lookup"><span data-stu-id="3e422-874">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="3e422-875">Access</span><span class="sxs-lookup"><span data-stu-id="3e422-875">Access</span></span>         | <span data-ttu-id="3e422-876">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3e422-876">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3e422-877">Тип</span><span class="sxs-lookup"><span data-stu-id="3e422-877">Type</span></span>           | <span data-ttu-id="3e422-878">Допустимые значения: БЕЗОПАСная \_ LEVELID \_ запрещена (0x0) более безопасная \_ LEVELID \_ фуллитрустед (0x40000)</span><span class="sxs-lookup"><span data-stu-id="3e422-878">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3e422-879">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3e422-879">Default</span></span>        | <span data-ttu-id="3e422-880">Более безопасная \_ LEVELID \_ фуллитрустед (0x40000)</span><span class="sxs-lookup"><span data-stu-id="3e422-880">SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3e422-881">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="3e422-881">Minimum system</span></span> | <span data-ttu-id="3e422-882">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e422-882">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

<span data-ttu-id="3e422-883">Приложение, которому вы готовы доверять с неограниченным доступом, должно иметь наиболее строгий уровень безопасности, присоединенный к нему.</span><span class="sxs-lookup"><span data-stu-id="3e422-883">An application that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="3e422-884">Приложения, которые не ограничены, могут загружать только неограниченные компоненты, в то время как запрещенные приложения не будут запускаться и поэтому не смогут загрузить какие бы то ни было компоненты.</span><span class="sxs-lookup"><span data-stu-id="3e422-884">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e422-885">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e422-885">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e422-886">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="3e422-886">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
