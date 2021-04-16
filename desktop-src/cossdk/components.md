---
description: Содержит объект для каждого компонента в связанном приложении.
ms.assetid: f502ba60-b2b1-4556-8f91-22a474e60e0d
title: Коллекция Components
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Components
api_type:
- COM
api_location: ''
ms.openlocfilehash: f68013985beff427b5681c5b78c2c00df9e69263
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539314"
---
# <a name="components-collection"></a><span data-ttu-id="8f223-103">Коллекция Components</span><span class="sxs-lookup"><span data-stu-id="8f223-103">Components collection</span></span>

<span data-ttu-id="8f223-104">Содержит объект для каждого компонента в связанном приложении.</span><span class="sxs-lookup"><span data-stu-id="8f223-104">Contains an object for each component in the related application.</span></span> <span data-ttu-id="8f223-105">Коллекция **Components** всегда связана с объектом в коллекции [**приложений**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="8f223-105">The **Components** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="8f223-106">Свойства, предоставляемые этими объектами, сохраняют параметры, сделанные на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-106">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="8f223-107">Эта коллекция поддерживает метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , но не метод [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="8f223-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="8f223-108">Чтобы установить или импортировать компоненты в приложение, используйте методы для объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="8f223-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="8f223-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="8f223-109">Members</span></span>

<span data-ttu-id="8f223-110">Коллекция **Components** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="8f223-110">The **Components** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="8f223-111">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="8f223-111">Related Collections</span></span>

<span data-ttu-id="8f223-112">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="8f223-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="8f223-113">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="8f223-113">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="8f223-114">**интерфацесфоркомпонент**</span><span class="sxs-lookup"><span data-stu-id="8f223-114">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)
-   [<span data-ttu-id="8f223-115">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8f223-115">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="8f223-116">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="8f223-116">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="8f223-117">**ролесфоркомпонент**</span><span class="sxs-lookup"><span data-stu-id="8f223-117">**RolesForComponent**</span></span>](rolesforcomponent.md)
-   [<span data-ttu-id="8f223-118">**субскриптионсфоркомпонент**</span><span class="sxs-lookup"><span data-stu-id="8f223-118">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

<span data-ttu-id="8f223-119">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="8f223-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="8f223-120">**Приложения**</span><span class="sxs-lookup"><span data-stu-id="8f223-120">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="8f223-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f223-121">Properties</span></span>

<span data-ttu-id="8f223-122">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="8f223-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="8f223-123">алловинпроксубскриберс</span><span class="sxs-lookup"><span data-stu-id="8f223-123">AllowInprocSubscribers</span></span>](#allowinprocsubscribers)
-   [<span data-ttu-id="8f223-124">Кодов</span><span class="sxs-lookup"><span data-stu-id="8f223-124">ApplicationID</span></span>](#applicationid)
-   [<span data-ttu-id="8f223-125">Разрядность</span><span class="sxs-lookup"><span data-stu-id="8f223-125">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="8f223-126">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="8f223-126">CLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="8f223-127">компонентакцессчекксенаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-127">ComponentAccessChecksEnabled</span></span>](#componentaccesschecksenabled)
-   [<span data-ttu-id="8f223-128">компоненттрансактионтимеаут</span><span class="sxs-lookup"><span data-stu-id="8f223-128">ComponentTransactionTimeout</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="8f223-129">компоненттрансактионтимеаутенаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-129">ComponentTransactionTimeoutEnabled</span></span>](#componenttransactiontimeoutenabled)
-   [<span data-ttu-id="8f223-130">комтиинтринсикс</span><span class="sxs-lookup"><span data-stu-id="8f223-130">COMTIIntrinsics</span></span>](#comtiintrinsics)
-   [<span data-ttu-id="8f223-131">конструктионенаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-131">ConstructionEnabled</span></span>](#constructionenabled)
-   [<span data-ttu-id="8f223-132">конструкторстринг</span><span class="sxs-lookup"><span data-stu-id="8f223-132">ConstructorString</span></span>](#constructorstring)
-   [<span data-ttu-id="8f223-133">креатионтимеаут</span><span class="sxs-lookup"><span data-stu-id="8f223-133">CreationTimeout</span></span>](#creationtimeout)
-   [<span data-ttu-id="8f223-134">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-134">Description</span></span>](#description)
-   [<span data-ttu-id="8f223-135">КОМПОНОВКИ</span><span class="sxs-lookup"><span data-stu-id="8f223-135">DLL</span></span>](#dll)
-   [<span data-ttu-id="8f223-136">евенттраккинженаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-136">EventTrackingEnabled</span></span>](#eventtrackingenabled)
-   [<span data-ttu-id="8f223-137">ексцептионкласс</span><span class="sxs-lookup"><span data-stu-id="8f223-137">ExceptionClass</span></span>](#exceptionclass)
-   [<span data-ttu-id="8f223-138">фиреинпараллел</span><span class="sxs-lookup"><span data-stu-id="8f223-138">FireInParallel</span></span>](#fireinparallel)
-   [<span data-ttu-id="8f223-139">иисинтринсикс</span><span class="sxs-lookup"><span data-stu-id="8f223-139">IISIntrinsics</span></span>](#iisintrinsics)
-   [<span data-ttu-id="8f223-140">инитиализесервераппликатион</span><span class="sxs-lookup"><span data-stu-id="8f223-140">InitializeServerApplication</span></span>](#initializeserverapplication)
-   [<span data-ttu-id="8f223-141">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="8f223-141">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="8f223-142">исевенткласс</span><span class="sxs-lookup"><span data-stu-id="8f223-142">IsEventClass</span></span>](#iseventclass)
-   [<span data-ttu-id="8f223-143">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="8f223-143">IsInstalled</span></span>](#isinstalled)
-   [<span data-ttu-id="8f223-144">исприватекомпонент</span><span class="sxs-lookup"><span data-stu-id="8f223-144">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="8f223-145">жустинтимеактиватион</span><span class="sxs-lookup"><span data-stu-id="8f223-145">JustInTimeActivation</span></span>](#justintimeactivation)
-   [<span data-ttu-id="8f223-146">лоадбаланЦингсуппортед</span><span class="sxs-lookup"><span data-stu-id="8f223-146">LoadBalancingSupported</span></span>](#loadbalancingsupported)
-   [<span data-ttu-id="8f223-147">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="8f223-147">MaxPoolSize</span></span>](#maxpoolsize)
-   [<span data-ttu-id="8f223-148">минпулсизе</span><span class="sxs-lookup"><span data-stu-id="8f223-148">MinPoolSize</span></span>](#minpoolsize)
-   [<span data-ttu-id="8f223-149">мултиинтерфацепублишерфилтерклсид</span><span class="sxs-lookup"><span data-stu-id="8f223-149">MultiInterfacePublisherFilterCLSID</span></span>](#multiinterfacepublisherfilterclsid)
-   [<span data-ttu-id="8f223-150">муструнинклиентконтекст</span><span class="sxs-lookup"><span data-stu-id="8f223-150">MustRunInClientContext</span></span>](#mustruninclientcontext)
-   [<span data-ttu-id="8f223-151">муструниндефаултконтекст</span><span class="sxs-lookup"><span data-stu-id="8f223-151">MustRunInDefaultContext</span></span>](#mustrunindefaultcontext)
-   [<span data-ttu-id="8f223-152">обжектпулинженаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-152">ObjectPoolingEnabled</span></span>](#objectpoolingenabled)
-   [<span data-ttu-id="8f223-153">ProgID:</span><span class="sxs-lookup"><span data-stu-id="8f223-153">ProgID</span></span>](#progid)
-   [<span data-ttu-id="8f223-154">PublisherID</span><span class="sxs-lookup"><span data-stu-id="8f223-154">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="8f223-155">соапассемблинаме</span><span class="sxs-lookup"><span data-stu-id="8f223-155">SoapAssemblyName</span></span>](#soapassemblyname)
-   [<span data-ttu-id="8f223-156">соаптипенаме</span><span class="sxs-lookup"><span data-stu-id="8f223-156">SoapTypeName</span></span>](#soaptypename)
-   [<span data-ttu-id="8f223-157">Синхронизация</span><span class="sxs-lookup"><span data-stu-id="8f223-157">Synchronization</span></span>](#synchronization)
-   [<span data-ttu-id="8f223-158">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="8f223-158">ThreadingModel</span></span>](#threadingmodel)
-   [<span data-ttu-id="8f223-159">Транзакция</span><span class="sxs-lookup"><span data-stu-id="8f223-159">Transaction</span></span>](#componenttransactiontimeout)
-   [<span data-ttu-id="8f223-160">тксисолатионлевел</span><span class="sxs-lookup"><span data-stu-id="8f223-160">TxIsolationLevel</span></span>](#txisolationlevel)
-   [<span data-ttu-id="8f223-161">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="8f223-161">VersionBuild</span></span>](#versionbuild)
-   [<span data-ttu-id="8f223-162">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="8f223-162">VersionMajor</span></span>](#versionmajor)
-   [<span data-ttu-id="8f223-163">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="8f223-163">VersionMinor</span></span>](#versionminor)
-   [<span data-ttu-id="8f223-164">версионсуббуилд</span><span class="sxs-lookup"><span data-stu-id="8f223-164">VersionSubBuild</span></span>](#versionsubbuild)

### <a name="allowinprocsubscribers"></a><span data-ttu-id="8f223-165">алловинпроксубскриберс</span><span class="sxs-lookup"><span data-stu-id="8f223-165">AllowInprocSubscribers</span></span>



| <span data-ttu-id="8f223-166">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-166">Entry</span></span> | <span data-ttu-id="8f223-167">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-167">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="8f223-168">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-168">Description</span></span>    | <span data-ttu-id="8f223-169">Включает в процесс подписчиков, если компонент является классом событий.</span><span class="sxs-lookup"><span data-stu-id="8f223-169">Enables in process subscribers if the component is an event class.</span></span> |
| <span data-ttu-id="8f223-170">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-170">Access</span></span>         | <span data-ttu-id="8f223-171">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-171">ReadWrite</span></span>                                                          |
| <span data-ttu-id="8f223-172">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-172">Type</span></span>           | <span data-ttu-id="8f223-173">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-173">Bool</span></span>                                                               |
| <span data-ttu-id="8f223-174">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-174">Default</span></span>        | <span data-ttu-id="8f223-175">True</span><span class="sxs-lookup"><span data-stu-id="8f223-175">True</span></span>                                                               |
| <span data-ttu-id="8f223-176">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-176">Minimum system</span></span> | <span data-ttu-id="8f223-177">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-177">Windows 2000</span></span>                                                       |



 

### <a name="applicationid"></a><span data-ttu-id="8f223-178">ApplicationID</span><span class="sxs-lookup"><span data-stu-id="8f223-178">ApplicationID</span></span>



| <span data-ttu-id="8f223-179">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-179">Entry</span></span> | <span data-ttu-id="8f223-180">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-180">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-181">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-181">Description</span></span>    | <span data-ttu-id="8f223-182">Идентификатор GUID для приложения, содержащего компонент.</span><span class="sxs-lookup"><span data-stu-id="8f223-182">The GUID for the application containing the component.</span></span> <span data-ttu-id="8f223-183">Должен быть допустимым идентификатором GUID приложения, который проверяется перед вызовом [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="8f223-183">Must be a valid application's GUID, which is verified before [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) is called.</span></span> <span data-ttu-id="8f223-184">Если это значение изменено на GUID для другого приложения, компонент перемещается в это приложение.</span><span class="sxs-lookup"><span data-stu-id="8f223-184">If this value is changed to be a GUID for a different application, the component moves to that application.</span></span> |
| <span data-ttu-id="8f223-185">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-185">Access</span></span>         | <span data-ttu-id="8f223-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-186">ReadWrite</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="8f223-187">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-187">Type</span></span>           | <span data-ttu-id="8f223-188">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-188">String</span></span>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8f223-189">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-189">Default</span></span>        | <span data-ttu-id="8f223-190">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f223-190">N/A</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8f223-191">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-191">Minimum system</span></span> | <span data-ttu-id="8f223-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-192">Windows 2000</span></span>                                                                                                                                                                                                                                                                                     |



 

### <a name="bitness"></a><span data-ttu-id="8f223-193">Разрядность</span><span class="sxs-lookup"><span data-stu-id="8f223-193">Bitness</span></span>



| <span data-ttu-id="8f223-194">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-194">Entry</span></span> | <span data-ttu-id="8f223-195">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-195">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-196">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-196">Description</span></span>    | <span data-ttu-id="8f223-197">Представляет двоичный тип разрядности компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-197">Represents the binary bitness type of a component.</span></span> <span data-ttu-id="8f223-198">В системах, использующих 64-разрядную версию Windows, это свойство различает 64-разрядные компоненты и 32-разрядные компоненты.</span><span class="sxs-lookup"><span data-stu-id="8f223-198">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="8f223-199">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-199">Access</span></span>         | <span data-ttu-id="8f223-200">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-200">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="8f223-201">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-201">Type</span></span>           | <span data-ttu-id="8f223-202">Длинные возможные значения: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="8f223-202">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                       |
| <span data-ttu-id="8f223-203">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-203">Default</span></span>        | <span data-ttu-id="8f223-204">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f223-204">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="8f223-205">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-205">Minimum system</span></span> | <span data-ttu-id="8f223-206">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f223-206">Windows XP</span></span>                                                                                                                                                          |



 

### <a name="clsid"></a><span data-ttu-id="8f223-207">CLSID</span><span class="sxs-lookup"><span data-stu-id="8f223-207">CLSID</span></span>



| <span data-ttu-id="8f223-208">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-208">Entry</span></span> | <span data-ttu-id="8f223-209">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-209">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-210">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-210">Description</span></span>    | <span data-ttu-id="8f223-211">Идентификатор GUID для компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-211">A GUID for the component.</span></span> <span data-ttu-id="8f223-212">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="8f223-212">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8f223-213">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-213">Access</span></span>         | <span data-ttu-id="8f223-214">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-214">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="8f223-215">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-215">Type</span></span>           | <span data-ttu-id="8f223-216">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-216">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="8f223-217">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-217">Default</span></span>        | <span data-ttu-id="8f223-218">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f223-218">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="8f223-219">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-219">Minimum system</span></span> | <span data-ttu-id="8f223-220">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-220">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="componentaccesschecksenabled"></a><span data-ttu-id="8f223-221">компонентакцессчекксенаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-221">ComponentAccessChecksEnabled</span></span>



| <span data-ttu-id="8f223-222">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-222">Entry</span></span> | <span data-ttu-id="8f223-223">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-223">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-224">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-224">Description</span></span>    | <span data-ttu-id="8f223-225">Указывает, выполняются ли проверки доступа на основе ролей при вызовах компонента и работают в сочетании со свойствами Акцессчеккслевел и Аппликатионакцессчекксенаблед в приложении.</span><span class="sxs-lookup"><span data-stu-id="8f223-225">Indicates whether role-based access checks are performed on calls into the component and works in conjunction with the AccessChecksLevel and ApplicationAccessChecksEnabled properties on the application.</span></span> |
| <span data-ttu-id="8f223-226">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-226">Access</span></span>         | <span data-ttu-id="8f223-227">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-227">ReadWrite</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="8f223-228">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-228">Type</span></span>           | <span data-ttu-id="8f223-229">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-229">Bool</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="8f223-230">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-230">Default</span></span>        | <span data-ttu-id="8f223-231">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-231">False</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="8f223-232">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-232">Minimum system</span></span> | <span data-ttu-id="8f223-233">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-233">Windows 2000</span></span>                                                                                                                                                                                               |



 

### <a name="componenttransactiontimeout"></a><span data-ttu-id="8f223-234">компоненттрансактионтимеаут</span><span class="sxs-lookup"><span data-stu-id="8f223-234">ComponentTransactionTimeout</span></span>



| <span data-ttu-id="8f223-235">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-235">Entry</span></span> | <span data-ttu-id="8f223-236">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-236">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-237">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-237">Description</span></span>    | <span data-ttu-id="8f223-238">При использовании в транзакции указывает период времени, в течение которого этот компонент вызывает тайм-аут транзакции. Значение по умолчанию составляет 60 секунд и не может быть длиннее 3600 секунд (1 час).</span><span class="sxs-lookup"><span data-stu-id="8f223-238">When used in a transaction, specifies the time period in which this component causes the transaction to time out. The default is 60 seconds and cannot be longer than 3600 seconds (1 hour).</span></span> <span data-ttu-id="8f223-239">Значение времени ожидания можно задать равным 0, указав бесконечный период ожидания транзакции.</span><span class="sxs-lookup"><span data-stu-id="8f223-239">The time-out value can be set to 0, specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="8f223-240">Для использования этого свойства Компоненттрансактионтимеаутенаблед должно иметь значение true.</span><span class="sxs-lookup"><span data-stu-id="8f223-240">For this property to be used, ComponentTransactionTimeoutEnabled must be True.</span></span> <span data-ttu-id="8f223-241">Значение этого свойства переопределяет глобальное время ожидания транзакции, заданное свойством Трансактионтимеаут коллекции [**локалкомпутер**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="8f223-241">The value of this property overrides the global transaction time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection.</span></span> |
| <span data-ttu-id="8f223-242">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-242">Access</span></span>         | <span data-ttu-id="8f223-243">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-243">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="8f223-244">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-244">Type</span></span>           | <span data-ttu-id="8f223-245">Long (0-3600)</span><span class="sxs-lookup"><span data-stu-id="8f223-245">Long (0-3600)</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8f223-246">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-246">Default</span></span>        | <span data-ttu-id="8f223-247">60</span><span class="sxs-lookup"><span data-stu-id="8f223-247">60</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="8f223-248">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-248">Minimum system</span></span> | <span data-ttu-id="8f223-249">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-249">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="componenttransactiontimeoutenabled"></a><span data-ttu-id="8f223-250">компоненттрансактионтимеаутенаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-250">ComponentTransactionTimeoutEnabled</span></span>



| <span data-ttu-id="8f223-251">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-251">Entry</span></span> | <span data-ttu-id="8f223-252">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-252">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-253">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-253">Description</span></span>    | <span data-ttu-id="8f223-254">Указывает, включен ли период ожидания транзакции для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-254">Specifies whether the transaction time-out period is enabled for this component.</span></span> <span data-ttu-id="8f223-255">По умолчанию функция времени ожидания транзакции отключена.</span><span class="sxs-lookup"><span data-stu-id="8f223-255">By default, the transaction time-out feature is disabled.</span></span> <span data-ttu-id="8f223-256">Если это свойство имеет значение true, используется тайм-аут, заданный параметром Компоненттрансактионтимеаут.</span><span class="sxs-lookup"><span data-stu-id="8f223-256">When this property is True, the time-out specified by ComponentTransactionTimeout is used.</span></span> <span data-ttu-id="8f223-257">Если это свойство имеет значение false, используется тайм-аут, заданный свойством Трансактионтимеаут коллекции [**локалкомпутер**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="8f223-257">When this property is False, the time-out specified by the TransactionTimeout property of the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="8f223-258">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-258">Access</span></span>         | <span data-ttu-id="8f223-259">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-259">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="8f223-260">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-260">Type</span></span>           | <span data-ttu-id="8f223-261">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-261">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8f223-262">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-262">Default</span></span>        | <span data-ttu-id="8f223-263">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-263">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8f223-264">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-264">Minimum system</span></span> | <span data-ttu-id="8f223-265">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-265">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="comtiintrinsics"></a><span data-ttu-id="8f223-266">комтиинтринсикс</span><span class="sxs-lookup"><span data-stu-id="8f223-266">COMTIIntrinsics</span></span>



| <span data-ttu-id="8f223-267">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-267">Entry</span></span> | <span data-ttu-id="8f223-268">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-268">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-269">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-269">Description</span></span>    | <span data-ttu-id="8f223-270">Разрешает передачу свойств контекста из интегратора транзакций COM (COMTI) в контекст для этого класса.</span><span class="sxs-lookup"><span data-stu-id="8f223-270">Enables passing of context properties from the COM Transaction Integrator (COMTI) into the context for this class.</span></span> <span data-ttu-id="8f223-271">COMTI упрощает задачу упаковки транзакций мэйнфрейма и бизнес-логики в качестве компонентов COM.</span><span class="sxs-lookup"><span data-stu-id="8f223-271">The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.</span></span> |
| <span data-ttu-id="8f223-272">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-272">Access</span></span>         | <span data-ttu-id="8f223-273">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-273">ReadWrite</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="8f223-274">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-274">Type</span></span>           | <span data-ttu-id="8f223-275">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-275">Bool</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="8f223-276">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-276">Default</span></span>        | <span data-ttu-id="8f223-277">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-277">False</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="8f223-278">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-278">Minimum system</span></span> | <span data-ttu-id="8f223-279">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-279">Windows 2000</span></span>                                                                                                                                                                                                         |



 

### <a name="constructionenabled"></a><span data-ttu-id="8f223-280">конструктионенаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-280">ConstructionEnabled</span></span>



| <span data-ttu-id="8f223-281">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-281">Entry</span></span> | <span data-ttu-id="8f223-282">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-282">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-283">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-283">Description</span></span>    | <span data-ttu-id="8f223-284">Определяет, передается ли Конструкторстринг объекту при его создании.</span><span class="sxs-lookup"><span data-stu-id="8f223-284">Determines whether the ConstructorString is passed to the object when it is constructed.</span></span> |
| <span data-ttu-id="8f223-285">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-285">Access</span></span>         | <span data-ttu-id="8f223-286">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-286">ReadWrite</span></span>                                                                                |
| <span data-ttu-id="8f223-287">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-287">Type</span></span>           | <span data-ttu-id="8f223-288">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-288">Bool</span></span>                                                                                     |
| <span data-ttu-id="8f223-289">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-289">Default</span></span>        | <span data-ttu-id="8f223-290">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-290">False</span></span>                                                                                    |
| <span data-ttu-id="8f223-291">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-291">Minimum system</span></span> | <span data-ttu-id="8f223-292">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-292">Windows 2000</span></span>                                                                             |



 

### <a name="constructorstring"></a><span data-ttu-id="8f223-293">конструкторстринг</span><span class="sxs-lookup"><span data-stu-id="8f223-293">ConstructorString</span></span>



| <span data-ttu-id="8f223-294">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-294">Entry</span></span> | <span data-ttu-id="8f223-295">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-295">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-296">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-296">Description</span></span>    | <span data-ttu-id="8f223-297">Строка инициализации для создания компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-297">Initialization string for component construction.</span></span> <span data-ttu-id="8f223-298">С помощью строк конструктора объектов можно создавать различные объекты из одного и того же универсального компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-298">You can create different objects from the same generic component by using object constructor strings.</span></span> <span data-ttu-id="8f223-299">Если Конструктионенаблед имеет значение false, это свойство игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8f223-299">If ConstructionEnabled is False, this property is ignored.</span></span> |
| <span data-ttu-id="8f223-300">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-300">Access</span></span>         | <span data-ttu-id="8f223-301">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-301">ReadWrite</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="8f223-302">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-302">Type</span></span>           | <span data-ttu-id="8f223-303">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-303">String</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="8f223-304">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-304">Default</span></span>        | <span data-ttu-id="8f223-305">""</span><span class="sxs-lookup"><span data-stu-id="8f223-305">""</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="8f223-306">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-306">Minimum system</span></span> | <span data-ttu-id="8f223-307">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-307">Windows 2000</span></span>                                                                                                                                                                                                       |



 

### <a name="creationtimeout"></a><span data-ttu-id="8f223-308">креатионтимеаут</span><span class="sxs-lookup"><span data-stu-id="8f223-308">CreationTimeout</span></span>



| <span data-ttu-id="8f223-309">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-309">Entry</span></span> | <span data-ttu-id="8f223-310">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-310">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-311">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-311">Description</span></span>    | <span data-ttu-id="8f223-312">При создании объекта — число миллисекунд до возвращения ошибки времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="8f223-312">When creating the object, number of milliseconds before a time-out error is returned.</span></span> <span data-ttu-id="8f223-313">Максимальное время ожидания составляет 2147483647 миллисекунд (около 25 дней).</span><span class="sxs-lookup"><span data-stu-id="8f223-313">The maximum time-out is 2147483647 milliseconds (about 25 days).</span></span> |
| <span data-ttu-id="8f223-314">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-314">Access</span></span>         | <span data-ttu-id="8f223-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-315">ReadWrite</span></span>                                                                                                                                              |
| <span data-ttu-id="8f223-316">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-316">Type</span></span>           | <span data-ttu-id="8f223-317">Long (0-2147483647)</span><span class="sxs-lookup"><span data-stu-id="8f223-317">Long (0-2147483647)</span></span>                                                                                                                                    |
| <span data-ttu-id="8f223-318">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-318">Default</span></span>        | <span data-ttu-id="8f223-319">0</span><span class="sxs-lookup"><span data-stu-id="8f223-319">0</span></span>                                                                                                                                                      |
| <span data-ttu-id="8f223-320">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-320">Minimum system</span></span> | <span data-ttu-id="8f223-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-321">Windows 2000</span></span>                                                                                                                                           |



 

### <a name="description"></a><span data-ttu-id="8f223-322">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-322">Description</span></span>



| <span data-ttu-id="8f223-323">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-323">Entry</span></span> | <span data-ttu-id="8f223-324">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-324">Value</span></span> |
|----------------|--------------------------|
| <span data-ttu-id="8f223-325">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-325">Description</span></span>    | <span data-ttu-id="8f223-326">Описывает компонент.</span><span class="sxs-lookup"><span data-stu-id="8f223-326">Describes the component.</span></span> |
| <span data-ttu-id="8f223-327">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-327">Access</span></span>         | <span data-ttu-id="8f223-328">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-328">ReadWrite</span></span>                |
| <span data-ttu-id="8f223-329">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-329">Type</span></span>           | <span data-ttu-id="8f223-330">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-330">String</span></span>                   |
| <span data-ttu-id="8f223-331">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-331">Default</span></span>        | <span data-ttu-id="8f223-332">""</span><span class="sxs-lookup"><span data-stu-id="8f223-332">""</span></span>                       |
| <span data-ttu-id="8f223-333">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-333">Minimum system</span></span> | <span data-ttu-id="8f223-334">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-334">Windows 2000</span></span>             |



 

### <a name="dll"></a><span data-ttu-id="8f223-335">DLL</span><span class="sxs-lookup"><span data-stu-id="8f223-335">DLL</span></span>



| <span data-ttu-id="8f223-336">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-336">Entry</span></span> | <span data-ttu-id="8f223-337">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-337">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="8f223-338">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-338">Description</span></span>    | <span data-ttu-id="8f223-339">Имя и путь к файлу, содержащему компонент.</span><span class="sxs-lookup"><span data-stu-id="8f223-339">The name and path of the file containing the component.</span></span> |
| <span data-ttu-id="8f223-340">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-340">Access</span></span>         | <span data-ttu-id="8f223-341">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-341">ReadOnly</span></span>                                                |
| <span data-ttu-id="8f223-342">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-342">Type</span></span>           | <span data-ttu-id="8f223-343">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-343">String</span></span>                                                  |
| <span data-ttu-id="8f223-344">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-344">Default</span></span>        | <span data-ttu-id="8f223-345">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f223-345">N/A</span></span>                                                     |
| <span data-ttu-id="8f223-346">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-346">Minimum system</span></span> | <span data-ttu-id="8f223-347">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-347">Windows 2000</span></span>                                            |



 

### <a name="eventtrackingenabled"></a><span data-ttu-id="8f223-348">евенттраккинженаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-348">EventTrackingEnabled</span></span>



| <span data-ttu-id="8f223-349">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-349">Entry</span></span> | <span data-ttu-id="8f223-350">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-350">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-351">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-351">Description</span></span>    | <span data-ttu-id="8f223-352">Определяет, выполняется ли трассировка событий.</span><span class="sxs-lookup"><span data-stu-id="8f223-352">Determines whether events are tracked.</span></span> <span data-ttu-id="8f223-353">События включают такие действия, как завершение работы приложения. Создание и освобождение объектов; ссылки на объект, согласованность, активация и деактивация; вызовы методов, возвраты и исключения; запуск транзакции, подготовка к фиксации и прерывание; подключение, выделение и повторное использование распределителя ресурсов; выделение и перезапуск потоков.</span><span class="sxs-lookup"><span data-stu-id="8f223-353">Events include actions such as application shutdown; object creation and release; object references, consistency, activation, and deactivation; method calls, returns, and exceptions; transaction startup, preparing to commit, and abort; resource dispenser connection, allocation, and recycling; thread allocation and recycling.</span></span> |
| <span data-ttu-id="8f223-354">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-354">Access</span></span>         | <span data-ttu-id="8f223-355">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-355">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="8f223-356">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-356">Type</span></span>           | <span data-ttu-id="8f223-357">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-357">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8f223-358">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-358">Default</span></span>        | <span data-ttu-id="8f223-359">True</span><span class="sxs-lookup"><span data-stu-id="8f223-359">True</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="8f223-360">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-360">Minimum system</span></span> | <span data-ttu-id="8f223-361">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-361">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="exceptionclass"></a><span data-ttu-id="8f223-362">ексцептионкласс</span><span class="sxs-lookup"><span data-stu-id="8f223-362">ExceptionClass</span></span>



| <span data-ttu-id="8f223-363">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-363">Entry</span></span> | <span data-ttu-id="8f223-364">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-364">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-365">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-365">Description</span></span>    | <span data-ttu-id="8f223-366">Идентификатор CLSID, который может быть идентификатором GUID или строкой моникера, для активации альтернативной программы в процессе работы с многократным сбоем программы очередей компонентов.</span><span class="sxs-lookup"><span data-stu-id="8f223-366">The CLSID, which can be a GUID or a moniker string, to activate an alternative program during the process of dealing with a repeatedly failing queued components program.</span></span> |
| <span data-ttu-id="8f223-367">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-367">Access</span></span>         | <span data-ttu-id="8f223-368">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-368">ReadWrite</span></span>                                                                                                                                                                 |
| <span data-ttu-id="8f223-369">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-369">Type</span></span>           | <span data-ttu-id="8f223-370">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-370">String</span></span>                                                                                                                                                                    |
| <span data-ttu-id="8f223-371">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-371">Default</span></span>        | <span data-ttu-id="8f223-372">""</span><span class="sxs-lookup"><span data-stu-id="8f223-372">""</span></span>                                                                                                                                                                        |
| <span data-ttu-id="8f223-373">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-373">Minimum system</span></span> | <span data-ttu-id="8f223-374">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-374">Windows 2000</span></span>                                                                                                                                                              |



 

### <a name="fireinparallel"></a><span data-ttu-id="8f223-375">фиреинпараллел</span><span class="sxs-lookup"><span data-stu-id="8f223-375">FireInParallel</span></span>



| <span data-ttu-id="8f223-376">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-376">Entry</span></span> | <span data-ttu-id="8f223-377">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-377">Value</span></span> |
|----------------|----------------------------------------------------------------------------|
| <span data-ttu-id="8f223-378">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-378">Description</span></span>    | <span data-ttu-id="8f223-379">Позволяет инициировать события параллельно, если компонент является классом событий.</span><span class="sxs-lookup"><span data-stu-id="8f223-379">Enables events to be fired in parallel if the component is an event class.</span></span> |
| <span data-ttu-id="8f223-380">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-380">Access</span></span>         | <span data-ttu-id="8f223-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-381">ReadWrite</span></span>                                                                  |
| <span data-ttu-id="8f223-382">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-382">Type</span></span>           | <span data-ttu-id="8f223-383">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-383">Bool</span></span>                                                                       |
| <span data-ttu-id="8f223-384">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-384">Default</span></span>        | <span data-ttu-id="8f223-385">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-385">False</span></span>                                                                      |
| <span data-ttu-id="8f223-386">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-386">Minimum system</span></span> | <span data-ttu-id="8f223-387">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-387">Windows 2000</span></span>                                                               |



 

### <a name="iisintrinsics"></a><span data-ttu-id="8f223-388">иисинтринсикс</span><span class="sxs-lookup"><span data-stu-id="8f223-388">IISIntrinsics</span></span>



| <span data-ttu-id="8f223-389">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-389">Entry</span></span> | <span data-ttu-id="8f223-390">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-391">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-391">Description</span></span>    | <span data-ttu-id="8f223-392">Включает передачу свойств контекста IIS, таких как объект сеанса приложения или объект сеанса пользователя, в контекст для этого класса.</span><span class="sxs-lookup"><span data-stu-id="8f223-392">Enables passing of IIS context properties, such as an application session object or a user session object, into the context for this class.</span></span> |
| <span data-ttu-id="8f223-393">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-393">Access</span></span>         | <span data-ttu-id="8f223-394">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-394">ReadWrite</span></span>                                                                                                                                   |
| <span data-ttu-id="8f223-395">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-395">Type</span></span>           | <span data-ttu-id="8f223-396">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-396">Bool</span></span>                                                                                                                                        |
| <span data-ttu-id="8f223-397">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-397">Default</span></span>        | <span data-ttu-id="8f223-398">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-398">False</span></span>                                                                                                                                       |
| <span data-ttu-id="8f223-399">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-399">Minimum system</span></span> | <span data-ttu-id="8f223-400">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-400">Windows 2000</span></span>                                                                                                                                |



 

### <a name="initializeserverapplication"></a><span data-ttu-id="8f223-401">инитиализесервераппликатион</span><span class="sxs-lookup"><span data-stu-id="8f223-401">InitializeServerApplication</span></span>



| <span data-ttu-id="8f223-402">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-402">Entry</span></span> | <span data-ttu-id="8f223-403">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-403">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8f223-404">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-404">Description</span></span>    | <span data-ttu-id="8f223-405">Указывает, используется ли компонент для инициализации серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="8f223-405">Indicates whether the component is used to initialize a server application.</span></span> |
| <span data-ttu-id="8f223-406">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-406">Access</span></span>         | <span data-ttu-id="8f223-407">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-407">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="8f223-408">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-408">Type</span></span>           | <span data-ttu-id="8f223-409">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-409">Bool</span></span>                                                                        |
| <span data-ttu-id="8f223-410">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-410">Default</span></span>        | <span data-ttu-id="8f223-411">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-411">False</span></span>                                                                       |
| <span data-ttu-id="8f223-412">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-412">Minimum system</span></span> | <span data-ttu-id="8f223-413">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f223-413">Windows Server 2003</span></span>                                                         |



 

### <a name="isenabled"></a><span data-ttu-id="8f223-414">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="8f223-414">IsEnabled</span></span>



| <span data-ttu-id="8f223-415">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-415">Entry</span></span> | <span data-ttu-id="8f223-416">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-416">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-417">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-417">Description</span></span>    | <span data-ttu-id="8f223-418">Значение false, если приложение или компонент COM+ отключены.</span><span class="sxs-lookup"><span data-stu-id="8f223-418">False if the COM+ application or component is disabled.</span></span> <span data-ttu-id="8f223-419">Если приложение или компонент COM+ включен, то параметр Enabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="8f223-419">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="8f223-420">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-420">Access</span></span>         | <span data-ttu-id="8f223-421">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-421">ReadWrite</span></span>                                                                                                                   |
| <span data-ttu-id="8f223-422">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-422">Type</span></span>           | <span data-ttu-id="8f223-423">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-423">Bool</span></span>                                                                                                                        |
| <span data-ttu-id="8f223-424">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-424">Default</span></span>        | <span data-ttu-id="8f223-425">True</span><span class="sxs-lookup"><span data-stu-id="8f223-425">True</span></span>                                                                                                                        |
| <span data-ttu-id="8f223-426">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-426">Minimum system</span></span> | <span data-ttu-id="8f223-427">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f223-427">Windows XP</span></span>                                                                                                                  |



 

### <a name="iseventclass"></a><span data-ttu-id="8f223-428">исевенткласс</span><span class="sxs-lookup"><span data-stu-id="8f223-428">IsEventClass</span></span>



| <span data-ttu-id="8f223-429">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-429">Entry</span></span> | <span data-ttu-id="8f223-430">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-430">Value</span></span> |
|----------------|----------------------------------------------------|
| <span data-ttu-id="8f223-431">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-431">Description</span></span>    | <span data-ttu-id="8f223-432">Указывает, является ли компонент классом событий.</span><span class="sxs-lookup"><span data-stu-id="8f223-432">Indicates whether the component is an event class.</span></span> |
| <span data-ttu-id="8f223-433">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-433">Access</span></span>         | <span data-ttu-id="8f223-434">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-434">ReadOnly</span></span>                                           |
| <span data-ttu-id="8f223-435">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-435">Type</span></span>           | <span data-ttu-id="8f223-436">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-436">Bool</span></span>                                               |
| <span data-ttu-id="8f223-437">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-437">Default</span></span>        | <span data-ttu-id="8f223-438">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-438">False</span></span>                                              |
| <span data-ttu-id="8f223-439">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-439">Minimum system</span></span> | <span data-ttu-id="8f223-440">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-440">Windows 2000</span></span>                                       |



 

### <a name="isinstalled"></a><span data-ttu-id="8f223-441">IsInstalled</span><span class="sxs-lookup"><span data-stu-id="8f223-441">IsInstalled</span></span>



| <span data-ttu-id="8f223-442">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-442">Entry</span></span> | <span data-ttu-id="8f223-443">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-443">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="8f223-444">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-444">Description</span></span>    | <span data-ttu-id="8f223-445">Указывает, установлен ли компонент в приложении.</span><span class="sxs-lookup"><span data-stu-id="8f223-445">Indicates whether the component is installed in an application.</span></span> |
| <span data-ttu-id="8f223-446">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-446">Access</span></span>         | <span data-ttu-id="8f223-447">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-447">ReadOnly</span></span>                                                        |
| <span data-ttu-id="8f223-448">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-448">Type</span></span>           | <span data-ttu-id="8f223-449">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-449">Bool</span></span>                                                            |
| <span data-ttu-id="8f223-450">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-450">Default</span></span>        | <span data-ttu-id="8f223-451">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-451">False</span></span>                                                           |
| <span data-ttu-id="8f223-452">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-452">Minimum system</span></span> | <span data-ttu-id="8f223-453">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f223-453">Windows Server 2003</span></span>                                             |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="8f223-454">исприватекомпонент</span><span class="sxs-lookup"><span data-stu-id="8f223-454">IsPrivateComponent</span></span>



| <span data-ttu-id="8f223-455">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-455">Entry</span></span> | <span data-ttu-id="8f223-456">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-456">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-457">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-457">Description</span></span>    | <span data-ttu-id="8f223-458">Определяет, является ли серверное приложение частным компонентом.</span><span class="sxs-lookup"><span data-stu-id="8f223-458">Determines whether a server application is a private component.</span></span> <span data-ttu-id="8f223-459">Частный компонент в серверном приложении может быть активирован только внутри приложения.</span><span class="sxs-lookup"><span data-stu-id="8f223-459">A private component in a server application can be activated only from within the application.</span></span> <span data-ttu-id="8f223-460">Например, при вызове [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для частного компонента он завершается сбоем вне процесса, но выполняется в процессе.</span><span class="sxs-lookup"><span data-stu-id="8f223-460">For example, if you call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) on a private component, it fails from out-of-process but succeeds in-process.</span></span> <span data-ttu-id="8f223-461">Напротив, при вызове **CoCreateInstance** для общедоступного компонента он будет выполнен как в процессе, так и вне процесса.</span><span class="sxs-lookup"><span data-stu-id="8f223-461">In contrast, if you call **CoCreateInstance** on a public component, it succeeds both in-process and out-of-process.</span></span> |
| <span data-ttu-id="8f223-462">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-462">Access</span></span>         | <span data-ttu-id="8f223-463">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-463">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8f223-464">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-464">Type</span></span>           | <span data-ttu-id="8f223-465">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-465">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8f223-466">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-466">Default</span></span>        | <span data-ttu-id="8f223-467">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-467">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="8f223-468">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-468">Minimum system</span></span> | <span data-ttu-id="8f223-469">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f223-469">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

### <a name="justintimeactivation"></a><span data-ttu-id="8f223-470">жустинтимеактиватион</span><span class="sxs-lookup"><span data-stu-id="8f223-470">JustInTimeActivation</span></span>



| <span data-ttu-id="8f223-471">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-471">Entry</span></span> | <span data-ttu-id="8f223-472">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-472">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-473">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-473">Description</span></span>    | <span data-ttu-id="8f223-474">Определяет, включена ли [JIT-активация](enabling-jit-activation-for-a-component.md) для компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-474">Determines whether [JIT activation](enabling-jit-activation-for-a-component.md) is enabled for the component.</span></span> <span data-ttu-id="8f223-475">Это свойство имеет значение true, если для [поддержки транзакций](setting-the-transaction-attribute.md) задано значение обязательно, требуется New или Supported.</span><span class="sxs-lookup"><span data-stu-id="8f223-475">This property is set to True when [transaction support](setting-the-transaction-attribute.md) is set to Required, Requires New, or Supported.</span></span> <span data-ttu-id="8f223-476">Если для Жустинтимеактиватион задано значение true, то для [поддержки синхронизации](setting-the-synchronization-attribute.md) должно быть задано значение обязательно (по умолчанию) или требуется New.</span><span class="sxs-lookup"><span data-stu-id="8f223-476">When JustInTimeActivation is set to True, [synchronization support](setting-the-synchronization-attribute.md) must be set to Required (the default) or Requires New.</span></span> |
| <span data-ttu-id="8f223-477">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-477">Access</span></span>         | <span data-ttu-id="8f223-478">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-478">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="8f223-479">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-479">Type</span></span>           | <span data-ttu-id="8f223-480">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-480">Bool</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="8f223-481">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-481">Default</span></span>        | <span data-ttu-id="8f223-482">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-482">False</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="8f223-483">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-483">Minimum system</span></span> | <span data-ttu-id="8f223-484">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-484">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="loadbalancingsupported"></a><span data-ttu-id="8f223-485">лоадбаланЦингсуппортед</span><span class="sxs-lookup"><span data-stu-id="8f223-485">LoadBalancingSupported</span></span>



| <span data-ttu-id="8f223-486">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-486">Entry</span></span> | <span data-ttu-id="8f223-487">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-487">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-488">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-488">Description</span></span>    | <span data-ttu-id="8f223-489">Если служба балансировки нагрузки компонентов установлена и включена на сервере, определяет, участвует ли компонент в балансировке нагрузки.</span><span class="sxs-lookup"><span data-stu-id="8f223-489">If the component load balancing service is installed and enabled on the server, determines whether the component participates in load balancing.</span></span> |
| <span data-ttu-id="8f223-490">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-490">Access</span></span>         | <span data-ttu-id="8f223-491">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-491">ReadWrite</span></span>                                                                                                                                        |
| <span data-ttu-id="8f223-492">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-492">Type</span></span>           | <span data-ttu-id="8f223-493">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-493">Bool</span></span>                                                                                                                                             |
| <span data-ttu-id="8f223-494">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-494">Default</span></span>        | <span data-ttu-id="8f223-495">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-495">False</span></span>                                                                                                                                            |
| <span data-ttu-id="8f223-496">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-496">Minimum system</span></span> | <span data-ttu-id="8f223-497">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-497">Windows 2000</span></span>                                                                                                                                     |



 

### <a name="maxpoolsize"></a><span data-ttu-id="8f223-498">MaxPoolSize</span><span class="sxs-lookup"><span data-stu-id="8f223-498">MaxPoolSize</span></span>



| <span data-ttu-id="8f223-499">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-499">Entry</span></span> | <span data-ttu-id="8f223-500">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-500">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="8f223-501">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-501">Description</span></span>    | <span data-ttu-id="8f223-502">Максимальное число объектов в пуле.</span><span class="sxs-lookup"><span data-stu-id="8f223-502">Maximum number of objects pooled.</span></span> |
| <span data-ttu-id="8f223-503">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-503">Access</span></span>         | <span data-ttu-id="8f223-504">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-504">ReadWrite</span></span>                         |
| <span data-ttu-id="8f223-505">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-505">Type</span></span>           | <span data-ttu-id="8f223-506">Long (1-1048576)</span><span class="sxs-lookup"><span data-stu-id="8f223-506">Long (1-1048576)</span></span>                  |
| <span data-ttu-id="8f223-507">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-507">Default</span></span>        | <span data-ttu-id="8f223-508">1048576</span><span class="sxs-lookup"><span data-stu-id="8f223-508">1048576</span></span>                           |
| <span data-ttu-id="8f223-509">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-509">Minimum system</span></span> | <span data-ttu-id="8f223-510">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-510">Windows 2000</span></span>                      |



 

### <a name="minpoolsize"></a><span data-ttu-id="8f223-511">минпулсизе</span><span class="sxs-lookup"><span data-stu-id="8f223-511">MinPoolSize</span></span>



| <span data-ttu-id="8f223-512">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-512">Entry</span></span> | <span data-ttu-id="8f223-513">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-513">Value</span></span> |
|----------------|-----------------------------------|
| <span data-ttu-id="8f223-514">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-514">Description</span></span>    | <span data-ttu-id="8f223-515">Минимальное число объектов в пуле.</span><span class="sxs-lookup"><span data-stu-id="8f223-515">Minimum number of objects pooled.</span></span> |
| <span data-ttu-id="8f223-516">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-516">Access</span></span>         | <span data-ttu-id="8f223-517">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-517">ReadWrite</span></span>                         |
| <span data-ttu-id="8f223-518">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-518">Type</span></span>           | <span data-ttu-id="8f223-519">Long (0-1048576)</span><span class="sxs-lookup"><span data-stu-id="8f223-519">Long (0-1048576)</span></span>                  |
| <span data-ttu-id="8f223-520">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-520">Default</span></span>        | <span data-ttu-id="8f223-521">0</span><span class="sxs-lookup"><span data-stu-id="8f223-521">0</span></span>                                 |
| <span data-ttu-id="8f223-522">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-522">Minimum system</span></span> | <span data-ttu-id="8f223-523">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-523">Windows 2000</span></span>                      |



 

### <a name="multiinterfacepublisherfilterclsid"></a><span data-ttu-id="8f223-524">мултиинтерфацепублишерфилтерклсид</span><span class="sxs-lookup"><span data-stu-id="8f223-524">MultiInterfacePublisherFilterCLSID</span></span>



| <span data-ttu-id="8f223-525">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-525">Entry</span></span> | <span data-ttu-id="8f223-526">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-526">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="8f223-527">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-527">Description</span></span>    | <span data-ttu-id="8f223-528">CLSID для фильтра издателя, используемого, если компонент является классом событий.</span><span class="sxs-lookup"><span data-stu-id="8f223-528">CLSID for the publisher filter used if the component is an event class.</span></span> |
| <span data-ttu-id="8f223-529">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-529">Access</span></span>         | <span data-ttu-id="8f223-530">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-530">ReadWrite</span></span>                                                               |
| <span data-ttu-id="8f223-531">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-531">Type</span></span>           | <span data-ttu-id="8f223-532">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-532">String</span></span>                                                                  |
| <span data-ttu-id="8f223-533">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-533">Default</span></span>        | <span data-ttu-id="8f223-534">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f223-534">N/A</span></span>                                                                     |
| <span data-ttu-id="8f223-535">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-535">Minimum system</span></span> | <span data-ttu-id="8f223-536">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-536">Windows 2000</span></span>                                                            |



 

### <a name="mustruninclientcontext"></a><span data-ttu-id="8f223-537">муструнинклиентконтекст</span><span class="sxs-lookup"><span data-stu-id="8f223-537">MustRunInClientContext</span></span>



| <span data-ttu-id="8f223-538">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-538">Entry</span></span> | <span data-ttu-id="8f223-539">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-539">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-540">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-540">Description</span></span>    | <span data-ttu-id="8f223-541">Указывает, что компонент должен быть активирован в контексте его исходного вызывающего.</span><span class="sxs-lookup"><span data-stu-id="8f223-541">Indicates that component must be activated in its original caller's context.</span></span> <span data-ttu-id="8f223-542">В противном случае активация завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8f223-542">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="8f223-543">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-543">Access</span></span>         | <span data-ttu-id="8f223-544">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-544">ReadWrite</span></span>                                                                                                 |
| <span data-ttu-id="8f223-545">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-545">Type</span></span>           | <span data-ttu-id="8f223-546">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-546">Bool</span></span>                                                                                                      |
| <span data-ttu-id="8f223-547">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-547">Default</span></span>        | <span data-ttu-id="8f223-548">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-548">False</span></span>                                                                                                     |
| <span data-ttu-id="8f223-549">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-549">Minimum system</span></span> | <span data-ttu-id="8f223-550">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f223-550">Windows XP</span></span>                                                                                                |



 

### <a name="mustrunindefaultcontext"></a><span data-ttu-id="8f223-551">муструниндефаултконтекст</span><span class="sxs-lookup"><span data-stu-id="8f223-551">MustRunInDefaultContext</span></span>



| <span data-ttu-id="8f223-552">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-552">Entry</span></span> | <span data-ttu-id="8f223-553">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-553">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-554">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-554">Description</span></span>    | <span data-ttu-id="8f223-555">Указывает, что компонент должен быть активирован в контексте вызывающего объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f223-555">Indicates that the component must be activated in the default caller's context.</span></span> <span data-ttu-id="8f223-556">В противном случае активация завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8f223-556">Otherwise, activation fails.</span></span> |
| <span data-ttu-id="8f223-557">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-557">Access</span></span>         | <span data-ttu-id="8f223-558">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-558">ReadWrite</span></span>                                                                                                    |
| <span data-ttu-id="8f223-559">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-559">Type</span></span>           | <span data-ttu-id="8f223-560">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-560">Bool</span></span>                                                                                                         |
| <span data-ttu-id="8f223-561">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-561">Default</span></span>        | <span data-ttu-id="8f223-562">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-562">False</span></span>                                                                                                        |
| <span data-ttu-id="8f223-563">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-563">Minimum system</span></span> | <span data-ttu-id="8f223-564">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-564">Windows 2000</span></span>                                                                                                 |



 

### <a name="objectpoolingenabled"></a><span data-ttu-id="8f223-565">обжектпулинженаблед</span><span class="sxs-lookup"><span data-stu-id="8f223-565">ObjectPoolingEnabled</span></span>



| <span data-ttu-id="8f223-566">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-566">Entry</span></span> | <span data-ttu-id="8f223-567">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-567">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-568">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-568">Description</span></span>    | <span data-ttu-id="8f223-569">Определяет, включена ли поддержка [пула объектов COM+](com--object-pooling.md) для компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-569">Determines whether [COM+ object pooling](com--object-pooling.md) is enabled for the component.</span></span> |
| <span data-ttu-id="8f223-570">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-570">Access</span></span>         | <span data-ttu-id="8f223-571">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-571">ReadWrite</span></span>                                                                                       |
| <span data-ttu-id="8f223-572">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-572">Type</span></span>           | <span data-ttu-id="8f223-573">Bool</span><span class="sxs-lookup"><span data-stu-id="8f223-573">Bool</span></span>                                                                                            |
| <span data-ttu-id="8f223-574">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-574">Default</span></span>        | <span data-ttu-id="8f223-575">Неверно</span><span class="sxs-lookup"><span data-stu-id="8f223-575">False</span></span>                                                                                           |
| <span data-ttu-id="8f223-576">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-576">Minimum system</span></span> | <span data-ttu-id="8f223-577">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-577">Windows 2000</span></span>                                                                                    |



 

### <a name="progid"></a><span data-ttu-id="8f223-578">ProgID:</span><span class="sxs-lookup"><span data-stu-id="8f223-578">ProgID</span></span>



| <span data-ttu-id="8f223-579">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-579">Entry</span></span> | <span data-ttu-id="8f223-580">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-580">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-581">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-581">Description</span></span>    | <span data-ttu-id="8f223-582">Понятное имя, используемое для идентификации компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-582">A friendly name used for identifying the component.</span></span> <span data-ttu-id="8f223-583">Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="8f223-583">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="8f223-584">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-584">Access</span></span>         | <span data-ttu-id="8f223-585">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-585">ReadOnly</span></span>                                                                                                                                                                              |
| <span data-ttu-id="8f223-586">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-586">Type</span></span>           | <span data-ttu-id="8f223-587">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-587">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="8f223-588">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-588">Default</span></span>        | <span data-ttu-id="8f223-589">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f223-589">N/A</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="8f223-590">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-590">Minimum system</span></span> | <span data-ttu-id="8f223-591">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-591">Windows 2000</span></span>                                                                                                                                                                          |



 

### <a name="publisherid"></a><span data-ttu-id="8f223-592">PublisherID</span><span class="sxs-lookup"><span data-stu-id="8f223-592">PublisherID</span></span>



| <span data-ttu-id="8f223-593">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-593">Entry</span></span> | <span data-ttu-id="8f223-594">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-594">Value</span></span> |
|----------------|------------------------------------------------------------------------|
| <span data-ttu-id="8f223-595">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-595">Description</span></span>    | <span data-ttu-id="8f223-596">Идентификатор издателя события, если компонент является классом событий.</span><span class="sxs-lookup"><span data-stu-id="8f223-596">Identifier for the event publisher if the component is an event class.</span></span> |
| <span data-ttu-id="8f223-597">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-597">Access</span></span>         | <span data-ttu-id="8f223-598">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-598">ReadWrite</span></span>                                                              |
| <span data-ttu-id="8f223-599">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-599">Type</span></span>           | <span data-ttu-id="8f223-600">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-600">String</span></span>                                                                 |
| <span data-ttu-id="8f223-601">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-601">Default</span></span>        | <span data-ttu-id="8f223-602">""</span><span class="sxs-lookup"><span data-stu-id="8f223-602">""</span></span>                                                                     |
| <span data-ttu-id="8f223-603">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-603">Minimum system</span></span> | <span data-ttu-id="8f223-604">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-604">Windows 2000</span></span>                                                           |



 

### <a name="soapassemblyname"></a><span data-ttu-id="8f223-605">соапассемблинаме</span><span class="sxs-lookup"><span data-stu-id="8f223-605">SoapAssemblyName</span></span>



| <span data-ttu-id="8f223-606">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-606">Entry</span></span> | <span data-ttu-id="8f223-607">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-607">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-608">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-608">Description</span></span>    | <span data-ttu-id="8f223-609">Идентификатор GUID, определяющий сборку GAC, которая выполняется, когда компонент вызывается как служба SOAP.</span><span class="sxs-lookup"><span data-stu-id="8f223-609">A GUID identifying the GAC assembly that is run when the component is invoked as a SOAP service.</span></span> |
| <span data-ttu-id="8f223-610">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-610">Access</span></span>         | <span data-ttu-id="8f223-611">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-611">ReadWrite</span></span>                                                                                        |
| <span data-ttu-id="8f223-612">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-612">Type</span></span>           | <span data-ttu-id="8f223-613">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-613">String</span></span>                                                                                           |
| <span data-ttu-id="8f223-614">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-614">Default</span></span>        | <span data-ttu-id="8f223-615">NULL</span><span class="sxs-lookup"><span data-stu-id="8f223-615">NULL</span></span>                                                                                             |
| <span data-ttu-id="8f223-616">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-616">Minimum system</span></span> | <span data-ttu-id="8f223-617">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f223-617">Windows Server 2003</span></span>                                                                              |



 

### <a name="soaptypename"></a><span data-ttu-id="8f223-618">соаптипенаме</span><span class="sxs-lookup"><span data-stu-id="8f223-618">SoapTypeName</span></span>



| <span data-ttu-id="8f223-619">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-619">Entry</span></span> | <span data-ttu-id="8f223-620">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-620">Value</span></span> |
|----------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-621">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-621">Description</span></span>    | <span data-ttu-id="8f223-622">Имя управляемого типа для компонента, который может быть вызван как служба SOAP.</span><span class="sxs-lookup"><span data-stu-id="8f223-622">The managed type name for a component that can be invoked as a SOAP service.</span></span> |
| <span data-ttu-id="8f223-623">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-623">Access</span></span>         | <span data-ttu-id="8f223-624">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-624">ReadWrite</span></span>                                                                    |
| <span data-ttu-id="8f223-625">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-625">Type</span></span>           | <span data-ttu-id="8f223-626">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-626">String</span></span>                                                                       |
| <span data-ttu-id="8f223-627">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-627">Default</span></span>        | <span data-ttu-id="8f223-628">NULL</span><span class="sxs-lookup"><span data-stu-id="8f223-628">NULL</span></span>                                                                         |
| <span data-ttu-id="8f223-629">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-629">Minimum system</span></span> | <span data-ttu-id="8f223-630">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f223-630">Windows Server 2003</span></span>                                                          |



 

### <a name="synchronization"></a><span data-ttu-id="8f223-631">Синхронизация</span><span class="sxs-lookup"><span data-stu-id="8f223-631">Synchronization</span></span>



| <span data-ttu-id="8f223-632">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-632">Entry</span></span> | <span data-ttu-id="8f223-633">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-633">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-634">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-634">Description</span></span>    | <span data-ttu-id="8f223-635">Определяет [синхронизацию](setting-the-synchronization-attribute.md) вызовов для компонента.</span><span class="sxs-lookup"><span data-stu-id="8f223-635">Determines call [synchronization](setting-the-synchronization-attribute.md) for the component.</span></span>                                                                                                     |
| <span data-ttu-id="8f223-636">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-636">Access</span></span>         | <span data-ttu-id="8f223-637">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-637">ReadWrite</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="8f223-638">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-638">Type</span></span>           | <span data-ttu-id="8f223-639">Длинные возможные значения: Комадминсинчронизатионигноред (0) Комадминсинчронизатионноне (1) Комадминсинчронизатионсуппортед (2) COMAdminSynchronizationRequired (3) COMAdminSynchronizationRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="8f223-639">Long Possible values:COMAdminSynchronizationIgnored (0)COMAdminSynchronizationNone (1)COMAdminSynchronizationSupported (2)COMAdminSynchronizationRequired (3)COMAdminSynchronizationRequiresNew (4)</span></span> |
| <span data-ttu-id="8f223-640">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-640">Default</span></span>        | <span data-ttu-id="8f223-641">Комадминсинчронизатионигноред (0)</span><span class="sxs-lookup"><span data-stu-id="8f223-641">COMAdminSynchronizationIgnored (0)</span></span>                                                                                                                                                                  |
| <span data-ttu-id="8f223-642">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-642">Minimum system</span></span> | <span data-ttu-id="8f223-643">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-643">Windows 2000</span></span>                                                                                                                                                                                        |



 

### <a name="threadingmodel"></a><span data-ttu-id="8f223-644">ThreadingModel.</span><span class="sxs-lookup"><span data-stu-id="8f223-644">ThreadingModel</span></span>



| <span data-ttu-id="8f223-645">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-645">Entry</span></span> | <span data-ttu-id="8f223-646">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-646">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-647">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-647">Description</span></span>    | <span data-ttu-id="8f223-648">Определяет, как экземпляры компонента назначаются потокам для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="8f223-648">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="8f223-649">Значения соответствуют моделям потоков COM.</span><span class="sxs-lookup"><span data-stu-id="8f223-649">Values correspond to COM threading models.</span></span>                                                                                        |
| <span data-ttu-id="8f223-650">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-650">Access</span></span>         | <span data-ttu-id="8f223-651">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-651">ReadOnly</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="8f223-652">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-652">Type</span></span>           | <span data-ttu-id="8f223-653">Длинные возможные значения: Комадминсреадингмоделапартмент (0) Комадминсреадингмоделфри (1) Комадминсреадингмоделмаин (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4) COMAdminThreadingModelNotSpecified (5)</span><span class="sxs-lookup"><span data-stu-id="8f223-653">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)COMAdminThreadingModelNotSpecified (5)</span></span> |
| <span data-ttu-id="8f223-654">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-654">Default</span></span>        | <span data-ttu-id="8f223-655">Н/Д</span><span class="sxs-lookup"><span data-stu-id="8f223-655">N/A</span></span>                                                                                                                                                                                                                       |
| <span data-ttu-id="8f223-656">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-656">Minimum system</span></span> | <span data-ttu-id="8f223-657">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-657">Windows 2000</span></span>                                                                                                                                                                                                              |



 

### <a name="transaction"></a><span data-ttu-id="8f223-658">Транзакция</span><span class="sxs-lookup"><span data-stu-id="8f223-658">Transaction</span></span>



| <span data-ttu-id="8f223-659">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-659">Entry</span></span> | <span data-ttu-id="8f223-660">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-660">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-661">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-661">Description</span></span>    | <span data-ttu-id="8f223-662">Определяет, как компонент поддерживает [транзакции](setting-the-transaction-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="8f223-662">Determines how a component supports [transactions](setting-the-transaction-attribute.md).</span></span> <span data-ttu-id="8f223-663">Рекомендуется использовать константы в перечислении, а не числовые значения.</span><span class="sxs-lookup"><span data-stu-id="8f223-663">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span> |
| <span data-ttu-id="8f223-664">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-664">Access</span></span>         | <span data-ttu-id="8f223-665">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-665">ReadWrite</span></span>                                                                                                                                                                              |
| <span data-ttu-id="8f223-666">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-666">Type</span></span>           | <span data-ttu-id="8f223-667">Длинные возможные значения: Комадминтрансактионигноред (0) Комадминтрансактионноне (1) Комадминтрансактионсуппортед (2) COMAdminTransactionRequired (3) COMAdminTransactionRequiresNew (4)</span><span class="sxs-lookup"><span data-stu-id="8f223-667">Long Possible values:COMAdminTransactionIgnored (0)COMAdminTransactionNone (1)COMAdminTransactionSupported (2)COMAdminTransactionRequired (3)COMAdminTransactionRequiresNew (4)</span></span>        |
| <span data-ttu-id="8f223-668">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-668">Default</span></span>        | <span data-ttu-id="8f223-669">Комадминтрансактионноне (1)</span><span class="sxs-lookup"><span data-stu-id="8f223-669">COMAdminTransactionNone (1)</span></span>                                                                                                                                                            |
| <span data-ttu-id="8f223-670">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-670">Minimum system</span></span> | <span data-ttu-id="8f223-671">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-671">Windows 2000</span></span>                                                                                                                                                                           |



 

### <a name="txisolationlevel"></a><span data-ttu-id="8f223-672">тксисолатионлевел</span><span class="sxs-lookup"><span data-stu-id="8f223-672">TxIsolationLevel</span></span>



| <span data-ttu-id="8f223-673">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-673">Entry</span></span> | <span data-ttu-id="8f223-674">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-674">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f223-675">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-675">Description</span></span>    | <span data-ttu-id="8f223-676">Указывает уровни изоляции транзакции.</span><span class="sxs-lookup"><span data-stu-id="8f223-676">Indicates the transaction isolation levels.</span></span> <span data-ttu-id="8f223-677">Существует пять уровней изоляции: None, READ UNCOMMITTED, READ COMMITTED, REPEATABLE READ и serialized.</span><span class="sxs-lookup"><span data-stu-id="8f223-677">There are five isolation levels: none, read uncommitted, read committed, repeatable read, and serialized.</span></span> <span data-ttu-id="8f223-678">Уровень изоляции по умолчанию сериализуется.</span><span class="sxs-lookup"><span data-stu-id="8f223-678">The default isolation level is serialized.</span></span>                           |
| <span data-ttu-id="8f223-679">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-679">Access</span></span>         | <span data-ttu-id="8f223-680">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8f223-680">ReadWrite</span></span>                                                                                                                                                                                                                  |
| <span data-ttu-id="8f223-681">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-681">Type</span></span>           | <span data-ttu-id="8f223-682">Длинные возможные значения: Комадминтксисолатионлевелани (0) Комадминтксисолатионлевелреадункоммиттед (1) Комадминтксисолатионлевелреадкоммиттед (2) COMAdminTxIsolationLevelRepeatableRead (3) COMAdminTxIsolationLevelSerializable (4)</span><span class="sxs-lookup"><span data-stu-id="8f223-682">Long Possible values:COMAdminTxIsolationLevelAny (0)COMAdminTxIsolationLevelReadUnCommitted (1)COMAdminTxIsolationLevelReadCommitted (2)COMAdminTxIsolationLevelRepeatableRead (3)COMAdminTxIsolationLevelSerializable (4)</span></span> |
| <span data-ttu-id="8f223-683">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-683">Default</span></span>        | <span data-ttu-id="8f223-684">Комадминтксисолатионлевелсериализабле (4)</span><span class="sxs-lookup"><span data-stu-id="8f223-684">COMAdminTxIsolationLevelSerializable (4)</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="8f223-685">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-685">Minimum system</span></span> | <span data-ttu-id="8f223-686">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8f223-686">Windows XP</span></span>                                                                                                                                                                                                                 |



 

### <a name="versionbuild"></a><span data-ttu-id="8f223-687">VersionBuild</span><span class="sxs-lookup"><span data-stu-id="8f223-687">VersionBuild</span></span>



| <span data-ttu-id="8f223-688">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-688">Entry</span></span> | <span data-ttu-id="8f223-689">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-689">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="8f223-690">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-690">Description</span></span>    | <span data-ttu-id="8f223-691">Идентификатор сборки версии.</span><span class="sxs-lookup"><span data-stu-id="8f223-691">Version build identifier.</span></span> |
| <span data-ttu-id="8f223-692">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-692">Access</span></span>         | <span data-ttu-id="8f223-693">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-693">ReadOnly</span></span>                  |
| <span data-ttu-id="8f223-694">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-694">Type</span></span>           | <span data-ttu-id="8f223-695">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-695">String</span></span>                    |
| <span data-ttu-id="8f223-696">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-696">Default</span></span>        | <span data-ttu-id="8f223-697">""</span><span class="sxs-lookup"><span data-stu-id="8f223-697">""</span></span>                        |
| <span data-ttu-id="8f223-698">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-698">Minimum system</span></span> | <span data-ttu-id="8f223-699">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-699">Windows 2000</span></span>              |



 

### <a name="versionmajor"></a><span data-ttu-id="8f223-700">VersionMajor</span><span class="sxs-lookup"><span data-stu-id="8f223-700">VersionMajor</span></span>



| <span data-ttu-id="8f223-701">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-701">Entry</span></span> | <span data-ttu-id="8f223-702">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-702">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="8f223-703">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-703">Description</span></span>    | <span data-ttu-id="8f223-704">Идентификатор версии.</span><span class="sxs-lookup"><span data-stu-id="8f223-704">Version identifier.</span></span> |
| <span data-ttu-id="8f223-705">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-705">Access</span></span>         | <span data-ttu-id="8f223-706">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-706">ReadOnly</span></span>            |
| <span data-ttu-id="8f223-707">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-707">Type</span></span>           | <span data-ttu-id="8f223-708">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-708">String</span></span>              |
| <span data-ttu-id="8f223-709">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-709">Default</span></span>        | <span data-ttu-id="8f223-710">""</span><span class="sxs-lookup"><span data-stu-id="8f223-710">""</span></span>                  |
| <span data-ttu-id="8f223-711">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-711">Minimum system</span></span> | <span data-ttu-id="8f223-712">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-712">Windows 2000</span></span>        |



 

### <a name="versionminor"></a><span data-ttu-id="8f223-713">VersionMinor</span><span class="sxs-lookup"><span data-stu-id="8f223-713">VersionMinor</span></span>



| <span data-ttu-id="8f223-714">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-714">Entry</span></span> | <span data-ttu-id="8f223-715">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-715">Value</span></span> |
|----------------|-------------------------|
| <span data-ttu-id="8f223-716">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-716">Description</span></span>    | <span data-ttu-id="8f223-717">Подтип версии.</span><span class="sxs-lookup"><span data-stu-id="8f223-717">Version sub-identifier.</span></span> |
| <span data-ttu-id="8f223-718">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-718">Access</span></span>         | <span data-ttu-id="8f223-719">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-719">ReadOnly</span></span>                |
| <span data-ttu-id="8f223-720">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-720">Type</span></span>           | <span data-ttu-id="8f223-721">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-721">String</span></span>                  |
| <span data-ttu-id="8f223-722">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-722">Default</span></span>        | <span data-ttu-id="8f223-723">""</span><span class="sxs-lookup"><span data-stu-id="8f223-723">""</span></span>                      |
| <span data-ttu-id="8f223-724">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-724">Minimum system</span></span> | <span data-ttu-id="8f223-725">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-725">Windows 2000</span></span>            |



 

### <a name="versionsubbuild"></a><span data-ttu-id="8f223-726">версионсуббуилд</span><span class="sxs-lookup"><span data-stu-id="8f223-726">VersionSubBuild</span></span>



| <span data-ttu-id="8f223-727">Ввод</span><span class="sxs-lookup"><span data-stu-id="8f223-727">Entry</span></span> | <span data-ttu-id="8f223-728">Значение</span><span class="sxs-lookup"><span data-stu-id="8f223-728">Value</span></span> |
|----------------|-------------------------------|
| <span data-ttu-id="8f223-729">Описание</span><span class="sxs-lookup"><span data-stu-id="8f223-729">Description</span></span>    | <span data-ttu-id="8f223-730">Идентификатор подсборки версии.</span><span class="sxs-lookup"><span data-stu-id="8f223-730">Version sub-build identifier.</span></span> |
| <span data-ttu-id="8f223-731">Access</span><span class="sxs-lookup"><span data-stu-id="8f223-731">Access</span></span>         | <span data-ttu-id="8f223-732">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="8f223-732">ReadOnly</span></span>                      |
| <span data-ttu-id="8f223-733">Тип</span><span class="sxs-lookup"><span data-stu-id="8f223-733">Type</span></span>           | <span data-ttu-id="8f223-734">Строка</span><span class="sxs-lookup"><span data-stu-id="8f223-734">String</span></span>                        |
| <span data-ttu-id="8f223-735">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="8f223-735">Default</span></span>        | <span data-ttu-id="8f223-736">""</span><span class="sxs-lookup"><span data-stu-id="8f223-736">""</span></span>                            |
| <span data-ttu-id="8f223-737">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="8f223-737">Minimum system</span></span> | <span data-ttu-id="8f223-738">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="8f223-738">Windows 2000</span></span>                  |



 

## <a name="see-also"></a><span data-ttu-id="8f223-739">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f223-739">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f223-740">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="8f223-740">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
