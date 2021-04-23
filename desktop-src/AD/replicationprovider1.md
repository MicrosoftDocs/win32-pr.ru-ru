---
title: Класс ReplicationProvider1
description: Базовый класс для экземпляра поставщика.
ms.assetid: c3c6efda-faa7-42af-a635-060967fdcc35
ms.tgt_platform: multiple
keywords:
- Active Directory класса ReplicationProvider1
- Active Directory класс ReplicationProvider1, описание
topic_type:
- apiref
api_name:
- ReplicationProvider1
- ReplicationProvider1.ClientLoadableCLSID
- ReplicationProvider1.CLSID
- ReplicationProvider1.Concurrency
- ReplicationProvider1.DefaultMachineName
- ReplicationProvider1.Enabled
- ReplicationProvider1.ImpersonationLevel
- ReplicationProvider1.InitializationReentrancy
- ReplicationProvider1.InitializationTimeoutInterval
- ReplicationProvider1.InitializeAsAdminFirst
- ReplicationProvider1.Name
- ReplicationProvider1.OperationTimeoutInterval
- ReplicationProvider1.PerLocaleInitialization
- ReplicationProvider1.PerUserInitialization
- ReplicationProvider1.Pure
- ReplicationProvider1.SecurityDescriptor
- ReplicationProvider1.SupportsExplicitShutdown
- ReplicationProvider1.SupportsExtendedStatus
- ReplicationProvider1.SupportsQuotas
- ReplicationProvider1.SupportsSendStatus
- ReplicationProvider1.SupportsShutdown
- ReplicationProvider1.SupportsThrottling
- ReplicationProvider1.UnloadTimeout
- ReplicationProvider1.Version
- ReplicationProvider1.HostingModel
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0098556fcbc1400ccd1042198903fec7e018ed57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071530"
---
# <a name="replicationprovider1-class"></a><span data-ttu-id="f3968-105">Класс ReplicationProvider1</span><span class="sxs-lookup"><span data-stu-id="f3968-105">ReplicationProvider1 class</span></span>

<span data-ttu-id="f3968-106">Базовый класс для экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3968-106">The base class for the provider instance.</span></span>

<span data-ttu-id="f3968-107">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f3968-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3968-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3968-108">Syntax</span></span>

``` syntax
class ReplicationProvider1 : __Win32Provider
{
  string   ClientLoadableCLSID;
  string   CLSID;
  sint32   Concurrency;
  string   DefaultMachineName;
  boolean  Enabled;
  sint32   ImpersonationLevel = 0;
  sint32   InitializationReentrancy = 0;
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
  string   HostingModel;
};
```

## <a name="members"></a><span data-ttu-id="f3968-109">Члены</span><span class="sxs-lookup"><span data-stu-id="f3968-109">Members</span></span>

<span data-ttu-id="f3968-110">Класс **ReplicationProvider1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f3968-110">The **ReplicationProvider1** class has these types of members:</span></span>

