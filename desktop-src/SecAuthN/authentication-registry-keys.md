---
description: При установке поставщика сети приложение должно создать разделы реестра и значения, описанные в этом разделе.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Разделы реестра для проверки подлинности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998728"
---
# <a name="authentication-registry-keys"></a><span data-ttu-id="bb53b-103">Разделы реестра для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="bb53b-103">Authentication Registry Keys</span></span>

<span data-ttu-id="bb53b-104">При установке поставщика сети приложение должно создать разделы реестра и значения, описанные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="bb53b-104">When it installs a network provider, your application should create the registry keys and values described in this topic.</span></span> <span data-ttu-id="bb53b-105">Эти ключи и значения предоставляют многопротокольному маршрутизатору сведения о сетевых поставщиках, установленных в системе.</span><span class="sxs-lookup"><span data-stu-id="bb53b-105">These keys and values provide information to the MPR about the network providers installed on the system.</span></span> <span data-ttu-id="bb53b-106">Многопротокольный маршрутизатор проверяет эти ключи при запуске и загружает найденные библиотеки DLL поставщика сети.</span><span class="sxs-lookup"><span data-stu-id="bb53b-106">The MPR checks these keys when it starts and loads the network provider DLLs that it finds.</span></span>

<span data-ttu-id="bb53b-107">Перед созданием набора ключей для хранения сведений о поставщике сети следует добавить имя поставщика сети в ключ **Order** .</span><span class="sxs-lookup"><span data-stu-id="bb53b-107">Before you create a set of keys to hold information about your network provider, you should add the name of your network provider to the **order** key.</span></span> <span data-ttu-id="bb53b-108">Этот ключ является подразделом следующего раздела:</span><span class="sxs-lookup"><span data-stu-id="bb53b-108">This key is a subkey of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

<span data-ttu-id="bb53b-109">Ключ **заказа** содержит одно значение, **провидерордер**, в котором перечислены установленные поставщики и указывается порядок, в котором они должны быть предприняты во время операций, которые циклически проходят через поставщиков, пока не будет найден принимающий поставщик.</span><span class="sxs-lookup"><span data-stu-id="bb53b-109">The **order** key contains a single value, **ProviderOrder**, which lists the installed providers and specifies the order in which they should be tried during operations that cycle through providers until an accepting provider is found.</span></span>

<span data-ttu-id="bb53b-110">Значение **провидерордер** содержит разделенный запятыми список имен ключей.</span><span class="sxs-lookup"><span data-stu-id="bb53b-110">The **ProviderOrder** value contains a comma-separated list of key names.</span></span> <span data-ttu-id="bb53b-111">Каждое имя ключа в **провидерордер** идентифицирует поставщик сети.</span><span class="sxs-lookup"><span data-stu-id="bb53b-111">Each key name in **ProviderOrder** identifies a network provider.</span></span> <span data-ttu-id="bb53b-112">Когда многопротокольный цикл проходит через поставщиков, он вызывает их в том порядке, в котором они отображаются в этом списке.</span><span class="sxs-lookup"><span data-stu-id="bb53b-112">When MPR cycles through the providers, it calls them in the order in which they appear in this list.</span></span>

<span data-ttu-id="bb53b-113">Имя поставщика, заданное в **провидерордер** , должно также использоваться в качестве имени раздела реестра, содержащего сведения об этом поставщике.</span><span class="sxs-lookup"><span data-stu-id="bb53b-113">The provider name set in **ProviderOrder** should also be used as the name of the registry key that contains information about that provider.</span></span> <span data-ttu-id="bb53b-114">Разделы реестра, относящиеся к поставщику, создаются в виде подразделов следующего раздела:</span><span class="sxs-lookup"><span data-stu-id="bb53b-114">The provider-specific registry keys are created as subkeys of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="bb53b-115">Иными словами, имена поставщиков, указанные в **провидерордер** , являются путем к реестру разделов, относящихся к поставщику сетевых услуг, относительно следующего пути:</span><span class="sxs-lookup"><span data-stu-id="bb53b-115">In other words, the provider names specified in **ProviderOrder** are the path to the registry of the network provider-specific keys, relative to the following path:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="bb53b-116">При установке службы поставщика сети приложение установки должно добавить ключ следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bb53b-116">When your network provider service is installed, the installation application should add a key as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

