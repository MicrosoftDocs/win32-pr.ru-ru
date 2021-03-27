---
description: Абстрактный класс, от которого наследуются все классы трассировки событий.
ms.assetid: 03eea902-5050-4ab2-8a72-9bff7777e234
title: Класс Евенттраце
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace
- EventTrace.EventSize
- EventTrace.ReservedHeaderField
- EventTrace.EventType
- EventTrace.TraceLevel
- EventTrace.TraceVersion
- EventTrace.ThreadId
- EventTrace.TimeStamp
- EventTrace.EventGuid
- EventTrace.KernelTime
- EventTrace.UserTime
- EventTrace.InstanceId
- EventTrace.ParentGuid
- EventTrace.ParentInstanceId
- EventTrace.MofData
- EventTrace.MofLength
api_type:
- NA
api_location: ''
ms.openlocfilehash: f04399942b39a2da5b746933884a436a65bb370c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810456"
---
# <a name="eventtrace-class"></a><span data-ttu-id="c52ab-103">Класс Евенттраце</span><span class="sxs-lookup"><span data-stu-id="c52ab-103">EventTrace class</span></span>

<span data-ttu-id="c52ab-104">Абстрактный класс, от которого наследуются все классы трассировки событий.</span><span class="sxs-lookup"><span data-stu-id="c52ab-104">An abstract class from which all event trace classes are derived.</span></span>

<span data-ttu-id="c52ab-105">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="c52ab-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c52ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c52ab-106">Syntax</span></span>

``` syntax
[abstract]
class EventTrace
{
  uint16 EventSize;
  uint16 ReservedHeaderField;
  uint8  EventType;
  uint8  TraceLevel;
  uint16 TraceVersion;
  uint64 ThreadId;
  uint64 TimeStamp;
  uint8  EventGuid[];
  uint32 KernelTime;
  uint32 UserTime;
  uint32 InstanceId;
  uint8  ParentGuid[];
  uint32 ParentInstanceId;
  uint32 MofData;
  uint32 MofLength;
};
```

## <a name="members"></a><span data-ttu-id="c52ab-107">Участники</span><span class="sxs-lookup"><span data-stu-id="c52ab-107">Members</span></span>

<span data-ttu-id="c52ab-108">Класс **евенттраце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c52ab-108">The **EventTrace** class has these types of members:</span></span>

