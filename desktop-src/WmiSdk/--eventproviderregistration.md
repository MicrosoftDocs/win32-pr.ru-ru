---
description: Используется для регистрации поставщиков событий с помощью инструментарий управления Windows (WMI) (WMI).
ms.assetid: d87f61a8-5549-4f33-ba67-31b5d72b5282
ms.tgt_platform: multiple
title: Класс __EventProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: caaad1b4ab03cfc1b43e4239b9144d3ceeade82f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693276"
---
# <a name="__eventproviderregistration-class"></a><span data-ttu-id="20332-103">\_\_Класс Евентпровидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="20332-103">\_\_EventProviderRegistration class</span></span>

<span data-ttu-id="20332-104">Класс System **\_ \_ евентпровидеррегистратион** используется для регистрации поставщиков событий с помощью инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="20332-104">The **\_\_EventProviderRegistration** system class is used to register event providers with Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="20332-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="20332-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="20332-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="20332-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20332-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20332-107">Syntax</span></span>

``` syntax
class __EventProviderRegistration : __ProviderRegistration
{
  string         EventQueryList[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="20332-108">Члены</span><span class="sxs-lookup"><span data-stu-id="20332-108">Members</span></span>

<span data-ttu-id="20332-109">Класс **\_ \_ евентпровидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="20332-109">The **\_\_EventProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="20332-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="20332-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20332-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="20332-111">Properties</span></span>

<span data-ttu-id="20332-112">Класс **\_ \_ евентпровидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="20332-112">The **\_\_EventProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20332-113">**евенткуерилист**</span><span class="sxs-lookup"><span data-stu-id="20332-113">**EventQueryList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20332-114">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="20332-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="20332-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="20332-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="20332-116">Один или инструментарий управления Windows (WMI) несколько запросов языка запросов (WQL), описывающих события, поддерживаемые поставщиком событий.</span><span class="sxs-lookup"><span data-stu-id="20332-116">One or more Windows Management Instrumentation Query Language (WQL) queries that describe the events that the event provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="20332-117">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="20332-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20332-118">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="20332-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="20332-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20332-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20332-120">Путь к объекту поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="20332-120">Object path to the event provider.</span></span> <span data-ttu-id="20332-121">Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="20332-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20332-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20332-122">Remarks</span></span>

<span data-ttu-id="20332-123">Только администраторы могут регистрировать или удалять поставщик событий, создавая экземпляр [**\_ \_ Win32Provider**](--win32provider.md) и [**\_ \_ евентпровидеррегистратион**](--eventconsumerproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="20332-123">Only administrators can register or delete an event provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and [**\_\_EventProviderRegistration**](--eventconsumerproviderregistration.md).</span></span> <span data-ttu-id="20332-124">Класс **\_ \_ евентпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="20332-124">The **\_\_EventProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20332-125">Требования</span><span class="sxs-lookup"><span data-stu-id="20332-125">Requirements</span></span>



| <span data-ttu-id="20332-126">Требование</span><span class="sxs-lookup"><span data-stu-id="20332-126">Requirement</span></span> | <span data-ttu-id="20332-127">Значение</span><span class="sxs-lookup"><span data-stu-id="20332-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="20332-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20332-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20332-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20332-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="20332-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20332-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20332-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20332-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="20332-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="20332-132">Namespace</span></span><br/>                | <span data-ttu-id="20332-133">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="20332-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="20332-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20332-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20332-135">**\_\_провидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="20332-135">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="20332-136">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="20332-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="20332-137">Регистрация поставщика событий</span><span class="sxs-lookup"><span data-stu-id="20332-137">Registering an Event Provider</span></span>](registering-an-event-provider.md)
</dt> <dt>

[<span data-ttu-id="20332-138">Создание поставщика событий</span><span class="sxs-lookup"><span data-stu-id="20332-138">Writing an Event Provider</span></span>](writing-an-event-provider.md)
</dt> </dl>

 

