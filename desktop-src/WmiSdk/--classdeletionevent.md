---
description: Представляет событие удаления класса, которое представляет собой тип встроенного события, создаваемого при удалении класса из пространства имен.
ms.assetid: dd44c03e-4d0d-4750-942d-495893d21650
ms.tgt_platform: multiple
title: Класс __ClassDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29242335edeffbdc44deebb3acacd5631fcc7b68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702382"
---
# <a name="__classdeletionevent-class"></a><span data-ttu-id="38fd6-103">\_\_Класс Классделетионевент</span><span class="sxs-lookup"><span data-stu-id="38fd6-103">\_\_ClassDeletionEvent class</span></span>

<span data-ttu-id="38fd6-104">Класс System **\_ \_ классделетионевент** представляет событие удаления класса, которое представляет собой тип [встроенного события](determining-the-type-of-event-to-receive.md) , создаваемого при удалении класса из пространства имен.</span><span class="sxs-lookup"><span data-stu-id="38fd6-104">The **\_\_ClassDeletionEvent** system class represents a class deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is removed from the namespace.</span></span>

<span data-ttu-id="38fd6-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="38fd6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="38fd6-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="38fd6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="38fd6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38fd6-107">Syntax</span></span>

``` syntax
class __ClassDeletionEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="38fd6-108">Члены</span><span class="sxs-lookup"><span data-stu-id="38fd6-108">Members</span></span>

<span data-ttu-id="38fd6-109">Класс **\_ \_ классделетионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38fd6-109">The **\_\_ClassDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="38fd6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="38fd6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38fd6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="38fd6-111">Properties</span></span>

<span data-ttu-id="38fd6-112">Класс **\_ \_ классделетионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38fd6-112">The **\_\_ClassDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38fd6-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="38fd6-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38fd6-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="38fd6-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="38fd6-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38fd6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38fd6-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="38fd6-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="38fd6-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="38fd6-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="38fd6-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="38fd6-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38fd6-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="38fd6-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="38fd6-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38fd6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38fd6-121">Копия только что удаленного класса, сообщаемого событием удаления класса.</span><span class="sxs-lookup"><span data-stu-id="38fd6-121">Copy of the newly deleted class reported by the class deletion event.</span></span> <span data-ttu-id="38fd6-122">Это свойство наследуется от [**\_ \_ классоператионевент**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="38fd6-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="38fd6-123">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="38fd6-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38fd6-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="38fd6-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="38fd6-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38fd6-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38fd6-126">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="38fd6-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="38fd6-127">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="38fd6-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="38fd6-128">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="38fd6-128">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="38fd6-129">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="38fd6-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="38fd6-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="38fd6-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38fd6-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38fd6-131">Remarks</span></span>

<span data-ttu-id="38fd6-132">Класс **\_ \_ классделетионевент** является производным от [**\_ \_ классоператионевент**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="38fd6-132">The **\_\_ClassDeletionEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38fd6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="38fd6-133">Requirements</span></span>



| <span data-ttu-id="38fd6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="38fd6-134">Requirement</span></span> | <span data-ttu-id="38fd6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="38fd6-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="38fd6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38fd6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="38fd6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38fd6-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="38fd6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38fd6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="38fd6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38fd6-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="38fd6-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38fd6-140">Namespace</span></span><br/>                | <span data-ttu-id="38fd6-141">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="38fd6-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="38fd6-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38fd6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38fd6-143">**\_\_классоператионевент**</span><span class="sxs-lookup"><span data-stu-id="38fd6-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="38fd6-144">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="38fd6-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

