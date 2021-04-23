---
description: Этот класс является классом типа события для событий реестра. Следующий синтаксис упрощен из MOF-кода.
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
ms.openlocfilehash: 2cd77ad0c12769c657b4e7c23c1fe1993a248481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897638"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="df1c4-104">\_ \_ Класс TypeGroup1 реестра v1</span><span class="sxs-lookup"><span data-stu-id="df1c4-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="df1c4-105">Этот класс является классом типа события для событий реестра.</span><span class="sxs-lookup"><span data-stu-id="df1c4-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="df1c4-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="df1c4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="df1c4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df1c4-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="df1c4-108">Участники</span><span class="sxs-lookup"><span data-stu-id="df1c4-108">Members</span></span>

<span data-ttu-id="df1c4-109">Класс **\_ \_ TypeGroup1 в реестре** версии 1 содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="df1c4-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="df1c4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="df1c4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df1c4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="df1c4-111">Properties</span></span>

<span data-ttu-id="df1c4-112">Класс **\_ \_ TypeGroup1 в реестре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="df1c4-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df1c4-113">елапседтиме</span><span class="sxs-lookup"><span data-stu-id="df1c4-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df1c4-114">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="df1c4-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df1c4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-116">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="df1c4-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="df1c4-117">Время, затраченное на выполнение операции в реестре.</span><span class="sxs-lookup"><span data-stu-id="df1c4-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="df1c4-118">Индекс</span><span class="sxs-lookup"><span data-stu-id="df1c4-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df1c4-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df1c4-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df1c4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-121">Квалификаторы: Вмидатаид (4)</span><span class="sxs-lookup"><span data-stu-id="df1c4-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="df1c4-122">Индекс подраздела для операции реестра (например, Енумератекэй).</span><span class="sxs-lookup"><span data-stu-id="df1c4-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="df1c4-123">кэйхандле</span><span class="sxs-lookup"><span data-stu-id="df1c4-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df1c4-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df1c4-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df1c4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-126">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="df1c4-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df1c4-127">Обработчик раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="df1c4-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="df1c4-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="df1c4-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df1c4-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="df1c4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df1c4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-131">Квалификаторы: Вмидатаид (5), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="df1c4-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="df1c4-132">Имя раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="df1c4-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="df1c4-133">Состояние</span><span class="sxs-lookup"><span data-stu-id="df1c4-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df1c4-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df1c4-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df1c4-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df1c4-136">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="df1c4-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="df1c4-137">Значение NTSTATUS операции реестра.</span><span class="sxs-lookup"><span data-stu-id="df1c4-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df1c4-138">Требования</span><span class="sxs-lookup"><span data-stu-id="df1c4-138">Requirements</span></span>



| <span data-ttu-id="df1c4-139">Требование</span><span class="sxs-lookup"><span data-stu-id="df1c4-139">Requirement</span></span> | <span data-ttu-id="df1c4-140">Значение</span><span class="sxs-lookup"><span data-stu-id="df1c4-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="df1c4-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df1c4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="df1c4-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df1c4-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="df1c4-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df1c4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="df1c4-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df1c4-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="df1c4-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df1c4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df1c4-146">**Реестр**</span><span class="sxs-lookup"><span data-stu-id="df1c4-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="df1c4-147">**Реестр \_ v1**</span><span class="sxs-lookup"><span data-stu-id="df1c4-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 




