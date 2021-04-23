---
description: Выступает в качестве родительского класса для классов регистрации для различных типов поставщиков.
ms.assetid: 1e5d95cb-0961-4be8-b80a-37b598c9ccfe
ms.tgt_platform: multiple
title: Класс __ProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7359f3d5cdcfb2447b724fd6d369a1029d8fcd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156618"
---
# <a name="__providerregistration-class"></a><span data-ttu-id="38a2f-103">\_\_Класс Провидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="38a2f-103">\_\_ProviderRegistration class</span></span>

<span data-ttu-id="38a2f-104">Абстрактный системный класс **\_ \_ провидеррегистратион** выступает в качестве родительского класса для классов регистрации для различных типов поставщиков.</span><span class="sxs-lookup"><span data-stu-id="38a2f-104">The **\_\_ProviderRegistration** abstract system class serves as the parent class for registration classes for various types of providers.</span></span>

<span data-ttu-id="38a2f-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="38a2f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="38a2f-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="38a2f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38a2f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38a2f-107">Syntax</span></span>

``` syntax
[abstract]
class __ProviderRegistration : __SystemClass
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="38a2f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="38a2f-108">Members</span></span>

<span data-ttu-id="38a2f-109">Класс **\_ \_ провидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38a2f-109">The **\_\_ProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="38a2f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="38a2f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38a2f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="38a2f-111">Properties</span></span>

<span data-ttu-id="38a2f-112">Класс **\_ \_ провидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38a2f-112">The **\_\_ProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38a2f-113">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="38a2f-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38a2f-114">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="38a2f-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="38a2f-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38a2f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38a2f-116">Ссылка на экземпляр [**\_ \_ поставщика**](--provider.md) , представляющий путь к объекту поставщика.</span><span class="sxs-lookup"><span data-stu-id="38a2f-116">Reference to an instance of [**\_\_Provider**](--provider.md) representing the object path to the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38a2f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38a2f-117">Remarks</span></span>

<span data-ttu-id="38a2f-118">Класс **\_ \_ провидеррегистратион** является производным от [**\_ \_ системкласс**](--systemclass.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="38a2f-118">The **\_\_ProviderRegistration** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="38a2f-119">Экземпляры класса System **\_ \_ провидеррегистратион** не создаются.</span><span class="sxs-lookup"><span data-stu-id="38a2f-119">Instances of the **\_\_ProviderRegistration** system class are never created.</span></span> <span data-ttu-id="38a2f-120">Классы, используемые поставщиками для создания экземпляров для регистрации, наследуются прямо или косвенно от этого класса.</span><span class="sxs-lookup"><span data-stu-id="38a2f-120">The classes that providers use to create instances for registration derive either directly or indirectly from this class.</span></span> <span data-ttu-id="38a2f-121">Ниже приведены классы:</span><span class="sxs-lookup"><span data-stu-id="38a2f-121">These classes are:</span></span>

[<span data-ttu-id="38a2f-122">**\_\_класспровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="38a2f-122">**\_\_ClassProviderRegistration**</span></span>](--classproviderregistration.md)

[<span data-ttu-id="38a2f-123">**\_\_евентконсумерпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="38a2f-123">**\_\_EventConsumerProviderRegistration**</span></span>](--eventconsumerproviderregistration.md)

[<span data-ttu-id="38a2f-124">**\_\_евентпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="38a2f-124">**\_\_EventProviderRegistration**</span></span>](--eventproviderregistration.md)

[<span data-ttu-id="38a2f-125">**\_\_инстанцепровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="38a2f-125">**\_\_InstanceProviderRegistration**</span></span>](--instanceproviderregistration.md)

[<span data-ttu-id="38a2f-126">**\_\_месодпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="38a2f-126">**\_\_MethodProviderRegistration**</span></span>](--methodproviderregistration.md)

[<span data-ttu-id="38a2f-127">**\_\_обжектпровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="38a2f-127">**\_\_ObjectProviderRegistration**</span></span>](--objectproviderregistration.md)

[<span data-ttu-id="38a2f-128">**\_\_пропертипровидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="38a2f-128">**\_\_PropertyProviderRegistration**</span></span>](--propertyproviderregistration.md)

<span data-ttu-id="38a2f-129">Только администраторы могут зарегистрировать или удалить поставщик, создав экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и зарегистрировав его.</span><span class="sxs-lookup"><span data-stu-id="38a2f-129">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="38a2f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="38a2f-130">Requirements</span></span>



| <span data-ttu-id="38a2f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="38a2f-131">Requirement</span></span> | <span data-ttu-id="38a2f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="38a2f-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="38a2f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38a2f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="38a2f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38a2f-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="38a2f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38a2f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="38a2f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38a2f-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="38a2f-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38a2f-137">Namespace</span></span><br/>                | <span data-ttu-id="38a2f-138">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="38a2f-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="38a2f-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38a2f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38a2f-140">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="38a2f-140">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="38a2f-141">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="38a2f-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="38a2f-142">Регистрация поставщика</span><span class="sxs-lookup"><span data-stu-id="38a2f-142">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

