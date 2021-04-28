---
description: Класс Registry_V1_TypeGroup1 — этот класс является классом типа события для событий реестра. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Класс Registry_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab0326f92d1b084f471f3dc1b57322f69aa645fd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106162"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="91a71-104">\_ \_ Класс TypeGroup1 реестра v1</span><span class="sxs-lookup"><span data-stu-id="91a71-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="91a71-105">Этот класс является классом типа события для событий реестра.</span><span class="sxs-lookup"><span data-stu-id="91a71-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="91a71-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="91a71-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a71-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91a71-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="91a71-108">Члены</span><span class="sxs-lookup"><span data-stu-id="91a71-108">Members</span></span>

<span data-ttu-id="91a71-109">Класс **\_ \_ TypeGroup1 в реестре** версии 1 содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="91a71-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="91a71-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="91a71-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91a71-111">Элемент Property</span><span class="sxs-lookup"><span data-stu-id="91a71-111">Properties</span></span>

<span data-ttu-id="91a71-112">Класс **\_ \_ TypeGroup1 в реестре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="91a71-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91a71-113">елапседтиме</span><span class="sxs-lookup"><span data-stu-id="91a71-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91a71-114">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="91a71-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="91a71-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91a71-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91a71-116">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="91a71-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="91a71-117">Время, затраченное на выполнение операции в реестре.</span><span class="sxs-lookup"><span data-stu-id="91a71-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="91a71-118">Индекс</span><span class="sxs-lookup"><span data-stu-id="91a71-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91a71-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91a71-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91a71-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91a71-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91a71-121">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="91a71-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="91a71-122">Индекс подраздела для операции реестра (например, Енумератекэй).</span><span class="sxs-lookup"><span data-stu-id="91a71-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="91a71-123">кэйхандле</span><span class="sxs-lookup"><span data-stu-id="91a71-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91a71-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91a71-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91a71-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91a71-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91a71-126">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="91a71-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="91a71-127">Обработчик раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="91a71-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="91a71-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="91a71-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91a71-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91a71-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91a71-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91a71-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91a71-131">Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="91a71-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="91a71-132">Имя раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="91a71-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="91a71-133">Состояние</span><span class="sxs-lookup"><span data-stu-id="91a71-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91a71-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91a71-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91a71-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91a71-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91a71-136">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="91a71-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="91a71-137">Значение NTSTATUS операции реестра.</span><span class="sxs-lookup"><span data-stu-id="91a71-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91a71-138">Требования</span><span class="sxs-lookup"><span data-stu-id="91a71-138">Requirements</span></span>



| <span data-ttu-id="91a71-139">Требование</span><span class="sxs-lookup"><span data-stu-id="91a71-139">Requirement</span></span> | <span data-ttu-id="91a71-140">Значение</span><span class="sxs-lookup"><span data-stu-id="91a71-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="91a71-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91a71-141">Minimum supported client</span></span><br/> | <span data-ttu-id="91a71-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91a71-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="91a71-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91a71-143">Minimum supported server</span></span><br/> | <span data-ttu-id="91a71-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="91a71-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="91a71-145">См. также</span><span class="sxs-lookup"><span data-stu-id="91a71-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a71-146">**Реестр**</span><span class="sxs-lookup"><span data-stu-id="91a71-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="91a71-147">**Реестр \_ v1**</span><span class="sxs-lookup"><span data-stu-id="91a71-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 




