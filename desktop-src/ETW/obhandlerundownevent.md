---
description: Представляет класс типа событий для событий обработчиков объектов, связанных с началом и концом сбора данных.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Класс Обхандлерундовневент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985720"
---
# <a name="obhandlerundownevent-class"></a><span data-ttu-id="b7232-103">Класс Обхандлерундовневент</span><span class="sxs-lookup"><span data-stu-id="b7232-103">ObHandleRundownEvent class</span></span>

<span data-ttu-id="b7232-104">Представляет класс типа событий для событий обработчиков объектов, связанных с началом и концом сбора данных.</span><span class="sxs-lookup"><span data-stu-id="b7232-104">Represents the event type class for object handle events related to the beginning and end of data collection.</span></span> <span data-ttu-id="b7232-105">Это событие включает в себя перечисление всех дескрипторов при выполнении очистки.</span><span class="sxs-lookup"><span data-stu-id="b7232-105">This event involves the enumerating of all handles when rundown is performed.</span></span>

<span data-ttu-id="b7232-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b7232-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7232-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7232-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="b7232-108">Участники</span><span class="sxs-lookup"><span data-stu-id="b7232-108">Members</span></span>

<span data-ttu-id="b7232-109">Класс **обхандлерундовневент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b7232-109">The **ObHandleRundownEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="b7232-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7232-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7232-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b7232-111">Properties</span></span>

<span data-ttu-id="b7232-112">Класс **обхандлерундовневент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b7232-112">The **ObHandleRundownEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7232-113">**Дескриптор**</span><span class="sxs-lookup"><span data-stu-id="b7232-113">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7232-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7232-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7232-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7232-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7232-116">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="b7232-116">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="b7232-117">Объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="b7232-117">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="b7232-118">**Объект**</span><span class="sxs-lookup"><span data-stu-id="b7232-118">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7232-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7232-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7232-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7232-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7232-121">Квалификаторы: [**Формат**](event-tracing-mof-qualifiers.md) ("x"), [**указатель**](event-tracing-mof-qualifiers.md), [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="b7232-121">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="b7232-122">Объект.</span><span class="sxs-lookup"><span data-stu-id="b7232-122">The object.</span></span>

</dd> <dt>

<span data-ttu-id="b7232-123">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="b7232-123">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7232-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b7232-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7232-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7232-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7232-126">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**Стрингтерминатион**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="b7232-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="b7232-127">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="b7232-127">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="b7232-128">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="b7232-128">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7232-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7232-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7232-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7232-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7232-131">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="b7232-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="b7232-132">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="b7232-132">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="b7232-133">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="b7232-133">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7232-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7232-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b7232-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b7232-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7232-136">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="b7232-136">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="b7232-137">Идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="b7232-137">The process identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7232-138">Требования</span><span class="sxs-lookup"><span data-stu-id="b7232-138">Requirements</span></span>



| <span data-ttu-id="b7232-139">Требование</span><span class="sxs-lookup"><span data-stu-id="b7232-139">Requirement</span></span> | <span data-ttu-id="b7232-140">Значение</span><span class="sxs-lookup"><span data-stu-id="b7232-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7232-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7232-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b7232-142">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b7232-142">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b7232-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7232-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b7232-144">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b7232-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b7232-145">MOF</span><span class="sxs-lookup"><span data-stu-id="b7232-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7232-146"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7232-146"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




