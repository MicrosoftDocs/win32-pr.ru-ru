---
description: Этот класс является классом типа события для событий запроса драйвера Complete. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Класс Дриверкомплетерекуест
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 57cf49d0e37dc870c0eb46c31ef39e0d81689811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984236"
---
# <a name="drivercompleterequest-class"></a><span data-ttu-id="74a32-104">Класс Дриверкомплетерекуест</span><span class="sxs-lookup"><span data-stu-id="74a32-104">DriverCompleteRequest class</span></span>

<span data-ttu-id="74a32-105">Этот класс является классом типа события для событий запроса драйвера Complete.</span><span class="sxs-lookup"><span data-stu-id="74a32-105">This class is the event type class for driver complete request events.</span></span>

<span data-ttu-id="74a32-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="74a32-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a32-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74a32-107">Syntax</span></span>

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="74a32-108">Участники</span><span class="sxs-lookup"><span data-stu-id="74a32-108">Members</span></span>

<span data-ttu-id="74a32-109">Класс **дриверкомплетерекуест** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74a32-109">The **DriverCompleteRequest** class has these types of members:</span></span>

-   [<span data-ttu-id="74a32-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="74a32-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74a32-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="74a32-111">Properties</span></span>

<span data-ttu-id="74a32-112">Класс **дриверкомплетерекуест** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74a32-112">The **DriverCompleteRequest** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74a32-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="74a32-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74a32-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74a32-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74a32-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74a32-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74a32-116">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="74a32-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="74a32-117">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="74a32-117">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="74a32-118">**раутинеаддр**</span><span class="sxs-lookup"><span data-stu-id="74a32-118">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74a32-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74a32-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74a32-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74a32-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74a32-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="74a32-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="74a32-122">Адрес вызываемой функции драйвера.</span><span class="sxs-lookup"><span data-stu-id="74a32-122">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="74a32-123">**уникматчид**</span><span class="sxs-lookup"><span data-stu-id="74a32-123">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74a32-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74a32-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74a32-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74a32-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74a32-126">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="74a32-126">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="74a32-127">Идентификатор, который однозначно идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="74a32-127">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="74a32-128">Используйте этот идентификатор для сопоставления с другими событиями драйвера, например с событием [**дриверкомплетерекуестретурн**](drivercompleterequestreturn.md) .</span><span class="sxs-lookup"><span data-stu-id="74a32-128">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74a32-129">Требования</span><span class="sxs-lookup"><span data-stu-id="74a32-129">Requirements</span></span>



| <span data-ttu-id="74a32-130">Требование</span><span class="sxs-lookup"><span data-stu-id="74a32-130">Requirement</span></span> | <span data-ttu-id="74a32-131">Значение</span><span class="sxs-lookup"><span data-stu-id="74a32-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74a32-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74a32-132">Minimum supported client</span></span><br/> | <span data-ttu-id="74a32-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74a32-133">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74a32-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74a32-134">Minimum supported server</span></span><br/> | <span data-ttu-id="74a32-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74a32-135">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74a32-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74a32-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a32-137">**дискио**</span><span class="sxs-lookup"><span data-stu-id="74a32-137">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




