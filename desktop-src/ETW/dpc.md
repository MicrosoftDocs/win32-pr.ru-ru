---
description: Этот класс является классом типа событий для событий отложенных вызовов процедур (DPC) устройства. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 46010179-7f0a-47dd-95fd-04d30fc597ba
title: Класс DPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DPC
- DPC.InitialTime
- DPC.Routine
api_type:
- NA
api_location: ''
ms.openlocfilehash: e0e756c2b41499a6e5b82129d609befc41d5e916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896857"
---
# <a name="dpc-class"></a><span data-ttu-id="b53b1-104">Класс DPC</span><span class="sxs-lookup"><span data-stu-id="b53b1-104">DPC class</span></span>

<span data-ttu-id="b53b1-105">Этот класс является классом типа событий для событий отложенных вызовов процедур (DPC) устройства.</span><span class="sxs-lookup"><span data-stu-id="b53b1-105">This class is the event type class for device deferred procedure call (DPC) events.</span></span>

<span data-ttu-id="b53b1-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="b53b1-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53b1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b53b1-107">Syntax</span></span>

``` syntax
[EventType{66, 68, 69}, EventTypeName{"ThreadDPC", "DPC", "TimerDPC"}]
class DPC : PerfInfo
{
  object InitialTime;
  uint32 Routine;
};
```

## <a name="members"></a><span data-ttu-id="b53b1-108">Участники</span><span class="sxs-lookup"><span data-stu-id="b53b1-108">Members</span></span>

<span data-ttu-id="b53b1-109">Класс **DPC** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b53b1-109">The **DPC** class has these types of members:</span></span>

-   [<span data-ttu-id="b53b1-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b53b1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b53b1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b53b1-111">Properties</span></span>

<span data-ttu-id="b53b1-112">Класс **DPC** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b53b1-112">The **DPC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b53b1-113">**инитиалтиме**</span><span class="sxs-lookup"><span data-stu-id="b53b1-113">**InitialTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b53b1-114">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="b53b1-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="b53b1-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b53b1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b53b1-116">Квалификаторы: Вмидатаид (1), Extension ("Вмитиме")</span><span class="sxs-lookup"><span data-stu-id="b53b1-116">Qualifiers: WmiDataId(1), Extension("WmiTime")</span></span>
</dt> </dl>

<span data-ttu-id="b53b1-117">Время записи DPC.</span><span class="sxs-lookup"><span data-stu-id="b53b1-117">DPC entry time.</span></span>

</dd> <dt>

<span data-ttu-id="b53b1-118">**Подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="b53b1-118">**Routine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b53b1-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b53b1-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b53b1-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b53b1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b53b1-121">Квалификаторы: Вмидатаид (2), Pointer</span><span class="sxs-lookup"><span data-stu-id="b53b1-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b53b1-122">Адрес подпрограммы DPC.</span><span class="sxs-lookup"><span data-stu-id="b53b1-122">Address of DPC routine.</span></span> <span data-ttu-id="b53b1-123">Используйте адрес с событиями Image, чтобы определить, какое изображение запущено.</span><span class="sxs-lookup"><span data-stu-id="b53b1-123">Use the address with the Image events to find which image started.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b53b1-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="b53b1-124">Remarks</span></span>

<span data-ttu-id="b53b1-125">Эти события регистрируются при входе DPC.</span><span class="sxs-lookup"><span data-stu-id="b53b1-125">These events are logged when a DPC is entered.</span></span> <span data-ttu-id="b53b1-126">Эти события используются для отслеживания и проверки поведения драйверов и компонентов режима ядра.</span><span class="sxs-lookup"><span data-stu-id="b53b1-126">You use these events to monitor and verify the behavior of drivers and kernel-mode components.</span></span> <span data-ttu-id="b53b1-127">Например, можно использовать события DPC, ISR и Image, чтобы определить, какие компоненты потратили слишком много времени на высокие уровни прерываний.</span><span class="sxs-lookup"><span data-stu-id="b53b1-127">For example, you can use DPC, ISR, and Image events to determine those components that spend too much time at high interrupt levels.</span></span> <span data-ttu-id="b53b1-128">События DPC и ISR имеют отметку времени записи, которая используется для расчета длительности подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="b53b1-128">DPC and ISR events have an entry time stamp which is used to compute the duration of the routines.</span></span> <span data-ttu-id="b53b1-129">События изображения считываются для создания областей памяти, сопоставленных с определенными модулями.</span><span class="sxs-lookup"><span data-stu-id="b53b1-129">The image events are read to construct the memory regions that map to certain modules.</span></span> <span data-ttu-id="b53b1-130">Сопоставление можно использовать для нахождение модуля, содержащего подпрограммы прерывания.</span><span class="sxs-lookup"><span data-stu-id="b53b1-130">You can use the mapping to locate the module that contains the interrupt routine.</span></span>

<span data-ttu-id="b53b1-131">Событие Тимердпк регистрируется, когда DPC срабатывает в результате истечения срока действия таймера, а событие Среаддпк регистрируется при выполнении потоковой обработки DPC.</span><span class="sxs-lookup"><span data-stu-id="b53b1-131">The TimerDPC event records when a DPC fires as a result of a timer expiration and the ThreadDPC event records when a threaded DPC executes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b53b1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="b53b1-132">Requirements</span></span>



| <span data-ttu-id="b53b1-133">Требование</span><span class="sxs-lookup"><span data-stu-id="b53b1-133">Requirement</span></span> | <span data-ttu-id="b53b1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="b53b1-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b53b1-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b53b1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b53b1-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b53b1-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b53b1-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b53b1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b53b1-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b53b1-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




