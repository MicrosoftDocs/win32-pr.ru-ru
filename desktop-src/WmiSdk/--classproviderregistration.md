---
description: Регистрирует поставщики классов в WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: Класс __ClassProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818969"
---
# <a name="__classproviderregistration-class"></a><span data-ttu-id="0d10d-103">\_\_Класс Класспровидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="0d10d-103">\_\_ClassProviderRegistration class</span></span>

<span data-ttu-id="0d10d-104">Класс System **\_ \_ класспровидеррегистратион** регистрирует поставщики классов в WMI.</span><span class="sxs-lookup"><span data-stu-id="0d10d-104">The **\_\_ClassProviderRegistration** system class registers class providers in WMI.</span></span>

<span data-ttu-id="0d10d-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0d10d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0d10d-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0d10d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d10d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d10d-107">Syntax</span></span>

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a><span data-ttu-id="0d10d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0d10d-108">Members</span></span>

<span data-ttu-id="0d10d-109">Класс **\_ \_ класспровидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0d10d-109">The **\_\_ClassProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="0d10d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d10d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d10d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d10d-111">Properties</span></span>

<span data-ttu-id="0d10d-112">Класс **\_ \_ класспровидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0d10d-112">The **\_\_ClassProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d10d-113">**качерефрешинтервал**</span><span class="sxs-lookup"><span data-stu-id="0d10d-113">**CacheRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-114">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d10d-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-116">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0d10d-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-117">**интерактионтипе**</span><span class="sxs-lookup"><span data-stu-id="0d10d-117">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-118">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="0d10d-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-120">Указывает, передает ли поставщик класса или экземпляра данные или использует WMI и репозиторий модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="0d10d-120">Indicates whether or not the class or instance provider supplies data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="0d10d-121">Поставщики услуг извлечения поддерживают динамический доступ к данным, а поставщики push-уведомлений хранят данные в репозитории CIM и используют инструментарий WMI для предоставления доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="0d10d-121">Pull providers support dynamic access to data, and push providers store data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="0d10d-122">Значение по умолчанию — 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="0d10d-122">The default value is 0 (zero).</span></span> <span data-ttu-id="0d10d-123">Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-123">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="0d10d-124">Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-124">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="0d10d-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>По **запросу** (0)</span><span class="sxs-lookup"><span data-stu-id="0d10d-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-126">Поставщик является поставщиком опрашивающей репликации.</span><span class="sxs-lookup"><span data-stu-id="0d10d-126">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="0d10d-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Принудительная отправка** (1)</span><span class="sxs-lookup"><span data-stu-id="0d10d-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-128">Поставщик является поставщиком услуг push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="0d10d-128">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="0d10d-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Пушверифи** (2)</span><span class="sxs-lookup"><span data-stu-id="0d10d-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-130">Поставщик — это поставщик принудительной проверки.</span><span class="sxs-lookup"><span data-stu-id="0d10d-130">Provider is a push-verify provider.</span></span> <span data-ttu-id="0d10d-131">Обратите внимание, что в настоящее время поставщики **пушверифи** не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0d10d-131">Note that **PushVerify** providers are not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d10d-132">**перусерсчема**</span><span class="sxs-lookup"><span data-stu-id="0d10d-132">**PerUserSchema**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-135">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0d10d-135">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-136">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="0d10d-136">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-137">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="0d10d-137">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d10d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-139">Путь к объекту поставщика класса.</span><span class="sxs-lookup"><span data-stu-id="0d10d-139">Object path to a class provider.</span></span> <span data-ttu-id="0d10d-140">Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-140">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-141">**куерисуппортлевелс**</span><span class="sxs-lookup"><span data-stu-id="0d10d-141">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-142">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0d10d-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-144">Массив типов поддержки, реализованных поставщиком для обработки запросов.</span><span class="sxs-lookup"><span data-stu-id="0d10d-144">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="0d10d-145">Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-145">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="0d10d-146">Поставщики классов должны поддерживать хотя бы один тип запросов.</span><span class="sxs-lookup"><span data-stu-id="0d10d-146">Class providers are required to support at least one type of query.</span></span> <span data-ttu-id="0d10d-147">Поставщики экземпляров могут установить **куерисуппортлевелс** в **значение NULL** , если они не поддерживают обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="0d10d-147">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="0d10d-148">Поставщики, поддерживающие запросы, реализуют метод [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) и устанавливают для этого свойства одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0d10d-148">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values:</span></span>

