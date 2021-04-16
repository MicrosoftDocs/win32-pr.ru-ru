---
title: Уровень компонентов Direct3D 12 Core 1.0
description: Основной уровень компонентов 1,0 является подмножеством полного набора функций Direct3D 12.
ms.topic: article
ms.date: 11/05/2019
ms.openlocfilehash: 42d13b71c516e55ecce378cf9cb415c45e520ba9
ms.sourcegitcommit: bba068130240d16de8a3f3468b7cd72b2cd760f6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2020
ms.locfileid: "105719120"
---
# <a name="the-direct3d-12-core-10-feature-level"></a>Уровень компонентов Direct3D 12 Core 1.0

Основной уровень компонентов 1,0 является подмножеством полного набора функций Direct3D 12. Уровень компонентов Core 1,0 может предоставляться категорией устройств, которые называются *устройствами только для вычислений*. Общая модель драйвера для устройств, предназначенных только для вычислений, — это модель вычислений Microsoft COMPUTE Driver (МКДМ). МКДМ — это масштабируемый одноранговый узел модели драйверов устройств Windows (WDDM), имеющий более широкую область.

Устройство, которое поддерживает *только* функции в базовом уровне, называется *основным устройством*.

> [!NOTE]
> *Устройство только для вычислений*, устройство *мкдм*, *базовое устройство уровня функций* и *Основное устройство* означают одно и то же. Для простоты мы предпочитаем *Основное устройство* .

## <a name="creating-a-core-device"></a>Создание базового устройства

Как правило, для создания устройства Direct3D 12 вызывается функция [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) и указывается минимальный уровень компонента.

Если указать уровень признаков от 9 до 12, то возвращенное устройство является устройством с богатыми возможностями, например традиционным графическим процессором (который поддерживает надмножество функций основного устройства). Основное устройство никогда не возвращается для этого диапазона уровней функций.

С другой стороны, если указать основной уровень компонентов (например, [**D3D_FEATURE_LEVEL::D 3D_FEATURE_LEVEL_1_0_CORE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)), то возвращаемое устройство может быть многофункциональным или базовым устройством.

```cpp
// d3dcommon.h
D3D_FEATURE_LEVEL_1_0_CORE = 0x1000
```

Если указан `_CORE` уровень компонента, то уровень среды выполнения и отладки проверяет, что функции, используемые приложением, разрешены этим `_CORE` уровнем функций. Этот набор функций определен далее в этом разделе.

## <a name="shader-model-for-core-devices"></a>Модель шейдера для основных устройств

Устройство ядра поддерживает модель шейдеров версии 5.0 +.

Среда выполнения выполняет преобразование моделей шейдера 5. x без ДКСИЛ в 6,0 ДКСИЛ. Поэтому драйверу требуется только поддержка 6. x.

## <a name="resource-management-model-for-core-devices"></a>Модель управления ресурсами для основных устройств

- Поддерживаемые измерения ресурсов: только необработанные и структурированные буферы (без типизированных буферов, texture1d/2D и т. д.)
- Нет поддержки зарезервированных (мозаичных) ресурсов
- Нет поддержки пользовательских куч
- Ни один из следующих флагов кучи не поддерживается:
  - D3D12_HEAP_FLAG_HARDWARE_PROTECTED
  - D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH
  - D3D12_HEAP_FLAG_ALLOW_DISPLAY
  - D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS (Обратите внимание, что требуются атомарные шейдеры, этот флаг предназначен для другого компонента, атомарных операций с разными адаптерами).

## <a name="resource-binding-model-for-core-devices"></a>Модель привязки ресурсов для основных устройств

- Поддержка только для уровня привязки ресурсов 1
- Исключения:
  - Нет поддержки для образцов текстуры
  - Поддержка 64 Уавс, например, уровень функции 11.1 + (в отличие от 8).
  - Реализациям не требуется реализовывать проверку границ для доступа шейдера к ресурсам через дескрипторы, доступ к которым вызывает неопределенное поведение.
    - В качестве побочным эффектом флаг диапазона дескрипторов D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_STATIC_KEEPING_BUFFER_BOUNDS_CHECKS в корневых сигнатурах не поддерживается.
- Дескрипторы UAV и CBV могут быть сделаны только для ресурсов из куч по умолчанию (без куч отправки и реадбакк). Это заставляет приложение выполнять копирование для получения данных между ЦП<->GPU.
- Несмотря на то, что это самый низкий уровень возможностей привязки, некоторые функции, которые необходимо выполнить даже на этом уровне, все еще стоит вызывать:
  - Кучи дескрипторов можно обновлять после записи списков команд (см. D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE в спецификации привязки ресурсов).
  - Корневые дескрипторы — это, по сути, ГПУВА указатели
    - Несмотря на отсутствие поддержки ММУ/ва, буфер VAs, используемый в корневых дескрипторах, может эмулироваться реализациями путем исправления адресов.

