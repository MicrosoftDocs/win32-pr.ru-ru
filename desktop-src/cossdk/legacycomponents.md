---
description: Содержит объект для каждого ненастроенного компонента в коллекции приложений. Ненастроенные компоненты не могут использовать службы COM+. Свойства, предоставляемые этими объектами, сохраняют параметры, сделанные на уровне компонента.
ms.assetid: 87f3b93f-71aa-4187-88d2-889c13d8bd06
title: Коллекция Легацикомпонентс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyComponents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5761950dcb0ceb5c857daf37ba2236733ec30c22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807282"
---
# <a name="legacycomponents-collection"></a><span data-ttu-id="84aa3-105">Коллекция Легацикомпонентс</span><span class="sxs-lookup"><span data-stu-id="84aa3-105">LegacyComponents collection</span></span>

<span data-ttu-id="84aa3-106">Содержит объект для каждого ненастроенного компонента в коллекции приложений.</span><span class="sxs-lookup"><span data-stu-id="84aa3-106">Contains an object for each unconfigured component in the Applications collection.</span></span> <span data-ttu-id="84aa3-107">Ненастроенные компоненты не могут использовать службы COM+.</span><span class="sxs-lookup"><span data-stu-id="84aa3-107">Unconfigured components cannot make use of COM+ services.</span></span> <span data-ttu-id="84aa3-108">Свойства, предоставляемые этими объектами, сохраняют параметры, сделанные на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="84aa3-108">The properties exposed by these objects hold settings made at the component level.</span></span>

