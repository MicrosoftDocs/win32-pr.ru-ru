---
title: Перечисление адаптеров с использованием DXCore
description: Рассмотрим основные функции Дкскоре с примерами кода, а также полный листинг исходного кода для минимального приложения Дкскоре.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: f1c21971f2daea69de1f317d1db8eceb9ec00118
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719124"
---
# <a name="using-dxcore-to-enumerate-adapters"></a><span data-ttu-id="e564e-103">Перечисление адаптеров с использованием DXCore</span><span class="sxs-lookup"><span data-stu-id="e564e-103">Using DXCore to enumerate adapters</span></span>

<span data-ttu-id="e564e-104">Дкскоре — это API перечисления адаптеров для устройств DirectX, поэтому некоторые его средства перекрываются с устройствами [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="e564e-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

<span data-ttu-id="e564e-105">Дкскоре позволяет раскрытие новых типов устройств в пользовательском режиме, например МКДМ (модель драйвера вычислений Майкрософт), для использования с [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [директмл](../direct3d12/dml.md)и [Windows машинное обучение](/windows/ai/windows-ml/).</span><span class="sxs-lookup"><span data-stu-id="e564e-105">DXCore enables the exposure of new device types to user mode, such as MCDM (Microsoft Compute Driver Model), for use with [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md), and [Windows Machine Learning](/windows/ai/windows-ml/).</span></span> <span data-ttu-id="e564e-106">Дкскоре, в отличие от DXGI, не предоставляет никаких сведений о технологиях и свойствах, связанных с отображением.</span><span class="sxs-lookup"><span data-stu-id="e564e-106">DXCore, unlike DXGI, does not provide any information about display-related technology or properties</span></span>

<span data-ttu-id="e564e-107">В следующих нескольких разделах мы рассмотрим основные возможности Дкскоре с примерами кода (написанными на [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span><span class="sxs-lookup"><span data-stu-id="e564e-107">In the next few sections, we'll take a look at the main features of DXCore with some code examples (written in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span></span> <span data-ttu-id="e564e-108">Приведенные ниже примеры кода извлекаются из полного листинга исходного кода, который можно найти в разделе [минимальное приложение дкскоре](dxcore-source-code.md).</span><span class="sxs-lookup"><span data-stu-id="e564e-108">The code examples shown below are extracted from the full source code listing that you can find in the topic [Minimal DXCore application](dxcore-source-code.md).</span></span>

## <a name="create-an-adapter-factory"></a><span data-ttu-id="e564e-109">Создание фабрики адаптеров</span><span class="sxs-lookup"><span data-stu-id="e564e-109">Create an adapter factory</span></span>

<span data-ttu-id="e564e-110">Чтобы начать перечисление адаптеров Дкскоре, создайте объект фабрики адаптеров, который представлен интерфейсом [**идкскореадаптерфактори**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="e564e-110">You begin DXCore adapter enumeration by creating an adapter factory object, which is represented by the [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span> <span data-ttu-id="e564e-111">Чтобы создать фабрику, включите `dxcore.h` файл заголовка и вызовите функцию Free [**дкскорекреатеадаптерфактори**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="e564e-111">To create a factory, include the `dxcore.h` header file, and call the [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free function.</span></span>

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a><span data-ttu-id="e564e-112">Получение списка адаптеров</span><span class="sxs-lookup"><span data-stu-id="e564e-112">Retrieve an adapter list</span></span>

<span data-ttu-id="e564e-113">В отличие от DXGI, вновь созданная Фабрика адаптеров Дкскоре не создает моментальный снимок состояния адаптера системы автоматически.</span><span class="sxs-lookup"><span data-stu-id="e564e-113">Unlike with DXGI, a newly-created DXCore adapter factory doesn't automatically create a snapshot of the adapter state of the system.</span></span> <span data-ttu-id="e564e-114">Вместо этого Дкскоре создает этот моментальный снимок при явном извлечении объекта списка адаптеров, представленного интерфейсом [**идкскореадаптерлист**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .</span><span class="sxs-lookup"><span data-stu-id="e564e-114">Instead, DXCore creates that snapshot when you explicitly retrieve an adapter list object, which is represented by the [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface.</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a><span data-ttu-id="e564e-115">Выберите подходящий адаптер из списка</span><span class="sxs-lookup"><span data-stu-id="e564e-115">Select an appropriate adapter from the list</span></span>

<span data-ttu-id="e564e-116">В этом разделе показано, как с помощью объекта списка адаптеров можно найти первый аппаратный адаптер в списке.</span><span class="sxs-lookup"><span data-stu-id="e564e-116">This section demonstrates how, given an adapter list object, you could find the first hardware adapter in the list.</span></span>

<span data-ttu-id="e564e-117">Метод [**идкскореадаптерлист:: жетадаптеркаунт**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) сообщает число элементов в списке, а [**идкскореадаптерлист::**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) извлекает конкретный адаптер по индексу.</span><span class="sxs-lookup"><span data-stu-id="e564e-117">The [**IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) method tells you the number of elements in the list, and [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) retrieves a specific adapter by index.</span></span>

<span data-ttu-id="e564e-118">Затем можно запросить свойства этого адаптера, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e564e-118">You can then query the properties of that adapter, by following these steps.</span></span>

- <span data-ttu-id="e564e-119">Во-первых, чтобы убедиться, что для этого адаптера в этой версии операционной системы можно получить значение заданного свойства, вызовите [**идкскореадаптер:: испропертисуппортед**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span><span class="sxs-lookup"><span data-stu-id="e564e-119">First, to confirm that it's valid to retrieve the value of a given property for this adapter on this operating system version, you call [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span></span> <span data-ttu-id="e564e-120">Передайте значение перечисления [**дкскореадаптерпроперти**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) , чтобы указать, о каком свойстве вы запрашиваете.</span><span class="sxs-lookup"><span data-stu-id="e564e-120">Pass a value of the [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) enumeration to identify which property you're querying about.</span></span>
- <span data-ttu-id="e564e-121">При необходимости подтвердите размер значения свойства с помощью вызова [**идкскореадаптер:: жетпропертисизе**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span><span class="sxs-lookup"><span data-stu-id="e564e-121">Optionally confirm the size of the property value with a call to [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span></span> <span data-ttu-id="e564e-122">Для свойства, такого как **дкскореадаптерпроперти::-Hardware**, которое является простым логическим, этот шаг не требуется.</span><span class="sxs-lookup"><span data-stu-id="e564e-122">For a property such as **DXCoreAdapterProperty::IsHardware**, which is a simple Boolean, this step isn't necessary.</span></span>
- <span data-ttu-id="e564e-123">И, наконец, получите значение свойства, вызвав [**идкскореадаптер:: Property**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="e564e-123">And, finally, retrieve the property's value by calling [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

const uint32_t count{ d3D12CoreComputeAdapters->GetAdapterCount() };

for (uint32_t i = 0; i < count; ++i)
{
    winrt::com_ptr<IDXCoreAdapter> candidateAdapter;
    winrt::check_hresult(
        d3D12CoreComputeAdapters->GetAdapter(i, candidateAdapter.put()));

    bool isHardware{ false };
    winrt::check_hresult(candidateAdapter->GetProperty(
        DXCoreAdapterProperty::IsHardware,
        &isHardware));

    if (isHardware)
    {
        // Choose the first hardware adapter, and stop looping.
        preferredAdapter = candidateAdapter;
        break;
    }

    // Otherwise, ensure that (as long as there are *any* adapters) we'll
    // at least choose one.
    if (!preferredAdapter)
    {
        preferredAdapter = candidateAdapter;
    }
}
```

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a><span data-ttu-id="e564e-124">Выбор предпочтительного адаптера путем сортировки списка адаптеров</span><span class="sxs-lookup"><span data-stu-id="e564e-124">Select the preferred adapter by sorting an adapter list</span></span>

<span data-ttu-id="e564e-125">Список адаптеров Дкскоре можно отсортировать, вызвав метод [идкскореадаптерлист:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .</span><span class="sxs-lookup"><span data-stu-id="e564e-125">You can sort a DXCore adapter list by calling the [IDXCoreAdapterList::Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) method.</span></span>

<span data-ttu-id="e564e-126">Перечисление [дкскореадаптерпреференце](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) определяет значения, представляющие критерии сортировки.</span><span class="sxs-lookup"><span data-stu-id="e564e-126">The [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) enumeration defines values that representing sort criteria.</span></span> <span data-ttu-id="e564e-127">Передайте массив этих значений для **сортировки**, а затем прочтите первый адаптер в итоговом отсортированном списке.</span><span class="sxs-lookup"><span data-stu-id="e564e-127">Pass an array of those values to **Sort**, and then read off the first adapter in the resulting sorted list.</span></span>

<span data-ttu-id="e564e-128">Чтобы определить, должен ли тип сортировки быть понятен по **сортировке**, сначала вызовите [Идкскореадаптерлист:: исадаптерпреференцесуппортед](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="e564e-128">To determine whether a sort type is going to be understood by **Sort**, first call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> TryFindHardwareHighPerformanceGraphicsAdapter()
{
    // You begin DXCore adapter enumeration by creating an adapter factory.
    winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
    winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));

    // From the factory, retrieve a list of all the Direct3D 12 Graphics adapters.
    winrt::com_ptr<IDXCoreAdapterList> d3D12GraphicsAdapters;
    GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS };
    winrt::check_hresult(
        adapterFactory->CreateAdapterList(_countof(attributes),
            attributes,
            d3D12GraphicsAdapters.put()));

    DXCoreAdapterPreference sortPreferences[]{
        DXCoreAdapterPreference::Hardware, DXCoreAdapterPreference::HighPerformance };

    // Ask the OS to sort for the highest performance hardware adapter.
    winrt::check_hresult(d3D12GraphicsAdapters->Sort(_countof(sortPreferences), sortPreferences));

    winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

    if (d3D12GraphicsAdapters->GetAdapterCount() > 0)
    {
        winrt::check_hresult(d3D12GraphicsAdapters->GetAdapter(0, preferredAdapter.put()));
    }

    return preferredAdapter;
}
```

## <a name="query-and-set-adapter-state-properties"></a><span data-ttu-id="e564e-129">Запрос и задание состояния адаптера (свойства)</span><span class="sxs-lookup"><span data-stu-id="e564e-129">Query and set adapter state (properties)</span></span>

<span data-ttu-id="e564e-130">Вы можете получить и установить состояние указанного элемента состояния адаптера, вызвав методы [**идкскореадаптер:: куеристате**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) и [**Идкскореадаптер:: setState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="e564e-130">You can retrieve and set the state of a specified state item of an adapter by calling the [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) and [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) methods.</span></span>

```cppwinrt
void SetDesiredMemoryReservation(winrt::com_ptr<IDXCoreAdapter> const& adapter, uint64_t reservation)
{
    DXCoreAdapterMemoryBudgetNodeSegmentGroup nodeSegmentGroup{};
    nodeSegmentGroup.nodeIndex = 0;
    nodeSegmentGroup.segmentGroup = DXCoreSegmentGroup::Local;

    DXCoreAdapterMemoryBudget memoryBudget{};
    winrt::check_hresult(adapter->QueryState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &memoryBudget));

    // Clamp the reservation to what's available.
    reservation = std::min<uint64_t>(reservation, memoryBudget.availableForReservation);

    winrt::check_hresult(adapter->SetState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &reservation));
}
```

<span data-ttu-id="e564e-131">На практике перед вызовом **куеристате** и **SetState** необходимо вызвать [искуеристатесуппортед](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).</span><span class="sxs-lookup"><span data-stu-id="e564e-131">In practice, before calling **QueryState** and **SetState**, you should call [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="adapter-list-freshness"></a><span data-ttu-id="e564e-132">Актуальность списка адаптеров</span><span class="sxs-lookup"><span data-stu-id="e564e-132">Adapter list freshness</span></span>

<span data-ttu-id="e564e-133">Если список адаптеров становится устаревшим из-за изменения системных условий, он будет помечен как таковой.</span><span class="sxs-lookup"><span data-stu-id="e564e-133">Should an adapter list become stale due to changing system conditions, it will be marked as such.</span></span> <span data-ttu-id="e564e-134">Чтобы определить актуальность списка адаптеров, можно опросить метод [**идкскореадаптерлист:: устареть**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .</span><span class="sxs-lookup"><span data-stu-id="e564e-134">You can determine an adapter list's freshness by polling its [**IDXCoreAdapterList::IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) method.</span></span>

<span data-ttu-id="e564e-135">Тем не менее, вы можете подписываться на уведомления о таких условиях, как устаревания.</span><span class="sxs-lookup"><span data-stu-id="e564e-135">More conveniently, though, you can subscribe to notifications for conditions such as staleness.</span></span> <span data-ttu-id="e564e-136">Для этого передайте [**дкскоренотификатионтипе:: адаптерлистстале**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) в [**Идкскореадаптерфактори:: регистеревентнотификатион**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)и безопасно сохраните возвращенный файл cookie для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="e564e-136">To do that, pass [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) to [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), and safely store the returned cookie for use later.</span></span>

```cppwinrt
uint32_t m_eventCookie = 0;
...
winrt::check_hresult(factory->RegisterEventNotification(
    m_adapters.get(),
    DXCoreNotificationType::AdapterListStale,
    OnAdapterListStale,
    this,
    &m_eventCookie));
...
static void WINAPI OnAdapterListStale(
    DXCoreNotificationType notificationType,
    IUnknown* staleObject,
    void* context)
{
    ...
}
```

<span data-ttu-id="e564e-137">Затем можно создать новый, текущий объект списка адаптеров из уже имеющегося объекта фабрики.</span><span class="sxs-lookup"><span data-stu-id="e564e-137">You can then generate a new, current, adapter list object from the factory object that you already have.</span></span> <span data-ttu-id="e564e-138">Обработка этих условий крайне важна для возможности беспрепятственно реагировать на такие события, как получение и удаление адаптера (графический процессор или специализированный адаптер вычислений), а также для надлежащего сдвига рабочих нагрузок в ответе.</span><span class="sxs-lookup"><span data-stu-id="e564e-138">Handling these conditions is critical to your ability to seamlessly respond to events such as adapter arrival and removal (whether that be a GPU, or a specialized compute adapter), and to appropriately shift workloads in response.</span></span>

<span data-ttu-id="e564e-139">Перед уничтожением объекта списка адаптеров необходимо использовать значение cookie для отмены регистрации этого объекта из уведомлений путем вызова [идкскореадаптерфактори:: унрегистеревентнотификатион](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span><span class="sxs-lookup"><span data-stu-id="e564e-139">Before you destroy the adapter list object, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span></span> <span data-ttu-id="e564e-140">Если вы не отмените регистрацию, при обнаружении ситуации будет создано неустранимое исключение.</span><span class="sxs-lookup"><span data-stu-id="e564e-140">If you don't unregister, then a fatal exception is raised when the situation is detected.</span></span>

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a><span data-ttu-id="e564e-141">Отображение сведений</span><span class="sxs-lookup"><span data-stu-id="e564e-141">Display information</span></span>

> [!NOTE]
> <span data-ttu-id="e564e-142">Дкскоре сам по себе не предоставляет никаких отображаемых сведений.</span><span class="sxs-lookup"><span data-stu-id="e564e-142">DXCore doesn't itself provide any display information.</span></span> <span data-ttu-id="e564e-143">При необходимости для получения этих сведений следует использовать класс среда выполнения Windows [**дисплаймонитор**](/uwp/api/windows.devices.display.displaymonitor) .</span><span class="sxs-lookup"><span data-stu-id="e564e-143">Where necessary, you should use the Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) class to retrieve this information.</span></span> <span data-ttu-id="e564e-144">[**LUID**](/windows/win32/api/winnt/ns-winnt-luid) адаптера предоставляет общий идентификатор, с помощью которого можно сопоставлять адаптер дкскоре с информацией [**дисплаймонитор. дисплайадаптерид**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) .</span><span class="sxs-lookup"><span data-stu-id="e564e-144">An adapter's [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) provides a common identifier that you can use to map a DXCore adapter to [**DisplayMonitor.DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) information.</span></span> <span data-ttu-id="e564e-145">Чтобы получить LUID адаптера, передайте [**дкскореадаптерпроперти:: инстанцелуид**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) в метод [**Идкскореадаптер:: Property**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="e564e-145">To obtain an adapter's LUID, pass [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) to the [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="e564e-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e564e-146">See also</span></span>

* [<span data-ttu-id="e564e-147">Приложение DXCore с минимальным набором функций</span><span class="sxs-lookup"><span data-stu-id="e564e-147">Minimal DXCore application</span></span>](dxcore-source-code.md)
* [<span data-ttu-id="e564e-148">Справочник по Дкскоре</span><span class="sxs-lookup"><span data-stu-id="e564e-148">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="e564e-149">Графика Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="e564e-149">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)