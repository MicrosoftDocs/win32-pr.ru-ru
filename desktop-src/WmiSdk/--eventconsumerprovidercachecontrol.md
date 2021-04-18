---
description: Определяет, когда WMI должен освободить поставщик потребителей событий.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: Класс __EventConsumerProviderCacheControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703319"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a><span data-ttu-id="4ec09-103">\_\_Класс Евентконсумерпровидеркачеконтрол</span><span class="sxs-lookup"><span data-stu-id="4ec09-103">\_\_EventConsumerProviderCacheControl class</span></span>

<span data-ttu-id="4ec09-104">Класс System **\_ \_ евентконсумерпровидеркачеконтрол** определяет, когда WMI должен освободить поставщик потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="4ec09-104">The **\_\_EventConsumerProviderCacheControl** system class determines when WMI should release an event consumer provider.</span></span> <span data-ttu-id="4ec09-105">Класс **\_ \_ евентконсумерпровидеркачеконтрол** является Singleton-классом.</span><span class="sxs-lookup"><span data-stu-id="4ec09-105">The **\_\_EventConsumerProviderCacheControl** class is a singleton class.</span></span> <span data-ttu-id="4ec09-106">Он расположен только в \\ корневом пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="4ec09-106">It is located only in the \\root namespace.</span></span>

<span data-ttu-id="4ec09-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4ec09-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4ec09-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4ec09-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec09-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ec09-109">Syntax</span></span>

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a><span data-ttu-id="4ec09-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4ec09-110">Members</span></span>

<span data-ttu-id="4ec09-111">Класс **\_ \_ евентконсумерпровидеркачеконтрол** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4ec09-111">The **\_\_EventConsumerProviderCacheControl** class has these types of members:</span></span>

-   [<span data-ttu-id="4ec09-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4ec09-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ec09-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4ec09-113">Properties</span></span>

<span data-ttu-id="4ec09-114">Класс **\_ \_ евентконсумерпровидеркачеконтрол** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4ec09-114">The **\_\_EventConsumerProviderCacheControl** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ec09-115">**клеарафтер**</span><span class="sxs-lookup"><span data-stu-id="4ec09-115">**ClearAfter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ec09-116">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4ec09-116">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4ec09-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4ec09-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4ec09-118">Интервал времени, по истечении которого WMI освобождает поставщик потребителей событий.</span><span class="sxs-lookup"><span data-stu-id="4ec09-118">Time interval after which WMI releases an event consumer provider.</span></span> <span data-ttu-id="4ec09-119">Интервал, указанный для выгрузки поставщика, может занять вдвое больше времени.</span><span class="sxs-lookup"><span data-stu-id="4ec09-119">It may take up to twice the interval specified to unload the provider.</span></span> <span data-ttu-id="4ec09-120">Время указано в [формате интервала](interval-format.md).</span><span class="sxs-lookup"><span data-stu-id="4ec09-120">The time is in [interval format](interval-format.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ec09-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ec09-121">Remarks</span></span>

<span data-ttu-id="4ec09-122">Класс **\_ \_ евентконсумерпровидеркачеконтрол** является производным от [**\_ \_ CacheControl**](--cachecontrol.md).</span><span class="sxs-lookup"><span data-stu-id="4ec09-122">The **\_\_EventConsumerProviderCacheControl** class is derived from [**\_\_CacheControl**](--cachecontrol.md).</span></span> <span data-ttu-id="4ec09-123">Дополнительные сведения об использовании этого класса см. [в разделе выгрузка поставщика](unloading-a-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4ec09-123">For more information about using this class, see [Unloading a Provider](unloading-a-provider.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec09-124">Требования</span><span class="sxs-lookup"><span data-stu-id="4ec09-124">Requirements</span></span>



| <span data-ttu-id="4ec09-125">Требование</span><span class="sxs-lookup"><span data-stu-id="4ec09-125">Requirement</span></span> | <span data-ttu-id="4ec09-126">Значение</span><span class="sxs-lookup"><span data-stu-id="4ec09-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4ec09-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ec09-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec09-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ec09-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4ec09-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ec09-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec09-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ec09-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4ec09-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4ec09-131">Namespace</span></span><br/>                | <span data-ttu-id="4ec09-132">Root</span><span class="sxs-lookup"><span data-stu-id="4ec09-132">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4ec09-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ec09-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec09-134">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="4ec09-134">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