<span data-ttu-id="bb53b-117">Где *providerName* — имя поставщика сети, указанное в значении **провидерордер** ключа **заказа** .</span><span class="sxs-lookup"><span data-stu-id="bb53b-117">Where *ProviderName* is the name of the network provider as specified in the **ProviderOrder** value of the **order** key.</span></span> <span data-ttu-id="bb53b-118">Значение **группы** в ключе *providerName* должно быть равно "нетворкпровидер".</span><span class="sxs-lookup"><span data-stu-id="bb53b-118">The **Group** value under the *ProviderName* key should be set to "NetworkProvider".</span></span> <span data-ttu-id="bb53b-119">Это идентифицирует службу в группе "поставщик сети".</span><span class="sxs-lookup"><span data-stu-id="bb53b-119">This identifies the service as being in the network provider group.</span></span>

<span data-ttu-id="bb53b-120">Также необходимо создать подраздел с *providerName*, **нетворкпровидер**.</span><span class="sxs-lookup"><span data-stu-id="bb53b-120">You must also create a subkey of *ProviderName*, **networkprovider**.</span></span> <span data-ttu-id="bb53b-121">Этот раздел содержит следующие значения, описывающие поставщик сети.</span><span class="sxs-lookup"><span data-stu-id="bb53b-121">This key contains the following values that describe the network provider.</span></span>



