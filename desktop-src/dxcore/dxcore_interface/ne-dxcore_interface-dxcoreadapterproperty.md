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
# <a name="dxcoreadapterproperty-enum"></a>Перечисление Дкскореадаптерпроперти

Определяет константы, указывающие свойства адаптера Дкскоре. Передайте одну из этих констант методу [идкскореадаптер:: жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы получить размер буфера, необходимый для получения значения соответствующего свойства. затем передайте ту же константу в метод [идкскореадаптер::-Property](./nf-dxcore_interface-idxcoreadapter-getproperty.md) , чтобы получить значение свойства в выделенном буфере.

## <a name="syntax"></a>Синтаксис

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

## <a name="constants"></a>Константы

### <a name="instanceluid"></a>инстанцелуид

Указывает свойство адаптера <em>инстанцелуид</em> , которое содержит локально уникальный идентификатор, представляющий адаптер. Это значение остается постоянным в течение времени существования этого адаптера. LUID адаптера изменяется при перезагрузке, обновлении драйвера или невозможности или включении устройства.

Свойство адаптера <em>инстанцелуид</em> имеет тип <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.

### <a name="driverversion"></a>дриверверсион

Указывает свойство адаптера <em>дриверверсион</em> , которое содержит версию драйвера, представленную в <b>WORD</b>s как <b>LARGE_INTEGER</b>.

Свойство адаптера <em>дриверверсион</em> имеет тип <b>Uint64_t</b>, представляющий логическое значение.

### <a name="driverdescription"></a>дривердескриптион

Указывает свойство адаптера <em>дривердескриптион</em> , которое содержит массив <b>char</b>s, заканчивающийся нулем, описывающий драйвер в кодировке <a href="/windows/win32/intl/unicode">UTF-8</a> .

Свойство адаптера <em>дривердескриптион</em> имеет тип <b>char *</b>.

### <a name="hardwareid"></a>хардвареид

Указывает свойство адаптера <em>хардвареид</em> , которое представляет части идентификатора оборудования PnP.

Свойство адаптера <em>хардвареид</em> имеет тип <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">дкскорехардвареид</a>.

### <a name="kmdmodelversion"></a>кмдмоделверсион

Указывает свойство адаптера <em>кмдмоделверсион</em> , представляющее модель драйвера.

Свойство адаптера <em>кмдмоделверсион</em> имеет тип <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>компутепримптионгрануларити

Указывает свойство адаптера <em>компутепримптионгрануларити</em> , представляющее гранулярность вычислений при вытеснении.

Свойство адаптера <em>компутепримптионгрануларити</em> имеет тип <b>uint16_t</b>, представляющий <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> значение.

### <a name="graphicspreemptiongranularity"></a>графикспримптионгрануларити

Указывает свойство адаптера <em>графикспримптионгрануларити</em> , которое представляет степень гранулярности приоритетного прерывания графики.

Свойство адаптера <em>графикспримптионгрануларити</em> имеет тип <b>uint16_t</b>, представляющий <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> значение.

### <a name="dedicatedadaptermemory"></a>дедикатедадаптермемори

Указывает свойство адаптера <em>дедикатедадаптермемори</em> , которое представляет число байтов выделенной памяти адаптера, которые не используются совместно с ЦП.

Свойство адаптера <em>дедикатедвидеомемори</em> имеет тип <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>дедикатедсистеммемори

Указывает свойство адаптера <em>дедикатедсистеммемори</em> , которое представляет число байтов выделенной системной памяти, которые не используются совместно с ЦП. Эта память выделяется из доступной системной памяти во время загрузки.

Свойство адаптера <em>дедикатедсистеммемори</em> имеет тип <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>шаредсистеммемори

Указывает свойство адаптера <em>шаредсистеммемори</em> , которое представляет число байтов общей системной памяти. Это максимальное значение системной памяти, которое может потребляться адаптером во время операции. Любые случайные объемы памяти, потребляемые драйвером при управлении и использовании видеопамяти, являются дополнительными.

Свойство адаптера <em>шаредсистеммемори</em> имеет тип <b>uint64_t</b>.

### <a name="acgcompatible"></a>акгкомпатибле

Указывает свойство адаптера <em>акгкомпатибле</em> , которое указывает, совместим ли адаптер с процессами, которые применяют произвольное Code Guard.

Свойство адаптера <em>акгкомпатибле</em> имеет тип <b>bool</b>.

### <a name="ishardware"></a>Оборудование

Указывает свойство адаптера <em>оборудования</em> , которое определяет, является ли этот адаптер аппаратным. Адаптером, который не является аппаратным адаптером, является программный адаптер.

Свойство адаптера <em>оборудования</em> имеет тип <b>bool</b>.

### <a name="isintegrated"></a>Интегрированный

Задает свойство адаптера <em>Integrated</em> , которое определяет, является ли адаптер интегрированным графическим процессором (ИГПУ).

Свойство адаптера <em>Integrated</em> имеет тип <b>bool</b>.

### <a name="isdetachable"></a>Докрепление

Задает свойство <em>адаптера,</em> которое определяет, был ли адаптер передан как Отсоединяемый или съемный.

Свойство адаптера, <em>присоединяемого</em> , имеет тип <b>bool</b>.

<b>Примечание</b>. Даже если <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">идкскореадаптер::-Property</a> указывает `false` на это свойство, адаптер по-прежнему может сообщать об удалении, например в случае неисправности или обновлении драйвера.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер:: жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [идкскореадаптер::](./nf-dxcore_interface-idxcoreadapter-getproperty.md)GetEnumerator, [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)