---
description: Класс Registry_TypeGroup1 — этот класс является классом типа события для событий реестра. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Класс Registry_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: d86412a950246bee4f9a692ab80e91b99d945c20
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106252"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="44653-104">\_Класс TypeGroup1 реестра</span><span class="sxs-lookup"><span data-stu-id="44653-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="44653-105">Этот класс является классом типа события для событий реестра.</span><span class="sxs-lookup"><span data-stu-id="44653-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="44653-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="44653-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="44653-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44653-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="44653-108">Члены</span><span class="sxs-lookup"><span data-stu-id="44653-108">Members</span></span>

<span data-ttu-id="44653-109">Класс **\_ TypeGroup1 реестра** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="44653-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="44653-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="44653-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44653-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="44653-111">Properties</span></span>

<span data-ttu-id="44653-112">Класс **\_ TypeGroup1 реестра** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44653-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44653-113">Индекс</span><span class="sxs-lookup"><span data-stu-id="44653-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44653-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44653-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44653-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44653-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44653-116">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="44653-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="44653-117">Индекс подраздела для операции реестра (например, Енумератекэй).</span><span class="sxs-lookup"><span data-stu-id="44653-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="44653-118">инитиалтиме</span><span class="sxs-lookup"><span data-stu-id="44653-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44653-119">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="44653-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="44653-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44653-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44653-121">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="44653-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="44653-122">Начальное время операции с реестром.</span><span class="sxs-lookup"><span data-stu-id="44653-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="44653-123">кэйхандле</span><span class="sxs-lookup"><span data-stu-id="44653-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44653-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44653-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44653-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44653-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44653-126">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="44653-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44653-127">Обработчик раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="44653-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="44653-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="44653-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44653-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="44653-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44653-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44653-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44653-131">Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="44653-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="44653-132">Имя раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="44653-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="44653-133">Состояние</span><span class="sxs-lookup"><span data-stu-id="44653-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44653-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44653-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44653-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="44653-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44653-136">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="44653-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44653-137">Значение NTSTATUS операции реестра.</span><span class="sxs-lookup"><span data-stu-id="44653-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44653-138">Требования</span><span class="sxs-lookup"><span data-stu-id="44653-138">Requirements</span></span>



| <span data-ttu-id="44653-139">Требование</span><span class="sxs-lookup"><span data-stu-id="44653-139">Requirement</span></span> | <span data-ttu-id="44653-140">Значение</span><span class="sxs-lookup"><span data-stu-id="44653-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44653-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44653-141">Minimum supported client</span></span><br/> | <span data-ttu-id="44653-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44653-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44653-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44653-143">Minimum supported server</span></span><br/> | <span data-ttu-id="44653-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="44653-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44653-145">См. также</span><span class="sxs-lookup"><span data-stu-id="44653-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44653-146">**Реестр**</span><span class="sxs-lookup"><span data-stu-id="44653-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




