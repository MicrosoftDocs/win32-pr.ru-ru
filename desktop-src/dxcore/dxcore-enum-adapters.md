---
title: Перечисление адаптеров с использованием DXCore
description: Рассмотрим основные функции Дкскоре с примерами кода, а также полный листинг исходного кода для минимального приложения Дкскоре.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: fc2120c85b48b89478d1a10c8cf853c947e6553d
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812356"
---
# <a name="using-dxcore-to-enumerate-adapters"></a>Перечисление адаптеров с использованием DXCore

Дкскоре — это API перечисления адаптеров для устройств DirectX, поэтому некоторые его средства перекрываются с устройствами [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).

дкскоре позволяет раскрытие новых типов устройств в пользовательском режиме, например мкдм (модель драйвера вычислений майкрософт), для использования с [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [директмл](/windows/ai/directml/dml)и [Windows Машинное обучение](/windows/ai/windows-ml/). Дкскоре, в отличие от DXGI, не предоставляет никаких сведений о технологиях и свойствах, связанных с отображением.

В следующих нескольких разделах мы рассмотрим основные возможности Дкскоре с примерами кода (написанными на [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)). Приведенные ниже примеры кода извлекаются из полного листинга исходного кода, который можно найти в разделе [минимальное приложение дкскоре](dxcore-source-code.md).

## <a name="create-an-adapter-factory"></a>Создание фабрики адаптеров

Чтобы начать перечисление адаптеров Дкскоре, создайте объект фабрики адаптеров, который представлен интерфейсом [**идкскореадаптерфактори**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) . Чтобы создать фабрику, включите `dxcore.h` файл заголовка и вызовите функцию Free [**дкскорекреатеадаптерфактори**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Получение списка адаптеров

В отличие от DXGI, вновь созданная Фабрика адаптеров Дкскоре не создает моментальный снимок состояния адаптера системы автоматически. Вместо этого Дкскоре создает этот моментальный снимок при явном извлечении объекта списка адаптеров, представленного интерфейсом [**идкскореадаптерлист**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Выберите подходящий адаптер из списка

В этом разделе показано, как с помощью объекта списка адаптеров можно найти первый аппаратный адаптер в списке.

Метод [**идкскореадаптерлист:: жетадаптеркаунт**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) сообщает число элементов в списке, а [**идкскореадаптерлист::**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) извлекает конкретный адаптер по индексу.

Затем можно запросить свойства этого адаптера, выполнив следующие действия.

- Во-первых, чтобы убедиться, что для этого адаптера в этой версии операционной системы можно получить значение заданного свойства, вызовите [**идкскореадаптер:: испропертисуппортед**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md). Передайте значение перечисления [**дкскореадаптерпроперти**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) , чтобы указать, о каком свойстве вы запрашиваете.
- При необходимости подтвердите размер значения свойства с помощью вызова [**идкскореадаптер:: жетпропертисизе**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md). Для свойства, такого как **дкскореадаптерпроперти::-Hardware**, которое является простым логическим, этот шаг не требуется.
- И, наконец, получите значение свойства, вызвав [**идкскореадаптер:: Property**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Выбор предпочтительного адаптера путем сортировки списка адаптеров

Список адаптеров Дкскоре можно отсортировать, вызвав метод [идкскореадаптерлист:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .

Перечисление [дкскореадаптерпреференце](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) определяет значения, представляющие критерии сортировки. Передайте массив этих значений для **сортировки**, а затем прочтите первый адаптер в итоговом отсортированном списке.

Чтобы определить, должен ли тип сортировки быть понятен по **сортировке**, сначала вызовите [Идкскореадаптерлист:: исадаптерпреференцесуппортед](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

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

## <a name="query-and-set-adapter-state-properties"></a>Запрос и задание состояния адаптера (свойства)

Вы можете получить и установить состояние указанного элемента состояния адаптера, вызвав методы [**идкскореадаптер:: куеристате**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) и [**Идкскореадаптер:: setState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .

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

На практике перед вызовом **куеристате** и **SetState** необходимо вызвать [искуеристатесуппортед](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).

## <a name="adapter-list-freshness"></a>Актуальность списка адаптеров

Если список адаптеров становится устаревшим из-за изменения системных условий, он будет помечен как таковой. Чтобы определить актуальность списка адаптеров, можно опросить метод [**идкскореадаптерлист:: устареть**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .

Тем не менее, вы можете подписываться на уведомления о таких условиях, как устаревания. Для этого передайте [**дкскоренотификатионтипе:: адаптерлистстале**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) в [**Идкскореадаптерфактори:: регистеревентнотификатион**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)и безопасно сохраните возвращенный файл cookie для последующего использования.

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

Затем можно создать новый, текущий объект списка адаптеров из уже имеющегося объекта фабрики. Обработка этих условий крайне важна для возможности беспрепятственно реагировать на такие события, как получение и удаление адаптера (графический процессор или специализированный адаптер вычислений), а также для надлежащего сдвига рабочих нагрузок в ответе.

Перед уничтожением объекта списка адаптеров необходимо использовать значение cookie для отмены регистрации этого объекта из уведомлений путем вызова [идкскореадаптерфактори:: унрегистеревентнотификатион](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Если вы не отмените регистрацию, при обнаружении ситуации будет создано неустранимое исключение.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Отображение сведений

> [!NOTE]
> Дкскоре сам по себе не предоставляет никаких отображаемых сведений. при необходимости для получения этих сведений следует использовать класс среда выполнения Windows [**дисплаймонитор**](/uwp/api/windows.devices.display.displaymonitor) . [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) адаптера предоставляет общий идентификатор, с помощью которого можно сопоставлять адаптер дкскоре с информацией [**дисплаймонитор. дисплайадаптерид**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) . Чтобы получить LUID адаптера, передайте [**дкскореадаптерпроперти:: инстанцелуид**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) в метод [**Идкскореадаптер:: Property**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .

## <a name="see-also"></a>См. также

* [Приложение DXCore с минимальным набором функций](dxcore-source-code.md)
* [Справочник по Дкскоре](./dxcore-reference.md)
* [Графика Direct3D 12](../direct3d12/direct3d-12-graphics.md)