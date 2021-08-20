---
description: Эта статья содержит рекомендации по оценке вектора движения с помощью API-интерфейсов видео Direct3D 12.
ms.assetid: ''
title: Оценка движения видео Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 0a49f7d3ec5e68ee6151b706be65866f1e156d6f876909c99b485356fb4df21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064125"
---
# <a name="direct3d-video-motion-estimation"></a>Оценка движения видео Direct3D

Эта статья содержит рекомендации по оценке вектора движения с помощью API-интерфейсов видео Direct3D 12. эта функция появилась в Windows 10 версии 2004 (10,0; Сборка 19041). Оценка движения — это процесс определения векторов движения, описывающих преобразование из одного 2D-изображения в другое. Оценка движения является важнейшей частью кодирования видео и может использоваться в алгоритмах преобразования частоты кадров. 

Хотя оценка движения может быть реализована с помощью шейдеров, целью функции оценки движения D3D12 является предоставление ускоренной функции для поиска движения с целью разгрузки этой части работы из трехмерной графики. Часто это происходит в форме предоставления средства оценки движения кодировщика видео GPU. Целью оценки движения D3D12 является оптический поток, но следует отметить, что средства оценки движения кодировщика могут быть оптимизированы для улучшения сжатия.


## <a name="checking-for-support"></a>Проверка поддержки

Определите поддержку для всех функций D3D Video, вызвав [ID3D12VideoDevice:: чеккфеатуресуппорт](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) и передав значение из перечисления [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) , чтобы указать компонент, для которого запрашивается поддержка. Чтобы запросить поддерживаемый размер блока и разрешения для заданного формата, используйте значение **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** и укажите структуру [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) для *пфеатуресуппортдата* , как показано в примере ниже. В текущем выпуске поддерживается только **DXGI_FORMAT_NV12** , поэтому для содержимого в других форматах может потребоваться преобразование цвета и downsampled для использования оценки движения.

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a>Объект контекста средства оценки движения

Объект [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) поддерживает контекст для операций оценки движения видео. Создайте новый экземпляр этого интерфейса, вызвав [ID3D12VideoDevice1:: креатевидеомотионестиматор](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).

Выбранный размер блока, точность и поддерживаемый диапазон размеров зависят от значений, поддерживаемых оборудованием, возвращенным при проверке компонентов **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** . Можно выбрать меньший диапазон размеров, чем поддерживается драйвером. Диапазон размера информирует внутренние размеры выделения.

```c++
D3D12_VIDEO_MOTION_ESTIMATOR_DESC motionEstimatorDesc = { 
    0, //NodeIndex
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionEstimator> spVideoMotionEstimator;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionEstimator(
    &motionEstimatorDesc, 
    nullptr,
    IID_PPV_ARGS(&spVideoMotionEstimator)));
```



## <a name="storage-of-motion-vectors"></a>служба хранилища векторов движения

[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) сохраняет векторы движения. Этот интерфейс используется структурой [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) , возвращаемой из [ID3D12VideoEncodeCommandList:: естиматемотион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion). Разрешаемая двухмерная текстура вывода — это [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) текстура, где R содержит горизонтальный компонент, а G содержит вертикальный компонент вектора движения. Эта текстура имеет размер, чтобы вместить одну пару компонентов на блок. Вызовите метод [ID3D12VideoEncodeCommandList:: ресолвемотионвекторхеап](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) , чтобы переводит выходные данные вектора движения **естиматемотион** из аппаратно зависимых форматов в единообразный формат, определенный API-интерфейсом оценки движения видео.