### <a name="structured-buffer-restrictions"></a>Ограничения структурированного буфера

Структурированные буферы должны иметь базовый адрес размером 4 байта, а шаг должен быть 2 или кратным 4. Случай для шага 2 — для приложений с 16-разрядными данными, особенно учитывая, что в D3D_FEATURE_LEVEL_1_0_CORE не поддерживается типизированные буферы.

Шаг, указанный в дескрипторах, должен соответствовать STRIDE, указанному в HLSL.  

## <a name="command-queue-support-for-core-devices"></a>Поддержка очереди команд для основных устройств

Вычислять и копировать только очереди (без 3D, видео и т. д.).

## <a name="shader-support-for-core-devices"></a>Поддержка шейдера для основных устройств

Только для шейдеров вычислений, без графических шейдеров (вершин, шейдеры пикселей и т. д.) и любых связанных функций, таких как целевые объекты рендеринга, цепочки буфера обмена, входной ассемблер.

### <a name="arithmetic-precision"></a>Арифметическая точность

Базовые устройства не должны поддерживать денорму для 16 разрядных операций с плавающей точкой.

## <a name="supported-apis-for-core-devices"></a>Поддерживаемые API для основных устройств

*Приведенный* ниже список представляет поддерживаемое подмножество полного прикладного программного интерфейса (API, которые *не* поддерживаются на уровне компонента Core 1,0).

### <a name="id3d12device-methods"></a>Методы ID3D12Device