<span data-ttu-id="84aa3-109">Эта коллекция поддерживает метод [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) , но не метод [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="84aa3-109">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="84aa3-110">Чтобы установить или импортировать компоненты в приложение, используйте методы для объекта [**комадминкаталог**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="84aa3-110">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="84aa3-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="84aa3-111">Members</span></span>

<span data-ttu-id="84aa3-112">Коллекция **легацикомпонентс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="84aa3-112">The **LegacyComponents** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="84aa3-113">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="84aa3-113">Related Collections</span></span>

<span data-ttu-id="84aa3-114">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="84aa3-114">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="84aa3-115">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="84aa3-115">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="84aa3-116">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="84aa3-116">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="84aa3-117">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="84aa3-117">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="84aa3-118">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="84aa3-118">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="84aa3-119">**Приложения**</span><span class="sxs-lookup"><span data-stu-id="84aa3-119">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="84aa3-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="84aa3-120">Properties</span></span>

<span data-ttu-id="84aa3-121">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="84aa3-121">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="84aa3-122">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="84aa3-122">AccessPermissions</span></span>](#accesspermissions)
-   [<span data-ttu-id="84aa3-123">активатеатстораже</span><span class="sxs-lookup"><span data-stu-id="84aa3-123">ActivateAtStorage</span></span>](#activateatstorage)
-   [<span data-ttu-id="84aa3-124">AppID</span><span class="sxs-lookup"><span data-stu-id="84aa3-124">AppID</span></span>](#appid)
-   [<span data-ttu-id="84aa3-125">AppName</span><span class="sxs-lookup"><span data-stu-id="84aa3-125">AppName</span></span>](#appname)
-   [<span data-ttu-id="84aa3-126">аусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="84aa3-126">AuthenticationLevel</span></span>](#authenticationlevel)
-   [<span data-ttu-id="84aa3-127">Разрядность</span><span class="sxs-lookup"><span data-stu-id="84aa3-127">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="84aa3-128">ClassName</span><span class="sxs-lookup"><span data-stu-id="84aa3-128">ClassName</span></span>](#classname)
-   [<span data-ttu-id="84aa3-129">ЭТОМУ</span><span class="sxs-lookup"><span data-stu-id="84aa3-129">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="84aa3-130">дллсуррогате</span><span class="sxs-lookup"><span data-stu-id="84aa3-130">DllSurrogate</span></span>](#dllsurrogate)
-   [<span data-ttu-id="84aa3-131">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="84aa3-131">InprocHandler32</span></span>](#inprochandler32)
-   [<span data-ttu-id="84aa3-132">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="84aa3-132">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="84aa3-133">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="84aa3-133">IsEnabled</span></span>](#isenabled)
-   [<span data-ttu-id="84aa3-134">лаунчпермиссионс</span><span class="sxs-lookup"><span data-stu-id="84aa3-134">LaunchPermissions</span></span>](#launchpermissions)
-   [<span data-ttu-id="84aa3-135">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="84aa3-135">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="84aa3-136">локальная служба.</span><span class="sxs-lookup"><span data-stu-id="84aa3-136">LocalService</span></span>](#localservice)
-   [<span data-ttu-id="84aa3-137">Пароль</span><span class="sxs-lookup"><span data-stu-id="84aa3-137">Password</span></span>](#password)
-   [<span data-ttu-id="84aa3-138">ProgID:</span><span class="sxs-lookup"><span data-stu-id="84aa3-138">ProgID</span></span>](#progid)
-   [<span data-ttu-id="84aa3-139">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="84aa3-139">RemoteServer</span></span>](#remoteserver)
-   [<span data-ttu-id="84aa3-140">Запуск</span><span class="sxs-lookup"><span data-stu-id="84aa3-140">RunAs</span></span>](#runas)
-   [<span data-ttu-id="84aa3-141">сервицепараметер</span><span class="sxs-lookup"><span data-stu-id="84aa3-141">ServiceParameter</span></span>](#serviceparameter)
-   [<span data-ttu-id="84aa3-142">срптрустлевел</span><span class="sxs-lookup"><span data-stu-id="84aa3-142">SRPTrustLevel</span></span>](#srptrustlevel)
-   [<span data-ttu-id="84aa3-143">ThreadingModel</span><span class="sxs-lookup"><span data-stu-id="84aa3-143">ThreadingModel</span></span>](#threadingmodel)

### <a name="accesspermissions"></a><span data-ttu-id="84aa3-144">AccessPermissions</span><span class="sxs-lookup"><span data-stu-id="84aa3-144">AccessPermissions</span></span>



| <span data-ttu-id="84aa3-145">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-145">Entry</span></span> | <span data-ttu-id="84aa3-146">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-146">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-147">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-147">Description</span></span>    | <span data-ttu-id="84aa3-148">Указывает учетные записи пользователей, которым разрешен или запрещен доступ к компоненту.</span><span class="sxs-lookup"><span data-stu-id="84aa3-148">Specifies the user accounts that are allowed or denied access to the component.</span></span> |
| <span data-ttu-id="84aa3-149">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-149">Access</span></span>         | <span data-ttu-id="84aa3-150">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-150">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="84aa3-151">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-151">Type</span></span>           | <span data-ttu-id="84aa3-152">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-152">String</span></span>                                                                          |
| <span data-ttu-id="84aa3-153">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-153">Default</span></span>        | <span data-ttu-id="84aa3-154">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-154">N/A</span></span>                                                                             |
| <span data-ttu-id="84aa3-155">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-155">Minimum system</span></span> | <span data-ttu-id="84aa3-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-156">Windows XP</span></span>                                                                      |



 

### <a name="activateatstorage"></a><span data-ttu-id="84aa3-157">активатеатстораже</span><span class="sxs-lookup"><span data-stu-id="84aa3-157">ActivateAtStorage</span></span>



| <span data-ttu-id="84aa3-158">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-158">Entry</span></span> | <span data-ttu-id="84aa3-159">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-159">Value</span></span> |
|----------------|------------------------------------------------------------------|
| <span data-ttu-id="84aa3-160">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-160">Description</span></span>    | <span data-ttu-id="84aa3-161">Указывает, следует ли запускать сервер на компьютере хранения данных.</span><span class="sxs-lookup"><span data-stu-id="84aa3-161">Specifies whether to run the server on the data storage machine.</span></span> |
| <span data-ttu-id="84aa3-162">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-162">Access</span></span>         | <span data-ttu-id="84aa3-163">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-163">ReadWrite</span></span>                                                        |
| <span data-ttu-id="84aa3-164">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-164">Type</span></span>           | <span data-ttu-id="84aa3-165">Допустимые значения строки: "N" "Y"</span><span class="sxs-lookup"><span data-stu-id="84aa3-165">String Possible values:"N""Y"</span></span>                                    |
| <span data-ttu-id="84aa3-166">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-166">Default</span></span>        | <span data-ttu-id="84aa3-167">"N"</span><span class="sxs-lookup"><span data-stu-id="84aa3-167">"N"</span></span>                                                              |
| <span data-ttu-id="84aa3-168">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-168">Minimum system</span></span> | <span data-ttu-id="84aa3-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-169">Windows XP</span></span>                                                       |



 

### <a name="appid"></a><span data-ttu-id="84aa3-170">AppID</span><span class="sxs-lookup"><span data-stu-id="84aa3-170">AppID</span></span>



| <span data-ttu-id="84aa3-171">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-171">Entry</span></span> | <span data-ttu-id="84aa3-172">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-172">Value</span></span> |
|----------------|---------------------|
| <span data-ttu-id="84aa3-173">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-173">Description</span></span>    | <span data-ttu-id="84aa3-174">Код приложения.</span><span class="sxs-lookup"><span data-stu-id="84aa3-174">The application ID.</span></span> |
| <span data-ttu-id="84aa3-175">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-175">Access</span></span>         | <span data-ttu-id="84aa3-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-176">ReadOnly</span></span>            |
| <span data-ttu-id="84aa3-177">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-177">Type</span></span>           | <span data-ttu-id="84aa3-178">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-178">String</span></span>              |
| <span data-ttu-id="84aa3-179">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-179">Default</span></span>        | <span data-ttu-id="84aa3-180">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-180">N/A</span></span>                 |
| <span data-ttu-id="84aa3-181">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-181">Minimum system</span></span> | <span data-ttu-id="84aa3-182">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-182">Windows XP</span></span>          |



 

### <a name="appname"></a><span data-ttu-id="84aa3-183">AppName</span><span class="sxs-lookup"><span data-stu-id="84aa3-183">AppName</span></span>



| <span data-ttu-id="84aa3-184">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-184">Entry</span></span> | <span data-ttu-id="84aa3-185">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-185">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="84aa3-186">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-186">Description</span></span>    | <span data-ttu-id="84aa3-187">Имя приложения.</span><span class="sxs-lookup"><span data-stu-id="84aa3-187">The name of the application.</span></span> |
| <span data-ttu-id="84aa3-188">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-188">Access</span></span>         | <span data-ttu-id="84aa3-189">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-189">ReadOnly</span></span>                     |
| <span data-ttu-id="84aa3-190">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-190">Type</span></span>           | <span data-ttu-id="84aa3-191">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-191">String</span></span>                       |
| <span data-ttu-id="84aa3-192">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-192">Default</span></span>        | <span data-ttu-id="84aa3-193">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-193">N/A</span></span>                          |
| <span data-ttu-id="84aa3-194">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-194">Minimum system</span></span> | <span data-ttu-id="84aa3-195">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-195">Windows XP</span></span>                   |



 

### <a name="authenticationlevel"></a><span data-ttu-id="84aa3-196">аусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="84aa3-196">AuthenticationLevel</span></span>



| <span data-ttu-id="84aa3-197">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-197">Entry</span></span> | <span data-ttu-id="84aa3-198">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-198">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-199">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-199">Description</span></span>    | <span data-ttu-id="84aa3-200">Задает уровень проверки подлинности для вызовов со значениями, соответствующими параметрам проверки подлинности удаленного вызова процедур (RPC).</span><span class="sxs-lookup"><span data-stu-id="84aa3-200">Sets authentication level for calls, with values corresponding to the Remote Procedure Call (RPC) authentication settings.</span></span> <span data-ttu-id="84aa3-201">При выборе Комадминаусентикатиондефаулт используется параметр в свойстве Дефаултаусентикатионлевел в коллекции [**локалкомпутер**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="84aa3-201">When COMAdminAuthenticationDefault is chosen, the setting in the DefaultAuthenticationLevel property within the [**LocalComputer**](localcomputer.md) collection is used.</span></span> |
| <span data-ttu-id="84aa3-202">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-202">Access</span></span>         | <span data-ttu-id="84aa3-203">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-203">ReadWrite</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="84aa3-204">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-204">Type</span></span>           | <span data-ttu-id="84aa3-205">Длинные возможные значения: Комадминаусентикатиондефаулт (0) Комадминаусентикатионноне (1) Комадминаусентикатионконнект (2) COMAdminAuthenticationCall (3) COMAdminAuthenticationPacket (4) COMAdminAuthenticationIntegrity (5) COMAdminAuthenticationPrivacy (6)</span><span class="sxs-lookup"><span data-stu-id="84aa3-205">Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6)</span></span>                                              |
| <span data-ttu-id="84aa3-206">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-206">Default</span></span>        | <span data-ttu-id="84aa3-207">Комадминаусентикатиондефаулт (0)</span><span class="sxs-lookup"><span data-stu-id="84aa3-207">COMAdminAuthenticationDefault (0)</span></span>                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="84aa3-208">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-208">Minimum system</span></span> | <span data-ttu-id="84aa3-209">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-209">Windows XP</span></span>                                                                                                                                                                                                                                                                                            |



 

> [!Note]  
> <span data-ttu-id="84aa3-210">Рекомендуется использовать константы в перечислении, а не числовые значения.</span><span class="sxs-lookup"><span data-stu-id="84aa3-210">It is recommended that you use the constants in the enumeration and not the numeric values.</span></span>

 

### <a name="bitness"></a><span data-ttu-id="84aa3-211">Разрядность</span><span class="sxs-lookup"><span data-stu-id="84aa3-211">Bitness</span></span>



| <span data-ttu-id="84aa3-212">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-212">Entry</span></span> | <span data-ttu-id="84aa3-213">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-213">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-214">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-214">Description</span></span>    | <span data-ttu-id="84aa3-215">Представляет двоичный тип разрядности компонента.</span><span class="sxs-lookup"><span data-stu-id="84aa3-215">Represents the binary bitness type of the component.</span></span> <span data-ttu-id="84aa3-216">В системах, использующих 64-разрядную версию Windows, это свойство различает 64-разрядные компоненты и 32-разрядные компоненты.</span><span class="sxs-lookup"><span data-stu-id="84aa3-216">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="84aa3-217">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-217">Access</span></span>         | <span data-ttu-id="84aa3-218">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-218">ReadOnly</span></span>                                                                                                                                                              |
| <span data-ttu-id="84aa3-219">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-219">Type</span></span>           | <span data-ttu-id="84aa3-220">Длинные возможные значения: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="84aa3-220">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                         |
| <span data-ttu-id="84aa3-221">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-221">Default</span></span>        | <span data-ttu-id="84aa3-222">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-222">N/A</span></span>                                                                                                                                                                   |
| <span data-ttu-id="84aa3-223">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-223">Minimum system</span></span> | <span data-ttu-id="84aa3-224">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-224">Windows XP</span></span>                                                                                                                                                            |



 

### <a name="classname"></a><span data-ttu-id="84aa3-225">ClassName</span><span class="sxs-lookup"><span data-stu-id="84aa3-225">ClassName</span></span>



| <span data-ttu-id="84aa3-226">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-226">Entry</span></span> | <span data-ttu-id="84aa3-227">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-227">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="84aa3-228">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-228">Description</span></span>    | <span data-ttu-id="84aa3-229">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="84aa3-229">The name of the class.</span></span> |
| <span data-ttu-id="84aa3-230">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-230">Access</span></span>         | <span data-ttu-id="84aa3-231">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-231">ReadOnly</span></span>               |
| <span data-ttu-id="84aa3-232">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-232">Type</span></span>           | <span data-ttu-id="84aa3-233">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-233">String</span></span>                 |
| <span data-ttu-id="84aa3-234">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-234">Default</span></span>        | <span data-ttu-id="84aa3-235">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-235">N/A</span></span>                    |
| <span data-ttu-id="84aa3-236">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-236">Minimum system</span></span> | <span data-ttu-id="84aa3-237">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-237">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="84aa3-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="84aa3-238">CLSID</span></span>



| <span data-ttu-id="84aa3-239">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-239">Entry</span></span> | <span data-ttu-id="84aa3-240">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-240">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-241">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-241">Description</span></span>    | <span data-ttu-id="84aa3-242">Идентификатор GUID для компонента.</span><span class="sxs-lookup"><span data-stu-id="84aa3-242">A GUID for the component.</span></span> <span data-ttu-id="84aa3-243">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="84aa3-243">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="84aa3-244">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-244">Access</span></span>         | <span data-ttu-id="84aa3-245">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-245">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="84aa3-246">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-246">Type</span></span>           | <span data-ttu-id="84aa3-247">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-247">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="84aa3-248">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-248">Default</span></span>        | <span data-ttu-id="84aa3-249">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-249">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="84aa3-250">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-250">Minimum system</span></span> | <span data-ttu-id="84aa3-251">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-251">Windows XP</span></span>                                                                                                                                                |



 

### <a name="dllsurrogate"></a><span data-ttu-id="84aa3-252">дллсуррогате</span><span class="sxs-lookup"><span data-stu-id="84aa3-252">DllSurrogate</span></span>



| <span data-ttu-id="84aa3-253">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-253">Entry</span></span> | <span data-ttu-id="84aa3-254">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-254">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="84aa3-255">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-255">Description</span></span>    | <span data-ttu-id="84aa3-256">Указывает полный путь к серверному приложению суррагате.</span><span class="sxs-lookup"><span data-stu-id="84aa3-256">Specifies the full path to a surragate server application.</span></span> |
| <span data-ttu-id="84aa3-257">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-257">Access</span></span>         | <span data-ttu-id="84aa3-258">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-258">ReadWrite</span></span>                                                  |
| <span data-ttu-id="84aa3-259">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-259">Type</span></span>           | <span data-ttu-id="84aa3-260">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-260">String</span></span>                                                     |
| <span data-ttu-id="84aa3-261">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-261">Default</span></span>        | <span data-ttu-id="84aa3-262">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-262">N/A</span></span>                                                        |
| <span data-ttu-id="84aa3-263">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-263">Minimum system</span></span> | <span data-ttu-id="84aa3-264">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-264">Windows XP</span></span>                                                 |



 

### <a name="inprochandler32"></a><span data-ttu-id="84aa3-265">InprocHandler32</span><span class="sxs-lookup"><span data-stu-id="84aa3-265">InprocHandler32</span></span>



| <span data-ttu-id="84aa3-266">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-266">Entry</span></span> | <span data-ttu-id="84aa3-267">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-267">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="84aa3-268">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-268">Description</span></span>    | <span data-ttu-id="84aa3-269">Указывает полный путь к 32-разрядной библиотеке DLL пользовательского обработчика.</span><span class="sxs-lookup"><span data-stu-id="84aa3-269">Specifies the full path to a 32-bit in-process custom handler DLL.</span></span> |
| <span data-ttu-id="84aa3-270">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-270">Access</span></span>         | <span data-ttu-id="84aa3-271">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-271">ReadWrite</span></span>                                                          |
| <span data-ttu-id="84aa3-272">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-272">Type</span></span>           | <span data-ttu-id="84aa3-273">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-273">String</span></span>                                                             |
| <span data-ttu-id="84aa3-274">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-274">Default</span></span>        | <span data-ttu-id="84aa3-275">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-275">N/A</span></span>                                                                |
| <span data-ttu-id="84aa3-276">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-276">Minimum system</span></span> | <span data-ttu-id="84aa3-277">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-277">Windows XP</span></span>                                                         |



 

### <a name="inprocserver32"></a><span data-ttu-id="84aa3-278">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="84aa3-278">InprocServer32</span></span>



| <span data-ttu-id="84aa3-279">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-279">Entry</span></span> | <span data-ttu-id="84aa3-280">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-280">Value</span></span> |
|----------------|------------------------------------------------------------|
| <span data-ttu-id="84aa3-281">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-281">Description</span></span>    | <span data-ttu-id="84aa3-282">Указывает полный путь к 32-разрядной библиотеке DLL внутрипроцессного сервера.</span><span class="sxs-lookup"><span data-stu-id="84aa3-282">Specifies the full path to a 32-bit in-process server DLL.</span></span> |
| <span data-ttu-id="84aa3-283">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-283">Access</span></span>         | <span data-ttu-id="84aa3-284">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-284">ReadWrite</span></span>                                                  |
| <span data-ttu-id="84aa3-285">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-285">Type</span></span>           | <span data-ttu-id="84aa3-286">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-286">String</span></span>                                                     |
| <span data-ttu-id="84aa3-287">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-287">Default</span></span>        | <span data-ttu-id="84aa3-288">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-288">N/A</span></span>                                                        |
| <span data-ttu-id="84aa3-289">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-289">Minimum system</span></span> | <span data-ttu-id="84aa3-290">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-290">Windows XP</span></span>                                                 |



 

### <a name="isenabled"></a><span data-ttu-id="84aa3-291">IsEnabled</span><span class="sxs-lookup"><span data-stu-id="84aa3-291">IsEnabled</span></span>



| <span data-ttu-id="84aa3-292">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-292">Entry</span></span> | <span data-ttu-id="84aa3-293">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-293">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-294">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-294">Description</span></span>    | <span data-ttu-id="84aa3-295">Если приложение или компонент COM+ отключены, параметр Enable имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="84aa3-295">If the COM+ application or component is disabled, IsEnabled is False.</span></span> <span data-ttu-id="84aa3-296">Если приложение или компонент COM+ включен, то параметр Enabled имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="84aa3-296">If the COM+ application or component is enabled, IsEnabled is True.</span></span> |
| <span data-ttu-id="84aa3-297">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-297">Access</span></span>         | <span data-ttu-id="84aa3-298">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-298">ReadWrite</span></span>                                                                                                                                 |
| <span data-ttu-id="84aa3-299">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-299">Type</span></span>           | <span data-ttu-id="84aa3-300">Bool</span><span class="sxs-lookup"><span data-stu-id="84aa3-300">Bool</span></span>                                                                                                                                      |
| <span data-ttu-id="84aa3-301">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-301">Default</span></span>        | <span data-ttu-id="84aa3-302">True</span><span class="sxs-lookup"><span data-stu-id="84aa3-302">True</span></span>                                                                                                                                      |
| <span data-ttu-id="84aa3-303">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-303">Minimum system</span></span> | <span data-ttu-id="84aa3-304">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-304">Windows XP</span></span>                                                                                                                                |



 

### <a name="launchpermissions"></a><span data-ttu-id="84aa3-305">лаунчпермиссионс</span><span class="sxs-lookup"><span data-stu-id="84aa3-305">LaunchPermissions</span></span>



| <span data-ttu-id="84aa3-306">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-306">Entry</span></span> | <span data-ttu-id="84aa3-307">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-307">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-308">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-308">Description</span></span>    | <span data-ttu-id="84aa3-309">Указывает учетные записи пользователей, которым разрешено или запрещено разрешение на запуск этого компонента.</span><span class="sxs-lookup"><span data-stu-id="84aa3-309">Specifies user accounts that are allowed or denied permission to start this component.</span></span> |
| <span data-ttu-id="84aa3-310">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-310">Access</span></span>         | <span data-ttu-id="84aa3-311">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-311">ReadWrite</span></span>                                                                              |
| <span data-ttu-id="84aa3-312">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-312">Type</span></span>           | <span data-ttu-id="84aa3-313">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-313">String</span></span>                                                                                 |
| <span data-ttu-id="84aa3-314">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-314">Default</span></span>        | <span data-ttu-id="84aa3-315">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-315">N/A</span></span>                                                                                    |
| <span data-ttu-id="84aa3-316">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-316">Minimum system</span></span> | <span data-ttu-id="84aa3-317">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-317">Windows XP</span></span>                                                                             |



 

### <a name="localserver32"></a><span data-ttu-id="84aa3-318">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="84aa3-318">LocalServer32</span></span>



| <span data-ttu-id="84aa3-319">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-319">Entry</span></span> | <span data-ttu-id="84aa3-320">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-320">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-321">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-321">Description</span></span>    | <span data-ttu-id="84aa3-322">Указывает полный путь к 32-битному локальному серверному приложению.</span><span class="sxs-lookup"><span data-stu-id="84aa3-322">Specifies the full path to a 32-bit local server application.</span></span> <span data-ttu-id="84aa3-323">Чтобы защитить систему безопасности системы, используйте заключенные в кавычки строки в пути, чтобы указать, где заканчивается имя исполняемого файла и начинаются аргументы.</span><span class="sxs-lookup"><span data-stu-id="84aa3-323">To help protect system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="84aa3-324">Например, " \\ " C: \\ Program Files \\ Files \\Application.exe\\ "param1 Param2".</span><span class="sxs-lookup"><span data-stu-id="84aa3-324">For example, "\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2".</span></span> |
| <span data-ttu-id="84aa3-325">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-325">Access</span></span>         | <span data-ttu-id="84aa3-326">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-326">ReadWrite</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="84aa3-327">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-327">Type</span></span>           | <span data-ttu-id="84aa3-328">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-328">String</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="84aa3-329">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-329">Default</span></span>        | <span data-ttu-id="84aa3-330">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-330">N/A</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="84aa3-331">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-331">Minimum system</span></span> | <span data-ttu-id="84aa3-332">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-332">Windows XP</span></span>                                                                                                                                                                                                                                                                                  |



 

### <a name="localservice"></a><span data-ttu-id="84aa3-333">локальная служба.</span><span class="sxs-lookup"><span data-stu-id="84aa3-333">LocalService</span></span>



| <span data-ttu-id="84aa3-334">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-334">Entry</span></span> | <span data-ttu-id="84aa3-335">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-335">Value</span></span> |
|----------------|-----------------------------------------------------|
| <span data-ttu-id="84aa3-336">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-336">Description</span></span>    | <span data-ttu-id="84aa3-337">Указывает полный путь к приложению службы.</span><span class="sxs-lookup"><span data-stu-id="84aa3-337">Specifies the full path to the service application.</span></span> |
| <span data-ttu-id="84aa3-338">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-338">Access</span></span>         | <span data-ttu-id="84aa3-339">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-339">ReadWrite</span></span>                                           |
| <span data-ttu-id="84aa3-340">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-340">Type</span></span>           | <span data-ttu-id="84aa3-341">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-341">String</span></span>                                              |
| <span data-ttu-id="84aa3-342">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-342">Default</span></span>        | <span data-ttu-id="84aa3-343">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-343">N/A</span></span>                                                 |
| <span data-ttu-id="84aa3-344">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-344">Minimum system</span></span> | <span data-ttu-id="84aa3-345">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-345">Windows XP</span></span>                                          |



 

### <a name="password"></a><span data-ttu-id="84aa3-346">Пароль</span><span class="sxs-lookup"><span data-stu-id="84aa3-346">Password</span></span>



| <span data-ttu-id="84aa3-347">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-347">Entry</span></span> | <span data-ttu-id="84aa3-348">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-348">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-349">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-349">Description</span></span>    | <span data-ttu-id="84aa3-350">Задает пароль, используемый процессом сервера для входа в систему с указанным удостоверением запуска от имени.</span><span class="sxs-lookup"><span data-stu-id="84aa3-350">Sets the password used by the server process to log on under the specified RunAs identity.</span></span> <span data-ttu-id="84aa3-351">Пароль должен быть задан в то же время, что и идентификатор запуска от имени, до использования команды [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), так как пароль и удостоверение проверяются перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="84aa3-351">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="84aa3-352">Если пароль и удостоверение не будут синхронизированы, компонент нельзя будет запустить до тех пор, пока администратор не запустит их.</span><span class="sxs-lookup"><span data-stu-id="84aa3-352">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="84aa3-353">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-353">Access</span></span>         | <span data-ttu-id="84aa3-354">WriteOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-354">WriteOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="84aa3-355">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-355">Type</span></span>           | <span data-ttu-id="84aa3-356">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-356">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="84aa3-357">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-357">Default</span></span>        | <span data-ttu-id="84aa3-358">NULL</span><span class="sxs-lookup"><span data-stu-id="84aa3-358">NULL</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="84aa3-359">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-359">Minimum system</span></span> | <span data-ttu-id="84aa3-360">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-360">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="progid"></a><span data-ttu-id="84aa3-361">ProgID:</span><span class="sxs-lookup"><span data-stu-id="84aa3-361">ProgID</span></span>



| <span data-ttu-id="84aa3-362">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-362">Entry</span></span> | <span data-ttu-id="84aa3-363">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-363">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-364">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-364">Description</span></span>    | <span data-ttu-id="84aa3-365">Имя, идентифицирующее компонент.</span><span class="sxs-lookup"><span data-stu-id="84aa3-365">A name identifying the component.</span></span> <span data-ttu-id="84aa3-366">Это свойство возвращается при вызове метода свойства Name для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="84aa3-366">This property is returned when the Name property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="84aa3-367">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-367">Access</span></span>         | <span data-ttu-id="84aa3-368">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-368">ReadOnly</span></span>                                                                                                                             |
| <span data-ttu-id="84aa3-369">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-369">Type</span></span>           | <span data-ttu-id="84aa3-370">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-370">String</span></span>                                                                                                                               |
| <span data-ttu-id="84aa3-371">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-371">Default</span></span>        | <span data-ttu-id="84aa3-372">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-372">N/A</span></span>                                                                                                                                  |
| <span data-ttu-id="84aa3-373">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-373">Minimum system</span></span> | <span data-ttu-id="84aa3-374">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-374">Windows XP</span></span>                                                                                                                           |



 

### <a name="remoteserver"></a><span data-ttu-id="84aa3-375">RemoteServer</span><span class="sxs-lookup"><span data-stu-id="84aa3-375">RemoteServer</span></span>



| <span data-ttu-id="84aa3-376">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-376">Entry</span></span> | <span data-ttu-id="84aa3-377">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-377">Value</span></span> |
|----------------|---------------------------------------|
| <span data-ttu-id="84aa3-378">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-378">Description</span></span>    | <span data-ttu-id="84aa3-379">Указывает компьютер удаленного сервера.</span><span class="sxs-lookup"><span data-stu-id="84aa3-379">Specifies the remote server computer.</span></span> |
| <span data-ttu-id="84aa3-380">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-380">Access</span></span>         | <span data-ttu-id="84aa3-381">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-381">ReadWrite</span></span>                             |
| <span data-ttu-id="84aa3-382">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-382">Type</span></span>           | <span data-ttu-id="84aa3-383">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-383">String</span></span>                                |
| <span data-ttu-id="84aa3-384">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-384">Default</span></span>        | <span data-ttu-id="84aa3-385">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-385">N/A</span></span>                                   |
| <span data-ttu-id="84aa3-386">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-386">Minimum system</span></span> | <span data-ttu-id="84aa3-387">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-387">Windows XP</span></span>                            |



 

### <a name="runas"></a><span data-ttu-id="84aa3-388">RunAs</span><span class="sxs-lookup"><span data-stu-id="84aa3-388">RunAs</span></span>



| <span data-ttu-id="84aa3-389">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-389">Entry</span></span> | <span data-ttu-id="84aa3-390">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-390">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-391">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-391">Description</span></span>    | <span data-ttu-id="84aa3-392">Указывает пользователя, удостоверение которого будет выполняться компонентом.</span><span class="sxs-lookup"><span data-stu-id="84aa3-392">Specifies the user under whose identity the component will run.</span></span> <span data-ttu-id="84aa3-393">Пароль должен быть задан в то же время, что и идентификатор запуска от имени, до использования команды [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), так как пароль и удостоверение проверяются перед сохранением.</span><span class="sxs-lookup"><span data-stu-id="84aa3-393">Password should be set at the same time as the RunAs identity, prior to using [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), because the password and identity are validated before being saved.</span></span> <span data-ttu-id="84aa3-394">Если пароль и удостоверение не будут синхронизированы, компонент нельзя будет запустить до тех пор, пока администратор не запустит их.</span><span class="sxs-lookup"><span data-stu-id="84aa3-394">If the password and identity get out of sync, the component cannot be launched until they are reset by an administrator.</span></span> |
| <span data-ttu-id="84aa3-395">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-395">Access</span></span>         | <span data-ttu-id="84aa3-396">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-396">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="84aa3-397">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-397">Type</span></span>           | <span data-ttu-id="84aa3-398">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-398">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="84aa3-399">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-399">Default</span></span>        | <span data-ttu-id="84aa3-400">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-400">N/A</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="84aa3-401">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-401">Minimum system</span></span> | <span data-ttu-id="84aa3-402">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-402">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |



 

### <a name="serviceparameter"></a><span data-ttu-id="84aa3-403">сервицепараметер</span><span class="sxs-lookup"><span data-stu-id="84aa3-403">ServiceParameter</span></span>



| <span data-ttu-id="84aa3-404">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-404">Entry</span></span> | <span data-ttu-id="84aa3-405">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-405">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-406">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-406">Description</span></span>    | <span data-ttu-id="84aa3-407">Указывает параметры, передаваемые в приложение при вызове в качестве приложения службы.</span><span class="sxs-lookup"><span data-stu-id="84aa3-407">Specifies the parameters passed to the application when invoked as a service application.</span></span> |
| <span data-ttu-id="84aa3-408">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-408">Access</span></span>         | <span data-ttu-id="84aa3-409">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-409">ReadWrite</span></span>                                                                                 |
| <span data-ttu-id="84aa3-410">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-410">Type</span></span>           | <span data-ttu-id="84aa3-411">Строка</span><span class="sxs-lookup"><span data-stu-id="84aa3-411">String</span></span>                                                                                    |
| <span data-ttu-id="84aa3-412">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-412">Default</span></span>        | <span data-ttu-id="84aa3-413">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-413">N/A</span></span>                                                                                       |
| <span data-ttu-id="84aa3-414">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-414">Minimum system</span></span> | <span data-ttu-id="84aa3-415">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-415">Windows XP</span></span>                                                                                |



 

### <a name="srptrustlevel"></a><span data-ttu-id="84aa3-416">срптрустлевел</span><span class="sxs-lookup"><span data-stu-id="84aa3-416">SRPTrustLevel</span></span>



| <span data-ttu-id="84aa3-417">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-417">Entry</span></span> | <span data-ttu-id="84aa3-418">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-418">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-419">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-419">Description</span></span>    | <span data-ttu-id="84aa3-420">Указывает уровень доверия для компонента в политике ограниченного использования программ (SRP).</span><span class="sxs-lookup"><span data-stu-id="84aa3-420">Indicates the software restriction policy (SRP) trust level of the component.</span></span> <span data-ttu-id="84aa3-421">Уровень доверия SRP относится к уровню доверия, который вы желаете присвоить компоненту.</span><span class="sxs-lookup"><span data-stu-id="84aa3-421">The SRP trust level refers to the level of trust that you are willing to give to a component.</span></span> <span data-ttu-id="84aa3-422">Неограниченный уровень доверия SRP соответствует более безопасному \_ \_ значению перечисления LEVELID фуллитрустед, а недопустимый уровень доверия SRP соответствует более безопасному \_ \_ неразрешенному значению LEVELID.</span><span class="sxs-lookup"><span data-stu-id="84aa3-422">An Unrestricted SRP trust level corresponds to the SAFER\_LEVELID\_FULLYTRUSTED enum value, while a Disallowed SRP trust level corresponds to the SAFER\_LEVELID\_DISALLOWED enum value.</span></span> <span data-ttu-id="84aa3-423">Перечисление уровней доверия определяется в Винсафер. h.</span><span class="sxs-lookup"><span data-stu-id="84aa3-423">The enumeration for the trust levels is defined in Winsafer.h.</span></span> |
| <span data-ttu-id="84aa3-424">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-424">Access</span></span>         | <span data-ttu-id="84aa3-425">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="84aa3-425">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="84aa3-426">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-426">Type</span></span>           | <span data-ttu-id="84aa3-427">Допустимые значения: БЕЗОПАСная \_ LEVELID \_ запрещена (0x0) более безопасная \_ LEVELID \_ фуллитрустед (0x40000)</span><span class="sxs-lookup"><span data-stu-id="84aa3-427">Long Possible values:SAFER\_LEVELID\_DISALLOWED (0x0)SAFER\_LEVELID\_FULLYTRUSTED (0x40000)</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="84aa3-428">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-428">Default</span></span>        | <span data-ttu-id="84aa3-429">более безопасный \_ LEVELID \_ фуллитрустед</span><span class="sxs-lookup"><span data-stu-id="84aa3-429">SAFER\_LEVELID\_FULLYTRUSTED</span></span>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="84aa3-430">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-430">Minimum system</span></span> | <span data-ttu-id="84aa3-431">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-431">Windows XP</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

<span data-ttu-id="84aa3-432">Компонент, который вы готовы к доверию с неограниченным доступом, должен иметь наиболее строгий уровень безопасности, подключенный к нему.</span><span class="sxs-lookup"><span data-stu-id="84aa3-432">A component that you are willing to trust with Unrestricted access should have the most stringent security attached to it.</span></span> <span data-ttu-id="84aa3-433">Приложения, которые не ограничены, могут загружать только неограниченные компоненты, в то время как запрещенные приложения не будут запускаться и поэтому не смогут загрузить какие бы то ни было компоненты.</span><span class="sxs-lookup"><span data-stu-id="84aa3-433">Applications that are Unrestricted can load only unrestricted components, while Disallowed applications will not be allowed to run and therefore cannot load any components.</span></span>

### <a name="threadingmodel"></a><span data-ttu-id="84aa3-434">ThreadingModel.</span><span class="sxs-lookup"><span data-stu-id="84aa3-434">ThreadingModel</span></span>



| <span data-ttu-id="84aa3-435">Ввод</span><span class="sxs-lookup"><span data-stu-id="84aa3-435">Entry</span></span> | <span data-ttu-id="84aa3-436">Значение</span><span class="sxs-lookup"><span data-stu-id="84aa3-436">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84aa3-437">Описание</span><span class="sxs-lookup"><span data-stu-id="84aa3-437">Description</span></span>    | <span data-ttu-id="84aa3-438">Определяет, как экземпляры компонента назначаются потокам для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="84aa3-438">Determines how instances of the component are assigned to threads for method execution.</span></span> <span data-ttu-id="84aa3-439">Значения соответствуют моделям потоков COM.</span><span class="sxs-lookup"><span data-stu-id="84aa3-439">Values correspond to COM threading models.</span></span>                                                  |
| <span data-ttu-id="84aa3-440">Access</span><span class="sxs-lookup"><span data-stu-id="84aa3-440">Access</span></span>         | <span data-ttu-id="84aa3-441">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="84aa3-441">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="84aa3-442">Тип</span><span class="sxs-lookup"><span data-stu-id="84aa3-442">Type</span></span>           | <span data-ttu-id="84aa3-443">Длинные возможные значения: Комадминсреадингмоделапартмент (0) Комадминсреадингмоделфри (1) Комадминсреадингмоделмаин (2) COMAdminThreadingModelBoth (3) COMAdminThreadingModelNeutral (4)</span><span class="sxs-lookup"><span data-stu-id="84aa3-443">Long Possible values:COMAdminThreadingModelApartment (0)COMAdminThreadingModelFree (1)COMAdminThreadingModelMain (2)COMAdminThreadingModelBoth (3)COMAdminThreadingModelNeutral (4)</span></span> |
| <span data-ttu-id="84aa3-444">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="84aa3-444">Default</span></span>        | <span data-ttu-id="84aa3-445">Н/Д</span><span class="sxs-lookup"><span data-stu-id="84aa3-445">N/A</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="84aa3-446">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="84aa3-446">Minimum system</span></span> | <span data-ttu-id="84aa3-447">Windows XP</span><span class="sxs-lookup"><span data-stu-id="84aa3-447">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="84aa3-448">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84aa3-448">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84aa3-449">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="84aa3-449">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