<dt>



 <span data-ttu-id="0d10d-149">("WQL: Унариселект")</span><span class="sxs-lookup"><span data-stu-id="0d10d-149">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d10d-150">("WQL: References")</span><span class="sxs-lookup"><span data-stu-id="0d10d-150">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d10d-151">("WQL: соединители")</span><span class="sxs-lookup"><span data-stu-id="0d10d-151">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0d10d-152">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="0d10d-152">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d10d-153">**референцедсеткуериес**</span><span class="sxs-lookup"><span data-stu-id="0d10d-153">**ReferencedSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-154">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0d10d-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-155">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-156">Один или несколько запросов, описывающих набор ссылочных классов, поддерживаемых поставщиком классов.</span><span class="sxs-lookup"><span data-stu-id="0d10d-156">One or more queries that describe the set of referenced classes that a class provider supports.</span></span> <span data-ttu-id="0d10d-157">Поставщики, которые могут предоставлять классы ассоциаций, должны содержать по крайней мере один запрос в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="0d10d-157">Providers that can supply association classes must include at least one query in this property.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-158">**ресултсеткуериес**</span><span class="sxs-lookup"><span data-stu-id="0d10d-158">**ResultSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-159">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0d10d-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-160">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-161">Один или несколько запросов, описывающих набор всех классов, которые могут быть предоставлены поставщиком класса, или надмножество этих классов.</span><span class="sxs-lookup"><span data-stu-id="0d10d-161">One or more queries that describe the set of all classes that can be supplied by the class provider, or a superset of those classes.</span></span> <span data-ttu-id="0d10d-162">Это свойство никогда не указывает подмножество поддерживаемых классов.</span><span class="sxs-lookup"><span data-stu-id="0d10d-162">This property never specifies a subset of supported classes.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-163">**ресинчронисеоннамеспацеопен**</span><span class="sxs-lookup"><span data-stu-id="0d10d-163">**ReSynchroniseOnNamespaceOpen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-164">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-166">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0d10d-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-167">**суппортсбатчинг**</span><span class="sxs-lookup"><span data-stu-id="0d10d-167">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-168">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-170">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0d10d-170">Not used.</span></span>