-   [<span data-ttu-id="f3968-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3968-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3968-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3968-112">Properties</span></span>

<span data-ttu-id="f3968-113">Класс **ReplicationProvider1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f3968-113">The **ReplicationProvider1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3968-114">**клиентлоадаблеклсид**</span><span class="sxs-lookup"><span data-stu-id="f3968-114">**ClientLoadableCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3968-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-117">Идентификатор класса, используемый WMI для определения необходимости загрузки высокопроизводительного поставщика в клиентский процесс или в процесс WMI.</span><span class="sxs-lookup"><span data-stu-id="f3968-117">Class identifier that WMI uses to determine whether or not to load a high performance provider into the client process or the WMI process.</span></span> <span data-ttu-id="f3968-118">Если поставщик и клиент расположены на одном компьютере, WMI загружает поставщик в процессе в клиенте с помощью **клиентлоадаблеклсид** в качестве идентификатора класса.</span><span class="sxs-lookup"><span data-stu-id="f3968-118">If both the provider and client are located on the same computer, WMI loads the provider in-process to the client by using **ClientLoadableCLSID** as the class identifier.</span></span> <span data-ttu-id="f3968-119">Когда поставщик и клиент расположены на разных компьютерах, Инструментарий WMI загружает поставщик в службу WMI.</span><span class="sxs-lookup"><span data-stu-id="f3968-119">When the provider and client are located on different computers, WMI loads the provider in-process to WMI.</span></span> <span data-ttu-id="f3968-120">Инструментарий WMI также использует **клиентлоадаблеклсид** для поддержки операций обновления.</span><span class="sxs-lookup"><span data-stu-id="f3968-120">WMI also uses **ClientLoadableCLSID** to support refresh operations.</span></span>

<span data-ttu-id="f3968-121">Дополнительные сведения см [. в разделе Регистрация поставщика High-Performance.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span><span class="sxs-lookup"><span data-stu-id="f3968-121">For more information, see [Registering a High-Performance Provider.](/windows/desktop/WmiSdk/registering-a-high-performance-provider)</span></span>

<span data-ttu-id="f3968-122">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-122">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-123">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="f3968-123">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3968-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-126">Идентификатор **GUID** , представляющий идентификатор класса (**CLSID**) COM-объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3968-126">**GUID** that represents the class identifier (**CLSID**) of the provider COM object.</span></span> <span data-ttu-id="f3968-127">Этот COM-объект должен содержать реализацию интерфейса [**ивбемпровидеринит**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) .</span><span class="sxs-lookup"><span data-stu-id="f3968-127">This COM object must contain an implementation of the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) interface.</span></span>

<span data-ttu-id="f3968-128">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-128">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-129">**Параллелизм**</span><span class="sxs-lookup"><span data-stu-id="f3968-129">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-130">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3968-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-131">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-132">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-132">Not used.</span></span>

<span data-ttu-id="f3968-133">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-133">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-134">**дефаултмачиненаме**</span><span class="sxs-lookup"><span data-stu-id="f3968-134">**DefaultMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3968-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-137">Определяет компьютер, на котором будет запущен поставщик.</span><span class="sxs-lookup"><span data-stu-id="f3968-137">Identifies the computer on which to start the provider.</span></span> <span data-ttu-id="f3968-138">Если поставщик запущен на локальном компьютере, он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f3968-138">If the provider runs on the local computer it is **NULL**.</span></span>

<span data-ttu-id="f3968-139">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-139">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-140">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="f3968-140">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-141">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-143">Если **значение — true**, этот экземпляр включен и может использоваться для выполнения клиентских запросов.</span><span class="sxs-lookup"><span data-stu-id="f3968-143">If **TRUE**, this instance is enabled and can be used to complete client requests.</span></span>

<span data-ttu-id="f3968-144">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-144">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-145">**хостингмодел**</span><span class="sxs-lookup"><span data-stu-id="f3968-145">**HostingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3968-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3968-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3968-148">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("хостингмодел")</span><span class="sxs-lookup"><span data-stu-id="f3968-148">Qualifiers: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("HostingModel")</span></span>
</dt> </dl>

<span data-ttu-id="f3968-149">Содержит модель размещения поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3968-149">Contains the hosting model of the provider.</span></span>

</dd> <dt>

<span data-ttu-id="f3968-150">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="f3968-150">**ImpersonationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-151">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3968-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-153">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="f3968-153">Reserved.</span></span> <span data-ttu-id="f3968-154">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="f3968-154">The default value is zero (0).</span></span>

<span data-ttu-id="f3968-155">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-155">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-156">**инитиализатионринтранци**</span><span class="sxs-lookup"><span data-stu-id="f3968-156">**InitializationReentrancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-157">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="f3968-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-159">Набор флагов, предоставляющих сведения о сериализации.</span><span class="sxs-lookup"><span data-stu-id="f3968-159">Set of flags that provide information about serialization.</span></span> <span data-ttu-id="f3968-160">Значение по умолчанию равно нулю (0).</span><span class="sxs-lookup"><span data-stu-id="f3968-160">The default value is zero (0).</span></span>

<span data-ttu-id="f3968-161">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-161">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f3968-162"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="f3968-162"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f3968-163">Все инициализации этого поставщика должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="f3968-163">All initialization of this provider must be serialized.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f3968-164"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f3968-164"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f3968-165">Все инициализации этого поставщика в одном пространстве имен должны быть сериализованы.</span><span class="sxs-lookup"><span data-stu-id="f3968-165">All initializations of this provider in the same namespace must be serialized.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="f3968-166"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="f3968-166"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="f3968-167">Сериализация инициализации не требуется.</span><span class="sxs-lookup"><span data-stu-id="f3968-167">No initialization serialization is necessary.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f3968-168">**инитиализатионтимеаутинтервал**</span><span class="sxs-lookup"><span data-stu-id="f3968-168">**InitializationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-169">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3968-169">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-170">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-171">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-171">Not used.</span></span>

<span data-ttu-id="f3968-172">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-172">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-173">**инитиализеасадминфирст**</span><span class="sxs-lookup"><span data-stu-id="f3968-173">**InitializeAsAdminFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-174">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-176">**Windows Server 2003:** Это свойство отключено.</span><span class="sxs-lookup"><span data-stu-id="f3968-176">**Windows Server 2003:** This property is disabled.</span></span>

<span data-ttu-id="f3968-177">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-177">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="f3968-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3968-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3968-181">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f3968-181">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f3968-182">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3968-182">The provider name.</span></span>

<span data-ttu-id="f3968-183">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-183">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-184">**оператионтимеаутинтервал**</span><span class="sxs-lookup"><span data-stu-id="f3968-184">**OperationTimeoutInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-185">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3968-185">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-186">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-187">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-187">Not used.</span></span>

<span data-ttu-id="f3968-188">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-188">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-189">**перлокалеинитиализатион**</span><span class="sxs-lookup"><span data-stu-id="f3968-189">**PerLocaleInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-190">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-191">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-192">Если **значение — true**, поставщик инициализируется для каждого языкового стандарта, когда пользователь соединяется с одним и тем же пространством имен более одного раза, используя разные языковые стандарты.</span><span class="sxs-lookup"><span data-stu-id="f3968-192">If **TRUE**, the provider is initialized for each locale when a user connects to the same namespace more than one time using different locales.</span></span> <span data-ttu-id="f3968-193">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="f3968-193">The default value is **FALSE**.</span></span>

<span data-ttu-id="f3968-194">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-194">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-195">**перусеринитиализатион**</span><span class="sxs-lookup"><span data-stu-id="f3968-195">**PerUserInitialization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-197">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-197">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-198">Если **значение — true**, поставщик инициализируется один раз для каждого пользователя NT LAN Manager (NTLM), который выполняет запросы к поставщику.</span><span class="sxs-lookup"><span data-stu-id="f3968-198">If **TRUE**, the provider is initialized one time for each NT LAN Manager (NTLM) user that makes requests to the provider.</span></span> <span data-ttu-id="f3968-199">Если **значение равно false** (по умолчанию), поставщик инициализируется один раз для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="f3968-199">If **FALSE** (default), the provider is initialized one time for all users.</span></span>

<span data-ttu-id="f3968-200">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-200">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-201">**Чистый**</span><span class="sxs-lookup"><span data-stu-id="f3968-201">**Pure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-202">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-202">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-203">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-203">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-204">Если **значение — true**, поставщик соглашается подготовиться к выгрузке путем вызова метода [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для всех необработанных точек интерфейса, когда WMI вызывает метод **Release** своего основного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f3968-204">If **TRUE**, the provider agrees to prepare to unload by calling [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on all outstanding interface points when WMI calls the **Release** method of its primary interface.</span></span> <span data-ttu-id="f3968-205">Поставщики, которые должны оставаться клиентами инструментария WMI после того, как они не работают, так как поставщики должны задать для **чистого** значения **false**.</span><span class="sxs-lookup"><span data-stu-id="f3968-205">Providers that must remain clients of WMI after they do not function as providers should set **Pure** to **FALSE**.</span></span> <span data-ttu-id="f3968-206">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="f3968-206">The default setting is **TRUE**.</span></span> <span data-ttu-id="f3968-207">Дополнительные сведения см. в подразделе «Примечания» этого раздела.</span><span class="sxs-lookup"><span data-stu-id="f3968-207">For more information, see the Remarks section of this topic.</span></span>

<span data-ttu-id="f3968-208">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-208">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-209">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f3968-209">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3968-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-212">Дескриптор безопасности (SD) в языке определения дескрипторов безопасности (SDDL), определяющий набор пользователей, которые могут успешно вызывать [**ивбемдекаупледрегистрар: Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) для несвязанного поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3968-212">Security descriptor (SD) in the Security Descriptor Definition Language (SDDL) that determines the set of users that can successfully call [**IWbemDecoupledRegistrar:Register**](/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register) for the decoupled provider.</span></span> <span data-ttu-id="f3968-213">Дополнительные сведения см. в разделе о [языке определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) в разделе "безопасность" Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f3968-213">For more information, see the [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) topic in the Security section of the Windows SDK.</span></span> <span data-ttu-id="f3968-214">Этот дескриптор безопасности используется только для несвязанных поставщиков и не влияет на других поставщиков.</span><span class="sxs-lookup"><span data-stu-id="f3968-214">This security descriptor is used only for decoupled providers, and does not affect other providers.</span></span> <span data-ttu-id="f3968-215">Дополнительные сведения см. [в разделе Включение поставщика в приложение](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span><span class="sxs-lookup"><span data-stu-id="f3968-215">For more information, see [Incorporating a Provider in an Application](/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application).</span></span>

<span data-ttu-id="f3968-216">Инструментарий WMI выполняет проверки доступа для несвязанных поставщиков, использующих интерфейсы [**ивбемпровидеринит**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) и [**ивбемобжектсинк**](/windows/desktop/WmiSdk/iwbemobjectsink) .</span><span class="sxs-lookup"><span data-stu-id="f3968-216">WMI performs access checks for decoupled providers that use the [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) and [**IWbemObjectSink**](/windows/desktop/WmiSdk/iwbemobjectsink) interfaces.</span></span> <span data-ttu-id="f3968-217">Если дескриптор безопасности имеет **значение NULL**, то для запуска несвязанного поставщика могут использоваться только приложения или службы, работающие под учетными записями LocalSystem, NetworkService, LocalService.</span><span class="sxs-lookup"><span data-stu-id="f3968-217">If the security descriptor is **NULL**, then only applications or services that run under the LocalSystem, NetworkService, LocalService accounts can run a decoupled provider.</span></span>

<span data-ttu-id="f3968-218">В следующей строке показан несвязанный поставщик, который будет запускаться только встроенными администраторами». О:БАГ: ОШИБКА: (A;; 0 x1;;; Ба) "</span><span class="sxs-lookup"><span data-stu-id="f3968-218">The following string shows a decoupled provider to be run only by built-in Administrators."O:BAG:BAD:(A;;0x1;;;BA)"</span></span>

<span data-ttu-id="f3968-219">Дополнительные сведения о настройке свойства **SecurityDescriptor** см. в разделе [обслуживание безопасности WMI](/windows/desktop/WmiSdk/maintaining-wmi-security).</span><span class="sxs-lookup"><span data-stu-id="f3968-219">For more information about setting the **SecurityDescriptor** property, see [Maintaining WMI Security](/windows/desktop/WmiSdk/maintaining-wmi-security).</span></span>

<span data-ttu-id="f3968-220">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-220">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-221">**суппортсексплиЦитшутдовн**</span><span class="sxs-lookup"><span data-stu-id="f3968-221">**SupportsExplicitShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-222">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-222">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-224">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-224">Not used.</span></span>

<span data-ttu-id="f3968-225">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-225">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-226">**суппортсекстендедстатус**</span><span class="sxs-lookup"><span data-stu-id="f3968-226">**SupportsExtendedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-227">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-228">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-229">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-229">Not used.</span></span>

<span data-ttu-id="f3968-230">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-230">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-231">**суппортскуотас**</span><span class="sxs-lookup"><span data-stu-id="f3968-231">**SupportsQuotas**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-232">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-233">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-233">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-234">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-234">Not used.</span></span>

<span data-ttu-id="f3968-235">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-235">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-236">**суппортссендстатус**</span><span class="sxs-lookup"><span data-stu-id="f3968-236">**SupportsSendStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-237">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-238">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-238">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-239">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-239">Not used.</span></span>

<span data-ttu-id="f3968-240">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-240">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-241">**суппортсшутдовн**</span><span class="sxs-lookup"><span data-stu-id="f3968-241">**SupportsShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-242">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-243">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-243">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-244">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-244">Not used.</span></span>

<span data-ttu-id="f3968-245">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-245">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-246">**суппортссроттлинг**</span><span class="sxs-lookup"><span data-stu-id="f3968-246">**SupportsThrottling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-247">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f3968-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-248">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-249">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f3968-249">Not used.</span></span>

<span data-ttu-id="f3968-250">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-250">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-251">**унлоадтимеаут**</span><span class="sxs-lookup"><span data-stu-id="f3968-251">**UnloadTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-252">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3968-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-254">[Формат даты и времени](/windows/desktop/WmiSdk/date-and-time-format) , указывающий, как долго WMI позволяет поставщику оставаться в состоянии простоя перед выгрузкой.</span><span class="sxs-lookup"><span data-stu-id="f3968-254">[Date and Time Format](/windows/desktop/WmiSdk/date-and-time-format) that specifies how long WMI allows the provider to remain idle before it is unloaded.</span></span> <span data-ttu-id="f3968-255">Как правило, поставщики запрашивают, что инструментарий WMI ожидает не более пяти минут.</span><span class="sxs-lookup"><span data-stu-id="f3968-255">Typically, providers request that WMI wait no longer than five minutes.</span></span>

<span data-ttu-id="f3968-256">Для текущей версии инструментария WMI значение этого свойства игнорируется.</span><span class="sxs-lookup"><span data-stu-id="f3968-256">For the current version of WMI, the value of this property is ignored.</span></span> <span data-ttu-id="f3968-257">Инструментарий WMI выгружает поставщик на основе значения времени ожидания во внутреннем классе \\ корневого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f3968-257">WMI unloads the provider based on the time-out value in an internal class in the \\root namespace.</span></span> <span data-ttu-id="f3968-258">Рекомендуется, чтобы поставщики установили **унлоадтимеаут**.</span><span class="sxs-lookup"><span data-stu-id="f3968-258">It is recommended that providers set **UnloadTimeout**.</span></span> <span data-ttu-id="f3968-259">Дополнительные сведения см. [в разделе выгрузка поставщика](/windows/desktop/WmiSdk/unloading-a-provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-259">For more information, see [Unloading a Provider](/windows/desktop/WmiSdk/unloading-a-provider).</span></span>

<span data-ttu-id="f3968-260">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-260">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> <dt>

<span data-ttu-id="f3968-261">**Version**</span><span class="sxs-lookup"><span data-stu-id="f3968-261">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3968-262">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f3968-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3968-263">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="f3968-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f3968-264">Версия поставщика.</span><span class="sxs-lookup"><span data-stu-id="f3968-264">Version of the provider.</span></span> <span data-ttu-id="f3968-265">Поддерживаемые версии: 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="f3968-265">The supported versions are 1 and 2.</span></span> <span data-ttu-id="f3968-266">Версия 2 повысит проверку достоверности для всех связанных регистраций свойств, в частности свойство [**имперсонатионлевел**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) .</span><span class="sxs-lookup"><span data-stu-id="f3968-266">Version 2 strengthens validity checks for all associated property registrations, specifically the [**ImpersonationLevel**](/windows/desktop/WmiSdk/swbemsecurity-impersonationlevel) property.</span></span>

<span data-ttu-id="f3968-267">Это свойство наследуется от [**\_ \_ Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span><span class="sxs-lookup"><span data-stu-id="f3968-267">This property is inherited from [**\_\_Win32Provider**](/windows/desktop/WmiSdk/--win32provider).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3968-268">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3968-268">Remarks</span></span>

<span data-ttu-id="f3968-269">Экземпляр этого класса представляет поставщик WMI для служб домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3968-269">An instance of this class represents the WMI provider for Active Directory Domain services.</span></span> <span data-ttu-id="f3968-270">По умолчанию используются следующие параметры.</span><span class="sxs-lookup"><span data-stu-id="f3968-270">The defaults are as follows:</span></span>

-   <span data-ttu-id="f3968-271">Name = "ReplProv1"</span><span class="sxs-lookup"><span data-stu-id="f3968-271">Name = "ReplProv1"</span></span>
-   <span data-ttu-id="f3968-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span><span class="sxs-lookup"><span data-stu-id="f3968-272">ClsID = "{29288F43-39B1-40db-B41F-CE899450E911}"</span></span>
-   <span data-ttu-id="f3968-273">Хостингмодел = "Нетворксервицехост"</span><span class="sxs-lookup"><span data-stu-id="f3968-273">HostingModel = "NetworkServiceHost"</span></span>

## <a name="requirements"></a><span data-ttu-id="f3968-274">Требования</span><span class="sxs-lookup"><span data-stu-id="f3968-274">Requirements</span></span>



| <span data-ttu-id="f3968-275">Требование</span><span class="sxs-lookup"><span data-stu-id="f3968-275">Requirement</span></span> | <span data-ttu-id="f3968-276">Значение</span><span class="sxs-lookup"><span data-stu-id="f3968-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3968-277">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3968-277">Minimum supported client</span></span><br/> | <span data-ttu-id="f3968-278">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f3968-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f3968-279">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3968-279">Minimum supported server</span></span><br/> | <span data-ttu-id="f3968-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3968-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3968-281">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3968-281">Namespace</span></span><br/>                | <span data-ttu-id="f3968-282">Корневой \\ микрософтактиведиректори</span><span class="sxs-lookup"><span data-stu-id="f3968-282">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="f3968-283">MOF</span><span class="sxs-lookup"><span data-stu-id="f3968-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3968-284"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3968-284"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3968-285">DLL</span><span class="sxs-lookup"><span data-stu-id="f3968-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3968-286"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3968-286"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3968-287">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3968-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3968-288">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="f3968-288">**\_\_Win32Provider**</span></span>](/windows/desktop/WmiSdk/--win32provider)
</dt> </dl>

 

