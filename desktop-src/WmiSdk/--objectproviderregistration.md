---
description: Выступает в качестве родительского класса для классов, которые используются для регистрации поставщиков классов и экземпляров в WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: Класс __ObjectProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345902"
---
# <a name="__objectproviderregistration-class"></a><span data-ttu-id="80d15-103">\_\_Класс Обжектпровидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="80d15-103">\_\_ObjectProviderRegistration class</span></span>

<span data-ttu-id="80d15-104">Абстрактный системный класс **\_ \_ обжектпровидеррегистратион** выступает в качестве родительского класса для классов, которые используются для регистрации поставщиков классов и экземпляров в WMI.</span><span class="sxs-lookup"><span data-stu-id="80d15-104">The **\_\_ObjectProviderRegistration** abstract system class serves as the parent class for classes that are used to register class and instance providers in WMI.</span></span>

<span data-ttu-id="80d15-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="80d15-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="80d15-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="80d15-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="80d15-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80d15-107">Syntax</span></span>

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="80d15-108">Члены</span><span class="sxs-lookup"><span data-stu-id="80d15-108">Members</span></span>

<span data-ttu-id="80d15-109">Класс **\_ \_ обжектпровидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="80d15-109">The **\_\_ObjectProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="80d15-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="80d15-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80d15-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="80d15-111">Properties</span></span>

<span data-ttu-id="80d15-112">Класс **\_ \_ обжектпровидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="80d15-112">The **\_\_ObjectProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80d15-113">**интерактионтипе**</span><span class="sxs-lookup"><span data-stu-id="80d15-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-114">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="80d15-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-116">Указывает, предоставляет ли поставщик класса или экземпляра собственные данные или использует WMI и репозиторий модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="80d15-116">Indicates whether or not the class or instance provider supplies its own data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="80d15-117">Поставщики услуг извлечения поддерживают динамический доступ к своим данным, а поставщики push-уведомлений хранят свои данные в репозитории CIM и используют инструментарий WMI для предоставления доступа к ним.</span><span class="sxs-lookup"><span data-stu-id="80d15-117">Pull providers support dynamic access to their data, and push providers store their data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="80d15-118">Дополнительные сведения см. в разделе [Определение состояния принудительной отправки или извлечения](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="80d15-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="80d15-119">Значение по умолчанию — 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="80d15-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="80d15-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>По **запросу** (0)</span><span class="sxs-lookup"><span data-stu-id="80d15-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="80d15-121">Поставщик является поставщиком опрашивающей репликации.</span><span class="sxs-lookup"><span data-stu-id="80d15-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="80d15-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Принудительная отправка** (1)</span><span class="sxs-lookup"><span data-stu-id="80d15-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="80d15-123">Поставщик является поставщиком услуг push-уведомлений.</span><span class="sxs-lookup"><span data-stu-id="80d15-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="80d15-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**Пушверифи** (2)</span><span class="sxs-lookup"><span data-stu-id="80d15-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="80d15-125">Поставщик — это поставщик принудительной проверки.</span><span class="sxs-lookup"><span data-stu-id="80d15-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="80d15-126">Обратите внимание, что в настоящее время принудительная проверка не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="80d15-126">Note that push-verify is not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80d15-127">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="80d15-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-128">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="80d15-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="80d15-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80d15-130">Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту поставщика объектов.</span><span class="sxs-lookup"><span data-stu-id="80d15-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents an object path to the object provider.</span></span> <span data-ttu-id="80d15-131">Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="80d15-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="80d15-132">**куерисуппортлевелс**</span><span class="sxs-lookup"><span data-stu-id="80d15-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="80d15-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="80d15-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-135">Массив типов поддержки, реализованных поставщиком для обработки запросов.</span><span class="sxs-lookup"><span data-stu-id="80d15-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="80d15-136">Поставщики классов не поддерживают запросы любого типа.</span><span class="sxs-lookup"><span data-stu-id="80d15-136">Class providers do not support any type of queries.</span></span> <span data-ttu-id="80d15-137">Поставщики экземпляров могут установить **куерисуппортлевелс** в **значение NULL** , если они не поддерживают обработку запросов.</span><span class="sxs-lookup"><span data-stu-id="80d15-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="80d15-138">Поставщики, поддерживающие запросы, реализуют метод [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) и присвойте этому свойству одно или несколько из следующих значений (тип свойства является массивом).</span><span class="sxs-lookup"><span data-stu-id="80d15-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values (the property type is an array).</span></span>

<span data-ttu-id="80d15-139">"WQL: Унариселект"</span><span class="sxs-lookup"><span data-stu-id="80d15-139">"WQL:UnarySelect"</span></span>

<span data-ttu-id="80d15-140">"WQL: References"</span><span class="sxs-lookup"><span data-stu-id="80d15-140">"WQL:References"</span></span>

