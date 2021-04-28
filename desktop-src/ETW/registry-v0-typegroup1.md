---
description: Класс Registry_V0_TypeGroup1 — этот класс является классом типа события для событий реестра. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Класс Registry_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106192"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="21326-104">\_Класс реестра v0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="21326-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="21326-105">Этот класс является классом типа события для событий реестра.</span><span class="sxs-lookup"><span data-stu-id="21326-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="21326-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="21326-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="21326-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21326-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="21326-108">Члены</span><span class="sxs-lookup"><span data-stu-id="21326-108">Members</span></span>

<span data-ttu-id="21326-109">Класс **реестра \_ v0 \_ TypeGroup1** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="21326-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="21326-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="21326-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21326-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="21326-111">Properties</span></span>

<span data-ttu-id="21326-112">Класс **реестра \_ v0 \_ TypeGroup1** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="21326-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="21326-113">елапседтиме</span><span class="sxs-lookup"><span data-stu-id="21326-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21326-114">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="21326-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="21326-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21326-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21326-116">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="21326-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="21326-117">Время, затраченное на выполнение операции в реестре.</span><span class="sxs-lookup"><span data-stu-id="21326-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="21326-118">кэйхандле</span><span class="sxs-lookup"><span data-stu-id="21326-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21326-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21326-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21326-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21326-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21326-121">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="21326-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="21326-122">Обработчик раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="21326-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="21326-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="21326-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21326-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="21326-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21326-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21326-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21326-126">Квалификаторы: Вмидатаид (4), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="21326-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="21326-127">Имя раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="21326-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="21326-128">Состояние</span><span class="sxs-lookup"><span data-stu-id="21326-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21326-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="21326-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="21326-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="21326-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21326-131">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="21326-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="21326-132">Значение NTSTATUS операции реестра.</span><span class="sxs-lookup"><span data-stu-id="21326-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21326-133">Требования</span><span class="sxs-lookup"><span data-stu-id="21326-133">Requirements</span></span>



| <span data-ttu-id="21326-134">Требование</span><span class="sxs-lookup"><span data-stu-id="21326-134">Requirement</span></span> | <span data-ttu-id="21326-135">Значение</span><span class="sxs-lookup"><span data-stu-id="21326-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="21326-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="21326-136">Minimum supported client</span></span><br/> | <span data-ttu-id="21326-137">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="21326-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="21326-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="21326-138">Minimum supported server</span></span><br/> | <span data-ttu-id="21326-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="21326-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="21326-140">См. также</span><span class="sxs-lookup"><span data-stu-id="21326-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21326-141">**\_V0 реестра**</span><span class="sxs-lookup"><span data-stu-id="21326-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




