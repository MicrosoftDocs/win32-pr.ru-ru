---
description: Используется для определения того, когда инструментарий WMI освобождает указатель Ивбемунбаундобжектсинк поставщиков событий.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: Класс __EventSinkCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693556"
---
# <a name="__eventsinkcachecontrol-class"></a><span data-ttu-id="8dde0-103">\_\_Класс Евентсинккачеконтрол</span><span class="sxs-lookup"><span data-stu-id="8dde0-103">\_\_EventSinkCacheControl class</span></span>

<span data-ttu-id="8dde0-104">Класс System **\_ \_ евентсинккачеконтрол** используется для определения того, когда WMI освобождает указатель [**ивбемунбаундобжектсинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="8dde0-104">The **\_\_EventSinkCacheControl** system class is used to determine when WMI releases an event consumer provider's [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) pointer.</span></span> <span data-ttu-id="8dde0-105">Класс **\_ \_ евентсинккачеконтрол** является Singleton-классом.</span><span class="sxs-lookup"><span data-stu-id="8dde0-105">The **\_\_EventSinkCacheControl** class is a singleton class.</span></span> <span data-ttu-id="8dde0-106">Он расположен только в \\ корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="8dde0-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="8dde0-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8dde0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8dde0-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8dde0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dde0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dde0-109">Syntax</span></span>

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="8dde0-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8dde0-110">Members</span></span>

<span data-ttu-id="8dde0-111">Класс **\_ \_ евентсинккачеконтрол** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8dde0-111">The **\_\_EventSinkCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="8dde0-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8dde0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dde0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8dde0-113">Properties</span></span>

<span data-ttu-id="8dde0-114">Класс **\_ \_ евентсинккачеконтрол** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8dde0-114">The **\_\_EventSinkCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dde0-115">**клеарафтер**</span><span class="sxs-lookup"><span data-stu-id="8dde0-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dde0-116">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8dde0-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8dde0-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="8dde0-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8dde0-118">Интервал времени, по истечении которого WMI освобождает поставщик событий.</span><span class="sxs-lookup"><span data-stu-id="8dde0-118">Time interval after which WMI releases an event provider.</span></span> <span data-ttu-id="8dde0-119">Интервал, указанный для выгрузки поставщика, может занять вдвое больше времени.</span><span class="sxs-lookup"><span data-stu-id="8dde0-119">It can take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="8dde0-120">Время указано в [формате интервала](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="8dde0-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dde0-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8dde0-121">Remarks</span></span>

<span data-ttu-id="8dde0-122">Класс **\_ \_ евентсинккачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="8dde0-122">The **\_\_EventSinkCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="8dde0-123">Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8dde0-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8dde0-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8dde0-124">Requirements</span></span>



| <span data-ttu-id="8dde0-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8dde0-125">Requirement</span></span> | <span data-ttu-id="8dde0-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8dde0-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8dde0-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8dde0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8dde0-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dde0-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8dde0-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8dde0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8dde0-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dde0-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8dde0-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8dde0-131">Namespace</span></span><br/>                | <span data-ttu-id="8dde0-132">Root</span><span class="sxs-lookup"><span data-stu-id="8dde0-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="8dde0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8dde0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dde0-134">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="8dde0-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




