---
description: Регистрирует поставщиков экземпляров в WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: Класс __InstanceProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702675"
---
# <a name="__instanceproviderregistration-class"></a><span data-ttu-id="2d08d-103">\_\_Класс Инстанцепровидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="2d08d-103">\_\_InstanceProviderRegistration class</span></span>

<span data-ttu-id="2d08d-104">Системный класс **\_ \_ инстанцепровидеррегистратион** регистрирует поставщиков экземпляров в WMI.</span><span class="sxs-lookup"><span data-stu-id="2d08d-104">The **\_\_InstanceProviderRegistration** system class registers instance providers in WMI.</span></span>

<span data-ttu-id="2d08d-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2d08d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2d08d-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2d08d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d08d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d08d-107">Syntax</span></span>

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="2d08d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2d08d-108">Members</span></span>

<span data-ttu-id="2d08d-109">Класс **\_ \_ инстанцепровидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d08d-109">The **\_\_InstanceProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="2d08d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d08d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2d08d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d08d-111">Properties</span></span>

<span data-ttu-id="2d08d-112">Класс **\_ \_ инстанцепровидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2d08d-112">The **\_\_InstanceProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2d08d-113">**интерактионтипе**</span><span class="sxs-lookup"><span data-stu-id="2d08d-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-114">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="2d08d-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-116">Указывает, что поставщик класса или экземпляра предоставляет данные или получает данные из WMI и репозитория модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="2d08d-116">Indicates that a class or instance provider supplies data, or retrieves data from WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="2d08d-117">Поставщики услуг извлечения поддерживают динамический доступ к своим данным. и поставщики push-уведомлений хранят свои данные в репозитории CIM и используют инструментарий WMI для предоставления доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="2d08d-117">Pull providers support dynamic access to their data; and push providers store their data in the CIM repository, and use WMI to provide access to it.</span></span> <span data-ttu-id="2d08d-118">Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="2d08d-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="2d08d-119">Значение по умолчанию — 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="2d08d-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="2d08d-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>По **запросу** (0)</span><span class="sxs-lookup"><span data-stu-id="2d08d-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2d08d-121">Поставщик является поставщиком опрашивающей репликации.</span><span class="sxs-lookup"><span data-stu-id="2d08d-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="2d08d-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Принудительная отправка** (1)</span><span class="sxs-lookup"><span data-stu-id="2d08d-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2d08d-123">Поставщик является поставщиком услуг push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2d08d-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="2d08d-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Пушверифи** (2)</span><span class="sxs-lookup"><span data-stu-id="2d08d-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2d08d-125">Поставщик — это поставщик принудительной проверки.</span><span class="sxs-lookup"><span data-stu-id="2d08d-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="2d08d-126">Обратите внимание, что в настоящее время поставщики Push-проверки не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2d08d-126">Note that push-verify providers are not currently supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d08d-127">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="2d08d-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-128">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="2d08d-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2d08d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-130">Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту для поставщика экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2d08d-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path to the instance provider.</span></span> <span data-ttu-id="2d08d-131">Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="2d08d-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d08d-132">**куерисуппортлевелс**</span><span class="sxs-lookup"><span data-stu-id="2d08d-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="2d08d-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-135">Массив типов поддержки, реализованных поставщиком для обработки запросов.</span><span class="sxs-lookup"><span data-stu-id="2d08d-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="2d08d-136">Поставщики классов не поддерживают все типы запросов.</span><span class="sxs-lookup"><span data-stu-id="2d08d-136">Class providers do not support all types of queries.</span></span> <span data-ttu-id="2d08d-137">Поставщики экземпляров могут установить **куерисуппортлевелс** в **значение NULL** , если они не поддерживают обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="2d08d-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="2d08d-138">Поставщики, поддерживающие запросы, реализуют метод [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) и присвойте этому свойству одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="2d08d-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="2d08d-139">("WQL: Унариселект")</span><span class="sxs-lookup"><span data-stu-id="2d08d-139">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2d08d-140">("WQL: References")</span><span class="sxs-lookup"><span data-stu-id="2d08d-140">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2d08d-141">("WQL: соединители")</span><span class="sxs-lookup"><span data-stu-id="2d08d-141">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="2d08d-142">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="2d08d-142">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2d08d-143">**суппортсбатчинг**</span><span class="sxs-lookup"><span data-stu-id="2d08d-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d08d-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-146">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2d08d-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2d08d-147">**суппортсделете**</span><span class="sxs-lookup"><span data-stu-id="2d08d-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d08d-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-150">Если **значение — true**, поставщик поддерживает удаление данных.</span><span class="sxs-lookup"><span data-stu-id="2d08d-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="2d08d-151">True</span><span class="sxs-lookup"><span data-stu-id="2d08d-151">True</span></span>
</dt> <dd>

