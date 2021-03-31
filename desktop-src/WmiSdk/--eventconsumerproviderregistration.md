---
description: Регистрирует поставщиков объектов-получателей событий с помощью инструментария WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: Класс __EventConsumerProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911975"
---
# <a name="__eventconsumerproviderregistration-class"></a><span data-ttu-id="3dc4a-103">\_\_Класс Евентконсумерпровидеррегистратион</span><span class="sxs-lookup"><span data-stu-id="3dc4a-103">\_\_EventConsumerProviderRegistration class</span></span>

<span data-ttu-id="3dc4a-104">Системный класс **\_ \_ евентконсумерпровидеррегистратион** регистрирует поставщиков потребителей событий с помощью WMI.</span><span class="sxs-lookup"><span data-stu-id="3dc4a-104">The **\_\_EventConsumerProviderRegistration** system class registers event consumer providers with WMI.</span></span>

<span data-ttu-id="3dc4a-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3dc4a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3dc4a-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3dc4a-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc4a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dc4a-107">Syntax</span></span>

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="3dc4a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3dc4a-108">Members</span></span>

<span data-ttu-id="3dc4a-109">Класс **\_ \_ евентконсумерпровидеррегистратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3dc4a-109">The **\_\_EventConsumerProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="3dc4a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dc4a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3dc4a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dc4a-111">Properties</span></span>

<span data-ttu-id="3dc4a-112">Класс **\_ \_ евентконсумерпровидеррегистратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3dc4a-112">The **\_\_EventConsumerProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3dc4a-113">**консумеркласснамес**</span><span class="sxs-lookup"><span data-stu-id="3dc4a-113">**ConsumerClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dc4a-114">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3dc4a-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3dc4a-115">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="3dc4a-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3dc4a-116">Массив имен логических классов потребителей, поддерживаемых поставщиком объектов событий.</span><span class="sxs-lookup"><span data-stu-id="3dc4a-116">Array of names of the logical consumer classes that the event consumer provider supports.</span></span>

</dd> <dt>

<span data-ttu-id="3dc4a-117">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="3dc4a-117">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dc4a-118">Тип данных: **\_ \_ поставщик**</span><span class="sxs-lookup"><span data-stu-id="3dc4a-118">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="3dc4a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3dc4a-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3dc4a-120">Путь к объекту поставщика.</span><span class="sxs-lookup"><span data-stu-id="3dc4a-120">Object path to the provider.</span></span> <span data-ttu-id="3dc4a-121">Это свойство наследуется от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="3dc4a-121">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dc4a-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3dc4a-122">Remarks</span></span>

<span data-ttu-id="3dc4a-123">Класс **\_ \_ евентконсумерпровидеррегистратион** является производным от [**\_ \_ провидеррегистратион**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="3dc4a-123">The **\_\_EventConsumerProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc4a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="3dc4a-124">Requirements</span></span>



| <span data-ttu-id="3dc4a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="3dc4a-125">Requirement</span></span> | <span data-ttu-id="3dc4a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="3dc4a-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3dc4a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dc4a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc4a-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dc4a-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3dc4a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dc4a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc4a-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dc4a-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3dc4a-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3dc4a-131">Namespace</span></span><br/>                | <span data-ttu-id="3dc4a-132">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="3dc4a-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3dc4a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dc4a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc4a-134">**\_\_провидеррегистратион**</span><span class="sxs-lookup"><span data-stu-id="3dc4a-134">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="3dc4a-135">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="3dc4a-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="3dc4a-136">Регистрация поставщика событий-получателя</span><span class="sxs-lookup"><span data-stu-id="3dc4a-136">Registering an Event Consumer Provider</span></span>](registering-an-event-consumer-provider.md)
</dt> <dt>

[<span data-ttu-id="3dc4a-137">Создание поставщика объектов событий</span><span class="sxs-lookup"><span data-stu-id="3dc4a-137">Writing an Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)
</dt> </dl>

 

