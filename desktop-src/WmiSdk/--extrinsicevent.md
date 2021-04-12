---
description: Выступает в качестве родительского класса для всех определяемых пользователем типов событий, также известных как внешние события.
ms.assetid: 8fddbcd1-7393-4a3b-8a10-a8b620efc19f
ms.tgt_platform: multiple
title: Класс __ExtrinsicEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtrinsicEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 76af7a9f32c24b8d44f81c60b0f2fca693c26f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272240"
---
# <a name="__extrinsicevent-class"></a><span data-ttu-id="be6e9-103">\_\_Класс Екстринсицевент</span><span class="sxs-lookup"><span data-stu-id="be6e9-103">\_\_ExtrinsicEvent class</span></span>

<span data-ttu-id="be6e9-104">Системный класс **\_ \_ екстринсицевент** является абстрактным базовым классом, который служит родительским классом для всех определяемых пользователем типов событий, также известных как [внешние события](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="be6e9-104">The **\_\_ExtrinsicEvent** system class is an abstract base class that serves as a parent class for all user-defined event types, also known as [extrinsic events](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="be6e9-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="be6e9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="be6e9-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="be6e9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be6e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be6e9-107">Syntax</span></span>

``` syntax
class __ExtrinsicEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="be6e9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="be6e9-108">Members</span></span>

<span data-ttu-id="be6e9-109">Класс **\_ \_ екстринсицевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be6e9-109">The **\_\_ExtrinsicEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="be6e9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="be6e9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be6e9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="be6e9-111">Properties</span></span>

<span data-ttu-id="be6e9-112">Класс **\_ \_ екстринсицевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be6e9-112">The **\_\_ExtrinsicEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be6e9-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="be6e9-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be6e9-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="be6e9-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="be6e9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be6e9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be6e9-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="be6e9-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="be6e9-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="be6e9-117">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="be6e9-118">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="be6e9-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="be6e9-119">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="be6e9-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be6e9-120">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="be6e9-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="be6e9-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be6e9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be6e9-122">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="be6e9-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="be6e9-123">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="be6e9-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="be6e9-124">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="be6e9-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="be6e9-125">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="be6e9-125">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="be6e9-126">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="be6e9-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be6e9-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be6e9-127">Remarks</span></span>

<span data-ttu-id="be6e9-128">Класс **\_ \_ екстринсицевент** является производным от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="be6e9-128">The **\_\_ExtrinsicEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be6e9-129">Требования</span><span class="sxs-lookup"><span data-stu-id="be6e9-129">Requirements</span></span>



| <span data-ttu-id="be6e9-130">Требование</span><span class="sxs-lookup"><span data-stu-id="be6e9-130">Requirement</span></span> | <span data-ttu-id="be6e9-131">Значение</span><span class="sxs-lookup"><span data-stu-id="be6e9-131">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="be6e9-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be6e9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="be6e9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be6e9-133">Windows Vista</span></span><br/>       |
| <span data-ttu-id="be6e9-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be6e9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="be6e9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be6e9-135">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="be6e9-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be6e9-136">Namespace</span></span><br/>                | <span data-ttu-id="be6e9-137">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="be6e9-137">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="be6e9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be6e9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6e9-139">**\_\_Событие**</span><span class="sxs-lookup"><span data-stu-id="be6e9-139">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="be6e9-140">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="be6e9-140">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

