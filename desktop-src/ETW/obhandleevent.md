---
description: Представляет класс типа события для событий создания или закрытия обработчика.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Класс Обхандливент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985717"
---
# <a name="obhandleevent-class"></a><span data-ttu-id="66764-103">Класс Обхандливент</span><span class="sxs-lookup"><span data-stu-id="66764-103">ObHandleEvent class</span></span>

<span data-ttu-id="66764-104">Представляет класс типа события для событий создания или закрытия обработчика.</span><span class="sxs-lookup"><span data-stu-id="66764-104">Represents the event type class for handle creation or closure events.</span></span>

<span data-ttu-id="66764-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="66764-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="66764-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66764-106">Syntax</span></span>

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a><span data-ttu-id="66764-107">Участники</span><span class="sxs-lookup"><span data-stu-id="66764-107">Members</span></span>

<span data-ttu-id="66764-108">Класс **обхандливент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="66764-108">The **ObHandleEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="66764-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="66764-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66764-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="66764-110">Properties</span></span>

<span data-ttu-id="66764-111">Класс **обхандливент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="66764-111">The **ObHandleEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66764-112">**Дескриптор**</span><span class="sxs-lookup"><span data-stu-id="66764-112">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66764-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66764-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66764-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66764-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66764-115">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="66764-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="66764-116">Объектный обработчик.</span><span class="sxs-lookup"><span data-stu-id="66764-116">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="66764-117">**Объект**</span><span class="sxs-lookup"><span data-stu-id="66764-117">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66764-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66764-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66764-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66764-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66764-120">Квалификаторы: [**Формат**](event-tracing-mof-qualifiers.md) ("x"), [**указатель**](event-tracing-mof-qualifiers.md), [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="66764-120">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="66764-121">Объект.</span><span class="sxs-lookup"><span data-stu-id="66764-121">The object.</span></span>

</dd> <dt>

<span data-ttu-id="66764-122">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="66764-122">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66764-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66764-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66764-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66764-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66764-125">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**Стрингтерминатион**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="66764-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="66764-126">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="66764-126">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="66764-127">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="66764-127">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66764-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66764-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66764-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66764-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66764-130">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="66764-130">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="66764-131">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="66764-131">The object type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66764-132">Требования</span><span class="sxs-lookup"><span data-stu-id="66764-132">Requirements</span></span>



| <span data-ttu-id="66764-133">Требование</span><span class="sxs-lookup"><span data-stu-id="66764-133">Requirement</span></span> | <span data-ttu-id="66764-134">Значение</span><span class="sxs-lookup"><span data-stu-id="66764-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66764-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66764-135">Minimum supported client</span></span><br/> | <span data-ttu-id="66764-136">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="66764-136">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="66764-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66764-137">Minimum supported server</span></span><br/> | <span data-ttu-id="66764-138">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="66764-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="66764-139">MOF</span><span class="sxs-lookup"><span data-stu-id="66764-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66764-140"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66764-140"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