<span data-ttu-id="2d08d-152">Поставщик поддерживает удаление классов или экземпляров путем реализации [**IWbemServices::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (поставщики классов) или [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (поставщики экземпляров).</span><span class="sxs-lookup"><span data-stu-id="2d08d-152">The provider supports class or instance deletion by implementing either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="2d08d-153">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d08d-153">False</span></span>
</dt> <dd>

<span data-ttu-id="2d08d-154">Поставщик не поддерживает удаление данных и возвращает **поставщик WBEM E, \_ \_ \_ не \_ поддерживающий** [**делетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) или [**делетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="2d08d-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d08d-155">**суппортсенумератион**</span><span class="sxs-lookup"><span data-stu-id="2d08d-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-156">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d08d-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-158">Если **значение — true**, поставщик поддерживает перечисление данных.</span><span class="sxs-lookup"><span data-stu-id="2d08d-158">If **True**, the provider supports data enumeration.</span></span>

<dt>



 <span data-ttu-id="2d08d-159">Условия</span><span class="sxs-lookup"><span data-stu-id="2d08d-159">(True)</span></span>


</dt> <dd>

<span data-ttu-id="2d08d-160">Поставщик поддерживает перечисление данных путем реализации одного из следующих методов [**IWbemServices:: креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (классы поставщиков) или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (поставщики экземпляров).</span><span class="sxs-lookup"><span data-stu-id="2d08d-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="2d08d-161">IsFalse</span><span class="sxs-lookup"><span data-stu-id="2d08d-161">(False)</span></span>


</dt> <dd>

<span data-ttu-id="2d08d-162">Поставщик не поддерживает перечисление данных и возвращает **поставщик WBEM \_ E \_ , \_ не \_ поддерживающий** [**креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) или [**креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="2d08d-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d08d-163">**суппортсжет**</span><span class="sxs-lookup"><span data-stu-id="2d08d-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-164">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d08d-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-166">Если **значение — true**, то поставщик класса или экземпляра поддерживает извлечение данных.</span><span class="sxs-lookup"><span data-stu-id="2d08d-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="2d08d-167">True</span><span class="sxs-lookup"><span data-stu-id="2d08d-167">True</span></span>
</dt> <dd>

<span data-ttu-id="2d08d-168">Поставщик поддерживает получение данных путем реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="2d08d-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="2d08d-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="2d08d-169">False</span></span>
</dt> <dd>

<span data-ttu-id="2d08d-170">Поставщик не поддерживает извлечение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** из [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="2d08d-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d08d-171">**суппортспут**</span><span class="sxs-lookup"><span data-stu-id="2d08d-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d08d-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-174">Если **значение — true**, то поставщик класса или экземпляра поддерживает изменение данных.</span><span class="sxs-lookup"><span data-stu-id="2d08d-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>



 <span data-ttu-id="2d08d-175">Условия</span><span class="sxs-lookup"><span data-stu-id="2d08d-175">(True)</span></span>


</dt> <dd>

<span data-ttu-id="2d08d-176">Поставщик поддерживает изменение класса или экземпляра, реализуя один из следующих методов: [**IWbemServices::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (поставщики классов) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (поставщики классов).</span><span class="sxs-lookup"><span data-stu-id="2d08d-176">The provider supports class or instance modification by implementing one of the following methods: [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="2d08d-177">IsFalse</span><span class="sxs-lookup"><span data-stu-id="2d08d-177">(False)</span></span>


</dt> <dd>

<span data-ttu-id="2d08d-178">Поставщик не поддерживает изменение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** [**путклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) или [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="2d08d-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2d08d-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="2d08d-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2d08d-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2d08d-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2d08d-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="2d08d-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2d08d-182">Не используется.</span><span class="sxs-lookup"><span data-stu-id="2d08d-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2d08d-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2d08d-183">Remarks</span></span>

<span data-ttu-id="2d08d-184">Класс **\_ \_ инстанцепровидеррегистратион** является производным от [**\_ \_ обжектпровидеррегистратион**](--objectproviderregistration.md), который является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="2d08d-184">The **\_\_InstanceProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="2d08d-185">Только администраторы могут зарегистрировать поставщик экземпляра, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и **\_ \_ инстанцепровидеррегистратион**.</span><span class="sxs-lookup"><span data-stu-id="2d08d-185">Only administrators can register an instance provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_InstanceProviderRegistration**.</span></span> <span data-ttu-id="2d08d-186">Только администраторы могут удалить поставщика.</span><span class="sxs-lookup"><span data-stu-id="2d08d-186">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d08d-187">Требования</span><span class="sxs-lookup"><span data-stu-id="2d08d-187">Requirements</span></span>



| <span data-ttu-id="2d08d-188">Требование</span><span class="sxs-lookup"><span data-stu-id="2d08d-188">Requirement</span></span> | <span data-ttu-id="2d08d-189">Значение</span><span class="sxs-lookup"><span data-stu-id="2d08d-189">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2d08d-190">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d08d-190">Minimum supported client</span></span><br/> | <span data-ttu-id="2d08d-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d08d-191">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2d08d-192">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d08d-192">Minimum supported server</span></span><br/> | <span data-ttu-id="2d08d-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d08d-193">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2d08d-194">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2d08d-194">Namespace</span></span><br/>                | <span data-ttu-id="2d08d-195">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="2d08d-195">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2d08d-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d08d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d08d-197">**\_\_обжектпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="2d08d-197">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="2d08d-198">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="2d08d-198">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2d08d-199">Регистрация поставщика класса</span><span class="sxs-lookup"><span data-stu-id="2d08d-199">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="2d08d-200">Регистрация поставщика экземпляра</span><span class="sxs-lookup"><span data-stu-id="2d08d-200">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

