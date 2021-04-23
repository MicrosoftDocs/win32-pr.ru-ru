---
description: Выступает в качестве родительского класса для классов, управляющих созданием событий, например событий таймера.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: Класс __EventGenerator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272921"
---
# <a name="__eventgenerator-class"></a><span data-ttu-id="6b50b-103">\_\_Класс Евентженератор</span><span class="sxs-lookup"><span data-stu-id="6b50b-103">\_\_EventGenerator class</span></span>

<span data-ttu-id="6b50b-104">Класс System **\_ \_ евентженератор** является абстрактным базовым классом, который служит родительским классом для классов, управляющих созданием событий, таких как [события таймера](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="6b50b-104">The **\_\_EventGenerator** system class is an abstract base class that serves as a parent class for classes that control the generation of events, such as [timer events](receiving-a-timed-or-repeating-event.md).</span></span>

<span data-ttu-id="6b50b-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b50b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6b50b-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6b50b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b50b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b50b-107">Syntax</span></span>

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a><span data-ttu-id="6b50b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="6b50b-108">Members</span></span>

<span data-ttu-id="6b50b-109">Класс **\_ \_ евентженератор** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="6b50b-109">The **\_\_EventGenerator** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b50b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b50b-110">Remarks</span></span>

<span data-ttu-id="6b50b-111">Класс **\_ \_ евентженератор** является производным от [**\_ \_ индикатионрелатед**](--indicationrelated.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="6b50b-111">The **\_\_EventGenerator** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b50b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="6b50b-112">Requirements</span></span>



| <span data-ttu-id="6b50b-113">Требование</span><span class="sxs-lookup"><span data-stu-id="6b50b-113">Requirement</span></span> | <span data-ttu-id="6b50b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="6b50b-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6b50b-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b50b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6b50b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b50b-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6b50b-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b50b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6b50b-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b50b-118">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6b50b-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b50b-119">Namespace</span></span><br/>                | <span data-ttu-id="6b50b-120">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="6b50b-120">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6b50b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b50b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b50b-122">**\_\_индикатионрелатед**</span><span class="sxs-lookup"><span data-stu-id="6b50b-122">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="6b50b-123">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="6b50b-123">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

