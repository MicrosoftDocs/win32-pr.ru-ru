---
description: Определяет, когда выгружается поставщик класса или экземпляра.
ms.assetid: 4cbeb820-8a65-4fab-97f1-2a973b2a4310
ms.tgt_platform: multiple
title: Класс __ObjectProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderCacheControl
- Root.__ObjectProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 53cfaa69afead4f436879f128a4d42e50d36fe67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703012"
---
# <a name="__objectprovidercachecontrol-class"></a><span data-ttu-id="787ee-103">\_\_Класс Обжектпровидеркачеконтрол</span><span class="sxs-lookup"><span data-stu-id="787ee-103">\_\_ObjectProviderCacheControl class</span></span>

<span data-ttu-id="787ee-104">Класс системы **\_ \_ обжектпровидеркачеконтрол** определяет, когда выгружается поставщик класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="787ee-104">The **\_\_ObjectProviderCacheControl** system class controls when a class or instance provider is unloaded.</span></span> <span data-ttu-id="787ee-105">Он расположен только в \\ корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="787ee-105">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="787ee-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="787ee-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="787ee-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="787ee-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="787ee-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="787ee-108">Syntax</span></span>

``` syntax
[singleton]
class __ObjectProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="787ee-109">Члены</span><span class="sxs-lookup"><span data-stu-id="787ee-109">Members</span></span>

<span data-ttu-id="787ee-110">Класс **\_ \_ обжектпровидеркачеконтрол** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="787ee-110">The **\_\_ObjectProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="787ee-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="787ee-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="787ee-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="787ee-112">Properties</span></span>

<span data-ttu-id="787ee-113">Класс **\_ \_ обжектпровидеркачеконтрол** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="787ee-113">The **\_\_ObjectProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="787ee-114">**клеарафтер**</span><span class="sxs-lookup"><span data-stu-id="787ee-114">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="787ee-115">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="787ee-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="787ee-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="787ee-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="787ee-117">Интервал времени, после которого WMI освобождает экземпляр, класс или поставщик метода.</span><span class="sxs-lookup"><span data-stu-id="787ee-117">Time interval after which WMI releases an instance, class, or method provider.</span></span> <span data-ttu-id="787ee-118">Время указано в [формате интервала](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="787ee-118">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="787ee-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="787ee-119">Remarks</span></span>

<span data-ttu-id="787ee-120">Класс **\_ \_ обжектпровидеркачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="787ee-120">The **\_\_ObjectProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="787ee-121">Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="787ee-121">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="787ee-122">Требования</span><span class="sxs-lookup"><span data-stu-id="787ee-122">Requirements</span></span>



| <span data-ttu-id="787ee-123">Требование</span><span class="sxs-lookup"><span data-stu-id="787ee-123">Requirement</span></span> | <span data-ttu-id="787ee-124">Значение</span><span class="sxs-lookup"><span data-stu-id="787ee-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="787ee-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="787ee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="787ee-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="787ee-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="787ee-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="787ee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="787ee-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="787ee-128">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="787ee-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="787ee-129">Namespace</span></span><br/>                | <span data-ttu-id="787ee-130">Root</span><span class="sxs-lookup"><span data-stu-id="787ee-130">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="787ee-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="787ee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787ee-132">**\_\_CacheControl**</span><span class="sxs-lookup"><span data-stu-id="787ee-132">**\_\_CacheControl**</span></span>](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[<span data-ttu-id="787ee-133">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="787ee-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="787ee-134">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="787ee-134">Receiving Events at All Times</span></span>](receiving-events-at-all-times.md)
</dt> </dl>

 

