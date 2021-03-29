---
description: Содержит один объект, соответствующий компьютеру, каталогом которого вы обращаетесь. Этот объект содержит сведения о параметрах на уровне компьютера.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: Коллекция LocalComputer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807900"
---
# <a name="localcomputer-collection"></a><span data-ttu-id="a8bc0-104">Коллекция LocalComputer</span><span class="sxs-lookup"><span data-stu-id="a8bc0-104">LocalComputer collection</span></span>

<span data-ttu-id="a8bc0-105">Содержит один объект, соответствующий компьютеру, каталогом которого вы обращаетесь.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-105">Contains a single object that corresponds to the computer whose catalog you are accessing.</span></span> <span data-ttu-id="a8bc0-106">Этот объект содержит сведения о параметрах на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-106">This object holds computer level settings information.</span></span> <span data-ttu-id="a8bc0-107">При вызове метода [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) для объекта, созданного из класса [**комадминкаталог**](comadmincatalog.md) , объект в коллекции **локалкомпутер** содержит сведения об удаленном компьютере, к каталогу которого вы обращаетесь.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-107">If you call the [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) method on an object created from the [**COMAdminCatalog**](comadmincatalog.md) class, the object in the **LocalComputer** collection contains information about the remote computer whose catalog you are accessing.</span></span>

<span data-ttu-id="a8bc0-108">Эта коллекция не поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a8bc0-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="a8bc0-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="a8bc0-109">Members</span></span>

<span data-ttu-id="a8bc0-110">Коллекция **локалкомпутер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-110">The **LocalComputer** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a8bc0-111">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="a8bc0-111">Related Collections</span></span>

<span data-ttu-id="a8bc0-112">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="a8bc0-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="a8bc0-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="a8bc0-114">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-114">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="a8bc0-115">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-115">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a8bc0-116">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="a8bc0-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="a8bc0-117">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="a8bc0-117">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="a8bc0-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8bc0-118">Properties</span></span>

