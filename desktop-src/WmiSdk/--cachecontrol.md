---
description: Класс является абстрактным базовым классом для классов, которые используются для определения того, когда WMI должен освободить объект модели COM.
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: Класс __CacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683706"
---
# <a name="__cachecontrol-class"></a><span data-ttu-id="5ab83-103">\_\_Класс CacheControl</span><span class="sxs-lookup"><span data-stu-id="5ab83-103">\_\_CacheControl class</span></span>

<span data-ttu-id="5ab83-104">Класс System **\_ \_ CacheControl** является абстрактным базовым классом для классов, которые используются для определения того, когда WMI должен освободить объект модели COM.</span><span class="sxs-lookup"><span data-stu-id="5ab83-104">The **\_\_CacheControl** system class is the abstract base class for classes that are used to determine when WMI should release a Component Object Model (COM) object.</span></span> <span data-ttu-id="5ab83-105">Экземпляры этого класса никогда не создаются.</span><span class="sxs-lookup"><span data-stu-id="5ab83-105">Instances of this class are never created.</span></span> <span data-ttu-id="5ab83-106">Класс **\_ \_ CacheControl** расположен только в корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="5ab83-106">The **\_\_CacheControl** class is located only in the root namespace.</span></span> <span data-ttu-id="5ab83-107">Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5ab83-107">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

<span data-ttu-id="5ab83-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5ab83-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5ab83-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5ab83-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab83-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ab83-110">Syntax</span></span>

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a><span data-ttu-id="5ab83-111">Члены</span><span class="sxs-lookup"><span data-stu-id="5ab83-111">Members</span></span>

<span data-ttu-id="5ab83-112">Класс **\_ \_ CacheControl** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="5ab83-112">The **\_\_CacheControl** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab83-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ab83-113">Remarks</span></span>

<span data-ttu-id="5ab83-114">Класс **\_ \_ CacheControl** является производным от [**\_ \_ системкласс**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="5ab83-114">The **\_\_CacheControl** class is derived from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ab83-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5ab83-115">Requirements</span></span>



| <span data-ttu-id="5ab83-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5ab83-116">Requirement</span></span> | <span data-ttu-id="5ab83-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5ab83-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5ab83-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ab83-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab83-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ab83-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5ab83-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ab83-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab83-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ab83-121">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5ab83-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5ab83-122">Namespace</span></span><br/>                | <span data-ttu-id="5ab83-123">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="5ab83-123">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5ab83-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ab83-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab83-125">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="5ab83-125">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="5ab83-126">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="5ab83-126">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5ab83-127">**\_\_евентконсумерпровидеркачеконтрол**</span><span class="sxs-lookup"><span data-stu-id="5ab83-127">**\_\_EventConsumerProviderCacheControl**</span></span>](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5ab83-128">**\_\_евентпровидеркачеконтрол**</span><span class="sxs-lookup"><span data-stu-id="5ab83-128">**\_\_EventProviderCacheControl**</span></span>](--eventprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5ab83-129">**\_\_евентсинккачеконтрол**</span><span class="sxs-lookup"><span data-stu-id="5ab83-129">**\_\_EventSinkCacheControl**</span></span>](--eventsinkcachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5ab83-130">**\_\_обжектпровидеркачеконтрол**</span><span class="sxs-lookup"><span data-stu-id="5ab83-130">**\_\_ObjectProviderCacheControl**</span></span>](--objectprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5ab83-131">\_\_пропертипровидеркачеконтрол</span><span class="sxs-lookup"><span data-stu-id="5ab83-131">\_\_PropertyProviderCacheControl</span></span>](--propertyprovidercachecontrol.md)
</dt> <dt>

[<span data-ttu-id="5ab83-132">Выгрузка поставщика</span><span class="sxs-lookup"><span data-stu-id="5ab83-132">Unloading a Provider</span></span>](unloading-a-provider.md)
</dt> </dl>

 

