---
description: Регистрирует сведения о физической реализации поставщика в WMI. Поставщики, не устанавливающие свойство Хостингмодел, по умолчанию загружаются в процесс Wmiprvse.exe как Нетворксервицехосторселфхост.
ms.assetid: 41e0d938-00c6-4f4c-8027-8b8512398dee
ms.tgt_platform: multiple
title: Класс __Win32Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0240c459ea2d09013379bfd7c3190ce691cf4cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999382"
---
# <a name="__win32provider-class"></a><span data-ttu-id="18cd6-104">\_\_Класс Win32Provider</span><span class="sxs-lookup"><span data-stu-id="18cd6-104">\_\_Win32Provider class</span></span>

<span data-ttu-id="18cd6-105">Системный класс **\_ \_ Win32Provider** регистрирует сведения о физической реализации поставщика в WMI.</span><span class="sxs-lookup"><span data-stu-id="18cd6-105">The **\_\_Win32Provider** system class registers information about the physical implementation of a provider in WMI.</span></span> <span data-ttu-id="18cd6-106">Поставщики, не устанавливающие свойство **хостингмодел** , по умолчанию загружаются в процесс Wmiprvse.exe как **нетворксервицехосторселфхост**.</span><span class="sxs-lookup"><span data-stu-id="18cd6-106">Providers that do not set the **HostingModel** property are loaded, by default, to run in a Wmiprvse.exe process as **NetworkServiceHostOrSelfHost**.</span></span>

<span data-ttu-id="18cd6-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="18cd6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="18cd6-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="18cd6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="18cd6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18cd6-109">Syntax</span></span>