```c++
D3D12_VIDEO_MOTION_VECTOR_HEAP_DESC MotionVectorHeapDesc = { 
    0, // NodeIndex 
    DXGI_FORMAT_NV12, 
    D3D12_VIDEO_MOTION_ESTIMATOR_SEARCH_BLOCK_SIZE_16X16,
    D3D12_VIDEO_MOTION_ESTIMATOR_VECTOR_PRECISION_QUARTER_PEL, 
    {1920, 1080, 1280, 720} // D3D12_VIDEO_SIZE_RANGE
    }; 

CComPtr<ID3D12VideoMotionVectorHeap> spVideoMotionVectorHeap;
VERIFY_SUCCEEDED(spVideoDevice->CreateVideoMotionVectorHeap(
    &MotionVectorHeapDesc, 
    nullptr, 
    IID_PPV_ARGS(&spVideoMotionVectorHeap)));
```

```cpp
    CD3DX12_RESOURCE_DESC::Tex2D(
        DXGI_FORMAT_R16G16_SINT, 
        Align(1920, 16) / 16, // This example uses a 16x16 block size. Pixel width and height
        Align(1080, 16) / 16, // are adjusted to store the vectors for those blocks.
        1, // ArraySize
        1  // MipLevels
        );

    ATL::CComPtr< ID3D12Resource > spResolvedMotionVectors;
    VERIFY_SUCCEEDED(pDevice->CreateCommittedResource(
        &Properties,
        D3D12_HEAP_FLAG_NONE,
        &resolvedMotionVectorDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        IID_PPV_ARGS(&spResolvedMotionVectors)));
```

 **ID3D12VideoMotionVectorHeap** также используется для передачи векторов подсказок в структуре [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .



## <a name="estimate-motion-in-a-command-list"></a>Оценка движения в списке команд

Вызовите [естиматемотион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) из [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) , чтобы вызвать операцию оценки движения.

Приведенный ниже пример выполняет поиск движения и разрешает векторы движения к двухмерной текстуре с [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).  Ресурсы D3D12, используемые в качестве входных данных для **естиматемотион** , должны находиться в [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) состоянии, а ресурс, записанный **ресолвемотионвекторхеап** , должен находиться в состоянии [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .

```cpp
const D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT outputArgs = {spVideoMotionVectorHeap};

const D3D12_VIDEO_MOTION_ESTIMATOR_INPUT inputArgs = {
    spCurrentResource,
    0,
    spReferenceResource,
    0,
    nullptr // pHintMotionVectorHeap
    };

spCommandList->EstimateMotion(spVideoMotionEstimator, &outputArgs, &inputArgs);

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_OUTPUT outputArgs = { 
    spResolvedMotionVectors,
    {}};

const D3D12_RESOLVE_VIDEO_MOTION_VECTOR_HEAP_INPUT inputArgs = {
    spVideoMotionVectorHeap,
    1920,
    1080
    };

spCommandList->ResolveMotionVectorHeap(&outputArgs, &inputArgs);
        
VERIFY(spCommandList->Close());

// Execute Commandlist.
ID3D12CommandList *ppCommandLists[1] = { spCommandList.p };
spCommandQueue->ExecuteCommandLists(1, ppCommandLists);
```


## <a name="protected-resources"></a>Защищенные ресурсы

Оценка вектора движения Direct3D 12 поддерживает чтение и запись в аппаратно защищенные ресурсы DRM, если поддерживается драйвером. Если входные ресурсы защищены аппаратным обеспечением DRM, то выходные данные также являются защищенным аппаратным ресурсом DRM. Методы, используемые для создания объекта контекста оценки движения и кучи векторов движения,  [ID3D12VideoDevice1:: креатевидеомотионестиматор](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) и [ID3D12VideoDevice1:: креатевидеомотионвекторхеап](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), оба принимают [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) , который используется для управления доступом к защищенным ресурсам. 

Используйте [ID3D12VideoMotionEstimator:: жетпротектедресаурцесессион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) и [ID3D12VideoMotionVectorHeap:: жетпротектедресаурцесессион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) для получения объектов **ID3D12ProtectedResourceSession** , предоставленных при создании объектов.



## <a name="related-topics"></a>Связанные темы

* [API-интерфейсы видео Direct3D 12](direct3d-12-video-apis.md)
* [Media Foundationое программное руководством](media-foundation-programming-guide.md)
