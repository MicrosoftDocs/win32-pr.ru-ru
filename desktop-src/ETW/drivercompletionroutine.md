---
description: Этот класс является классом типа события для выполнения подпрограмм драйвера. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: deb4f0b2-d73f-4ccf-b39b-6e92b32489fb
title: Класс Дриверкомплетионраутине
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompletionRoutine
- DriverCompletionRoutine.Routine
- DriverCompletionRoutine.Irp
- DriverCompletionRoutine.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2b43862169cbe8f192f8fb9db561c2e101f377b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896854"
---
# <a name="drivercompletionroutine-class"></a><span data-ttu-id="bf391-104">Класс Дриверкомплетионраутине</span><span class="sxs-lookup"><span data-stu-id="bf391-104">DriverCompletionRoutine class</span></span>

<span data-ttu-id="bf391-105">Этот класс является классом типа события для выполнения подпрограмм драйвера.</span><span class="sxs-lookup"><span data-stu-id="bf391-105">This class is the event type class for driver complete routine events.</span></span>

<span data-ttu-id="bf391-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="bf391-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf391-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf391-107">Syntax</span></span>

``` syntax
[EventType{37}, EventTypeName{"DrvComplRout"}]
class DriverCompletionRoutine : DiskIo
{
  uint32 Routine;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="bf391-108">Участники</span><span class="sxs-lookup"><span data-stu-id="bf391-108">Members</span></span>

<span data-ttu-id="bf391-109">Класс **дриверкомплетионраутине** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bf391-109">The **DriverCompletionRoutine** class has these types of members:</span></span>

-   [<span data-ttu-id="bf391-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bf391-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf391-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="bf391-111">Properties</span></span>

<span data-ttu-id="bf391-112">Класс **дриверкомплетионраутине** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bf391-112">The **DriverCompletionRoutine** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf391-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="bf391-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf391-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf391-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf391-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf391-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf391-116">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="bf391-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bf391-117">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="bf391-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="bf391-118">**Подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="bf391-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf391-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf391-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf391-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf391-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf391-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="bf391-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bf391-122">Адрес вызываемой функции драйвера.</span><span class="sxs-lookup"><span data-stu-id="bf391-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="bf391-123">**уникматчид**</span><span class="sxs-lookup"><span data-stu-id="bf391-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf391-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf391-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf391-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bf391-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf391-126">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="bf391-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="bf391-127">Идентификатор, который однозначно идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="bf391-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="bf391-128">Используйте этот идентификатор для сопоставления с другими событиями драйвера, например с событием [**дриверкомплетерекуест**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="bf391-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf391-129">Требования</span><span class="sxs-lookup"><span data-stu-id="bf391-129">Requirements</span></span>



| <span data-ttu-id="bf391-130">Требование</span><span class="sxs-lookup"><span data-stu-id="bf391-130">Requirement</span></span> | <span data-ttu-id="bf391-131">Значение</span><span class="sxs-lookup"><span data-stu-id="bf391-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bf391-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf391-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bf391-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf391-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bf391-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf391-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bf391-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf391-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf391-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf391-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf391-137">**дискио**</span><span class="sxs-lookup"><span data-stu-id="bf391-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




