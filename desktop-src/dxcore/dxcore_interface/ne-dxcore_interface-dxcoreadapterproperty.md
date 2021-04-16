---
title: 'DXCoreAdapterProperty '
description: Определяет константы, указывающие свойства адаптера Дкскоре.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 645f0a890aac9a50cdf2987c0736a85142a91aff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719131"
---
# <a name="dxcoreadapterproperty-enum"></a><span data-ttu-id="db1f9-103">Перечисление Дкскореадаптерпроперти</span><span class="sxs-lookup"><span data-stu-id="db1f9-103">DXCoreAdapterProperty enum</span></span>

<span data-ttu-id="db1f9-104">Определяет константы, указывающие свойства адаптера Дкскоре.</span><span class="sxs-lookup"><span data-stu-id="db1f9-104">Defines constants that specify DXCore adapter properties.</span></span> <span data-ttu-id="db1f9-105">Передайте одну из этих констант методу [идкскореадаптер:: жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы получить размер буфера, необходимый для получения значения соответствующего свойства. затем передайте ту же константу в метод [идкскореадаптер::-Property](./nf-dxcore_interface-idxcoreadapter-getproperty.md) , чтобы получить значение свойства в выделенном буфере.</span><span class="sxs-lookup"><span data-stu-id="db1f9-105">Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) method to retrieve the property's value in a buffer that you allocate.</span></span>

