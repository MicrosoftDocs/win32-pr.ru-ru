---
description: Сообщает о событии удаления экземпляра, которое представляет собой тип встроенного события, создаваемого при удалении экземпляра из пространства имен.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: Класс __InstanceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702678"
---
# <a name="__instancedeletionevent-class"></a><span data-ttu-id="fe06e-103">\_\_Класс Инстанцеделетионевент</span><span class="sxs-lookup"><span data-stu-id="fe06e-103">\_\_InstanceDeletionEvent class</span></span>

<span data-ttu-id="fe06e-104">Класс System **\_ \_ инстанцеделетионевент** сообщает о событии удаления экземпляра, которое представляет собой тип [встроенного события](determining-the-type-of-event-to-receive.md) , создаваемого при удалении экземпляра из пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fe06e-104">The **\_\_InstanceDeletionEvent** system class reports an instance deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance is deleted from the namespace.</span></span>

<span data-ttu-id="fe06e-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="fe06e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fe06e-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="fe06e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe06e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe06e-107">Syntax</span></span>

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="fe06e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="fe06e-108">Members</span></span>

<span data-ttu-id="fe06e-109">Класс **\_ \_ инстанцеделетионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fe06e-109">The **\_\_InstanceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="fe06e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fe06e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe06e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="fe06e-111">Properties</span></span>

<span data-ttu-id="fe06e-112">Класс **\_ \_ инстанцеделетионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fe06e-112">The **\_\_InstanceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fe06e-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="fe06e-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe06e-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="fe06e-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fe06e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fe06e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe06e-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="fe06e-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="fe06e-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="fe06e-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe06e-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="fe06e-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe06e-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="fe06e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fe06e-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fe06e-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe06e-121">Копия удаленного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fe06e-121">Copy of the instance that was deleted.</span></span> <span data-ttu-id="fe06e-122">Это свойство наследуется от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="fe06e-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe06e-123">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="fe06e-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe06e-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fe06e-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fe06e-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fe06e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fe06e-126">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="fe06e-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="fe06e-127">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="fe06e-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="fe06e-128">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="fe06e-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="fe06e-129">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="fe06e-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="fe06e-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fe06e-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe06e-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe06e-131">Remarks</span></span>

<span data-ttu-id="fe06e-132">Класс **\_ \_ инстанцеделетионевент** является производным от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="fe06e-132">The **\_\_InstanceDeletionEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="fe06e-133">**Удаление ресурса: \_ \_ инстанцеделетионевент**</span><span class="sxs-lookup"><span data-stu-id="fe06e-133">**Deletion of a resource: \_\_InstanceDeletionEvent**</span></span>

<span data-ttu-id="fe06e-134">Чтобы гарантировать, что конкретная антивирусная программа продолжит работать на компьютере, можно написать сценарий, отслеживающий процессы на компьютере, чтобы определить, не прекращаются ли они.</span><span class="sxs-lookup"><span data-stu-id="fe06e-134">If you want to ensure that a particular antivirus scanner program continues to run on a computer, you can write a script that monitors the processes on the computer to determine whether any of them stop.</span></span>

<span data-ttu-id="fe06e-135">Запросы уведомлений, которые запрашивают уведомление об удалении ресурса и используют встроенные события, используют синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="fe06e-135">Notification queries that request notification of the deletion of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a><span data-ttu-id="fe06e-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="fe06e-136">Examples</span></span>

<span data-ttu-id="fe06e-137">Пример кода VBScript " [мониторинг процесса удаления](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) " в коллекции TechNet использует **\_ \_ инстанцеделетионевент** для отслеживания первого вхождения события удаления экземпляра WMI для [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="fe06e-137">The [Monitor process deletion event](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript code sample on TechNet Gallery uses **\_\_InstanceDeletionEvent** to monitor the first occurrence of a WMI instance deletion event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe06e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="fe06e-138">Requirements</span></span>



| <span data-ttu-id="fe06e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="fe06e-139">Requirement</span></span> | <span data-ttu-id="fe06e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="fe06e-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fe06e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe06e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fe06e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fe06e-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fe06e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe06e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fe06e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fe06e-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fe06e-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fe06e-145">Namespace</span></span><br/>                | <span data-ttu-id="fe06e-146">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="fe06e-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fe06e-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe06e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe06e-148">**\_\_инстанцеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="fe06e-148">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="fe06e-149">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="fe06e-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