| <span data-ttu-id="bb53b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="bb53b-122">Value</span></span>                       | <span data-ttu-id="bb53b-123">Описание</span><span class="sxs-lookup"><span data-stu-id="bb53b-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb53b-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="bb53b-124">**Name**</span></span><br/>         | <span data-ttu-id="bb53b-125">Содержит имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="bb53b-125">Contains the name of the provider.</span></span> <span data-ttu-id="bb53b-126">Это имя отображается пользователю как имя сети в диалоговых окнах обзор и должно соответствовать полю **лппровидер** , возвращенному в структурах [**нетресаурце**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) .</span><span class="sxs-lookup"><span data-stu-id="bb53b-126">This name is displayed to the user as the name of the network in the browse dialog boxes and should match the **lpProvider** field returned in [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures.</span></span> <span data-ttu-id="bb53b-127">Это имя должно быть некоторым вариантом названия продукта, желательно с указанием компании, чтобы оно было понятным и уникальным.</span><span class="sxs-lookup"><span data-stu-id="bb53b-127">This name should be some variation of the product name, preferably with some indication of the company as well, so that it is clear and unique.</span></span> <span data-ttu-id="bb53b-128">"MS-LanMan", например, является хорошим именем, тогда как "сеть" будет неудовлетворительным выбором.</span><span class="sxs-lookup"><span data-stu-id="bb53b-128">"MS-LanMan" for example is a good name, whereas "The Net" would be a poor choice.</span></span><br/> |
| <span data-ttu-id="bb53b-129">**провидерпас**</span><span class="sxs-lookup"><span data-stu-id="bb53b-129">**ProviderPath**</span></span><br/> | <span data-ttu-id="bb53b-130">Содержит полный путь библиотеки DLL, которая реализует поставщик сети.</span><span class="sxs-lookup"><span data-stu-id="bb53b-130">Contains the full path of the DLL that implements the network provider.</span></span> <span data-ttu-id="bb53b-131">Многопротокольный вызов [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) по этому пути.</span><span class="sxs-lookup"><span data-stu-id="bb53b-131">MPR calls [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) on this path.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="bb53b-132">Следующие значения используются только поставщиками сети, которые поддерживают функции управления учетными данными [**нплогоннотифи**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) и [**нппассвордчанженотифи**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span><span class="sxs-lookup"><span data-stu-id="bb53b-132">The following values are used only by network providers that support the credential management functions, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span></span>



| <span data-ttu-id="bb53b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bb53b-133">Value</span></span>                              | <span data-ttu-id="bb53b-134">Описание</span><span class="sxs-lookup"><span data-stu-id="bb53b-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb53b-135">**Класс**</span><span class="sxs-lookup"><span data-stu-id="bb53b-135">**Class**</span></span><br/>               | <span data-ttu-id="bb53b-136">**DWORD** , определяющий класс или тип функций поставщика, поддерживаемых этим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="bb53b-136">A **DWORD** that identifies the class, or type, of provider functionality that this provider supports.</span></span> <span data-ttu-id="bb53b-137">При необходимости значения могут быть соединены оператором **или** .</span><span class="sxs-lookup"><span data-stu-id="bb53b-137">Values may be joined by the **OR** operator when appropriate.</span></span> <span data-ttu-id="bb53b-138">Допустимыми значениями для этого являются \_ класс WN Network \_ , класс \_ учетных данных WN \_ , класс WN \_ PRIMARY \_ аусент \_ и \_ класс службы WN \_ .</span><span class="sxs-lookup"><span data-stu-id="bb53b-138">Valid values for this are WN\_NETWORK\_CLASS, WN\_CREDENTIAL\_CLASS, WN\_PRIMARY\_AUTHENT\_CLASS, and WN\_SERVICE\_CLASS.</span></span><br/> <span data-ttu-id="bb53b-139">Несмотря на то, что поставщик может поддерживать функциональность основного средства проверки подлинности, для определения основного средства проверки подлинности будет использоваться другое средство.</span><span class="sxs-lookup"><span data-stu-id="bb53b-139">Although a provider may support primary authenticator functionality, another means will be used to determine which authenticator is primary.</span></span><br/> <span data-ttu-id="bb53b-140">**Windows XP и 2000:** Переключение основного средства проверки подлинности не поддерживается, поэтому это значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bb53b-140">**Windows XP/2000:** Switching primary authenticators is not supported, so this value is ignored.</span></span> <br/> |
| <span data-ttu-id="bb53b-141">**аусентпровидерпас**</span><span class="sxs-lookup"><span data-stu-id="bb53b-141">**AuthentProviderPath**</span></span><br/> | <span data-ttu-id="bb53b-142">Это полное имя файла библиотеки DLL, в которой экспортируются функции управления учетными данными.</span><span class="sxs-lookup"><span data-stu-id="bb53b-142">This is the fully qualified file name for the DLL that exports the Credential Management Functions.</span></span> <span data-ttu-id="bb53b-143">Это значение полезно (но не требуется), только если поставщик определен как класс УЧЕТных данных \_ или поставщик первичного \_ аусент \_ класса.</span><span class="sxs-lookup"><span data-stu-id="bb53b-143">This value is useful (but not required) only when the provider is identified as being a CREDENTIAL\_CLASS or PRIMARY\_AUTHENT\_CLASS provider.</span></span> <span data-ttu-id="bb53b-144">Если это значение отсутствует для поставщика этого класса, предполагается, что функции управления учетными данными должны быть экспортированы из библиотеки DLL, определяемой значением Провидерпас.</span><span class="sxs-lookup"><span data-stu-id="bb53b-144">If this value is not present for a provider of this class, the credential management functions are expected to be exported from the DLL identified by the ProviderPath value.</span></span> <span data-ttu-id="bb53b-145">Это значение используется только в том случае, если желательно упаковать сетевые функции и функции диспетчера учетных данных в отдельных библиотеках DLL.</span><span class="sxs-lookup"><span data-stu-id="bb53b-145">This value is used only if it is desirable to package the network functions and the credential manager functions in separate DLLs.</span></span><br/>  |



 

<span data-ttu-id="bb53b-146">В дополнение к значениям, используемым для регистрации поставщиков сетевых услуг и диспетчеров учетных данных, можно добавить значение в реестр, чтобы зарегистрировать библиотеку DLL для получения уведомлений о подключении.</span><span class="sxs-lookup"><span data-stu-id="bb53b-146">In addition to the values used to register network providers and credential managers, you can add a value to the registry to register a DLL to receive connection notifications.</span></span> <span data-ttu-id="bb53b-147">Для этого создайте \_ значение reg Expand \_ SZ в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="bb53b-147">To do so, create a REG\_EXPAND\_SZ value under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

<span data-ttu-id="bb53b-148">Это значение должно указывать путь к библиотеке DLL, реализующей [API уведомления о соединении](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="bb53b-148">This value should specify the path to a DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span> <span data-ttu-id="bb53b-149">Имя этого значения может быть любым, если оно не конфликтует с уже существующими именами значений.</span><span class="sxs-lookup"><span data-stu-id="bb53b-149">The name of this value can be anything you want, as long as it does not conflict with preexisting value names.</span></span>

## <a name="example"></a><span data-ttu-id="bb53b-150">Пример</span><span class="sxs-lookup"><span data-stu-id="bb53b-150">Example</span></span>

<span data-ttu-id="bb53b-151">В следующем примере показаны разделы реестра для системы с двумя установленными поставщиками сети: LanmanWorkStation и Аносернетсвк.</span><span class="sxs-lookup"><span data-stu-id="bb53b-151">The following example shows the registry keys for a system that has two network providers installed: LanmanWorkStation and AnotherNetSvc.</span></span> <span data-ttu-id="bb53b-152">Аносернетсвк также является диспетчером учетных данных.</span><span class="sxs-lookup"><span data-stu-id="bb53b-152">AnotherNetSvc is also a credential manager.</span></span> <span data-ttu-id="bb53b-153">В этом примере имена ключей имеют полужирное начертание, а имена значений — курсивом.</span><span class="sxs-lookup"><span data-stu-id="bb53b-153">In the example, key names are bold and value names are italic.</span></span>

<span data-ttu-id="bb53b-154">**HKey \_ \_** \\  \\  \\  \\  \\ **Порядок** нетворкпровидер управления CurrentControlSet системы локального компьютера</span><span class="sxs-lookup"><span data-stu-id="bb53b-154">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**order**</span></span>

<span data-ttu-id="bb53b-155">*Провидерордер* = "LanmanWorkStation, аносернетсвк"</span><span class="sxs-lookup"><span data-stu-id="bb53b-155">*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"</span></span>

<span data-ttu-id="bb53b-156">**HKey \_ Локальный \_ компьютер** \\ **система** \\ **CurrentControlSet** \\ **элемент управления** \\ **нетворкпровидер** \\ **нотифеес**</span><span class="sxs-lookup"><span data-stu-id="bb53b-156">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="bb53b-157">*Минотифяпп* = "c: \\ подключение \\connect.dll"</span><span class="sxs-lookup"><span data-stu-id="bb53b-157">*MyNotifyApp* = "c:\\connect\\connect.dll"</span></span>

<span data-ttu-id="bb53b-158">**HKey \_ Локальная система \_ машинного** \\  \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation**</span><span class="sxs-lookup"><span data-stu-id="bb53b-158">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**</span></span>\\

<span data-ttu-id="bb53b-159">*Group* = "нетворкпровидер"</span><span class="sxs-lookup"><span data-stu-id="bb53b-159">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="bb53b-160">**HKey \_ Локальный \_ компьютер** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **нетворкпровидер**</span><span class="sxs-lookup"><span data-stu-id="bb53b-160">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**\\**NetworkProvider**</span></span>

<span data-ttu-id="bb53b-161">*Name* = "NT LanMan"*провидерпас* = "ntlanman.dll"</span><span class="sxs-lookup"><span data-stu-id="bb53b-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span></span>

<span data-ttu-id="bb53b-162">*Class* = 0x00000001 ( \_ класс WN Network \_ )</span><span class="sxs-lookup"><span data-stu-id="bb53b-162">*Class* = 0x00000001 (WN\_NETWORK\_CLASS)</span></span>

<span data-ttu-id="bb53b-163">**HKey \_ Локальная система \_ машинного** \\  \\ **CurrentControlSet** \\ **Services** \\ **аносернетсвк**</span><span class="sxs-lookup"><span data-stu-id="bb53b-163">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**</span></span>\\

<span data-ttu-id="bb53b-164">*Group* = "нетворкпровидер"</span><span class="sxs-lookup"><span data-stu-id="bb53b-164">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="bb53b-165">**HKey \_ Локальный \_ компьютер** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **аносернетсвк** \\ **нетворкпровидер**</span><span class="sxs-lookup"><span data-stu-id="bb53b-165">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**\\**NetworkProvider**</span></span>

<span data-ttu-id="bb53b-166">*Name* = "другая сеть"*провидерпас* = "c: \\ другой \\anet.dll"</span><span class="sxs-lookup"><span data-stu-id="bb53b-166">*Name* = "Another Network"*ProviderPath* = "c:\\another\\anet.dll"</span></span>

<span data-ttu-id="bb53b-167">*Class* = 0x00000003 (класс \_ \_ \| \_ учетных данных класса WN Network WN \_ )</span><span class="sxs-lookup"><span data-stu-id="bb53b-167">*Class* = 0x00000003 (WN\_NETWORK\_CLASS \| WN\_CREDENTIAL\_CLASS)</span></span>

<span data-ttu-id="bb53b-168">*Аусентпровидерпас* = "c: \\ другой \\anetCM.dll"</span><span class="sxs-lookup"><span data-stu-id="bb53b-168">*AuthentProviderPath* = "c:\\another\\anetCM.dll"</span></span>

 

