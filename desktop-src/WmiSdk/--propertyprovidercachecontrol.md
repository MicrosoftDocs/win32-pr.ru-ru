---
description: Управляет кэшем при выгрузке поставщика свойств.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: Класс __PropertyProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d153049a9635b4b77a1ad09ca0ee64835b9bcfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264803"
---
# <a name="__propertyprovidercachecontrol-class"></a><span data-ttu-id="85649-103">\_\_Класс Пропертипровидеркачеконтрол</span><span class="sxs-lookup"><span data-stu-id="85649-103">\_\_PropertyProviderCacheControl class</span></span>

<span data-ttu-id="85649-104">Класс **\_ \_ пропертипровидеркачеконтрол** управляет кэшем при выгрузке поставщика свойств.</span><span class="sxs-lookup"><span data-stu-id="85649-104">The **\_\_PropertyProviderCacheControl** class controls the cache when a property provider is unloaded.</span></span> <span data-ttu-id="85649-105">Этот класс существует только в \\ корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="85649-105">This class exists only in the \\root namespace.</span></span>

<span data-ttu-id="85649-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="85649-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="85649-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="85649-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="85649-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85649-108">Syntax</span></span>

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="85649-109">Члены</span><span class="sxs-lookup"><span data-stu-id="85649-109">Members</span></span>

<span data-ttu-id="85649-110">Класс **\_ \_ пропертипровидеркачеконтрол** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="85649-110">The **\_\_PropertyProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="85649-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="85649-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85649-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="85649-112">Properties</span></span>

<span data-ttu-id="85649-113">Класс **\_ \_ пропертипровидеркачеконтрол** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="85649-113">The **\_\_PropertyProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85649-114">**клеарафтер**</span><span class="sxs-lookup"><span data-stu-id="85649-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85649-115">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="85649-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="85649-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="85649-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="85649-117">Интервал времени после освобождения WMI поставщиком свойств.</span><span class="sxs-lookup"><span data-stu-id="85649-117">Time interval after WMI releases a property provider.</span></span> <span data-ttu-id="85649-118">Время указано в формате интервала.</span><span class="sxs-lookup"><span data-stu-id="85649-118">The time is in the interval format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85649-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85649-119">Remarks</span></span>

<span data-ttu-id="85649-120">Класс **\_ \_ пропертипровидеркачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="85649-120">The **\_\_PropertyProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="85649-121">Дополнительные сведения см. [в разделе выгрузка поставщика](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="85649-121">For more information, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85649-122">Требования</span><span class="sxs-lookup"><span data-stu-id="85649-122">Requirements</span></span>



| <span data-ttu-id="85649-123">Требование</span><span class="sxs-lookup"><span data-stu-id="85649-123">Requirement</span></span> | <span data-ttu-id="85649-124">Значение</span><span class="sxs-lookup"><span data-stu-id="85649-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="85649-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85649-125">Minimum supported client</span></span><br/> | <span data-ttu-id="85649-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85649-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="85649-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85649-127">Minimum supported server</span></span><br/> | <span data-ttu-id="85649-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85649-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="85649-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="85649-129">Namespace</span></span><br/>                | <span data-ttu-id="85649-130">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="85649-130">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="85649-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85649-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85649-132">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="85649-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