<span data-ttu-id="a8bc0-119">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="a8bc0-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a8bc0-120">аппликатионпроксирсн</span><span class="sxs-lookup"><span data-stu-id="a8bc0-120">ApplicationProxyRSN</span></span>](#applicationproxyrsn)
-   [<span data-ttu-id="a8bc0-121">Цисенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-121">CISEnabled</span></span>](#cisenabled)
-   [<span data-ttu-id="a8bc0-122">дкоменаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-122">DCOMEnabled</span></span>](#dcomenabled)
-   [<span data-ttu-id="a8bc0-123">дефаултаусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="a8bc0-123">DefaultAuthenticationLevel</span></span>](#defaultauthenticationlevel)
-   [<span data-ttu-id="a8bc0-124">дефаултимперсонатионлевел</span><span class="sxs-lookup"><span data-stu-id="a8bc0-124">DefaultImpersonationLevel</span></span>](#defaultimpersonationlevel)
-   [<span data-ttu-id="a8bc0-125">дефаулттоинтернетпортс</span><span class="sxs-lookup"><span data-stu-id="a8bc0-125">DefaultToInternetPorts</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="a8bc0-126">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-126">Description</span></span>](#description)
-   [<span data-ttu-id="a8bc0-127">дспартитионлукупенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-127">DSPartitionLookupEnabled</span></span>](#dspartitionlookupenabled)
-   [<span data-ttu-id="a8bc0-128">интернетпортслистед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-128">InternetPortsListed</span></span>](#internetportslisted)
-   [<span data-ttu-id="a8bc0-129">Маршрутизатор</span><span class="sxs-lookup"><span data-stu-id="a8bc0-129">IsRouter</span></span>](#isrouter)
-   [<span data-ttu-id="a8bc0-130">лоадбаланЦингклсид</span><span class="sxs-lookup"><span data-stu-id="a8bc0-130">LoadBalancingCLSID</span></span>](#loadbalancingclsid)
-   [<span data-ttu-id="a8bc0-131">локалпартитионлукупенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-131">LocalPartitionLookupEnabled</span></span>](#localpartitionlookupenabled)
-   [<span data-ttu-id="a8bc0-132">Name</span><span class="sxs-lookup"><span data-stu-id="a8bc0-132">Name</span></span>](#name)
-   [<span data-ttu-id="a8bc0-133">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a8bc0-133">OperatingSystem</span></span>](#operatingsystem)
-   [<span data-ttu-id="a8bc0-134">партитионсенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-134">PartitionsEnabled</span></span>](#partitionsenabled)
-   [<span data-ttu-id="a8bc0-135">Порты</span><span class="sxs-lookup"><span data-stu-id="a8bc0-135">Ports</span></span>](#defaulttointernetports)
-   [<span data-ttu-id="a8bc0-136">ресаурцепулинженаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-136">ResourcePoolingEnabled</span></span>](#resourcepoolingenabled)
-   [<span data-ttu-id="a8bc0-137">рпкпроксенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-137">RPCProxyEnabled</span></span>](#rpcproxyenabled)
-   [<span data-ttu-id="a8bc0-138">секуререференцесенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-138">SecureReferencesEnabled</span></span>](#securereferencesenabled)
-   [<span data-ttu-id="a8bc0-139">секурититраккинженаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-139">SecurityTrackingEnabled</span></span>](#securitytrackingenabled)
-   [<span data-ttu-id="a8bc0-140">српактиватеасактиваторчеккс</span><span class="sxs-lookup"><span data-stu-id="a8bc0-140">SRPActivateAsActivatorChecks</span></span>](#srpactivateasactivatorchecks)
-   [<span data-ttu-id="a8bc0-141">српруннингобжектчеккс</span><span class="sxs-lookup"><span data-stu-id="a8bc0-141">SRPRunningObjectChecks</span></span>](#srprunningobjectchecks)
-   [<span data-ttu-id="a8bc0-142">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="a8bc0-142">TransactionTimeout</span></span>](#transactiontimeout)

### <a name="applicationproxyrsn"></a><span data-ttu-id="a8bc0-143">аппликатионпроксирсн</span><span class="sxs-lookup"><span data-stu-id="a8bc0-143">ApplicationProxyRSN</span></span>



| <span data-ttu-id="a8bc0-144">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-144">Entry</span></span> | <span data-ttu-id="a8bc0-145">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-145">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="a8bc0-146">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-146">Description</span></span>    | <span data-ttu-id="a8bc0-147">Имя удаленного сервера, используемое прокси-серверами приложений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-147">Remote server name used by application proxies by default.</span></span> |
| <span data-ttu-id="a8bc0-148">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-148">Access</span></span>         | <span data-ttu-id="a8bc0-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-149">ReadWrite</span></span>                                                  |
| <span data-ttu-id="a8bc0-150">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-150">Type</span></span>           | <span data-ttu-id="a8bc0-151">Строка</span><span class="sxs-lookup"><span data-stu-id="a8bc0-151">String</span></span>                                                     |
| <span data-ttu-id="a8bc0-152">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-152">Default</span></span>        | <span data-ttu-id="a8bc0-153">""</span><span class="sxs-lookup"><span data-stu-id="a8bc0-153">""</span></span>                                                         |
| <span data-ttu-id="a8bc0-154">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-154">Minimum system</span></span> | <span data-ttu-id="a8bc0-155">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-155">Windows 2000</span></span>                                               |



 

### <a name="cisenabled"></a><span data-ttu-id="a8bc0-156">Цисенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-156">CISEnabled</span></span>



| <span data-ttu-id="a8bc0-157">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-157">Entry</span></span> | <span data-ttu-id="a8bc0-158">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-158">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="a8bc0-159">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-159">Description</span></span>    | <span data-ttu-id="a8bc0-160">Указывает, включены ли Интернет-службы COM.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-160">Indicates whether COM Internet Services is enabled.</span></span> |
| <span data-ttu-id="a8bc0-161">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-161">Access</span></span>         | <span data-ttu-id="a8bc0-162">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-162">ReadWrite</span></span>                                           |
| <span data-ttu-id="a8bc0-163">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-163">Type</span></span>           | <span data-ttu-id="a8bc0-164">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-164">Bool</span></span>                                                |
| <span data-ttu-id="a8bc0-165">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-165">Default</span></span>        | <span data-ttu-id="a8bc0-166">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8bc0-166">False</span></span>                                               |
| <span data-ttu-id="a8bc0-167">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-167">Minimum system</span></span> | <span data-ttu-id="a8bc0-168">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-168">Windows 2000</span></span>                                        |



 

### <a name="dcomenabled"></a><span data-ttu-id="a8bc0-169">дкоменаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-169">DCOMEnabled</span></span>



| <span data-ttu-id="a8bc0-170">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-170">Entry</span></span> | <span data-ttu-id="a8bc0-171">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-171">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="a8bc0-172">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-172">Description</span></span>    | <span data-ttu-id="a8bc0-173">Задайте значение true, чтобы включить DCOM на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-173">Set to True to enable DCOM on the computer.</span></span> |
| <span data-ttu-id="a8bc0-174">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-174">Access</span></span>         | <span data-ttu-id="a8bc0-175">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-175">ReadWrite</span></span>                                   |
| <span data-ttu-id="a8bc0-176">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-176">Type</span></span>           | <span data-ttu-id="a8bc0-177">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-177">Bool</span></span>                                        |
| <span data-ttu-id="a8bc0-178">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-178">Default</span></span>        | <span data-ttu-id="a8bc0-179">True</span><span class="sxs-lookup"><span data-stu-id="a8bc0-179">True</span></span>                                        |
| <span data-ttu-id="a8bc0-180">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-180">Minimum system</span></span> | <span data-ttu-id="a8bc0-181">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-181">Windows 2000</span></span>                                |



 

### <a name="defaultauthenticationlevel"></a><span data-ttu-id="a8bc0-182">дефаултаусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="a8bc0-182">DefaultAuthenticationLevel</span></span>



| <span data-ttu-id="a8bc0-183">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-183">Entry</span></span> | <span data-ttu-id="a8bc0-184">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-184">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-185">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-185">Description</span></span>    | <span data-ttu-id="a8bc0-186">Уровень проверки подлинности, используемый приложениями, для которых задана проверка подлинности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-186">Authentication level used by applications that have Authentication set to Default.</span></span> <span data-ttu-id="a8bc0-187">Значения соответствуют параметрам проверки подлинности удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="a8bc0-187">Values correspond to the Remote Procedure Call (RPC) authentication settings.</span></span>                                                                                         |
| <span data-ttu-id="a8bc0-188">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-188">Access</span></span>         | <span data-ttu-id="a8bc0-189">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-189">ReadWrite</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="a8bc0-190">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-190">Type</span></span>           | <span data-ttu-id="a8bc0-191">Длинные возможные значения: Комадминаусентикатиондефаулт (0) Комадминаусентикатионноне (1) Комадминаусентикатионконнект (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-191">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span> |
| <span data-ttu-id="a8bc0-192">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-192">Default</span></span>        | <span data-ttu-id="a8bc0-193">Комадминаусентикатионконнект (2)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-193">COMAdminAuthenticationConnect (2)</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="a8bc0-194">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-194">Minimum system</span></span> | <span data-ttu-id="a8bc0-195">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-195">Windows 2000</span></span>                                                                                                                                                                                                                                             |



 

> [!Note]  
> <span data-ttu-id="a8bc0-196">Комадминаусентикатиондефаулт сопоставляется с Комадминаусентикатионконнект, когда COM вызывает [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="a8bc0-196">COMAdminAuthenticationDefault is mapped to COMAdminAuthenticationConnect when COM calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a8bc0-197">Рекомендуется использовать константы в перечислении, а не числовые значения.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-197">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="defaultimpersonationlevel"></a><span data-ttu-id="a8bc0-198">дефаултимперсонатионлевел</span><span class="sxs-lookup"><span data-stu-id="a8bc0-198">DefaultImpersonationLevel</span></span>



| <span data-ttu-id="a8bc0-199">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-199">Entry</span></span> | <span data-ttu-id="a8bc0-200">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-200">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-201">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-201">Description</span></span>    | <span data-ttu-id="a8bc0-202">Уровень олицетворения, который можно разрешить, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-202">Impersonation level to allow if one is not set.</span></span>                                                                                                               |
| <span data-ttu-id="a8bc0-203">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-203">Access</span></span>         | <span data-ttu-id="a8bc0-204">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-204">ReadWrite</span></span>                                                                                                                                                     |
| <span data-ttu-id="a8bc0-205">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-205">Type</span></span>           | <span data-ttu-id="a8bc0-206">Длинные возможные значения: Комадминимперсонатионанонимаус (1) Комадминимперсонатионидентифи (2) Комадминимперсонатионимперсонате (3) COMAdminImpersonationDelegate (4)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-206">Long Possible values:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4)</span></span> |
| <span data-ttu-id="a8bc0-207">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-207">Default</span></span>        | <span data-ttu-id="a8bc0-208">Комадминимперсонатионидентифи (2)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-208">COMAdminImpersonationIdentify (2)</span></span>                                                                                                                             |
| <span data-ttu-id="a8bc0-209">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-209">Minimum system</span></span> | <span data-ttu-id="a8bc0-210">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-210">Windows 2000</span></span>                                                                                                                                                  |



 

> [!Note]  
> <span data-ttu-id="a8bc0-211">Рекомендуется использовать константы в перечислении, а не числовые значения.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-211">It is recommended that you use the constants in the enumeration, and not the numeric values.</span></span>

 

### <a name="defaulttointernetports"></a><span data-ttu-id="a8bc0-212">дефаулттоинтернетпортс</span><span class="sxs-lookup"><span data-stu-id="a8bc0-212">DefaultToInternetPorts</span></span>



| <span data-ttu-id="a8bc0-213">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-213">Entry</span></span> | <span data-ttu-id="a8bc0-214">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-214">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-215">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-215">Description</span></span>    | <span data-ttu-id="a8bc0-216">Определяет, должен ли тип порта, указанный по умолчанию, быть в Интернете (true) или интрасети (false).</span><span class="sxs-lookup"><span data-stu-id="a8bc0-216">Determines whether the default type of port provided should be Internet (True) or intranet (False).</span></span> |
| <span data-ttu-id="a8bc0-217">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-217">Access</span></span>         | <span data-ttu-id="a8bc0-218">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-218">ReadWrite</span></span>                                                                                           |
| <span data-ttu-id="a8bc0-219">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-219">Type</span></span>           | <span data-ttu-id="a8bc0-220">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-220">Bool</span></span>                                                                                                |
| <span data-ttu-id="a8bc0-221">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-221">Default</span></span>        | <span data-ttu-id="a8bc0-222">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8bc0-222">False</span></span>                                                                                               |
| <span data-ttu-id="a8bc0-223">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-223">Minimum system</span></span> | <span data-ttu-id="a8bc0-224">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-224">Windows 2000</span></span>                                                                                        |



 

### <a name="description"></a><span data-ttu-id="a8bc0-225">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-225">Description</span></span>



| <span data-ttu-id="a8bc0-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-226">Entry</span></span> | <span data-ttu-id="a8bc0-227">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-227">Value</span></span> |
|----------------|--------------------------------|
| <span data-ttu-id="a8bc0-228">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-228">Description</span></span>    | <span data-ttu-id="a8bc0-229">Описание компьютера.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-229">A description of the computer.</span></span> |
| <span data-ttu-id="a8bc0-230">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-230">Access</span></span>         | <span data-ttu-id="a8bc0-231">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-231">ReadWrite</span></span>                      |
| <span data-ttu-id="a8bc0-232">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-232">Type</span></span>           | <span data-ttu-id="a8bc0-233">Строка</span><span class="sxs-lookup"><span data-stu-id="a8bc0-233">String</span></span>                         |
| <span data-ttu-id="a8bc0-234">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-234">Default</span></span>        | <span data-ttu-id="a8bc0-235">""</span><span class="sxs-lookup"><span data-stu-id="a8bc0-235">""</span></span>                             |
| <span data-ttu-id="a8bc0-236">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-236">Minimum system</span></span> | <span data-ttu-id="a8bc0-237">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-237">Windows 2000</span></span>                   |



 

### <a name="dspartitionlookupenabled"></a><span data-ttu-id="a8bc0-238">дспартитионлукупенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-238">DSPartitionLookupEnabled</span></span>



| <span data-ttu-id="a8bc0-239">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-239">Entry</span></span> | <span data-ttu-id="a8bc0-240">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-240">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-241">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-241">Description</span></span>    | <span data-ttu-id="a8bc0-242">Указывает, проверяется ли пользователь сопоставлений секций в хранилище домена.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-242">Indicates whether the user of the partition mappings is checked into the domain store.</span></span> |
| <span data-ttu-id="a8bc0-243">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-243">Access</span></span>         | <span data-ttu-id="a8bc0-244">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-244">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="a8bc0-245">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-245">Type</span></span>           | <span data-ttu-id="a8bc0-246">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-246">Bool</span></span>                                                                                   |
| <span data-ttu-id="a8bc0-247">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-247">Default</span></span>        | <span data-ttu-id="a8bc0-248">True</span><span class="sxs-lookup"><span data-stu-id="a8bc0-248">True</span></span>                                                                                   |
| <span data-ttu-id="a8bc0-249">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-249">Minimum system</span></span> | <span data-ttu-id="a8bc0-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8bc0-250">Windows Server 2003</span></span>                                                                    |



 

### <a name="internetportslisted"></a><span data-ttu-id="a8bc0-251">интернетпортслистед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-251">InternetPortsListed</span></span>



| <span data-ttu-id="a8bc0-252">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-252">Entry</span></span> | <span data-ttu-id="a8bc0-253">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-253">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-254">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-254">Description</span></span>    | <span data-ttu-id="a8bc0-255">Определяет, должны ли порты, перечисленные в свойстве Ports, использоваться для Интернета (true) или для интрасети (false).</span><span class="sxs-lookup"><span data-stu-id="a8bc0-255">Determines whether the ports listed in the Ports property are to be used for Internet (True) or for intranet (False).</span></span> |
| <span data-ttu-id="a8bc0-256">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-256">Access</span></span>         | <span data-ttu-id="a8bc0-257">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-257">ReadWrite</span></span>                                                                                                             |
| <span data-ttu-id="a8bc0-258">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-258">Type</span></span>           | <span data-ttu-id="a8bc0-259">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-259">Bool</span></span>                                                                                                                  |
| <span data-ttu-id="a8bc0-260">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-260">Default</span></span>        | <span data-ttu-id="a8bc0-261">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8bc0-261">False</span></span>                                                                                                                 |
| <span data-ttu-id="a8bc0-262">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-262">Minimum system</span></span> | <span data-ttu-id="a8bc0-263">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-263">Windows 2000</span></span>                                                                                                          |



 

### <a name="isrouter"></a><span data-ttu-id="a8bc0-264">Маршрутизатор</span><span class="sxs-lookup"><span data-stu-id="a8bc0-264">IsRouter</span></span>



| <span data-ttu-id="a8bc0-265">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-265">Entry</span></span> | <span data-ttu-id="a8bc0-266">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-266">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-267">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-267">Description</span></span>    | <span data-ttu-id="a8bc0-268">Задайте значение true, если компьютер является маршрутизатором для службы балансировки нагрузки компонентов (распределения загрузки).</span><span class="sxs-lookup"><span data-stu-id="a8bc0-268">Set to True if the computer is a router for the component load balancing (CLB) service.</span></span> <span data-ttu-id="a8bc0-269">Это свойство может иметь значение true, только если на компьютере установлена служба балансировки нагрузки компонентов. в противном случае для ошибок с КОМАДМИН \_ E \_ требуется \_ другая \_ платформа.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-269">This property can be set to True only if the component load balancing service is currently installed on the computer; otherwise, it errors with COMADMIN\_E\_REQUIRES\_DIFFERENT\_PLATFORM.</span></span> |
| <span data-ttu-id="a8bc0-270">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-270">Access</span></span>         | <span data-ttu-id="a8bc0-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-271">ReadWrite</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a8bc0-272">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-272">Type</span></span>           | <span data-ttu-id="a8bc0-273">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-273">Bool</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a8bc0-274">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-274">Default</span></span>        | <span data-ttu-id="a8bc0-275">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8bc0-275">False</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a8bc0-276">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-276">Minimum system</span></span> | <span data-ttu-id="a8bc0-277">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-277">Windows 2000</span></span>                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="a8bc0-278">Если это свойство имеет значение true, сервер распределения загрузки настроен и запускается при запуске.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-278">If this property is set to True, the CLB server is configured and starts at startup.</span></span> <span data-ttu-id="a8bc0-279">Сервер добавляется в коллекцию Аппликатионклустер, если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-279">The server is added to the ApplicationCluster collection if it is not already present.</span></span>

### <a name="loadbalancingclsid"></a><span data-ttu-id="a8bc0-280">лоадбаланЦингклсид</span><span class="sxs-lookup"><span data-stu-id="a8bc0-280">LoadBalancingCLSID</span></span>



| <span data-ttu-id="a8bc0-281">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-281">Entry</span></span> | <span data-ttu-id="a8bc0-282">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-282">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="a8bc0-283">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-283">Description</span></span>    | <span data-ttu-id="a8bc0-284">Идентификатор CLSID объекта для балансировки.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-284">The CLSID of the object to balance.</span></span> |
| <span data-ttu-id="a8bc0-285">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-285">Access</span></span>         | <span data-ttu-id="a8bc0-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-286">ReadWrite</span></span>                           |
| <span data-ttu-id="a8bc0-287">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-287">Type</span></span>           | <span data-ttu-id="a8bc0-288">Строка</span><span class="sxs-lookup"><span data-stu-id="a8bc0-288">String</span></span>                              |
| <span data-ttu-id="a8bc0-289">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-289">Default</span></span>        | <span data-ttu-id="a8bc0-290">NULL</span><span class="sxs-lookup"><span data-stu-id="a8bc0-290">NULL</span></span>                                |
| <span data-ttu-id="a8bc0-291">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-291">Minimum system</span></span> | <span data-ttu-id="a8bc0-292">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8bc0-292">Windows XP</span></span>                          |



 

### <a name="localpartitionlookupenabled"></a><span data-ttu-id="a8bc0-293">локалпартитионлукупенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-293">LocalPartitionLookupEnabled</span></span>



| <span data-ttu-id="a8bc0-294">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-294">Entry</span></span> | <span data-ttu-id="a8bc0-295">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-295">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-296">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-296">Description</span></span>    | <span data-ttu-id="a8bc0-297">Указывает, проверяются ли пользователь в сопоставлении секций в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-297">Indicates whether the user of the partition mappings is checked into the local store.</span></span> |
| <span data-ttu-id="a8bc0-298">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-298">Access</span></span>         | <span data-ttu-id="a8bc0-299">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-299">ReadWrite</span></span>                                                                             |
| <span data-ttu-id="a8bc0-300">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-300">Type</span></span>           | <span data-ttu-id="a8bc0-301">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-301">Bool</span></span>                                                                                  |
| <span data-ttu-id="a8bc0-302">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-302">Default</span></span>        | <span data-ttu-id="a8bc0-303">True</span><span class="sxs-lookup"><span data-stu-id="a8bc0-303">True</span></span>                                                                                  |
| <span data-ttu-id="a8bc0-304">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-304">Minimum system</span></span> | <span data-ttu-id="a8bc0-305">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8bc0-305">Windows Server 2003</span></span>                                                                   |



 

### <a name="name"></a><span data-ttu-id="a8bc0-306">Имя</span><span class="sxs-lookup"><span data-stu-id="a8bc0-306">Name</span></span>



| <span data-ttu-id="a8bc0-307">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-307">Entry</span></span> | <span data-ttu-id="a8bc0-308">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-308">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-309">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-309">Description</span></span>    | <span data-ttu-id="a8bc0-310">Имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-310">The name of the computer.</span></span> <span data-ttu-id="a8bc0-311">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-311">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a8bc0-312">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-312">Access</span></span>         | <span data-ttu-id="a8bc0-313">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="a8bc0-313">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a8bc0-314">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-314">Type</span></span>           | <span data-ttu-id="a8bc0-315">Строка</span><span class="sxs-lookup"><span data-stu-id="a8bc0-315">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a8bc0-316">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-316">Default</span></span>        | <span data-ttu-id="a8bc0-317">"Мой компьютер"</span><span class="sxs-lookup"><span data-stu-id="a8bc0-317">"My Computer"</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a8bc0-318">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-318">Minimum system</span></span> | <span data-ttu-id="a8bc0-319">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-319">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a><span data-ttu-id="a8bc0-320">OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a8bc0-320">OperatingSystem</span></span>



| <span data-ttu-id="a8bc0-321">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-321">Entry</span></span> | <span data-ttu-id="a8bc0-322">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-322">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-323">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-323">Description</span></span>    | <span data-ttu-id="a8bc0-324">Операционная система, установленная на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-324">The operating system installed on the local computer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a8bc0-325">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-325">Access</span></span>         | <span data-ttu-id="a8bc0-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a8bc0-327">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-327">Type</span></span>           | <span data-ttu-id="a8bc0-328">Длинные возможные значения: Комадминоснотинитиализед (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) комадминосункновн (6) комадминосвиндовскспперсонал (11) комадминосвиндовсксппрофессионал (12) COMAdminOSWindowsNETStandardServer (13) COMAdminOSWindowsNETEnterpriseServer (14) COMAdminOSWindowsNETDatacenterServer (15) COMAdminOSWindowsNETWebServer (16)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-328">Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3\_1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknown (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16)</span></span> |
| <span data-ttu-id="a8bc0-329">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-329">Default</span></span>        | <span data-ttu-id="a8bc0-330">Комадминоснотинитиализед (0)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-330">COMAdminOSNotInitialized (0)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="a8bc0-331">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-331">Minimum system</span></span> | <span data-ttu-id="a8bc0-332">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-332">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a><span data-ttu-id="a8bc0-333">партитионсенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-333">PartitionsEnabled</span></span>



| <span data-ttu-id="a8bc0-334">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-334">Entry</span></span> | <span data-ttu-id="a8bc0-335">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-335">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-336">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-336">Description</span></span>    | <span data-ttu-id="a8bc0-337">Указывает, можно ли использовать разделы COM+ на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-337">Indicates whether COM+ partitions can be used on the local computer.</span></span> <span data-ttu-id="a8bc0-338">Если это свойство имеет значение false, то любая попытка использовать секции COM+ приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-338">If this property is False, any attempt to use COM+ partitions results in an error.</span></span> |
| <span data-ttu-id="a8bc0-339">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-339">Access</span></span>         | <span data-ttu-id="a8bc0-340">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-340">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="a8bc0-341">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-341">Type</span></span>           | <span data-ttu-id="a8bc0-342">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-342">Bool</span></span>                                                                                                                                                    |
| <span data-ttu-id="a8bc0-343">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-343">Default</span></span>        | <span data-ttu-id="a8bc0-344">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8bc0-344">False</span></span>                                                                                                                                                   |
| <span data-ttu-id="a8bc0-345">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-345">Minimum system</span></span> | <span data-ttu-id="a8bc0-346">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8bc0-346">Windows Server 2003</span></span>                                                                                                                                     |



 

### <a name="ports"></a><span data-ttu-id="a8bc0-347">Порты</span><span class="sxs-lookup"><span data-stu-id="a8bc0-347">Ports</span></span>



| <span data-ttu-id="a8bc0-348">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-348">Entry</span></span> | <span data-ttu-id="a8bc0-349">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-349">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-350">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-350">Description</span></span>    | <span data-ttu-id="a8bc0-351">Строка, описывающая порты, предназначенные для использования в Интернете или в интрасети, в зависимости от свойства Интернетпортслистед; Например, "500-599:600-800".</span><span class="sxs-lookup"><span data-stu-id="a8bc0-351">A string describing ports that are for either Internet or intranet use, depending on the InternetPortsListed property; for example, "500-599: 600-800".</span></span> |
| <span data-ttu-id="a8bc0-352">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-352">Access</span></span>         | <span data-ttu-id="a8bc0-353">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-353">ReadWrite</span></span>                                                                                                                                               |
| <span data-ttu-id="a8bc0-354">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-354">Type</span></span>           | <span data-ttu-id="a8bc0-355">Строка</span><span class="sxs-lookup"><span data-stu-id="a8bc0-355">String</span></span>                                                                                                                                                  |
| <span data-ttu-id="a8bc0-356">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-356">Default</span></span>        | <span data-ttu-id="a8bc0-357">""</span><span class="sxs-lookup"><span data-stu-id="a8bc0-357">""</span></span>                                                                                                                                                      |
| <span data-ttu-id="a8bc0-358">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-358">Minimum system</span></span> | <span data-ttu-id="a8bc0-359">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-359">Windows 2000</span></span>                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a><span data-ttu-id="a8bc0-360">ресаурцепулинженаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-360">ResourcePoolingEnabled</span></span>



| <span data-ttu-id="a8bc0-361">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-361">Entry</span></span> | <span data-ttu-id="a8bc0-362">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-362">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="a8bc0-363">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-363">Description</span></span>    | <span data-ttu-id="a8bc0-364">Включает использование распределителя ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-364">Enables use of resource dispensers.</span></span> |
| <span data-ttu-id="a8bc0-365">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-365">Access</span></span>         | <span data-ttu-id="a8bc0-366">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-366">ReadWrite</span></span>                           |
| <span data-ttu-id="a8bc0-367">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-367">Type</span></span>           | <span data-ttu-id="a8bc0-368">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-368">Bool</span></span>                                |
| <span data-ttu-id="a8bc0-369">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-369">Default</span></span>        | <span data-ttu-id="a8bc0-370">True</span><span class="sxs-lookup"><span data-stu-id="a8bc0-370">True</span></span>                                |
| <span data-ttu-id="a8bc0-371">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-371">Minimum system</span></span> | <span data-ttu-id="a8bc0-372">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-372">Windows 2000</span></span>                        |



 

### <a name="rpcproxyenabled"></a><span data-ttu-id="a8bc0-373">рпкпроксенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-373">RPCProxyEnabled</span></span>



| <span data-ttu-id="a8bc0-374">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-374">Entry</span></span> | <span data-ttu-id="a8bc0-375">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-375">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-376">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-376">Description</span></span>    | <span data-ttu-id="a8bc0-377">Определяет, включен ли прокси-сервер RPC IIS.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-377">Controls whether the RPC IIS proxy is enabled.</span></span> <span data-ttu-id="a8bc0-378">Прокси-сервер RPC IIS используется вместе со службами IIS для переадресации вызовов механизма RPC из служб IIS и является одним из основных компонентов Интернет-служб COM, которые включены путем установки Цисенаблед в значение true.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-378">The RPC IIS proxy is used in conjunction with IIS to forward calls to the RPC mechanism from IIS and is one of the core pieces of COM Internet Services, which is enabled by setting CISEnabled to True.</span></span> <span data-ttu-id="a8bc0-379">Дополнительные сведения о Рпкпроксенаблед см. в разделе [безопасность RPC HTTP](/windows/desktop/Rpc/rpc-over-http-security).</span><span class="sxs-lookup"><span data-stu-id="a8bc0-379">For more information on RPCProxyEnabled, see [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security).</span></span> |
| <span data-ttu-id="a8bc0-380">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-380">Access</span></span>         | <span data-ttu-id="a8bc0-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-381">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="a8bc0-382">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-382">Type</span></span>           | <span data-ttu-id="a8bc0-383">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-383">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a8bc0-384">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-384">Default</span></span>        | <span data-ttu-id="a8bc0-385">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8bc0-385">False</span></span>                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a8bc0-386">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-386">Minimum system</span></span> | <span data-ttu-id="a8bc0-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-387">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a><span data-ttu-id="a8bc0-388">секуререференцесенаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-388">SecureReferencesEnabled</span></span>



| <span data-ttu-id="a8bc0-389">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-389">Entry</span></span> | <span data-ttu-id="a8bc0-390">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-391">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-391">Description</span></span>    | <span data-ttu-id="a8bc0-392">Обеспечивает защиту на компьютерах DCOM, которые являются безопасными между процессами в методах [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) и [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="a8bc0-392">Enforces in DCOM computers that cross-process calls to [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods are secured.</span></span> |
| <span data-ttu-id="a8bc0-393">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-393">Access</span></span>         | <span data-ttu-id="a8bc0-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-394">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="a8bc0-395">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-395">Type</span></span>           | <span data-ttu-id="a8bc0-396">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-396">Bool</span></span>                                                                                                                                                                      |
| <span data-ttu-id="a8bc0-397">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-397">Default</span></span>        | <span data-ttu-id="a8bc0-398">Неверно</span><span class="sxs-lookup"><span data-stu-id="a8bc0-398">False</span></span>                                                                                                                                                                     |
| <span data-ttu-id="a8bc0-399">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-399">Minimum system</span></span> | <span data-ttu-id="a8bc0-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-400">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a><span data-ttu-id="a8bc0-401">секурититраккинженаблед</span><span class="sxs-lookup"><span data-stu-id="a8bc0-401">SecurityTrackingEnabled</span></span>



| <span data-ttu-id="a8bc0-402">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-402">Entry</span></span> | <span data-ttu-id="a8bc0-403">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-403">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="a8bc0-404">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-404">Description</span></span>    | <span data-ttu-id="a8bc0-405">Задайте значение true, если включено отслеживание безопасности для объектов.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-405">Set to True if security tracking is enabled on objects.</span></span> |
| <span data-ttu-id="a8bc0-406">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-406">Access</span></span>         | <span data-ttu-id="a8bc0-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-407">ReadWrite</span></span>                                               |
| <span data-ttu-id="a8bc0-408">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-408">Type</span></span>           | <span data-ttu-id="a8bc0-409">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-409">Bool</span></span>                                                    |
| <span data-ttu-id="a8bc0-410">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-410">Default</span></span>        | <span data-ttu-id="a8bc0-411">True</span><span class="sxs-lookup"><span data-stu-id="a8bc0-411">True</span></span>                                                    |
| <span data-ttu-id="a8bc0-412">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-412">Minimum system</span></span> | <span data-ttu-id="a8bc0-413">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-413">Windows 2000</span></span>                                            |



 

### <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="a8bc0-414">српактиватеасактиваторчеккс</span><span class="sxs-lookup"><span data-stu-id="a8bc0-414">SRPActivateAsActivatorChecks</span></span>



| <span data-ttu-id="a8bc0-415">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-415">Entry</span></span> | <span data-ttu-id="a8bc0-416">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-416">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-417">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-417">Description</span></span>    | <span data-ttu-id="a8bc0-418">Определяет, каким образом политика ограниченного использования программ (SRP) обрабатывает подключения активатора.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-418">Determines how the software restriction policy (SRP) handles activate-as-activator connections.</span></span> <span data-ttu-id="a8bc0-419">Если задано значение true, то уровень доверия SRP, настроенный для объекта сервера, сравнивается с уровнем доверия SRP объекта клиента, а уровень доверия выше (более строгий) используется для запуска объекта сервера.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-419">If set to True, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and the higher (more stringent) trust level is used to run the server object.</span></span> <span data-ttu-id="a8bc0-420">Если задано значение false, объект сервера выполняется с уровнем доверия SRP объекта клиента независимо от уровня доверия SRP, с которым настроен сервер.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-420">If set to False, the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which the server is configured.</span></span> |
| <span data-ttu-id="a8bc0-421">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-421">Access</span></span>         | <span data-ttu-id="a8bc0-422">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-422">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a8bc0-423">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-423">Type</span></span>           | <span data-ttu-id="a8bc0-424">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-424">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a8bc0-425">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-425">Default</span></span>        | <span data-ttu-id="a8bc0-426">True</span><span class="sxs-lookup"><span data-stu-id="a8bc0-426">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a8bc0-427">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-427">Minimum system</span></span> | <span data-ttu-id="a8bc0-428">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8bc0-428">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a><span data-ttu-id="a8bc0-429">српруннингобжектчеккс</span><span class="sxs-lookup"><span data-stu-id="a8bc0-429">SRPRunningObjectChecks</span></span>



| <span data-ttu-id="a8bc0-430">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-430">Entry</span></span> | <span data-ttu-id="a8bc0-431">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-431">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-432">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-432">Description</span></span>    | <span data-ttu-id="a8bc0-433">Определяет, каким способом политика ограниченного использования программ (SRP) обрабатывает попытки подключения к существующим процессам.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-433">Determines how the software restriction policy (SRP) handles attempted connections to existing processes.</span></span> <span data-ttu-id="a8bc0-434">Если задано значение false, попытки подключения к работающим объектам не проверяются на наличие соответствующих уровней доверия SRP.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-434">If set to False, attempts to connect to running objects are not checked for appropriate SRP trust levels.</span></span> <span data-ttu-id="a8bc0-435">Если задано значение true, то выполняемый объект должен иметь уровень доверия "равный" или выше (более строгий) SRP, чем объект клиента.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-435">If set to True, the running object must have an equal or higher (more stringent) SRP trust level than the client object.</span></span> <span data-ttu-id="a8bc0-436">Например, клиентский объект с неограниченным уровнем доверия SRP не может подключиться к выполняющемуся объекту с недопустимым уровнем доверия SRP.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-436">For example, a client object with an Unrestricted SRP trust level cannot connect to a running object with a Disallowed SRP trust level.</span></span> |
| <span data-ttu-id="a8bc0-437">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-437">Access</span></span>         | <span data-ttu-id="a8bc0-438">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-438">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a8bc0-439">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-439">Type</span></span>           | <span data-ttu-id="a8bc0-440">Bool</span><span class="sxs-lookup"><span data-stu-id="a8bc0-440">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a8bc0-441">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-441">Default</span></span>        | <span data-ttu-id="a8bc0-442">True</span><span class="sxs-lookup"><span data-stu-id="a8bc0-442">True</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="a8bc0-443">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-443">Minimum system</span></span> | <span data-ttu-id="a8bc0-444">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a8bc0-444">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a><span data-ttu-id="a8bc0-445">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="a8bc0-445">TransactionTimeout</span></span>



| <span data-ttu-id="a8bc0-446">Ввод</span><span class="sxs-lookup"><span data-stu-id="a8bc0-446">Entry</span></span> | <span data-ttu-id="a8bc0-447">Значение</span><span class="sxs-lookup"><span data-stu-id="a8bc0-447">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8bc0-448">Описание</span><span class="sxs-lookup"><span data-stu-id="a8bc0-448">Description</span></span>    | <span data-ttu-id="a8bc0-449">При выполнении множества операций в рамках транзакции необходимо задать достаточное значение в секундах.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-449">Should be set to a sufficient value in seconds if you are doing numerous operations within a transaction.</span></span> <span data-ttu-id="a8bc0-450">Время ожидания по умолчанию составляет 60 секунд, а максимальное время ожидания составляет 3600 секунд (1 час).</span><span class="sxs-lookup"><span data-stu-id="a8bc0-450">The default time-out period is 60 seconds, and the maximum time-out period is 3600 seconds (1 hour).</span></span> <span data-ttu-id="a8bc0-451">Если задать для этого свойства значение 0, время ожидания транзакции будет отключено.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-451">Setting this property to 0 disables transaction time-outs.</span></span> <span data-ttu-id="a8bc0-452">Это свойство может быть переопределено отдельными компонентами с помощью свойства Компоненттрансактионтимеаут коллекции [**Components**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="a8bc0-452">This property can be overridden by individual components by using the ComponentTransactionTimeout property of the [**Components**](components.md) collection.</span></span> |
| <span data-ttu-id="a8bc0-453">Access</span><span class="sxs-lookup"><span data-stu-id="a8bc0-453">Access</span></span>         | <span data-ttu-id="a8bc0-454">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a8bc0-454">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="a8bc0-455">Тип</span><span class="sxs-lookup"><span data-stu-id="a8bc0-455">Type</span></span>           | <span data-ttu-id="a8bc0-456">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="a8bc0-456">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a8bc0-457">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a8bc0-457">Default</span></span>        | <span data-ttu-id="a8bc0-458">60</span><span class="sxs-lookup"><span data-stu-id="a8bc0-458">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a8bc0-459">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="a8bc0-459">Minimum system</span></span> | <span data-ttu-id="a8bc0-460">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a8bc0-460">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a><span data-ttu-id="a8bc0-461">Пример</span><span class="sxs-lookup"><span data-stu-id="a8bc0-461">Example</span></span>

<span data-ttu-id="a8bc0-462">В следующем примере Microsoft Visual Basic показано, как подключиться к удаленному компьютеру и получить его свойство Секурититраккинженаблед с помощью коллекции **локалкомпутер** удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-462">The following Microsoft Visual Basic example demonstrates how to connect to a remote computer and get its SecurityTrackingEnabled property by using the **LocalComputer** collection of the remote computer.</span></span> <span data-ttu-id="a8bc0-463">Чтобы использовать этот пример, добавьте библиотеку типов администрирования COM+ в качестве ссылки на проект Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-463">To use this example, add the COM+ Admin Type Library as a reference to your Visual Basic project.</span></span>


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



<span data-ttu-id="a8bc0-464">Чтобы использовать функцию, укажите строковое значение для имени удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-464">To use the function, provide a string value for the name of the remote computer.</span></span> <span data-ttu-id="a8bc0-465">В следующем Visual Basic коде показано, как подключиться к компьютеру с именем Имя_удаленного_компьютера.</span><span class="sxs-lookup"><span data-stu-id="a8bc0-465">The following Visual Basic code shows how to connect to the computer named "RemoteComputerName".</span></span>


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a><span data-ttu-id="a8bc0-466">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8bc0-466">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8bc0-467">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="a8bc0-467">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
