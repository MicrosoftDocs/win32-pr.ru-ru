---
description: Этот класс является родительским для событий изображений. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Класс Image
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985596"
---
# <a name="image-class"></a><span data-ttu-id="48f6d-104">Класс Image</span><span class="sxs-lookup"><span data-stu-id="48f6d-104">Image class</span></span>

<span data-ttu-id="48f6d-105">Этот класс является родительским для событий изображений.</span><span class="sxs-lookup"><span data-stu-id="48f6d-105">This class is the parent class for image events.</span></span>

<span data-ttu-id="48f6d-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="48f6d-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="48f6d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48f6d-107">Syntax</span></span>

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="48f6d-108">Участники</span><span class="sxs-lookup"><span data-stu-id="48f6d-108">Members</span></span>

<span data-ttu-id="48f6d-109">Класс **Image** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="48f6d-109">The **Image** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="48f6d-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="48f6d-110">Remarks</span></span>

<span data-ttu-id="48f6d-111">Чтобы включить события изображений в сеансе ведения журнала ядра NT, укажите **флаг \_ \_ \_ \_ загрузки изображения флага трассировки событий** в элементе **енаблефлагс** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) при вызове функции [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="48f6d-111">To enable image events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_IMAGE\_LOAD** flag in the **EnableFlags** member of the [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="48f6d-112">Потребители трассировки событий могут реализовать специальную обработку событий загрузки изображения, вызвав функцию [**сеттрацекаллбакк**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) и указав [**имажелоадгуид**](nt-kernel-logger-constants.md) в качестве параметра *пгуид* .</span><span class="sxs-lookup"><span data-stu-id="48f6d-112">Event trace consumers can implement special processing for image load events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ImageLoadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="48f6d-113">Используйте следующие типы событий для обнаружения событий загрузки изображений при использовании событий.</span><span class="sxs-lookup"><span data-stu-id="48f6d-113">Use the following event types to identify image load events when consuming events.</span></span>



| <span data-ttu-id="48f6d-114">Тип события</span><span class="sxs-lookup"><span data-stu-id="48f6d-114">Event type</span></span>                                                          | <span data-ttu-id="48f6d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="48f6d-115">Description</span></span>                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48f6d-116">**Событие \_ \_ \_ Загрузка типа трассировки**(значение типа события — 10)</span><span class="sxs-lookup"><span data-stu-id="48f6d-116">**EVENT\_TRACE\_TYPE\_LOAD**(Event type value is 10)</span></span><br/>     | <span data-ttu-id="48f6d-117">Событие загрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="48f6d-117">Image load event.</span></span> <span data-ttu-id="48f6d-118">Создается при загрузке библиотеки DLL или исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="48f6d-118">Generated when a DLL or executable file is loaded.</span></span> <span data-ttu-id="48f6d-119">Поставщик создает только одно событие при первой загрузке заданной библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="48f6d-119">The provider generates only one event for the first time a given DLL is loaded.</span></span> <span data-ttu-id="48f6d-120">Класс [**MOF \_ загрузки образа**](image-load.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="48f6d-120">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="48f6d-121">**Событие \_ \_ \_ Конец типа трассировки**(значение типа события — 2)</span><span class="sxs-lookup"><span data-stu-id="48f6d-121">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>       | <span data-ttu-id="48f6d-122">Событие выгрузки изображения.</span><span class="sxs-lookup"><span data-stu-id="48f6d-122">Image unload event.</span></span> <span data-ttu-id="48f6d-123">Создается при выгрузке библиотеки DLL или исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="48f6d-123">Generated when a DLL or executable file is unloaded.</span></span> <span data-ttu-id="48f6d-124">Поставщик создает только одно событие для последней выгрузки данной библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="48f6d-124">The provider generates only one event for the last time a given DLL is unloaded.</span></span> <span data-ttu-id="48f6d-125">Класс [**MOF \_ загрузки образа**](image-load.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="48f6d-125">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="48f6d-126">**Событие \_ \_Тип трассировки \_ \_ Start контроллера домена**(значение типа события — 3)</span><span class="sxs-lookup"><span data-stu-id="48f6d-126">**EVENT\_TRACE\_TYPE\_DC\_START**(Event type value is 3)</span></span><br/> | <span data-ttu-id="48f6d-127">Событие начала сбора данных.</span><span class="sxs-lookup"><span data-stu-id="48f6d-127">Data collection start event.</span></span> <span data-ttu-id="48f6d-128">Перечисляет все загруженные изображения в начале трассировки.</span><span class="sxs-lookup"><span data-stu-id="48f6d-128">Enumerates all loaded images at the beginning of the trace.</span></span> <span data-ttu-id="48f6d-129">Класс [**MOF \_ загрузки образа**](image-load.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="48f6d-129">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                  |
| <span data-ttu-id="48f6d-130">**Событие \_ \_Тип трассировки \_ \_ конец контроллера домена**(значение типа события — 4)</span><span class="sxs-lookup"><span data-stu-id="48f6d-130">**EVENT\_TRACE\_TYPE\_DC\_END**(Event type value is 4)</span></span><br/>   | <span data-ttu-id="48f6d-131">Событие окончания сбора данных.</span><span class="sxs-lookup"><span data-stu-id="48f6d-131">Data collection end event.</span></span> <span data-ttu-id="48f6d-132">Перечисляет все загруженные изображения в конце трассировки.</span><span class="sxs-lookup"><span data-stu-id="48f6d-132">Enumerates all loaded images at the end of the trace.</span></span> <span data-ttu-id="48f6d-133">Класс [**MOF \_ загрузки образа**](image-load.md) определяет данные события для этого события.</span><span class="sxs-lookup"><span data-stu-id="48f6d-133">The [**Image\_Load**](image-load.md) MOF class defines the event data for this event.</span></span>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="48f6d-134">Требования</span><span class="sxs-lookup"><span data-stu-id="48f6d-134">Requirements</span></span>



| <span data-ttu-id="48f6d-135">Требование</span><span class="sxs-lookup"><span data-stu-id="48f6d-135">Requirement</span></span> | <span data-ttu-id="48f6d-136">Значение</span><span class="sxs-lookup"><span data-stu-id="48f6d-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48f6d-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48f6d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="48f6d-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48f6d-138">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="48f6d-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48f6d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="48f6d-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48f6d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48f6d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48f6d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f6d-142">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="48f6d-142">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="48f6d-143">**\_Загрузка образа**</span><span class="sxs-lookup"><span data-stu-id="48f6d-143">**Image\_Load**</span></span>](image-load.md)
</dt> <dt>

[<span data-ttu-id="48f6d-144">**\_V0 изображения**</span><span class="sxs-lookup"><span data-stu-id="48f6d-144">**Image\_V0**</span></span>](image-v0.md)
</dt> <dt>

[<span data-ttu-id="48f6d-145">**Образ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="48f6d-145">**Image\_V1**</span></span>](image-v1.md)
</dt> </dl>

 

 