<span data-ttu-id="80d15-141">"WQL: соединители"</span><span class="sxs-lookup"><span data-stu-id="80d15-141">"WQL:Associators"</span></span>

<span data-ttu-id="80d15-142">"WQL: V1ProviderDefined"</span><span class="sxs-lookup"><span data-stu-id="80d15-142">"WQL:V1ProviderDefined"</span></span>

</dd> <dt>

<span data-ttu-id="80d15-143">**суппортсбатчинг**</span><span class="sxs-lookup"><span data-stu-id="80d15-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80d15-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-146">Не используется.</span><span class="sxs-lookup"><span data-stu-id="80d15-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="80d15-147">**суппортсделете**</span><span class="sxs-lookup"><span data-stu-id="80d15-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80d15-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-150">Если **значение — true**, поставщик поддерживает удаление данных.</span><span class="sxs-lookup"><span data-stu-id="80d15-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="80d15-151">True</span><span class="sxs-lookup"><span data-stu-id="80d15-151">True</span></span>
</dt> <dd>

<span data-ttu-id="80d15-152">Поставщик поддерживает удаление классов или экземпляров путем реализации одного из следующих методов [**::D елетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (поставщики классов) или [**IWbemServices::D елетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (поставщики экземпляров).</span><span class="sxs-lookup"><span data-stu-id="80d15-152">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="80d15-153">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d15-153">False</span></span>
</dt> <dd>

<span data-ttu-id="80d15-154">Поставщик не поддерживает удаление данных и возвращает **поставщик WBEM E, \_ \_ \_ не \_ поддерживающий** [**делетеклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) или [**делетеинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="80d15-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80d15-155">**суппортсенумератион**</span><span class="sxs-lookup"><span data-stu-id="80d15-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-156">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80d15-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-157">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-158">Если **значение — true**, поставщик поддерживает перечисление данных.</span><span class="sxs-lookup"><span data-stu-id="80d15-158">If **True**, the provider supports data enumeration.</span></span>

<dt>

<span data-ttu-id="80d15-159">True</span><span class="sxs-lookup"><span data-stu-id="80d15-159">True</span></span>
</dt> <dd>

<span data-ttu-id="80d15-160">Поставщик поддерживает перечисление данных путем реализации одного из следующих методов [**IWbemServices:: креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (классы поставщиков) или [**IWbemServices:: креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (поставщики экземпляров).</span><span class="sxs-lookup"><span data-stu-id="80d15-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="80d15-161">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d15-161">False</span></span>
</dt> <dd>

<span data-ttu-id="80d15-162">Поставщик не поддерживает перечисление данных и возвращает **поставщик WBEM \_ E \_ , \_ не \_ поддерживающий** [**креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) или [**креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="80d15-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80d15-163">**суппортсжет**</span><span class="sxs-lookup"><span data-stu-id="80d15-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-164">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80d15-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-166">Если **значение — true**, то поставщик класса или экземпляра поддерживает извлечение данных.</span><span class="sxs-lookup"><span data-stu-id="80d15-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="80d15-167">True</span><span class="sxs-lookup"><span data-stu-id="80d15-167">True</span></span>
</dt> <dd>

<span data-ttu-id="80d15-168">Поставщик поддерживает получение данных путем реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="80d15-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="80d15-169">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d15-169">False</span></span>
</dt> <dd>

<span data-ttu-id="80d15-170">Поставщик не поддерживает извлечение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** из [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="80d15-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80d15-171">**суппортспут**</span><span class="sxs-lookup"><span data-stu-id="80d15-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80d15-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-174">Если **значение — true**, то поставщик класса или экземпляра поддерживает изменение данных.</span><span class="sxs-lookup"><span data-stu-id="80d15-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="80d15-175">True</span><span class="sxs-lookup"><span data-stu-id="80d15-175">True</span></span>
</dt> <dd>

<span data-ttu-id="80d15-176">Поставщик поддерживает изменение класса или экземпляра путем реализации одного из следующих методов [**::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (поставщики классов) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (поставщики классов).</span><span class="sxs-lookup"><span data-stu-id="80d15-176">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>

<span data-ttu-id="80d15-177">Неверно</span><span class="sxs-lookup"><span data-stu-id="80d15-177">False</span></span>
</dt> <dd>

<span data-ttu-id="80d15-178">Поставщик не поддерживает изменение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** [**путклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) или [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="80d15-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="80d15-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="80d15-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80d15-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="80d15-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80d15-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="80d15-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="80d15-182">Не используется.</span><span class="sxs-lookup"><span data-stu-id="80d15-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="80d15-183">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80d15-183">Remarks</span></span>

<span data-ttu-id="80d15-184">Класс **\_ \_ обжектпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="80d15-184">The **\_\_ObjectProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="80d15-185">Поставщики классов должны присвоить свойству **Суппортсенумератион** **значение true** , поскольку поставщики должны иметь возможность предоставлять Инструментарий WMI со списком их классов.</span><span class="sxs-lookup"><span data-stu-id="80d15-185">Class providers must set the **SupportsEnumeration** property to **True** because the providers must be able to supply WMI with a list of their classes.</span></span> <span data-ttu-id="80d15-186">Если поставщик класса пытается установить это свойство в **значение false**, WMI помечает регистрацию как недопустимую.</span><span class="sxs-lookup"><span data-stu-id="80d15-186">If a class provider attempts to set this property to **False**, WMI flags the registration as illegal.</span></span> <span data-ttu-id="80d15-187">Поставщики экземпляров не обязательно должны поддерживать перечисление и могут установить для **суппортсенумератион** значение **true** или **false**.</span><span class="sxs-lookup"><span data-stu-id="80d15-187">Instance providers are not required to support enumeration, and can choose to set **SupportsEnumeration** to either **True** or **False**.</span></span>

<span data-ttu-id="80d15-188">Поставщик, который устанавливает **куерисуппортлевелс** в "WQL: унариселект", может принимать запрос, состоящий из базовой инструкции SELECT, которая поддерживается в WMI версии 1,0.</span><span class="sxs-lookup"><span data-stu-id="80d15-188">A provider that sets **QuerySupportLevels** to "WQL:UnarySelect" can accept a query that consists of the basic SELECT statement as supported in WMI version 1.0.</span></span> <span data-ttu-id="80d15-189">Как поставщик классов, так и поставщики экземпляров должны иметь возможность обрабатывать системное свойство **\_ \_ класса** .</span><span class="sxs-lookup"><span data-stu-id="80d15-189">Both class and instance providers are expected to be able to handle the **\_\_CLASS** system property.</span></span> <span data-ttu-id="80d15-190">Поставщики классов также должны обрабатывать свойство системы **\_ \_ суперкласса** и оператор ISA.</span><span class="sxs-lookup"><span data-stu-id="80d15-190">Class providers are also expected to process the **\_\_SUPERCLASS** system property and the ISA operator.</span></span> <span data-ttu-id="80d15-191">Оператор ISA используется для расширения результирующего набора на производные классы.</span><span class="sxs-lookup"><span data-stu-id="80d15-191">The ISA operator is used to expand a result set to derived classes.</span></span> <span data-ttu-id="80d15-192">Если поставщику предоставлен запрос, который он не может интерпретировать, он запрашивает его обработку WMI, возвращая **\_ \_ слишком \_ сложное значение ошибки WBEM E** .</span><span class="sxs-lookup"><span data-stu-id="80d15-192">If a provider is given a query that it cannot interpret, it requests that WMI handle it by returning the **WBEM\_E\_TOO\_COMPLEX** error value.</span></span> <span data-ttu-id="80d15-193">Описание допустимого синтаксиса WQL см. в разделе [запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="80d15-193">For a description of valid WQL syntax, see [Querying with WQL](querying-with-wql.md).</span></span>

<span data-ttu-id="80d15-194">Поставщик, устанавливающий **куерисуппортлевелс** в **WQL: V1ProviderDefined** , может попытаться поддерживать более крупный набор синтаксиса SQL на своем собственном риске, например в `ORDER BY` предложении.</span><span class="sxs-lookup"><span data-stu-id="80d15-194">A provider that sets **QuerySupportLevels** to **WQL:V1ProviderDefined** can try to support a larger set of the SQL syntax at its own risk, such as the `ORDER BY` clause.</span></span> <span data-ttu-id="80d15-195">Инструментарий WMI не интерпретирует дополнительные предложения или пытается убедиться в правильности результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="80d15-195">WMI does not interpret the additional clauses, or attempt to ensure that the result set is correct.</span></span>

<span data-ttu-id="80d15-196">Только администраторы могут зарегистрировать или удалить поставщик, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и зарегистрировав его.</span><span class="sxs-lookup"><span data-stu-id="80d15-196">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="80d15-197">Требования</span><span class="sxs-lookup"><span data-stu-id="80d15-197">Requirements</span></span>



| <span data-ttu-id="80d15-198">Требование</span><span class="sxs-lookup"><span data-stu-id="80d15-198">Requirement</span></span> | <span data-ttu-id="80d15-199">Значение</span><span class="sxs-lookup"><span data-stu-id="80d15-199">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="80d15-200">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80d15-200">Minimum supported client</span></span><br/> | <span data-ttu-id="80d15-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80d15-201">Windows Vista</span></span><br/>       |
| <span data-ttu-id="80d15-202">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80d15-202">Minimum supported server</span></span><br/> | <span data-ttu-id="80d15-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80d15-203">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="80d15-204">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="80d15-204">Namespace</span></span><br/>                | <span data-ttu-id="80d15-205">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="80d15-205">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="80d15-206">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80d15-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80d15-207">**\_\_провидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="80d15-207">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="80d15-208">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="80d15-208">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="80d15-209">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="80d15-209">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

