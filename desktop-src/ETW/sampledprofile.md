---
description: Этот класс является классом типа события для выборки событий профиля. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Класс Сампледпрофиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985937"
---
# <a name="sampledprofile-class"></a><span data-ttu-id="3854a-104">Класс Сампледпрофиле</span><span class="sxs-lookup"><span data-stu-id="3854a-104">SampledProfile class</span></span>

<span data-ttu-id="3854a-105">Этот класс является классом типа события для выборки событий профиля.</span><span class="sxs-lookup"><span data-stu-id="3854a-105">This class is the event type class for sampled profile events.</span></span>

<span data-ttu-id="3854a-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="3854a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="3854a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3854a-107">Syntax</span></span>

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a><span data-ttu-id="3854a-108">Участники</span><span class="sxs-lookup"><span data-stu-id="3854a-108">Members</span></span>

<span data-ttu-id="3854a-109">Класс **сампледпрофиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3854a-109">The **SampledProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="3854a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3854a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3854a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3854a-111">Properties</span></span>

<span data-ttu-id="3854a-112">Класс **сампледпрофиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3854a-112">The **SampledProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3854a-113">**Количество**</span><span class="sxs-lookup"><span data-stu-id="3854a-113">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3854a-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3854a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3854a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3854a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3854a-116">Квалификаторы: Вмидатаид (3)</span><span class="sxs-lookup"><span data-stu-id="3854a-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="3854a-117">Не используется.</span><span class="sxs-lookup"><span data-stu-id="3854a-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3854a-118">**инструктионпоинтер**</span><span class="sxs-lookup"><span data-stu-id="3854a-118">**InstructionPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3854a-119">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3854a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3854a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3854a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3854a-121">Квалификаторы: Вмидатаид (1), Pointer</span><span class="sxs-lookup"><span data-stu-id="3854a-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="3854a-122">Адрес образа, который был запущен на момент выборки процессора.</span><span class="sxs-lookup"><span data-stu-id="3854a-122">Address of the image that was running at the time the processor was sampled.</span></span>

</dd> <dt>

<span data-ttu-id="3854a-123">**Tидентификатор**</span><span class="sxs-lookup"><span data-stu-id="3854a-123">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3854a-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3854a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3854a-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3854a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3854a-126">Квалификаторы: Вмидатаид (2)</span><span class="sxs-lookup"><span data-stu-id="3854a-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="3854a-127">Идентификатор потока, который был запущен на момент выборки процессора.</span><span class="sxs-lookup"><span data-stu-id="3854a-127">Thread identifier of the thread that was running at the time the processor was sampled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3854a-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="3854a-128">Remarks</span></span>

<span data-ttu-id="3854a-129">Эти события предоставляют примерный профиль выполнения.</span><span class="sxs-lookup"><span data-stu-id="3854a-129">These events provide a sampled execution profile.</span></span> <span data-ttu-id="3854a-130">Событие записывает, что было выполнено на процессоре.</span><span class="sxs-lookup"><span data-stu-id="3854a-130">The event records what was being executed on the processor.</span></span> <span data-ttu-id="3854a-131">События Image можно использовать для указания двоичного модуля, содержащего эту инструкцию.</span><span class="sxs-lookup"><span data-stu-id="3854a-131">You can use the Image events to identify the binary module containing that instruction.</span></span> <span data-ttu-id="3854a-132">Затем эти сведения можно использовать для создания профиля выполнения в течение времени трассировки.</span><span class="sxs-lookup"><span data-stu-id="3854a-132">You can then use this information to produce an execution profile for the duration of the trace.</span></span>

## <a name="requirements"></a><span data-ttu-id="3854a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="3854a-133">Requirements</span></span>



| <span data-ttu-id="3854a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="3854a-134">Requirement</span></span> | <span data-ttu-id="3854a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3854a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3854a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3854a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3854a-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3854a-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3854a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3854a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3854a-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3854a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