## <a name="syntax"></a><span data-ttu-id="db1f9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db1f9-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterProperty : uint32_t
{
  InstanceLuid = 0,
  DriverVersion = 1,
  DriverDescription = 2,
  HardwareID = 3,
  KmdModelVersion = 4,
  ComputePreemptionGranularity = 5,
  GraphicsPreemptionGranularity = 6,
  DedicatedAdapterMemory = 7,
  DedicatedSystemMemory = 8,
  SharedSystemMemory = 9,
  AcgCompatible = 10,
  IsHardware = 11,
  IsIntegrated = 12,
  IsDetachable = 13
};
```

## <a name="constants"></a><span data-ttu-id="db1f9-107">Константы</span><span class="sxs-lookup"><span data-stu-id="db1f9-107">Constants</span></span>

### <a name="instanceluid"></a><span data-ttu-id="db1f9-108">инстанцелуид</span><span class="sxs-lookup"><span data-stu-id="db1f9-108">InstanceLuid</span></span>

<span data-ttu-id="db1f9-109">Указывает свойство адаптера <em>инстанцелуид</em> , которое содержит локально уникальный идентификатор, представляющий адаптер.</span><span class="sxs-lookup"><span data-stu-id="db1f9-109">Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter.</span></span> <span data-ttu-id="db1f9-110">Это значение остается постоянным в течение времени существования этого адаптера.</span><span class="sxs-lookup"><span data-stu-id="db1f9-110">This value remains constant for the lifetime of this adapter.</span></span> <span data-ttu-id="db1f9-111">LUID адаптера изменяется при перезагрузке, обновлении драйвера или невозможности или включении устройства.</span><span class="sxs-lookup"><span data-stu-id="db1f9-111">The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.</span></span>

<span data-ttu-id="db1f9-112">Свойство адаптера <em>инстанцелуид</em> имеет тип <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-112">The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span></span>

### <a name="driverversion"></a><span data-ttu-id="db1f9-113">дриверверсион</span><span class="sxs-lookup"><span data-stu-id="db1f9-113">DriverVersion</span></span>

<span data-ttu-id="db1f9-114">Указывает свойство адаптера <em>дриверверсион</em> , которое содержит версию драйвера, представленную в <b>WORD</b>s как <b>LARGE_INTEGER</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-114">Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.</span></span>

<span data-ttu-id="db1f9-115">Свойство адаптера <em>дриверверсион</em> имеет тип <b>Uint64_t</b>, представляющий логическое значение.</span><span class="sxs-lookup"><span data-stu-id="db1f9-115">The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.</span></span>

### <a name="driverdescription"></a><span data-ttu-id="db1f9-116">дривердескриптион</span><span class="sxs-lookup"><span data-stu-id="db1f9-116">DriverDescription</span></span>

<span data-ttu-id="db1f9-117">Указывает свойство адаптера <em>дривердескриптион</em> , которое содержит массив <b>char</b>s, заканчивающийся нулем, описывающий драйвер в кодировке <a href="/windows/win32/intl/unicode">UTF-8</a> .</span><span class="sxs-lookup"><span data-stu-id="db1f9-117">Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.</span></span>

<span data-ttu-id="db1f9-118">Свойство адаптера <em>дривердескриптион</em> имеет тип <b>char \*</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-118">The <em>DriverDescription</em> adapter property has type <b>char\*</b>.</span></span>

### <a name="hardwareid"></a><span data-ttu-id="db1f9-119">хардвареид</span><span class="sxs-lookup"><span data-stu-id="db1f9-119">HardwareID</span></span>

<span data-ttu-id="db1f9-120">Указывает свойство адаптера <em>хардвареид</em> , которое представляет части идентификатора оборудования PnP.</span><span class="sxs-lookup"><span data-stu-id="db1f9-120">Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.</span></span>

<span data-ttu-id="db1f9-121">Свойство адаптера <em>хардвареид</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">дкскорехардвареид</a>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-121">The <em>HardwareID</em> adapter property has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span></span>

### <a name="kmdmodelversion"></a><span data-ttu-id="db1f9-122">кмдмоделверсион</span><span class="sxs-lookup"><span data-stu-id="db1f9-122">KmdModelVersion</span></span>

<span data-ttu-id="db1f9-123">Указывает свойство адаптера <em>кмдмоделверсион</em> , представляющее модель драйвера.</span><span class="sxs-lookup"><span data-stu-id="db1f9-123">Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.</span></span>

<span data-ttu-id="db1f9-124">Свойство адаптера <em>кмдмоделверсион</em> имеет тип <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-124">The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span></span>

### <a name="computepreemptiongranularity"></a><span data-ttu-id="db1f9-125">компутепримптионгрануларити</span><span class="sxs-lookup"><span data-stu-id="db1f9-125">ComputePreemptionGranularity</span></span>

<span data-ttu-id="db1f9-126">Указывает свойство адаптера <em>компутепримптионгрануларити</em> , представляющее гранулярность вычислений при вытеснении.</span><span class="sxs-lookup"><span data-stu-id="db1f9-126">Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.</span></span>

<span data-ttu-id="db1f9-127">Свойство адаптера <em>компутепримптионгрануларити</em> имеет тип <b>uint16_t</b>, представляющий <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> значение.</span><span class="sxs-lookup"><span data-stu-id="db1f9-127">The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="graphicspreemptiongranularity"></a><span data-ttu-id="db1f9-128">графикспримптионгрануларити</span><span class="sxs-lookup"><span data-stu-id="db1f9-128">GraphicsPreemptionGranularity</span></span>

<span data-ttu-id="db1f9-129">Указывает свойство адаптера <em>графикспримптионгрануларити</em> , которое представляет степень гранулярности приоритетного прерывания графики.</span><span class="sxs-lookup"><span data-stu-id="db1f9-129">Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.</span></span>

<span data-ttu-id="db1f9-130">Свойство адаптера <em>графикспримптионгрануларити</em> имеет тип <b>uint16_t</b>, представляющий <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> значение.</span><span class="sxs-lookup"><span data-stu-id="db1f9-130">The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="dedicatedadaptermemory"></a><span data-ttu-id="db1f9-131">дедикатедадаптермемори</span><span class="sxs-lookup"><span data-stu-id="db1f9-131">DedicatedAdapterMemory</span></span>

<span data-ttu-id="db1f9-132">Указывает свойство адаптера <em>дедикатедадаптермемори</em> , которое представляет число байтов выделенной памяти адаптера, которые не используются совместно с ЦП.</span><span class="sxs-lookup"><span data-stu-id="db1f9-132">Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.</span></span>

<span data-ttu-id="db1f9-133">Свойство адаптера <em>дедикатедвидеомемори</em> имеет тип <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-133">The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="dedicatedsystemmemory"></a><span data-ttu-id="db1f9-134">дедикатедсистеммемори</span><span class="sxs-lookup"><span data-stu-id="db1f9-134">DedicatedSystemMemory</span></span>

<span data-ttu-id="db1f9-135">Указывает свойство адаптера <em>дедикатедсистеммемори</em> , которое представляет число байтов выделенной системной памяти, которые не используются совместно с ЦП.</span><span class="sxs-lookup"><span data-stu-id="db1f9-135">Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU.</span></span> <span data-ttu-id="db1f9-136">Эта память выделяется из доступной системной памяти во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="db1f9-136">This memory is allocated from available system memory at boot time.</span></span>

<span data-ttu-id="db1f9-137">Свойство адаптера <em>дедикатедсистеммемори</em> имеет тип <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-137">The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="sharedsystemmemory"></a><span data-ttu-id="db1f9-138">шаредсистеммемори</span><span class="sxs-lookup"><span data-stu-id="db1f9-138">SharedSystemMemory</span></span>

<span data-ttu-id="db1f9-139">Указывает свойство адаптера <em>шаредсистеммемори</em> , которое представляет число байтов общей системной памяти.</span><span class="sxs-lookup"><span data-stu-id="db1f9-139">Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory.</span></span> <span data-ttu-id="db1f9-140">Это максимальное значение системной памяти, которое может потребляться адаптером во время операции.</span><span class="sxs-lookup"><span data-stu-id="db1f9-140">This is the maximum value of system memory that may be consumed by the adapter during operation.</span></span> <span data-ttu-id="db1f9-141">Любые случайные объемы памяти, потребляемые драйвером при управлении и использовании видеопамяти, являются дополнительными.</span><span class="sxs-lookup"><span data-stu-id="db1f9-141">Any incidental memory consumed by the driver as it manages and uses video memory is additional.</span></span>

<span data-ttu-id="db1f9-142">Свойство адаптера <em>шаредсистеммемори</em> имеет тип <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-142">The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="acgcompatible"></a><span data-ttu-id="db1f9-143">акгкомпатибле</span><span class="sxs-lookup"><span data-stu-id="db1f9-143">AcgCompatible</span></span>

<span data-ttu-id="db1f9-144">Указывает свойство адаптера <em>акгкомпатибле</em> , которое указывает, совместим ли адаптер с процессами, которые применяют произвольное Code Guard.</span><span class="sxs-lookup"><span data-stu-id="db1f9-144">Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.</span></span>

<span data-ttu-id="db1f9-145">Свойство адаптера <em>акгкомпатибле</em> имеет тип <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-145">The <em>AcgCompatible</em> adapter property has type <b>bool</b>.</span></span>

### <a name="ishardware"></a><span data-ttu-id="db1f9-146">Оборудование</span><span class="sxs-lookup"><span data-stu-id="db1f9-146">IsHardware</span></span>

<span data-ttu-id="db1f9-147">Указывает свойство адаптера <em>оборудования</em> , которое определяет, является ли этот адаптер аппаратным.</span><span class="sxs-lookup"><span data-stu-id="db1f9-147">Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter.</span></span> <span data-ttu-id="db1f9-148">Адаптером, который не является аппаратным адаптером, является программный адаптер.</span><span class="sxs-lookup"><span data-stu-id="db1f9-148">An adapter that's not a hardware adapter is a software adapter.</span></span>

<span data-ttu-id="db1f9-149">Свойство адаптера <em>оборудования</em> имеет тип <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-149">The <em>IsHardware</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isintegrated"></a><span data-ttu-id="db1f9-150">Интегрированный</span><span class="sxs-lookup"><span data-stu-id="db1f9-150">IsIntegrated</span></span>

<span data-ttu-id="db1f9-151">Задает свойство адаптера <em>Integrated</em> , которое определяет, является ли адаптер интегрированным графическим процессором (ИГПУ).</span><span class="sxs-lookup"><span data-stu-id="db1f9-151">Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).</span></span>

<span data-ttu-id="db1f9-152">Свойство адаптера <em>Integrated</em> имеет тип <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-152">The <em>IsIntegrated</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isdetachable"></a><span data-ttu-id="db1f9-153">Докрепление</span><span class="sxs-lookup"><span data-stu-id="db1f9-153">IsDetachable</span></span>

<span data-ttu-id="db1f9-154">Задает свойство <em>адаптера,</em> которое определяет, был ли адаптер передан как Отсоединяемый или съемный.</span><span class="sxs-lookup"><span data-stu-id="db1f9-154">Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.</span></span>

<span data-ttu-id="db1f9-155">Свойство адаптера, <em>присоединяемого</em> , имеет тип <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-155">The <em>IsDetachable</em> adapter property has type <b>bool</b>.</span></span>

<span data-ttu-id="db1f9-156"><b>Примечание</b>.</span><span class="sxs-lookup"><span data-stu-id="db1f9-156"><b>Note</b>.</span></span> <span data-ttu-id="db1f9-157">Даже если <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">идкскореадаптер::-Property</a> указывает `false` на это свойство, адаптер по-прежнему может сообщать об удалении, например в случае неисправности или обновлении драйвера.</span><span class="sxs-lookup"><span data-stu-id="db1f9-157">Even if <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.</span></span>

## <a name="see-also"></a><span data-ttu-id="db1f9-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db1f9-158">See also</span></span>

<span data-ttu-id="db1f9-159">[Идкскореадаптер:: жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [идкскореадаптер::](./nf-dxcore_interface-idxcoreadapter-getproperty.md)GetEnumerator, [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="db1f9-159">[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>