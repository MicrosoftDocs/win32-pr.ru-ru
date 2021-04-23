---
description: Интерфейс Икспропертисет изначально разрабатывался как эффективный способ задания и получения свойств устройства в драйверах WDM, используя Кспрокси для преобразования вызовов метода COM в пользовательском режиме в наборы свойств режима ядра, используемые драйверами класса потоковой передачи WDM. Этот интерфейс теперь также используется для передачи сведений строго между программными компонентами. В некоторых случаях программные компоненты должны реализовывать этот интерфейс или использовать интерфейс Иксконтрол (описанный в пакете DDK по DirectShow). Например, если вы создаете программный декодер MPEG-2 для использования с DVD-навигатором, необходимо реализовать один из этих интерфейсов и также поддерживать наборы свойств, связанных с DVD, которые навигатор будет передавать декодеру. ПИН-коды могут поддерживать один из этих интерфейсов, чтобы другие ПИН-коды или фильтры могли устанавливать или извлекать их свойства. Обратите внимание, что другой интерфейс с таким именем существует в файле заголовка дсаунд. h. Два интерфейса несовместимы. Интерфейс Иксконтрол, документированный в пакете DDK по DirectShow, теперь является рекомендуемым интерфейсом для передачи наборов свойств между драйверами WDM и компонентами пользовательского режима. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Интерфейс Икспропертисет (Кспрокси. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494331"
---
# <a name="ikspropertyset-interface"></a><span data-ttu-id="80b9d-109">Интерфейс Икспропертисет</span><span class="sxs-lookup"><span data-stu-id="80b9d-109">IKsPropertySet interface</span></span>

<span data-ttu-id="80b9d-110">`IKsPropertySet`Изначально интерфейс был разработан как эффективный способ установки и извлечения свойств устройства в драйверах WDM, используя кспрокси для преобразования вызовов методов COM пользовательского режима в наборы свойств режима ядра, используемые драйверами класса потоковой передачи WDM.</span><span class="sxs-lookup"><span data-stu-id="80b9d-110">The `IKsPropertySet` interface was originally designed as an efficient way to set and retrieve device properties on WDM drivers, using KSProxy to translate the user-mode COM method calls into the kernel-mode property sets used by WDM streaming class drivers.</span></span> <span data-ttu-id="80b9d-111">Этот интерфейс теперь также используется для передачи сведений строго между программными компонентами.</span><span class="sxs-lookup"><span data-stu-id="80b9d-111">This interface is now also used to pass information strictly between software components.</span></span>

<span data-ttu-id="80b9d-112">В некоторых случаях программные компоненты должны реализовывать этот интерфейс или использовать интерфейс **иксконтрол** (описанный в пакете DDK по DirectShow).</span><span class="sxs-lookup"><span data-stu-id="80b9d-112">In some cases, software components must implement either this interface, or else the **IKsControl** interface (documented in the DirectShow DDK).</span></span> <span data-ttu-id="80b9d-113">Например, если вы создаете программный декодер MPEG-2 для использования с DVD- [навигатором](dvd-navigator-filter.md), необходимо реализовать один из этих интерфейсов и также поддерживать наборы свойств, связанных с DVD, которые навигатор будет передавать декодеру.</span><span class="sxs-lookup"><span data-stu-id="80b9d-113">For example, if you are writing a software MPEG-2 decoder for use with the [DVD Navigator](dvd-navigator-filter.md), you must implement one of these interfaces and also support the DVD-related property sets that the Navigator will send to the decoder.</span></span> <span data-ttu-id="80b9d-114">ПИН-коды могут поддерживать один из этих интерфейсов, чтобы другие ПИН-коды или фильтры могли устанавливать или извлекать их свойства.</span><span class="sxs-lookup"><span data-stu-id="80b9d-114">Pins may support one of these interfaces to allow other pins or filters to set or retrieve their properties.</span></span>

> [!Note]  
> <span data-ttu-id="80b9d-115">Другой интерфейс с таким именем существует в файле заголовка дсаунд. h.</span><span class="sxs-lookup"><span data-stu-id="80b9d-115">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="80b9d-116">Два интерфейса несовместимы.</span><span class="sxs-lookup"><span data-stu-id="80b9d-116">The two interfaces are not compatible.</span></span> <span data-ttu-id="80b9d-117">Интерфейс **иксконтрол** , документированный в пакете DDK по DirectShow, теперь является рекомендуемым интерфейсом для передачи наборов свойств между драйверами WDM и компонентами пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="80b9d-117">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

## <a name="members"></a><span data-ttu-id="80b9d-118">Элементы</span><span class="sxs-lookup"><span data-stu-id="80b9d-118">Members</span></span>

<span data-ttu-id="80b9d-119">Интерфейс **икспропертисет** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="80b9d-119">The **IKsPropertySet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="80b9d-120">**Икспропертисет** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="80b9d-120">**IKsPropertySet** also has these types of members:</span></span>

-   [<span data-ttu-id="80b9d-121">Методы</span><span class="sxs-lookup"><span data-stu-id="80b9d-121">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="80b9d-122">Методы</span><span class="sxs-lookup"><span data-stu-id="80b9d-122">Methods</span></span>

<span data-ttu-id="80b9d-123">Интерфейс **икспропертисет** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="80b9d-123">The **IKsPropertySet** interface has these methods.</span></span>



| <span data-ttu-id="80b9d-124">Метод</span><span class="sxs-lookup"><span data-stu-id="80b9d-124">Method</span></span>                                                  | <span data-ttu-id="80b9d-125">Описание</span><span class="sxs-lookup"><span data-stu-id="80b9d-125">Description</span></span>                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="80b9d-126">**Получить**</span><span class="sxs-lookup"><span data-stu-id="80b9d-126">**Get**</span></span>](ikspropertyset-get.md)                       | <span data-ttu-id="80b9d-127">Извлекает свойство, определяемое идентификатором GUID набора свойств и ИДЕНТИФИКАТОРом свойства.</span><span class="sxs-lookup"><span data-stu-id="80b9d-127">Retrieves a property identified by a property set GUID and a property ID.</span></span><br/> |
| [<span data-ttu-id="80b9d-128">**куерисуппортед**</span><span class="sxs-lookup"><span data-stu-id="80b9d-128">**QuerySupported**</span></span>](ikspropertyset-querysupported.md) | <span data-ttu-id="80b9d-129">Определяет, поддерживает ли объект заданный набор свойств.</span><span class="sxs-lookup"><span data-stu-id="80b9d-129">Determines whether an object supports a specified property set.</span></span><br/>           |
| [<span data-ttu-id="80b9d-130">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="80b9d-130">**Set**</span></span>](ikspropertyset-set.md)                       | <span data-ttu-id="80b9d-131">Задает свойство, определяемое идентификатором GUID набора свойств и ИДЕНТИФИКАТОРом свойства.</span><span class="sxs-lookup"><span data-stu-id="80b9d-131">Sets a property identified by a property set GUID and a property ID.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="80b9d-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80b9d-132">Remarks</span></span>

<span data-ttu-id="80b9d-133">Перед Кспрокси. h необходимо включить KS. h.</span><span class="sxs-lookup"><span data-stu-id="80b9d-133">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b9d-134">Требования</span><span class="sxs-lookup"><span data-stu-id="80b9d-134">Requirements</span></span>



| <span data-ttu-id="80b9d-135">Требование</span><span class="sxs-lookup"><span data-stu-id="80b9d-135">Requirement</span></span> | <span data-ttu-id="80b9d-136">Значение</span><span class="sxs-lookup"><span data-stu-id="80b9d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80b9d-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80b9d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="80b9d-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80b9d-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="80b9d-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80b9d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="80b9d-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="80b9d-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="80b9d-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="80b9d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b9d-142"><dt>Кспрокси. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b9d-142"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="80b9d-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80b9d-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="80b9d-144"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80b9d-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b9d-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80b9d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b9d-146">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="80b9d-146">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
