---
title: Новые возможности Direct3D 12
description: В этом разделе описывается наиболее значительная новая документация по Direct3D 12, доступная для различных выпусков.
ms.assetid: 38F41E05-FECB-41DE-8D30-09733FBEAC48
ms.localizationpriority: high
ms.topic: article
ms.date: 12/05/2019
ms.openlocfilehash: ec3ecc9e68fc4711def2c364793eca32804d8d04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548917"
---
# <a name="whats-new-in-direct3d-12"></a>Новые возможности Direct3D 12

В этом разделе описывается наиболее значительная новая документация по Direct3D 12, доступная для различных выпусков.

Сведения о получении и установке Direct3D см. в разделе [Установка среды программирования Direct3D 12](./directx-12-programming-environment-set-up.md).

## <a name="direct3d-12-on-windows-7"></a>Direct3D 12 в Windows 7

- Теперь разработчики могут использовать [Direct3D 12 в Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/) .

## <a name="windows-10-may-2019-update"></a>Обновления Windows 10 за май 2019 г.

Эти функции и API были добавлены или обновлены для Windows 10 версии 1903 (10,0; Сборка 18362) &mdash; , также известная как Windows 10, может обновить 2019.

- [Заливка переменной скорости (ВРС)](./vrs.md). Позволяет выделять показатели производительности и мощности отрисовки по тарифам, которые зависят от готового образа.
- [Модель шейдера HLSL 6,4](../direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12.md). Описывает встроенные функции машинного обучения, добавленные в модель шейдера HLSL 6,4.
- Перечисление [**D3D12_DRED_VERSION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_dred_version) . Определяет константы, указывающие версию удаленных расширенных данных устройства (НАПРАВЛЯТЬ).
- Структура [**D3D12_FEATURE_DATA_D3D12_OPTIONS6**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) . Указывает уровень поддержки, предоставляемый адаптером для метакоммандс.
- Структура [**D3D12_FEATURE_DATA_QUERY_META_COMMAND**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_query_meta_command) . Указывает уровень поддержки, предоставляемый адаптером для метакоммандс.
- Перечисление [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) . Определяет константы, определяющие уровень скорости заливки (для заливки переменной скорости или ВРС).
- Интерфейс [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) и его методы. Используется для настройки режима оптимизации фоновой обработки драйвера. Также см. раздел [Оптимизация фонового шейдера](https://devblogs.microsoft.com/directx/background-shader-optimizations/).
- Интерфейс [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) и его методы. Предоставляет доступ среды выполнения к удаленным устройствам данных расширенных данных (НАПРАВЛЯТЬ).
- Интерфейс [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) и его методы. Управляет параметрами устройства, которые удалили Расширенные данные (НАПРАВЛЯТЬ).
- Интерфейс [**D3D12GraphicsCommandList5**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist5) и его методы. Поддержка заливки переменной скорости (ВРС).

Перечисление [**D3D_SHADER_MODEL**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) Обновлено с добавлением **D3D_SHADER_MODEL_6_5** константы (функция экспериментального уровня).

Перечисление [**D3D12_COMMAND_LIST_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) Обновлено добавлением **D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE** константы.

Перечисление [**D3D12_FEATURE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) Обновлено добавлением **D3D12_FEATURE_D3D12_OPTIONS6** и **D3D12_FEATURE_QUERY_META_COMMAND** констант.

Перечисление [**D3D12_RESOURCE_STATES**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) Обновлено добавлением **D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE** константы.

## <a name="windows-10-version-1809"></a>Windows 10, версия 1809

Эти функции и API были добавлены или обновлены для Windows 10 версии 1809 (10,0; Сборка 17763) &mdash; также называется обновлением Windows 10 октября 2018.

- [РайтраЦинг Direct3D 12](./direct3d-12-raytracing.md)
- [Проходы рендеринга Direct3D 12](./direct3d-12-render-passes.md)

## <a name="windows-10-version-1709"></a>Windows 10 версии 1709

Эти интерфейсы были добавлены в документацию по Direct3D для Windows 10 версии 1709.

-   [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) расширяет функциональные возможности создания ограждений, поддерживая извлечение флагов, переданных для создания ограждения.
-   [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) расширяет список доступных графических команд путем поддержки записи непосредственных значений непосредственно в буфер.
-   [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) расширяет функциональные возможности виртуального адаптера путем создания специальных диагностических куч в системной памяти, которые сохраняются даже в случае сбоя GPU или устройства.

Перечисление [**\_ \_ модели**](/windows/win32/api/d3d12/ne-d3d12-d3d_shader_model) шейдера D3D имеет новое **значение \_ модели шейдера D3D \_ \_ 6 \_ 1** , описывающее модель шейдера 6,1.

В перечислении [**\_ компонентов D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_feature) также имеется **Новая \_ функция D3D12 \_ D3D12 \_ OPTIONS3** и **D3D12 \_ функции \_ существующие \_ кучи** . Как предполагает имена, эти значения позволяют проверить наличие дополнительных параметров Direct3D12, а также проверку поддержки существующих куч.

## <a name="windows-10-version-1703"></a>Windows 10 версии 1703

Эти разделы добавлены в документацию по Direct3D для Windows 10, версия 1703.

-   Структура [**\_ \_ \_ потока \_ состояния конвейера**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) [**ID3D12Device2:: креатепипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) и D3D12 представляет новый и более надежный способ создания псос и объединяет реализовывать для создания графики и конвейеров вычислений.
-   Метод [**ID3D12Device1:: CreatePipelineLibrary1**](https://www.bing.com/search?q=**ID3D12Device1::CreatePipelineLibrary1**) расширяет интерфейс библиотеки конвейера, чтобы принять псос, созданный с помощью новой структуры Streaming, унифицированной [**\_ \_ \_ потоковой \_ передачи состояния конвейера D3D12**](/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc) .
-   Функция [**D3D12EnableExperimentalFeatures**](/windows/win32/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) позволяет разработчикам экспериментировать с определенными функциями в области разработки, используя компьютер в режиме разработчика.
-   Существует пять новых интерфейсов (см. [иерархию интерфейсов](interface-hierarchy.md)):
    -   [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1)
    -   [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1)
    -   [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2)
    -   [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2)
    -   [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools)
-   См. [Обзор модели шейдера HLSL 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), в которой описаны встроенные операции для многопотоковых шейдеров пикселей и вычислений.
-   Использование [**ID3D12Device:: сетстаблеповерстате**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) изменилось.
-   Некоторые новые возможности Direct3D 11 описаны в статье [функции direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   [**Атомиккопибуфферуинт**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint) и [**AtomicCopyBufferUINT64**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64) позволяют использовать **отложенную кратковременную блокировку** для сокращения задержки первиевед.
-   [**ID3D12Device2:: креатепипелинестате**](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate) и [**омсетдепсбаундс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-omsetdepthbounds) позволяют выполнять **тестирование с** ограничениями глубины на поддерживаемом оборудовании.
-   [**Ресолвесубресаурцерегион**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion) включает **частичное разрешение** вспомогательных ресурсов для оптимизации производительности.
-   [**Сетсамплепоситионс**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) включает **примеры программных позиций** на поддерживаемом оборудовании.

## <a name="november-2016-documentation-update"></a>Обновление документации по ноябрь 2016

-   Редакция примечаний для [**ID3D12GraphicsCommandList::D искардресаурце**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource).
-   Уточнение "Decay" состояния (см. статью [использование барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)).
-   Файл заголовка D3dx12. h, который называется в [вспомогательных структурах и функциях для D3D12](helper-structures-and-functions-for-d3d12.md), можно скачать непосредственно из [вспомогательной библиотеки D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).

## <a name="august-2016-documentation-update-2"></a>Обновление 2 для документации 2016 августа

-   Новый раздел руководств, посвященный [уровню отладки D3D12](understanding-the-d3d12-debug-layer.md).

    Ниже описаны три новых интерфейса слоя отладки (в режиме предварительного просмотра): [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1), [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1), [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1).

## <a name="august-2016-documentation-update-1"></a>Обновление 1 для документации 2016 августа

-   Редакция [использования барьеров ресурсов для синхронизации состояний ресурсов в Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).
-   Редакция [доступа к ресурсам с несколькими очередями](./user-mode-heap-synchronization.md#multi-queue-resource-access).

## <a name="windows-10-version-1607"></a>Windows 10, версия 1607

Эти разделы добавлены в документацию по Direct3D для Windows 10, версия 1607.

-   [Корневая сигнатура версии 1,1](root-signature-version-1-1.md) : Общие сведения об обновленных корневых сигнатурах, что позволяет приложениям указывать статические или временные дескрипторы и данные, что может помочь в оптимизации графических драйверов.
-   Метод [**ID3D12Device1:: креатепипелинелибрари**](/windows/win32/api/d3d12/nf-d3d12-id3d12device1-createpipelinelibrary) описывает преимущества создания библиотеки конвейера.
-   Существует три новых интерфейса (см. [иерархию интерфейсов](interface-hierarchy.md)):
    -   [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary)
    -   [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1)
    -   [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer)
-   См. [Обзор модели шейдера HLSL 6,0](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md), в которой описаны встроенные операции для многопотоковых шейдеров пикселей и вычислений.
-   Использование [**ID3D12Device:: сетстаблеповерстате**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate) изменилось.
-   Некоторые новые возможности Direct3D 11 описаны в статье [функции direct3d 11,4](../direct3d11/direct3d-11-4-features.md).
-   Обновлен диапазон поддерживаемых библиотек для Direct3D 12, см. раздел **Поддерживаемые средства и библиотеки** [программы установки среды программирования Direct3D 12](directx-12-programming-environment-set-up.md).
-   [Использование DirectX с дисплеями с широким динамическим диапазоном и расширенным управлением цветами](../direct3darticles/high-dynamic-range.md)
-   [Отображение частоты обновления переменных](../direct3ddxgi/variable-refresh-rate-displays.md)
-   [Усовершенствования DXGI 1,5](../direct3ddxgi/dxgi-1-5-improvements.md)

## <a name="related-topics"></a>Связанные темы

* [Руководство по программированию для Direct3D 12](directx-12-programming-guide.md)