``` syntax
class __Win32Provider : __Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  string   HostingModel;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy;
  datetime InitializationTimeoutInterval;
  boolean  InitializeAsAdminFirst;
  string   Name;
  datetime OperationTimeoutInterval;
  boolean  PerLocaleInitialization = FALSE;
  boolean  PerUserInitialization = FALSE;
  boolean  Pure = TRUE;
  string   SecurityDescriptor;
  boolean  SupportsExplicitShutdown;
  boolean  SupportsExtendedStatus;
  boolean  SupportsQuotas;
  boolean  SupportsSendStatus;
  boolean  SupportsShutdown;
  boolean  SupportsThrottling;
  datetime UnloadTimeout;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="18cd6-110">Члены</span><span class="sxs-lookup"><span data-stu-id="18cd6-110">Members</span></span>

<span data-ttu-id="18cd6-111">Класс **\_ \_ Win32Provider** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18cd6-111">The **\_\_Win32Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="18cd6-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="18cd6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18cd6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="18cd6-113">Properties</span></span>

<span data-ttu-id="18cd6-114">Класс **\_ \_ Win32Provider** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18cd6-114">The **\_\_Win32Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18cd6-115">**клиентлоадаблеклсид**</span><span class="sxs-lookup"><span data-stu-id="18cd6-115">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18cd6-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-118">Идентификатор класса, используемый WMI для определения необходимости загрузки высокопроизводительного поставщика в клиентский процесс или в процесс WMI.</span><span class="sxs-lookup"><span data-stu-id="18cd6-118">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="18cd6-119">Если поставщик и клиент расположены на одном компьютере, WMI загружает поставщик в процессе в клиенте с помощью **клиентлоадаблеклсид** в качестве идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="18cd6-119">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="18cd6-120">Когда поставщик и клиент расположены на разных компьютерах, Инструментарий WMI загружает поставщик в службу WMI.</span><span class="sxs-lookup"><span data-stu-id="18cd6-120">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="18cd6-121">Инструментарий WMI также использует **клиентлоадаблеклсид** для поддержки операций обновления.</span><span class="sxs-lookup"><span data-stu-id="18cd6-121">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="18cd6-122">Дополнительные сведения см [. в разделе Регистрация поставщика High-Performance.](registering-a-high-performance-provider.md)</span><span class="sxs-lookup"><span data-stu-id="18cd6-122">For more information, see [Registering a High-Performance Provider.](registering-a-high-performance-provider.md)</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-123">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="18cd6-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18cd6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-126">Идентификатор **GUID** , представляющий идентификатор класса (**CLSID**) COM-объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="18cd6-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="18cd6-127">Этот COM-объект должен содержать реализацию интерфейса [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="18cd6-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-128">**Параллелизм**</span><span class="sxs-lookup"><span data-stu-id="18cd6-128">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="18cd6-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-131">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-131">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-132">**дефаултмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="18cd6-132">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18cd6-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-135">Определяет компьютер, на котором будет запущен поставщик.</span><span class="sxs-lookup"><span data-stu-id="18cd6-135">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="18cd6-136">Если поставщик запущен на локальном компьютере, он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="18cd6-136">If the provider runs on the local computer it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-137">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="18cd6-137">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-140">Если **значение — true**, этот экземпляр включен и может использоваться для выполнения клиентских запросов.</span><span class="sxs-lookup"><span data-stu-id="18cd6-140">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-141">**хостингмодел**</span><span class="sxs-lookup"><span data-stu-id="18cd6-141">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18cd6-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-144">Это свойство состоит из значений из свойств **хостингграуп** и **хостингспеЦификатион** [**\_ поставщиков MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .</span><span class="sxs-lookup"><span data-stu-id="18cd6-144">This property is composed of values from the [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) **HostingGroup** and **HostingSpecification** properties.</span></span> <span data-ttu-id="18cd6-145">Значение этого свойства указывает, как WMI загружает поставщик и учетную запись безопасности, под которой он выполняется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-145">The value of this property specifies how WMI loads the provider and the security account it runs under.</span></span> <span data-ttu-id="18cd6-146">Дополнительные сведения о настройке свойства **хостингмодел** см. в разделе [Размещение поставщика и безопасность](provider-hosting-and-security.md) и [Регистрация поставщика](registering-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="18cd6-146">For more information about setting the **HostingModel** property, see [Provider Hosting and Security](provider-hosting-and-security.md) and [Registering a Provider](registering-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-147">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="18cd6-147">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-148">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="18cd6-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-150">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="18cd6-150">Reserved.</span></span> <span data-ttu-id="18cd6-151">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="18cd6-151">The default value is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-152">**инитиализатионринтранци**</span><span class="sxs-lookup"><span data-stu-id="18cd6-152">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-153">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="18cd6-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-154">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-155">Набор флагов, предоставляющих сведения о сериализации.</span><span class="sxs-lookup"><span data-stu-id="18cd6-155">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="18cd6-156">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="18cd6-156">The default value is zero (0).</span></span>

<dt>

<span data-ttu-id="18cd6-157">0</span><span class="sxs-lookup"><span data-stu-id="18cd6-157">0</span></span>
</dt> <dd>

<span data-ttu-id="18cd6-158">Все инициализации этого поставщика должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="18cd6-158">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-159">1</span><span class="sxs-lookup"><span data-stu-id="18cd6-159">1</span></span>
</dt> <dd>

<span data-ttu-id="18cd6-160">Все инициализации этого поставщика в одном пространстве имен должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="18cd6-160">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-161">2</span><span class="sxs-lookup"><span data-stu-id="18cd6-161">2</span></span>
</dt> <dd>

<span data-ttu-id="18cd6-162">Сериализация инициализации не требуется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-162">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="18cd6-163">**инитиализатионтимеаутинтервал**</span><span class="sxs-lookup"><span data-stu-id="18cd6-163">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-164">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18cd6-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-166">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-167">**инитиализеасадминфирст**</span><span class="sxs-lookup"><span data-stu-id="18cd6-167">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-168">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-170">TBD</span><span class="sxs-lookup"><span data-stu-id="18cd6-170">TBD</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-171">**Name**</span><span class="sxs-lookup"><span data-stu-id="18cd6-171">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18cd6-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-174">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="18cd6-174">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-175">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="18cd6-175">The provider name.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-176">**оператионтимеаутинтервал**</span><span class="sxs-lookup"><span data-stu-id="18cd6-176">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-177">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18cd6-177">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-179">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-179">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-180">**перлокалеинитиализатион**</span><span class="sxs-lookup"><span data-stu-id="18cd6-180">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-181">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-182">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-183">Если **значение — true**, поставщик инициализируется для каждого языкового стандарта, когда пользователь соединяется с одним и тем же пространством имен более одного раза, используя разные языковые стандарты.</span><span class="sxs-lookup"><span data-stu-id="18cd6-183">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="18cd6-184">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="18cd6-184">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-185">**перусеринитиализатион**</span><span class="sxs-lookup"><span data-stu-id="18cd6-185">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-186">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-186">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-187">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-187">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-188">Если **значение — true**, поставщик инициализируется один раз для каждого пользователя NT LAN Manager (NTLM), который выполняет запросы к поставщику.</span><span class="sxs-lookup"><span data-stu-id="18cd6-188">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="18cd6-189">Если **значение равно false** (по умолчанию), поставщик инициализируется один раз для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="18cd6-189">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-190">**Чистый**</span><span class="sxs-lookup"><span data-stu-id="18cd6-190">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-191">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-193">Если **значение — true**, поставщик соглашается подготовиться к выгрузке путем вызова метода [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для всех необработанных точек интерфейса, когда WMI вызывает метод **Release** своего основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="18cd6-193">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="18cd6-194">Поставщики, которые должны оставаться клиентами инструментария WMI после того, как они не работают, так как поставщики должны задать для **чистого** значения **false**.</span><span class="sxs-lookup"><span data-stu-id="18cd6-194">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="18cd6-195">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="18cd6-195">The default setting is **TRUE**.</span></span> <span data-ttu-id="18cd6-196">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="18cd6-196">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-197">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="18cd6-197">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="18cd6-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-199">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-200">Дескриптор безопасности (SD) в языке определения дескрипторов безопасности (SDDL), определяющий набор пользователей, которые могут успешно вызывать [**ивбемдекаупледрегистрар: Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) для несвязанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="18cd6-200">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="18cd6-201">Дополнительные сведения см. в разделе о [языке определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) в разделе "безопасность" Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="18cd6-201">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="18cd6-202">Этот дескриптор безопасности используется только для несвязанных поставщиков и не влияет на других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="18cd6-202">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="18cd6-203">Дополнительные сведения см. [в разделе Включение поставщика в приложение](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="18cd6-203">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span>

<span data-ttu-id="18cd6-204">Инструментарий WMI выполняет проверки доступа для несвязанных поставщиков, использующих интерфейсы [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и [**ивбемобжектсинк**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="18cd6-204">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](iwbemobjectsink.md) interfaces.</span></span> <span data-ttu-id="18cd6-205">Если дескриптор безопасности имеет **значение NULL**, то для запуска несвязанного поставщика могут использоваться только приложения или службы, работающие под учетными записями LocalSystem, NetworkService, LocalService.</span><span class="sxs-lookup"><span data-stu-id="18cd6-205">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="18cd6-206">В следующей строке показан несвязанный поставщик, который будет запускаться только встроенными администраторами». О:БАГ: ОШИБКА: (A;; 0 x1;;; Ба) "</span><span class="sxs-lookup"><span data-stu-id="18cd6-206">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="18cd6-207">Дополнительные сведения о настройке свойства **SecurityDescriptor** см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="18cd6-207">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-208">**суппортсексплиЦитшутдовн**</span><span class="sxs-lookup"><span data-stu-id="18cd6-208">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-209">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-210">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-211">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-212">**суппортсекстендедстатус**</span><span class="sxs-lookup"><span data-stu-id="18cd6-212">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-213">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-215">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-216">**суппортскуотас**</span><span class="sxs-lookup"><span data-stu-id="18cd6-216">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-217">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-218">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-219">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-219">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-220">**суппортссендстатус**</span><span class="sxs-lookup"><span data-stu-id="18cd6-220">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-221">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-222">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-223">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-223">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-224">**суппортсшутдовн**</span><span class="sxs-lookup"><span data-stu-id="18cd6-224">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-225">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-227">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-227">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-228">**суппортссроттлинг**</span><span class="sxs-lookup"><span data-stu-id="18cd6-228">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-229">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="18cd6-229">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-230">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-230">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-231">Не используется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-231">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-232">**унлоадтимеаут**</span><span class="sxs-lookup"><span data-stu-id="18cd6-232">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-233">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="18cd6-233">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-234">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-234">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-235">[Формат даты и времени](date-and-time-format.md) , указывающий, как долго WMI позволяет поставщику оставаться в состоянии простоя перед выгрузкой.</span><span class="sxs-lookup"><span data-stu-id="18cd6-235">[Date and Time Format](date-and-time-format.md) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="18cd6-236">Как правило, поставщики запрашивают, что инструментарий WMI ожидает не более пяти минут.</span><span class="sxs-lookup"><span data-stu-id="18cd6-236">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="18cd6-237">Для текущей версии инструментария WMI значение этого свойства игнорируется.</span><span class="sxs-lookup"><span data-stu-id="18cd6-237">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="18cd6-238">Инструментарий WMI выгружает поставщик на основе значения времени ожидания во внутреннем классе \\ корневого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="18cd6-238">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="18cd6-239">Рекомендуется, чтобы поставщики установили **унлоадтимеаут**.</span><span class="sxs-lookup"><span data-stu-id="18cd6-239">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="18cd6-240">Дополнительные сведения см. [в разделе выгрузка поставщика](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="18cd6-240">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="18cd6-241">**Version**</span><span class="sxs-lookup"><span data-stu-id="18cd6-241">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18cd6-242">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="18cd6-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="18cd6-243">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="18cd6-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="18cd6-244">Версия поставщика.</span><span class="sxs-lookup"><span data-stu-id="18cd6-244">Version of the provider.</span></span> <span data-ttu-id="18cd6-245">Поддерживаемые версии: 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="18cd6-245">The supported versions are 1 and 2.</span></span> <span data-ttu-id="18cd6-246">Версия 2 повысит проверку достоверности для всех связанных регистраций свойств, в частности свойство [**имперсонатионлевел**](swbemsecurity-impersonationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="18cd6-246">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18cd6-247">Комментарии</span><span class="sxs-lookup"><span data-stu-id="18cd6-247">Remarks</span></span>

<span data-ttu-id="18cd6-248">Класс **\_ \_ Win32Provider** является производным от [**\_ \_ provider**](--provider.md).</span><span class="sxs-lookup"><span data-stu-id="18cd6-248">The **\_\_Win32Provider** class is derived from [**\_\_Provider**](--provider.md).</span></span>

<span data-ttu-id="18cd6-249">Большинство поставщиков могут принимать значения по умолчанию для свойства **инитиализатионринтранци** .</span><span class="sxs-lookup"><span data-stu-id="18cd6-249">Most providers can accept the default values for the **InitializationReentrancy** property.</span></span> <span data-ttu-id="18cd6-250">Однако если поставщик может поддерживать одновременную инициализацию для отдельных пользователей, этому свойству можно присвоить значение 1 (одно).</span><span class="sxs-lookup"><span data-stu-id="18cd6-250">However, if a provider can support simultaneous initialization for separate users, this property can be set to 1 (one).</span></span> <span data-ttu-id="18cd6-251">Если требуется сериализованная инициализация, **инитиализатионринтранци** остается равным 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="18cd6-251">If serialized initialization is necessary, **InitializationReentrancy** remains 0 (zero).</span></span> <span data-ttu-id="18cd6-252">В обоих экземплярах **перусеринитиализатион** имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="18cd6-252">In both instances, **PerUserInitialization** is set to **TRUE**.</span></span>

<span data-ttu-id="18cd6-253">Чистый поставщик или поставщик, устанавливающий для **чистого** свойства **значение true**, существует только для запросов служб из приложений и WMI.</span><span class="sxs-lookup"><span data-stu-id="18cd6-253">A pure provider or a provider that sets the **Pure** property to **TRUE**, exists only to service requests from applications and WMI.</span></span> <span data-ttu-id="18cd6-254">Большинство поставщиков являются чистыми поставщиками.</span><span class="sxs-lookup"><span data-stu-id="18cd6-254">Most providers are pure providers.</span></span> <span data-ttu-id="18cd6-255">Исключением является нечистый поставщик.</span><span class="sxs-lookup"><span data-stu-id="18cd6-255">A nonpure provider is the exception.</span></span> <span data-ttu-id="18cd6-256">Нечистые поставщики переходят на роль клиента после завершения обслуживания запросов.</span><span class="sxs-lookup"><span data-stu-id="18cd6-256">Nonpure providers transition to the role of client after they complete servicing requests.</span></span>

<span data-ttu-id="18cd6-257">Примером нечистого поставщика является поставщик push-уведомлений, который начинает выдавать запросы и отправляет запросы инструментария WMI после завершения инициализации.</span><span class="sxs-lookup"><span data-stu-id="18cd6-257">An example of a nonpure provider is a push provider that starts to issue queries, and makes requests of WMI after it completes initialization.</span></span> <span data-ttu-id="18cd6-258">Поставщик услуг push-уведомлений не имеет обязанностей, за исключением обновления репозитория CIM данными во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="18cd6-258">A push provider does not have responsibilities except to update the CIM repository with data at initialization time.</span></span> <span data-ttu-id="18cd6-259">После обновления репозитория поставщик push-уведомлений может ожидать выгрузки или перехода к роли клиента.</span><span class="sxs-lookup"><span data-stu-id="18cd6-259">After updating the repository, a push provider can wait to be unloaded, or transition to the role of client.</span></span> <span data-ttu-id="18cd6-260">Поставщик push-уведомлений, который ожидает выгрузки, является чистым поставщиком.</span><span class="sxs-lookup"><span data-stu-id="18cd6-260">The push provider that waits to be unloaded is a pure provider.</span></span> <span data-ttu-id="18cd6-261">Поставщик push-уведомлений, участвующий в действиях клиента, не является чистым.</span><span class="sxs-lookup"><span data-stu-id="18cd6-261">The push provider that participates in client activities is nonpure.</span></span>

<span data-ttu-id="18cd6-262">Инструментарий WMI должен иметь возможность отличить чистые поставщики от нечистых поставщиков, чтобы они могли определить, когда его можно будет обезопасить.</span><span class="sxs-lookup"><span data-stu-id="18cd6-262">WMI must be able to distinguish pure providers from non-pure providers so that it can determine when it is safe to shut down.</span></span> <span data-ttu-id="18cd6-263">Инструментарий WMI должен ожидать, пока все операции, затрагивающие нечистые поставщики, не закончится, прежде чем он сможет безопасно завершить работу.</span><span class="sxs-lookup"><span data-stu-id="18cd6-263">WMI must wait for all operations that involve non-pure providers to complete before it can shut down safely.</span></span>

## <a name="requirements"></a><span data-ttu-id="18cd6-264">Требования</span><span class="sxs-lookup"><span data-stu-id="18cd6-264">Requirements</span></span>



| <span data-ttu-id="18cd6-265">Требование</span><span class="sxs-lookup"><span data-stu-id="18cd6-265">Requirement</span></span> | <span data-ttu-id="18cd6-266">Значение</span><span class="sxs-lookup"><span data-stu-id="18cd6-266">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="18cd6-267">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18cd6-267">Minimum supported client</span></span><br/> | <span data-ttu-id="18cd6-268">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18cd6-268">Windows Vista</span></span><br/>       |
| <span data-ttu-id="18cd6-269">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18cd6-269">Minimum supported server</span></span><br/> | <span data-ttu-id="18cd6-270">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18cd6-270">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="18cd6-271">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18cd6-271">Namespace</span></span><br/>                | <span data-ttu-id="18cd6-272">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="18cd6-272">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="18cd6-273">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18cd6-273">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18cd6-274">**\_\_Поставщик**</span><span class="sxs-lookup"><span data-stu-id="18cd6-274">**\_\_Provider**</span></span>](/windows/desktop/WmiSdk/--provider)
</dt> <dt>

[<span data-ttu-id="18cd6-275">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="18cd6-275">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="18cd6-276">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="18cd6-276">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