-   [<span data-ttu-id="c52ab-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c52ab-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c52ab-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c52ab-110">Properties</span></span>

<span data-ttu-id="c52ab-111">Класс **евенттраце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c52ab-111">The **EventTrace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c52ab-112">**евентгуид**</span><span class="sxs-lookup"><span data-stu-id="c52ab-112">**EventGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-113">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c52ab-113">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-115">Квалификаторы: **вмидатаид** (8), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="c52ab-115">Qualifiers: **WmiDataId** (8), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-116">Идентификатор GUID класса трассировки событий для этого события.</span><span class="sxs-lookup"><span data-stu-id="c52ab-116">Event trace class GUID of this event.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-117">**евентсизе**</span><span class="sxs-lookup"><span data-stu-id="c52ab-117">**EventSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-118">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c52ab-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-120">Квалификаторы: **вмидатаид** (1)</span><span class="sxs-lookup"><span data-stu-id="c52ab-120">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-121">Общее число байтов события.</span><span class="sxs-lookup"><span data-stu-id="c52ab-121">Total number of bytes of the event.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-122">**EventType**</span><span class="sxs-lookup"><span data-stu-id="c52ab-122">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-123">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c52ab-123">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-125">Квалификаторы: **вмидатаид** (3)</span><span class="sxs-lookup"><span data-stu-id="c52ab-125">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-126">Тип события, определяемый поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c52ab-126">Provider-defined event type.</span></span> <span data-ttu-id="c52ab-127">Указывает, какой класс типа событий следует использовать для расшифровки данных событий, определяемых поставщиком (данные, на которые указывает **мофдата**.</span><span class="sxs-lookup"><span data-stu-id="c52ab-127">Tells you which event type class to use to decipher the provider-defined event data (the data pointed to by **MofData**.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-128">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="c52ab-128">**InstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c52ab-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-131">Квалификаторы: **вмидатаид** (11)</span><span class="sxs-lookup"><span data-stu-id="c52ab-131">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-132">Идентификатор этого экземпляра события.</span><span class="sxs-lookup"><span data-stu-id="c52ab-132">Identifier of this event instance.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-133">**кернелтиме**</span><span class="sxs-lookup"><span data-stu-id="c52ab-133">**KernelTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c52ab-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-136">Квалификаторы: **вмидатаид** (9)</span><span class="sxs-lookup"><span data-stu-id="c52ab-136">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-137">Затраченное время выполнения инструкций режима ядра в тактах ЦП.</span><span class="sxs-lookup"><span data-stu-id="c52ab-137">Elapsed execution time for kernel-mode instructions, in CPU ticks.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-138">**мофдата**</span><span class="sxs-lookup"><span data-stu-id="c52ab-138">**MofData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c52ab-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-141">Квалификаторы: **вмидатаид** (14), **указатель**</span><span class="sxs-lookup"><span data-stu-id="c52ab-141">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-142">Указатель на данные события, зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="c52ab-142">Pointer to the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-143">**мофленгс**</span><span class="sxs-lookup"><span data-stu-id="c52ab-143">**MofLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c52ab-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-146">Квалификаторы: **вмидатаид** (15)</span><span class="sxs-lookup"><span data-stu-id="c52ab-146">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-147">Длина данных события, зависящего от поставщика.</span><span class="sxs-lookup"><span data-stu-id="c52ab-147">Length of the provider-specific event data.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-148">**парентгуид**</span><span class="sxs-lookup"><span data-stu-id="c52ab-148">**ParentGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-149">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c52ab-149">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-151">Квалификаторы: **вмидатаид** (12), **Max** (16)</span><span class="sxs-lookup"><span data-stu-id="c52ab-151">Qualifiers: **WmiDataId** (12), **Max** (16)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-152">Идентификатор GUID класса трассировки событий родительского экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c52ab-152">Event trace class GUID of the parent instance.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-153">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="c52ab-153">**ParentInstanceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-154">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c52ab-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-156">Квалификаторы: **вмидатаид** (13)</span><span class="sxs-lookup"><span data-stu-id="c52ab-156">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-157">Идентификатор данных родительского экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c52ab-157">Identifier of the parent instance data.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-158">**ресерведхеадерфиелд**</span><span class="sxs-lookup"><span data-stu-id="c52ab-158">**ReservedHeaderField**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-159">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c52ab-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-161">Квалификаторы: **вмидатаид** (2)</span><span class="sxs-lookup"><span data-stu-id="c52ab-161">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-162">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="c52ab-162">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-163">**Tидентификатор**</span><span class="sxs-lookup"><span data-stu-id="c52ab-163">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-164">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c52ab-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-166">Квалификаторы: **вмидатаид** (6), **pointer**</span><span class="sxs-lookup"><span data-stu-id="c52ab-166">Qualifiers: **WmiDataId** (6), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-167">Указывает поток, создавший событие.</span><span class="sxs-lookup"><span data-stu-id="c52ab-167">Identifies the thread that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-168">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="c52ab-168">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-169">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c52ab-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-171">Квалификаторы: **вмидатаид** (7)</span><span class="sxs-lookup"><span data-stu-id="c52ab-171">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-172">Содержит дату и время возникновения события.</span><span class="sxs-lookup"><span data-stu-id="c52ab-172">Contains the date and time when the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-173">**TraceLevel**</span><span class="sxs-lookup"><span data-stu-id="c52ab-173">**TraceLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-174">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c52ab-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-176">Квалификаторы: **вмидатаид** (4)</span><span class="sxs-lookup"><span data-stu-id="c52ab-176">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-177">Определяемое поставщиком значение, которое определяет степень серьезности, используемую для создания события.</span><span class="sxs-lookup"><span data-stu-id="c52ab-177">Provider-defined value that defines the severity level used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-178">**трацеверсион**</span><span class="sxs-lookup"><span data-stu-id="c52ab-178">**TraceVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-179">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c52ab-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-181">Квалификаторы: **вмидатаид** (5)</span><span class="sxs-lookup"><span data-stu-id="c52ab-181">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-182">Номер версии, определяемый поставщиком, для класса трассировки событий, используемого для создания события.</span><span class="sxs-lookup"><span data-stu-id="c52ab-182">Provider-defined version number of the event trace class used to generate the event.</span></span>

</dd> <dt>

<span data-ttu-id="c52ab-183">**усертиме**</span><span class="sxs-lookup"><span data-stu-id="c52ab-183">**UserTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c52ab-184">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c52ab-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c52ab-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c52ab-186">Квалификаторы: **вмидатаид** (10)</span><span class="sxs-lookup"><span data-stu-id="c52ab-186">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="c52ab-187">Затраченное время выполнения инструкций пользовательского режима в тактах ЦП.</span><span class="sxs-lookup"><span data-stu-id="c52ab-187">Elapsed execution time for user-mode instructions, in CPU ticks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c52ab-188">Примечания</span><span class="sxs-lookup"><span data-stu-id="c52ab-188">Remarks</span></span>

<span data-ttu-id="c52ab-189">Не используйте эти свойства.</span><span class="sxs-lookup"><span data-stu-id="c52ab-189">Do not use these properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="c52ab-190">Требования</span><span class="sxs-lookup"><span data-stu-id="c52ab-190">Requirements</span></span>



| <span data-ttu-id="c52ab-191">Требование</span><span class="sxs-lookup"><span data-stu-id="c52ab-191">Requirement</span></span> | <span data-ttu-id="c52ab-192">Значение</span><span class="sxs-lookup"><span data-stu-id="c52ab-192">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c52ab-193">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c52ab-193">Minimum supported client</span></span><br/> | <span data-ttu-id="c52ab-194">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c52ab-194">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c52ab-195">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c52ab-195">Minimum supported server</span></span><br/> | <span data-ttu-id="c52ab-196">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c52ab-196">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c52ab-197">MOF</span><span class="sxs-lookup"><span data-stu-id="c52ab-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c52ab-198"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c52ab-198"><dt>Wmi.mof</dt></span></span> </dl> |



 

 




