---
description: Этот класс является классом типа события для событий вызова основной функции драйвера. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Класс Дривермажорфунктионкалл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: c944b11c9019ba5244850f035bfc7c02d5ca3350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984232"
---
# <a name="drivermajorfunctioncall-class"></a><span data-ttu-id="7573a-104">Класс Дривермажорфунктионкалл</span><span class="sxs-lookup"><span data-stu-id="7573a-104">DriverMajorFunctionCall class</span></span>

<span data-ttu-id="7573a-105">Этот класс является классом типа события для событий вызова основной функции драйвера.</span><span class="sxs-lookup"><span data-stu-id="7573a-105">This class is the event type class for driver major function call events.</span></span>

<span data-ttu-id="7573a-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="7573a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7573a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7573a-107">Syntax</span></span>

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a><span data-ttu-id="7573a-108">Участники</span><span class="sxs-lookup"><span data-stu-id="7573a-108">Members</span></span>

<span data-ttu-id="7573a-109">Класс **дривермажорфунктионкалл** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7573a-109">The **DriverMajorFunctionCall** class has these types of members:</span></span>

-   [<span data-ttu-id="7573a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7573a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7573a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7573a-111">Properties</span></span>

<span data-ttu-id="7573a-112">Класс **дривермажорфунктионкалл** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7573a-112">The **DriverMajorFunctionCall** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7573a-113">**Закрыт**</span><span class="sxs-lookup"><span data-stu-id="7573a-113">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7573a-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7573a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7573a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7573a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7573a-116">Квалификаторы: Вмидатаид (4), Pointer</span><span class="sxs-lookup"><span data-stu-id="7573a-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7573a-117">Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**дискио \_ TypeGroup1**](diskio-typegroup1.md) , чтобы определить тип операции ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="7573a-117">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> <dt>

<span data-ttu-id="7573a-118">**IRP**</span><span class="sxs-lookup"><span data-stu-id="7573a-118">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7573a-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7573a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7573a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7573a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7573a-121">Квалификаторы: Вмидатаид (5), Pointer</span><span class="sxs-lookup"><span data-stu-id="7573a-121">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7573a-122">Пакет запроса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="7573a-122">IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="7573a-123">**мажорфунктион**</span><span class="sxs-lookup"><span data-stu-id="7573a-123">**MajorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7573a-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7573a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7573a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7573a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7573a-126">Квалификаторы: Вмидатаид (1)</span><span class="sxs-lookup"><span data-stu-id="7573a-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="7573a-127">Код, определяющий вызываемую основную функцию.</span><span class="sxs-lookup"><span data-stu-id="7573a-127">Code that identifies the major function being called.</span></span>

</dd> <dt>

<span data-ttu-id="7573a-128">**минорфунктион**</span><span class="sxs-lookup"><span data-stu-id="7573a-128">**MinorFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7573a-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7573a-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7573a-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7573a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7573a-131">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="7573a-131">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7573a-132">Код, иденитифиес вызываемую вспомогательную функцию.</span><span class="sxs-lookup"><span data-stu-id="7573a-132">Code that idenitifies the minor function being called.</span></span>

</dd> <dt>

<span data-ttu-id="7573a-133">**раутинеаддр**</span><span class="sxs-lookup"><span data-stu-id="7573a-133">**RoutineAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7573a-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7573a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7573a-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7573a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7573a-136">Квалификаторы: Вмидатаид (3), Pointer</span><span class="sxs-lookup"><span data-stu-id="7573a-136">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="7573a-137">Адрес вызываемой функции драйвера.</span><span class="sxs-lookup"><span data-stu-id="7573a-137">Address of the driver function being called.</span></span>

</dd> <dt>

<span data-ttu-id="7573a-138">**уникматчид**</span><span class="sxs-lookup"><span data-stu-id="7573a-138">**UniqMatchId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7573a-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7573a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7573a-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7573a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7573a-141">Квалификаторы: Вмидатаид (6)</span><span class="sxs-lookup"><span data-stu-id="7573a-141">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="7573a-142">Идентификатор, который однозначно идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="7573a-142">Identifier that uniquely identifies request.</span></span> <span data-ttu-id="7573a-143">Используйте этот идентификатор для сопоставления с другими событиями драйвера, например с событием [**дриверкомплетерекуест**](drivercompleterequest.md) .</span><span class="sxs-lookup"><span data-stu-id="7573a-143">Use this identifier to correlate with the other driver events, for example, the [**DriverCompleteRequest**](drivercompleterequest.md) event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7573a-144">Требования</span><span class="sxs-lookup"><span data-stu-id="7573a-144">Requirements</span></span>



| <span data-ttu-id="7573a-145">Требование</span><span class="sxs-lookup"><span data-stu-id="7573a-145">Requirement</span></span> | <span data-ttu-id="7573a-146">Значение</span><span class="sxs-lookup"><span data-stu-id="7573a-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7573a-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7573a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7573a-148">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7573a-148">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7573a-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7573a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7573a-150">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7573a-150">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7573a-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7573a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7573a-152">**дискио**</span><span class="sxs-lookup"><span data-stu-id="7573a-152">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




