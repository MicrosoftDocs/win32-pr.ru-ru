---
description: Представляет класс типа события для обработчика повторяющихся событий.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: Класс Обхандледупликативент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986004"
---
# <a name="obhandleduplicateevent-class"></a><span data-ttu-id="6da40-103">Класс Обхандледупликативент</span><span class="sxs-lookup"><span data-stu-id="6da40-103">ObHandleDuplicateEvent class</span></span>

<span data-ttu-id="6da40-104">Представляет класс типа события для обработчика повторяющихся событий.</span><span class="sxs-lookup"><span data-stu-id="6da40-104">Represents the event type class for handle duplication events.</span></span>

<span data-ttu-id="6da40-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6da40-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da40-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6da40-106">Syntax</span></span>

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a><span data-ttu-id="6da40-107">Участники</span><span class="sxs-lookup"><span data-stu-id="6da40-107">Members</span></span>

<span data-ttu-id="6da40-108">Класс **обхандледупликативент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6da40-108">The **ObHandleDuplicateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6da40-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="6da40-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6da40-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="6da40-110">Properties</span></span>

<span data-ttu-id="6da40-111">Класс **обхандледупликативент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6da40-111">The **ObHandleDuplicateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6da40-112">**Объект**</span><span class="sxs-lookup"><span data-stu-id="6da40-112">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6da40-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6da40-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6da40-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6da40-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6da40-115">Квалификаторы: [**Формат**](event-tracing-mof-qualifiers.md) ("x"), [**указатель**](event-tracing-mof-qualifiers.md), [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="6da40-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="6da40-116">Объект.</span><span class="sxs-lookup"><span data-stu-id="6da40-116">The object.</span></span>

</dd> <dt>

<span data-ttu-id="6da40-117">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="6da40-117">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6da40-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6da40-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6da40-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6da40-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6da40-120">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="6da40-120">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="6da40-121">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="6da40-121">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="6da40-122">**саурцехандле**</span><span class="sxs-lookup"><span data-stu-id="6da40-122">**SourceHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6da40-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6da40-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6da40-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6da40-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6da40-125">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="6da40-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="6da40-126">Маркер исходного объекта.</span><span class="sxs-lookup"><span data-stu-id="6da40-126">The handle of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="6da40-127">**таржесандле**</span><span class="sxs-lookup"><span data-stu-id="6da40-127">**TargetHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6da40-128">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6da40-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6da40-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6da40-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6da40-130">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="6da40-130">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="6da40-131">Маркер целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6da40-131">The handle of the target object.</span></span>

</dd> <dt>

<span data-ttu-id="6da40-132">**таржетпроцессид**</span><span class="sxs-lookup"><span data-stu-id="6da40-132">**TargetProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6da40-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6da40-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6da40-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6da40-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6da40-135">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="6da40-135">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="6da40-136">Идентификатор процесса целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="6da40-136">The process identifier of the target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6da40-137">Требования</span><span class="sxs-lookup"><span data-stu-id="6da40-137">Requirements</span></span>



| <span data-ttu-id="6da40-138">Требование</span><span class="sxs-lookup"><span data-stu-id="6da40-138">Requirement</span></span> | <span data-ttu-id="6da40-139">Значение</span><span class="sxs-lookup"><span data-stu-id="6da40-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da40-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6da40-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6da40-141">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6da40-141">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6da40-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6da40-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6da40-143">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6da40-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6da40-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6da40-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6da40-145"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6da40-145"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




