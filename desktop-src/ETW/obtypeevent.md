---
description: Представляет класс типа события для событий типа объекта, связанных с началом и окончанием сбора данных.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Класс Обтипивент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156727"
---
# <a name="obtypeevent-class"></a><span data-ttu-id="9ffca-103">Класс Обтипивент</span><span class="sxs-lookup"><span data-stu-id="9ffca-103">ObTypeEvent class</span></span>

<span data-ttu-id="9ffca-104">Представляет класс типа события для событий типа объекта, связанных с началом и окончанием сбора данных.</span><span class="sxs-lookup"><span data-stu-id="9ffca-104">Represents the event type class for object type events related to the beginning and end of data collection.</span></span> <span data-ttu-id="9ffca-105">Это событие включает сопоставление значений индекса типа с именами типов.</span><span class="sxs-lookup"><span data-stu-id="9ffca-105">This event involves the mapping of the type index values to the type names.</span></span>

<span data-ttu-id="9ffca-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9ffca-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ffca-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ffca-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a><span data-ttu-id="9ffca-108">Участники</span><span class="sxs-lookup"><span data-stu-id="9ffca-108">Members</span></span>

<span data-ttu-id="9ffca-109">Класс **обтипивент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ffca-109">The **ObTypeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="9ffca-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ffca-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ffca-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ffca-111">Properties</span></span>

<span data-ttu-id="9ffca-112">Класс **обтипивент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ffca-112">The **ObTypeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ffca-113">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="9ffca-113">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffca-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ffca-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ffca-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ffca-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ffca-116">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="9ffca-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9ffca-117">Тип объекта.</span><span class="sxs-lookup"><span data-stu-id="9ffca-117">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="9ffca-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="9ffca-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffca-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ffca-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ffca-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ffca-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ffca-121">Квалификаторы: [**вмидатаид**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="9ffca-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="9ffca-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9ffca-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9ffca-123">**Имени**</span><span class="sxs-lookup"><span data-stu-id="9ffca-123">**TypeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ffca-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ffca-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ffca-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ffca-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ffca-126">Квалификаторы: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**Стрингтерминатион**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**вмидатаид**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="9ffca-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="9ffca-127">Имя типа.</span><span class="sxs-lookup"><span data-stu-id="9ffca-127">The type name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ffca-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9ffca-128">Requirements</span></span>



| <span data-ttu-id="9ffca-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9ffca-129">Requirement</span></span> | <span data-ttu-id="9ffca-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9ffca-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ffca-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ffca-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9ffca-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9ffca-132">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9ffca-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ffca-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9ffca-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9ffca-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9ffca-135">MOF</span><span class="sxs-lookup"><span data-stu-id="9ffca-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ffca-136"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ffca-136"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




