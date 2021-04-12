---
description: Представляет системное событие.
ms.assetid: 84099483-03e4-4c21-b680-f0975b18c1f6
ms.tgt_platform: multiple
title: Класс __SystemEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 7cc443c9e130106c2f5e8a05a1a2983927f1963e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265886"
---
# <a name="__systemevent-class"></a><span data-ttu-id="90297-103">\_\_Класс Системевент</span><span class="sxs-lookup"><span data-stu-id="90297-103">\_\_SystemEvent class</span></span>

<span data-ttu-id="90297-104">Системный класс **\_ \_ системевент** представляет системное событие.</span><span class="sxs-lookup"><span data-stu-id="90297-104">The **\_\_SystemEvent** system class represents a system event.</span></span>

<span data-ttu-id="90297-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="90297-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="90297-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="90297-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90297-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90297-107">Syntax</span></span>

``` syntax
class __SystemEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="90297-108">Члены</span><span class="sxs-lookup"><span data-stu-id="90297-108">Members</span></span>

<span data-ttu-id="90297-109">Класс **\_ \_ системевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="90297-109">The **\_\_SystemEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="90297-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="90297-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90297-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="90297-111">Properties</span></span>

<span data-ttu-id="90297-112">Класс **\_ \_ системевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="90297-112">The **\_\_SystemEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90297-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="90297-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90297-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="90297-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="90297-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="90297-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90297-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="90297-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="90297-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="90297-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="90297-118">**Пустой** список управления доступом (ACL) в [**\_ дескрипторе безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет всем всем времени неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="90297-118">A **NULL** Access Control List (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="90297-119">Дополнительные сведения см. в разделе [Создание дескриптора безопасности для нового объекта](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="90297-119">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="90297-120">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="90297-120">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90297-121">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="90297-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="90297-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="90297-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90297-123">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="90297-123">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="90297-124">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="90297-124">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="90297-125">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="90297-125">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="90297-126">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="90297-126">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="90297-127">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="90297-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90297-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90297-128">Remarks</span></span>

<span data-ttu-id="90297-129">Класс **\_ \_ системевент** является производным от класса [**\_ \_ екстринсицевент**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="90297-129">The **\_\_SystemEvent** class is derived from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="90297-130">Требования</span><span class="sxs-lookup"><span data-stu-id="90297-130">Requirements</span></span>



| <span data-ttu-id="90297-131">Требование</span><span class="sxs-lookup"><span data-stu-id="90297-131">Requirement</span></span> | <span data-ttu-id="90297-132">Значение</span><span class="sxs-lookup"><span data-stu-id="90297-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="90297-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90297-133">Minimum supported client</span></span><br/> | <span data-ttu-id="90297-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90297-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="90297-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90297-135">Minimum supported server</span></span><br/> | <span data-ttu-id="90297-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90297-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="90297-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="90297-137">Namespace</span></span><br/>                | <span data-ttu-id="90297-138">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="90297-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="90297-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90297-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90297-140">**\_\_екстринсицевент**</span><span class="sxs-lookup"><span data-stu-id="90297-140">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

[<span data-ttu-id="90297-141">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="90297-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