<span data-ttu-id="0d10d-171">Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-171">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-172">**суппортсделете**</span><span class="sxs-lookup"><span data-stu-id="0d10d-172">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-173">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-174">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-175">Если **значение — true**, поставщик поддерживает удаление данных.</span><span class="sxs-lookup"><span data-stu-id="0d10d-175">If **TRUE**, the provider supports data deletion.</span></span> <span data-ttu-id="0d10d-176">Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-176">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="0d10d-177">Условия</span><span class="sxs-lookup"><span data-stu-id="0d10d-177">(True)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-178">Поставщик поддерживает удаление классов или экземпляров путем реализации одного из следующих методов [**::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (поставщики классов) или [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (поставщики экземпляров).</span><span class="sxs-lookup"><span data-stu-id="0d10d-178">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="0d10d-179">IsFalse</span><span class="sxs-lookup"><span data-stu-id="0d10d-179">(False)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-180">Поставщик не поддерживает удаление данных и возвращает **поставщик WBEM E, \_ \_ \_ не \_ поддерживающий** [**делетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) или [**делетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="0d10d-180">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d10d-181">**суппортсенумератион**</span><span class="sxs-lookup"><span data-stu-id="0d10d-181">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-182">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-183">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-184">Если **значение — true**, поставщик поддерживает перечисление данных.</span><span class="sxs-lookup"><span data-stu-id="0d10d-184">If **TRUE**, the provider supports data enumeration.</span></span> <span data-ttu-id="0d10d-185">Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-185">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="0d10d-186">Условия</span><span class="sxs-lookup"><span data-stu-id="0d10d-186">(True)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-187">Поставщик поддерживает перечисление данных путем реализации одного из следующих методов [**IWbemServices:: креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (классы поставщиков) или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (поставщики экземпляров).</span><span class="sxs-lookup"><span data-stu-id="0d10d-187">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="0d10d-188">IsFalse</span><span class="sxs-lookup"><span data-stu-id="0d10d-188">(False)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-189">Поставщик не поддерживает перечисление данных и возвращает **поставщик WBEM \_ E \_ , \_ не \_ поддерживающий** [**креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) или [**креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="0d10d-189">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d10d-190">**суппортсжет**</span><span class="sxs-lookup"><span data-stu-id="0d10d-190">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-191">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-193">Если **значение — true**, то поставщик класса или экземпляра поддерживает извлечение данных.</span><span class="sxs-lookup"><span data-stu-id="0d10d-193">If **TRUE**, the class or instance provider supports data retrieval.</span></span> <span data-ttu-id="0d10d-194">Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-194">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="0d10d-195">Условия</span><span class="sxs-lookup"><span data-stu-id="0d10d-195">(True)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-196">Поставщик поддерживает получение данных путем реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="0d10d-196">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>



 <span data-ttu-id="0d10d-197">IsFalse</span><span class="sxs-lookup"><span data-stu-id="0d10d-197">(False)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-198">Поставщик не поддерживает извлечение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** из [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="0d10d-198">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d10d-199">**суппортспут**</span><span class="sxs-lookup"><span data-stu-id="0d10d-199">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-200">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-201">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-202">Если **значение — true**, то поставщик класса или экземпляра поддерживает изменение данных.</span><span class="sxs-lookup"><span data-stu-id="0d10d-202">If **TRUE**, the class or instance provider supports data modification.</span></span> <span data-ttu-id="0d10d-203">Это свойство наследуется от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-203">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="0d10d-204">Условия</span><span class="sxs-lookup"><span data-stu-id="0d10d-204">(True)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-205">Поставщик поддерживает изменение класса или экземпляра путем реализации одного из следующих методов [**::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (поставщики классов) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (поставщики классов).</span><span class="sxs-lookup"><span data-stu-id="0d10d-205">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="0d10d-206">IsFalse</span><span class="sxs-lookup"><span data-stu-id="0d10d-206">(False)</span></span>


</dt> <dd>

<span data-ttu-id="0d10d-207">Поставщик не поддерживает изменение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** [**путклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) или [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="0d10d-207">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d10d-208">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="0d10d-208">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-209">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-210">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-211">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0d10d-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-212">**супппортсбатчинг**</span><span class="sxs-lookup"><span data-stu-id="0d10d-212">**SuppportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-213">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d10d-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-214">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-215">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0d10d-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-216">**унсуппортедкуериес**</span><span class="sxs-lookup"><span data-stu-id="0d10d-216">**UnsupportedQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-217">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0d10d-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-218">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-219">Один или несколько запросов, описывающих набор классов, которые не поддерживаются поставщиком класса.</span><span class="sxs-lookup"><span data-stu-id="0d10d-219">One or more queries that describe the set of classes that the class provider does not support.</span></span> <span data-ttu-id="0d10d-220">Это свойство используется для вычитания из набора классов, подразумеваемых **ресултсеткуериес**.</span><span class="sxs-lookup"><span data-stu-id="0d10d-220">Use this property to subtract from the set of classes implied by **ResultSetQueries**.</span></span>

</dd> <dt>

<span data-ttu-id="0d10d-221">**Version**</span><span class="sxs-lookup"><span data-stu-id="0d10d-221">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d10d-222">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d10d-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d10d-223">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0d10d-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0d10d-224">Версия этого поставщика класса.</span><span class="sxs-lookup"><span data-stu-id="0d10d-224">Version of this class provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d10d-225">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d10d-225">Remarks</span></span>

<span data-ttu-id="0d10d-226">Класс **\_ \_ класспровидеррегистратион** является производным от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md), который является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-226">The **\_\_ClassProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="0d10d-227">Свойства, наследуемые от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md) , указывают, поддерживает ли поставщик класса получение, изменение, удаление, перечисление и обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="0d10d-227">The properties inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) indicate whether or not the class provider supports data retrieval, modification, deletion, enumeration and query processing.</span></span> <span data-ttu-id="0d10d-228">Свойство **интерактионтипе** указывает, предназначен ли поставщик класса в качестве поставщика Pull или Push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="0d10d-228">The **InteractionType** property specifies whether or not the class provider is designed as a pull or push provider.</span></span> <span data-ttu-id="0d10d-229">Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="0d10d-229">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<span data-ttu-id="0d10d-230">Класс [**\_ \_ провидеррегистратион**](--providerregistration.md) определяет свойство [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="0d10d-230">The [**\_\_ProviderRegistration**](--providerregistration.md) class defines the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) property.</span></span> <span data-ttu-id="0d10d-231">Только администраторы могут зарегистрировать поставщик, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и **\_ \_ класспровидеррегистратион**.</span><span class="sxs-lookup"><span data-stu-id="0d10d-231">Only administrators can register a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_ClassProviderRegistration**.</span></span> <span data-ttu-id="0d10d-232">Только администраторы могут удалить поставщика.</span><span class="sxs-lookup"><span data-stu-id="0d10d-232">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d10d-233">Требования</span><span class="sxs-lookup"><span data-stu-id="0d10d-233">Requirements</span></span>



| <span data-ttu-id="0d10d-234">Требование</span><span class="sxs-lookup"><span data-stu-id="0d10d-234">Requirement</span></span> | <span data-ttu-id="0d10d-235">Значение</span><span class="sxs-lookup"><span data-stu-id="0d10d-235">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0d10d-236">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d10d-236">Minimum supported client</span></span><br/> | <span data-ttu-id="0d10d-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d10d-237">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0d10d-238">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d10d-238">Minimum supported server</span></span><br/> | <span data-ttu-id="0d10d-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d10d-239">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0d10d-240">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0d10d-240">Namespace</span></span><br/>                | <span data-ttu-id="0d10d-241">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="0d10d-241">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0d10d-242">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d10d-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d10d-243">**\_\_обжектпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="0d10d-243">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="0d10d-244">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="0d10d-244">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="0d10d-245">Регистрация поставщика класса</span><span class="sxs-lookup"><span data-stu-id="0d10d-245">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="0d10d-246">Регистрация поставщика экземпляра</span><span class="sxs-lookup"><span data-stu-id="0d10d-246">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="0d10d-247">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="0d10d-247">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

