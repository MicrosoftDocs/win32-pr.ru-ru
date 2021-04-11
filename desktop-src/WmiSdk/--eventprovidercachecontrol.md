---
description: Определяет, когда выгружается поставщик событий.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: Класс __EventProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265383"
---
# <a name="__eventprovidercachecontrol-class"></a><span data-ttu-id="1d12c-103">\_\_Класс Евентпровидеркачеконтрол</span><span class="sxs-lookup"><span data-stu-id="1d12c-103">\_\_EventProviderCacheControl class</span></span>

<span data-ttu-id="1d12c-104">Класс системы **\_ \_ евентпровидеркачеконтрол** управляет моментом выгрузки поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="1d12c-104">The **\_\_EventProviderCacheControl** system class controls when an event provider is unloaded.</span></span> <span data-ttu-id="1d12c-105">Он расположен только в \\ корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="1d12c-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="1d12c-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1d12c-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1d12c-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1d12c-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d12c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d12c-108">Syntax</span></span>

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="1d12c-109">Члены</span><span class="sxs-lookup"><span data-stu-id="1d12c-109">Members</span></span>

<span data-ttu-id="1d12c-110">Класс **\_ \_ евентпровидеркачеконтрол** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1d12c-110">The **\_\_EventProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="1d12c-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d12c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d12c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1d12c-112">Properties</span></span>

<span data-ttu-id="1d12c-113">Класс **\_ \_ евентпровидеркачеконтрол** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1d12c-113">The **\_\_EventProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d12c-114">**клеарафтер**</span><span class="sxs-lookup"><span data-stu-id="1d12c-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d12c-115">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d12c-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d12c-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1d12c-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1d12c-117">Интервал времени после инструментарий управления Windows (WMI) (WMI) освобождает поставщик событий.</span><span class="sxs-lookup"><span data-stu-id="1d12c-117">Time interval after Windows Management Instrumentation (WMI) releases an event provider.</span></span> <span data-ttu-id="1d12c-118">Время указано в [формате интервала](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="1d12c-118">The time is in [interval format](interval-format.md).</span></span> <span data-ttu-id="1d12c-119">Интервал, указанный для выгрузки поставщика, может занять вдвое больше времени.</span><span class="sxs-lookup"><span data-stu-id="1d12c-119">It may take up to twice the interval specified to unload the provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d12c-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d12c-120">Remarks</span></span>

<span data-ttu-id="1d12c-121">Класс **\_ \_ евентпровидеркачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="1d12c-121">The **\_\_EventProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span>

<span data-ttu-id="1d12c-122">Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1d12c-122">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d12c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1d12c-123">Requirements</span></span>



| <span data-ttu-id="1d12c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1d12c-124">Requirement</span></span> | <span data-ttu-id="1d12c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1d12c-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1d12c-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d12c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1d12c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d12c-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1d12c-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d12c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1d12c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d12c-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1d12c-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d12c-130">Namespace</span></span><br/>                | <span data-ttu-id="1d12c-131">Root</span><span class="sxs-lookup"><span data-stu-id="1d12c-131">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1d12c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d12c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d12c-133">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="1d12c-133">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="1d12c-134">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="1d12c-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

