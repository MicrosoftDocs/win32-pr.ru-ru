---
description: Регистрирует поставщики свойств в WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: Класс __PropertyProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545767"
---
# <a name="__propertyproviderregistration-class"></a><span data-ttu-id="a5315-103">\_\_Класс Пропертипровидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="a5315-103">\_\_PropertyProviderRegistration class</span></span>

<span data-ttu-id="a5315-104">Системный класс **\_ \_ пропертипровидеррегистратион** регистрирует поставщиков свойств в WMI.</span><span class="sxs-lookup"><span data-stu-id="a5315-104">The **\_\_PropertyProviderRegistration** system class registers property providers in WMI.</span></span>

<span data-ttu-id="a5315-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a5315-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a5315-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a5315-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5315-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5315-107">Syntax</span></span>

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a><span data-ttu-id="a5315-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a5315-108">Members</span></span>

<span data-ttu-id="a5315-109">Класс **\_ \_ пропертипровидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a5315-109">The **\_\_PropertyProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="a5315-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5315-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5315-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a5315-111">Properties</span></span>

<span data-ttu-id="a5315-112">Класс **\_ \_ пропертипровидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a5315-112">The **\_\_PropertyProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a5315-113">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="a5315-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5315-114">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="a5315-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="a5315-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a5315-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a5315-116">Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="a5315-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the property provider.</span></span> <span data-ttu-id="a5315-117">Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="a5315-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="a5315-118">**суппортсжет**</span><span class="sxs-lookup"><span data-stu-id="a5315-118">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5315-119">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a5315-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a5315-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a5315-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a5315-121">Описывает, поддерживает ли поставщик класса или экземпляра извлечение данных.</span><span class="sxs-lookup"><span data-stu-id="a5315-121">Describes whether the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="a5315-122">True</span><span class="sxs-lookup"><span data-stu-id="a5315-122">True</span></span>
</dt> <dd>

<span data-ttu-id="a5315-123">Поставщик поддерживает получение данных путем реализации [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="a5315-123">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="a5315-124">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5315-124">False</span></span>
</dt> <dd>

<span data-ttu-id="a5315-125">Поставщик не поддерживает извлечение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** из [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="a5315-125">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a5315-126">**суппортспут**</span><span class="sxs-lookup"><span data-stu-id="a5315-126">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5315-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a5315-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a5315-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a5315-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a5315-129">Описывает, поддерживает ли поставщик класса или экземпляра изменение данных.</span><span class="sxs-lookup"><span data-stu-id="a5315-129">Describes whether the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="a5315-130">True</span><span class="sxs-lookup"><span data-stu-id="a5315-130">True</span></span>
</dt> <dd>

<span data-ttu-id="a5315-131">Поставщик поддерживает изменение класса или экземпляра, реализуя один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="a5315-131">The provider supports class or instance modification by implementing one of the following methods:</span></span>

-   <span data-ttu-id="a5315-132">[**IWbemServices::P утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (поставщики классов)</span><span class="sxs-lookup"><span data-stu-id="a5315-132">[**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers)</span></span>
-   <span data-ttu-id="a5315-133">[**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (поставщики классов)</span><span class="sxs-lookup"><span data-stu-id="a5315-133">[**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers)</span></span>

</dd> <dt>

<span data-ttu-id="a5315-134">Неверно</span><span class="sxs-lookup"><span data-stu-id="a5315-134">False</span></span>
</dt> <dd>

<span data-ttu-id="a5315-135">Поставщик не поддерживает изменение данных и возвращает **\_ поставщик WBEM E, \_ \_ не \_ поддерживающий** [**путклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) или [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="a5315-135">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5315-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5315-136">Remarks</span></span>

<span data-ttu-id="a5315-137">Класс **\_ \_ пропертипровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="a5315-137">The **\_\_PropertyProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="a5315-138">Только администраторы могут зарегистрировать поставщик свойств, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и **\_ \_ пропертипровидеррегистратион**.</span><span class="sxs-lookup"><span data-stu-id="a5315-138">Only administrators can register a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_PropertyProviderRegistration**.</span></span> <span data-ttu-id="a5315-139">Только администраторы могут удалить поставщик свойств.</span><span class="sxs-lookup"><span data-stu-id="a5315-139">Only administrators can delete a property provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5315-140">Требования</span><span class="sxs-lookup"><span data-stu-id="a5315-140">Requirements</span></span>



| <span data-ttu-id="a5315-141">Требование</span><span class="sxs-lookup"><span data-stu-id="a5315-141">Requirement</span></span> | <span data-ttu-id="a5315-142">Значение</span><span class="sxs-lookup"><span data-stu-id="a5315-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a5315-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5315-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a5315-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5315-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a5315-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5315-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a5315-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5315-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="a5315-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a5315-147">Namespace</span></span><br/>                | <span data-ttu-id="a5315-148">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="a5315-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="a5315-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5315-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5315-150">**\_\_провидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="a5315-150">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="a5315-151">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="a5315-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="a5315-152">Регистрация поставщика свойств</span><span class="sxs-lookup"><span data-stu-id="a5315-152">Registering a Property Provider</span></span>](registering-a-property-provider.md)
</dt> </dl>

 