* [ID3D12Device:: Чеккфеатуресуппорт](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
* [ID3D12Device:: Копидескрипторс](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptors)
* [ID3D12Device:: Копидескрипторссимпле](/windows/win32/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)
* [ID3D12Device:: Креатекоммандаллокатор](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator)
* [ID3D12Device:: Креатекоммандлист](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)
* [ID3D12Device:: Креатекоммандкуеуе](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)
* [ID3D12Device:: Креатекоммандсигнатуре](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandsignature)
* [ID3D12Device:: Креатекоммиттедресаурце](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
* [ID3D12Device:: Креатекомпутепипелинестате](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate)
* [ID3D12Device:: Креатеконстантбуффервиев](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createconstantbufferview)
* [ID3D12Device:: Креатедескрипторхеап](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)
* [ID3D12Device:: Креатефенце](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence)
* [ID3D12Device:: CreateHeap](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)
* [ID3D12Device:: Креатеплацедресаурце](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createplacedresource)
* [ID3D12Device:: Креатекуерихеап](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createqueryheap)
* [ID3D12Device:: Креатерутсигнатуре](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)
* [ID3D12Device:: Креатешадерресаурцевиев](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)
* [ID3D12Device:: Креатешаредхандле](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle)
* [ID3D12Device:: Креатеунордередакцессвиев](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)
* [ID3D12Device:: вытеснение](/windows/win32/api/d3d12/nf-d3d12-id3d12device-evict)
* [ID3D12Device:: Жетадаптерлуид](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)
* [ID3D12Device:: GetCopyableFootprints](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
* [ID3D12Device:: Жеткустомхеаппропертиес](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcustomheapproperties)
* [ID3D12Device:: Жетдескрипторхандлеинкрементсизе](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)
* [ID3D12Device:: Жетдевицеремоведреасон](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdeviceremovedreason)
* [ID3D12Device:: Жетнодекаунт](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getnodecount)
* [ID3D12Device:: Жетресаурцеаллокатионинфо](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)
* [ID3D12Device:: Макересидент](/windows/win32/api/d3d12/nf-d3d12-id3d12device-makeresident)
* [ID3D12Device:: Опеншаредхандле](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandle)
* [ID3D12Device:: Опеншаредхандлебинаме](/windows/win32/api/d3d12/nf-d3d12-id3d12device-opensharedhandlebyname)
* [ID3D12Device:: Сетстаблеповерстате](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)

### <a name="id3d12device1-methods"></a>Методы ID3D12Device1

* [ID3D12Device1:: Креатепипелинелибрари](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary)
* [ID3D12Device1:: Сетевентонмултиплефенцекомплетион](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-seteventonmultiplefencecompletion)
* [ID3D12Device1:: Сетресиденцисетевентонмултиплефенцекомплетионприорити](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority)

### <a name="id3d12device2-methods"></a>Методы ID3D12Device2

* [ID3D12Device2:: Креатепипелинестате](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)

### <a name="id3d12device3-methods"></a>Методы ID3D12Device3

* [ID3D12Device3:: Опенексистингхеапфромаддресс](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-openexistingheapfromaddress)
* [ID3D12Device3:: Опенексистингхеапфромфилемаппинг](/previous-versions/windows/desktop/legacy/mt813613(v%3Dvs.85))
* [ID3D12Device3:: Енкуеуемакересидент](/windows/win32/api/d3d12/nf-d3d12-id3d12device3-enqueuemakeresident)

### <a name="id3d12device4-methods"></a>Методы ID3D12Device4

* [ID3D12Device4::GetResourceAllocationInfo1](/windows/win32/api/d3d12/nf-d3d12-id3d12device4-getresourceallocationinfo1)

### <a name="id3d12device5-methods"></a>Методы ID3D12Device5

* [ID3D12Device5:: Креатеметакомманд](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createmetacommand)
* [ID3D12Device5:: Креатестатеобжект](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-createstateobject)
* [ID3D12Device5:: Енумератеметакоммандпараметерс](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommandparameters)
* [ID3D12Device5:: Енумератеметакоммандс](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-enumeratemetacommands)
* [ID3D12Device5:: Ремоведевице](/windows/win32/api/d3d12/nf-d3d12-id3d12device5-removedevice)

### <a name="id3d12commandqueue-methods"></a>Методы ID3D12CommandQueue

* [ID3D12CommandQueue:: Бегиневент](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-beginevent)
* [ID3D12CommandQueue:: Ендевент](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-endevent)
* [ID3D12CommandQueue:: Ексекутекоммандлистс](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)
* [ID3D12CommandQueue:: Жетклокккалибратион](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)
* [ID3D12CommandQueue:: DESC](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getdesc)
* [ID3D12CommandQueue:: Жеттиместампфрекуенци](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)
* [ID3D12CommandQueue:: SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-setmarker)
* [ID3D12CommandQueue:: сигнал](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
* [ID3D12CommandQueue:: wait](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)

### <a name="id3d12commandlist-methods"></a>Методы ID3D12CommandList

* [ID3D12CommandList:: GetType](/windows/win32/api/d3d12/nf-d3d12-id3d12commandlist-gettype)

### <a name="id3d12graphicscommandlist-methods"></a>Методы ID3D12GraphicsCommandList

* [ID3D12GraphicsCommandList:: Бегиневент](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginevent)
* [ID3D12GraphicsCommandList:: Бегинкуери](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery)
* [ID3D12GraphicsCommandList:: Клеарстате](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
* [ID3D12GraphicsCommandList:: Клеарунордередакцессвиевфлоат](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
* [ID3D12GraphicsCommandList:: Клеарунордередакцессвиевуинт](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
* [ID3D12GraphicsCommandList:: Close](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
* [ID3D12GraphicsCommandList:: Копибуфферрегион](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
* [ID3D12GraphicsCommandList:: Копиресаурце](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
* [ID3D12GraphicsCommandList:: Копитекстуререгион](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
* [ID3D12GraphicsCommandList::D Patch](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
* [ID3D12GraphicsCommandList:: Ендевент](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endevent)
* [ID3D12GraphicsCommandList:: Ендкуери](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery)
* [ID3D12GraphicsCommandList:: Reset](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
* [ID3D12GraphicsCommandList:: Ресолвекуеридата](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
* [ID3D12GraphicsCommandList:: Ресаурцебарриер](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstant](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
* [ID3D12GraphicsCommandList::SetComputeRoot32BitConstants](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
* [ID3D12GraphicsCommandList:: Сеткомпутерутконстантбуффервиев](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
* [ID3D12GraphicsCommandList:: Сеткомпутерутдескриптортабле](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
* [ID3D12GraphicsCommandList:: Сеткомпутерутшадерресаурцевиев](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
* [ID3D12GraphicsCommandList:: Сеткомпутерутсигнатуре](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
* [ID3D12GraphicsCommandList:: Сеткомпутерутунордередакцессвиев](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
* [ID3D12GraphicsCommandList:: Сетдескрипторхеапс](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
* [ID3D12GraphicsCommandList:: SetMarker](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setmarker)
* [ID3D12GraphicsCommandList:: Сетпипелинестате](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
* [ID3D12GraphicsCommandList:: Сетпредикатион](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

### <a name="id3d12graphicscommandlist1-methods"></a>Методы ID3D12GraphicsCommandList1

* [ID3D12GraphicsCommandList1:: Атомиккопибуфферуинт](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
* [ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)

### <a name="id3d12graphicscommandlist2-methods"></a>Методы ID3D12GraphicsCommandList2

* [ID3D12GraphicsCommandList2:: Вритебуффериммедиате](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate)

### <a name="id3d12graphicscommandlist4-methods"></a>Методы ID3D12GraphicsCommandList4

* [ID3D12GraphicsCommandList4:: Ексекутеметакомманд](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-executemetacommand)
* [ID3D12GraphicsCommandList4:: Инитиализеметакомманд](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-initializemetacommand)
