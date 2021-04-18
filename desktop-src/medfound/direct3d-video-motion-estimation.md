---
description: Эта статья содержит рекомендации по оценке вектора движения с помощью API-интерфейсов видео Direct3D 12.
ms.assetid: ''
title: Оценка движения видео Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 7fdb6146e1bb77c673eb89d944bcf42a8babce49
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "105719873"
---
# <a name="direct3d-video-motion-estimation"></a><span data-ttu-id="0f760-103">Оценка движения видео Direct3D</span><span class="sxs-lookup"><span data-stu-id="0f760-103">Direct3D video motion estimation</span></span>

<span data-ttu-id="0f760-104">Эта статья содержит рекомендации по оценке вектора движения с помощью API-интерфейсов видео Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0f760-104">This article contains guidance for motion vector estimation with Direct3D 12 video APIs.</span></span> <span data-ttu-id="0f760-105">Эта функция появилась в Windows 10 версии 2004 (10,0; Сборка 19041).</span><span class="sxs-lookup"><span data-stu-id="0f760-105">This feature was introduced in Windows 10, version 2004 (10.0; Build 19041).</span></span> <span data-ttu-id="0f760-106">Оценка движения — это процесс определения векторов движения, описывающих преобразование из одного 2D-изображения в другое.</span><span class="sxs-lookup"><span data-stu-id="0f760-106">Motion estimation is the process of determining motion vectors that describe the transformation from one 2D image to another.</span></span> <span data-ttu-id="0f760-107">Оценка движения является важнейшей частью кодирования видео и может использоваться в алгоритмах преобразования частоты кадров.</span><span class="sxs-lookup"><span data-stu-id="0f760-107">Motion estimation is an essential part of video encoding and can be used in frame rate conversion algorithms.</span></span> 

<span data-ttu-id="0f760-108">Хотя оценка движения может быть реализована с помощью шейдеров, целью функции оценки движения D3D12 является предоставление ускоренной функции для поиска движения с целью разгрузки этой части работы из трехмерной графики.</span><span class="sxs-lookup"><span data-stu-id="0f760-108">While motion estimation can be implemented with shaders, the purpose of the D3D12 Motion Estimation feature is to expose fixed function acceleration for motion searching to offload this part of the work from 3D.</span></span> <span data-ttu-id="0f760-109">Часто это происходит в форме предоставления средства оценки движения кодировщика видео GPU.</span><span class="sxs-lookup"><span data-stu-id="0f760-109">Often this comes in the form of exposing the GPU video encoder motion estimator.</span></span> <span data-ttu-id="0f760-110">Целью оценки движения D3D12 является оптический поток, но следует отметить, что средства оценки движения кодировщика могут быть оптимизированы для улучшения сжатия.</span><span class="sxs-lookup"><span data-stu-id="0f760-110">The goal of D3D12 Motion estimation is optical flow, but it should be noted that encoder motion estimators may be optimized for improving compression.</span></span>


## <a name="checking-for-support"></a><span data-ttu-id="0f760-111">Проверка поддержки</span><span class="sxs-lookup"><span data-stu-id="0f760-111">Checking for Support</span></span>

<span data-ttu-id="0f760-112">Определите поддержку для всех функций D3D Video, вызвав [ID3D12VideoDevice:: чеккфеатуресуппорт](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) и передав значение из перечисления [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) , чтобы указать компонент, для которого запрашивается поддержка.</span><span class="sxs-lookup"><span data-stu-id="0f760-112">Determine support for all D3D video features by calling [ID3D12VideoDevice::CheckFeatureSupport](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) and passing in a value from the [D3D12_FEATURE_VIDEO](/windows/win32/api/d3d12video/ne-d3d12video-d3d12_feature_video) enumeration to specify the feature for which support is being queried.</span></span> <span data-ttu-id="0f760-113">Чтобы запросить поддерживаемый размер блока и разрешения для заданного формата, используйте значение **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** и укажите структуру [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) для *пфеатуресуппортдата* , как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="0f760-113">To query the supported block size and resolutions for a given format, use the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** value and supply a [D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_feature_data_video_motion_estimator) structure for the *pFeatureSupportData* as shown in the example below.</span></span> <span data-ttu-id="0f760-114">В текущем выпуске поддерживается только **DXGI_FORMAT_NV12** , поэтому для содержимого в других форматах может потребоваться преобразование цвета и downsampled для использования оценки движения.</span><span class="sxs-lookup"><span data-stu-id="0f760-114">In the current release, only **DXGI_FORMAT_NV12** is supported, so content in other formats may need to be color converted and downsampled to use motion estimation.</span></span>

```C++
D3D12_FEATURE_DATA_VIDEO_MOTION_ESTIMATOR MotionEstimatorSupport = {0u, DXGI_FORMAT_NV12};
VERIFY(spVideoDevice->CheckFeatureSupport(D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR, &MotionEstimatorSupport, sizeof(MotionEstimatorSupport)));
```

## <a name="the-motion-estimator-context-object"></a><span data-ttu-id="0f760-115">Объект контекста средства оценки движения</span><span class="sxs-lookup"><span data-stu-id="0f760-115">The motion estimator context object</span></span>

<span data-ttu-id="0f760-116">Объект [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) поддерживает контекст для операций оценки движения видео.</span><span class="sxs-lookup"><span data-stu-id="0f760-116">The [ID3D12VideoMotionEstimator](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionestimator) object maintains context for video motion estimation operations.</span></span> <span data-ttu-id="0f760-117">Создайте новый экземпляр этого интерфейса, вызвав [ID3D12VideoDevice1:: креатевидеомотионестиматор](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span><span class="sxs-lookup"><span data-stu-id="0f760-117">Create a new instance of this interface by calling [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator).</span></span>

<span data-ttu-id="0f760-118">Выбранный размер блока, точность и поддерживаемый диапазон размеров зависят от значений, поддерживаемых оборудованием, возвращенным при проверке компонентов **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** .</span><span class="sxs-lookup"><span data-stu-id="0f760-118">The selected block size, precision, and supported size range would depend on values supported by hardware returned from the **D3D12_FEATURE_VIDEO_MOTION_ESTIMATOR** feature check.</span></span> <span data-ttu-id="0f760-119">Можно выбрать меньший диапазон размеров, чем поддерживается драйвером.</span><span class="sxs-lookup"><span data-stu-id="0f760-119">You can select a smaller size range than the driver supports.</span></span> <span data-ttu-id="0f760-120">Диапазон размера информирует внутренние размеры выделения.</span><span class="sxs-lookup"><span data-stu-id="0f760-120">Size range informs internal allocation sizes.</span></span>

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



## <a name="storage-of-motion-vectors"></a><span data-ttu-id="0f760-121">Хранение векторов движения</span><span class="sxs-lookup"><span data-stu-id="0f760-121">Storage of motion vectors</span></span>

<span data-ttu-id="0f760-122">[ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) сохраняет векторы движения.</span><span class="sxs-lookup"><span data-stu-id="0f760-122">The [ID3D12VideoMotionVectorHeap](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videomotionvectorheap) stores motion vectors.</span></span> <span data-ttu-id="0f760-123">Этот интерфейс используется структурой [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) , возвращаемой из [ID3D12VideoEncodeCommandList:: естиматемотион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span><span class="sxs-lookup"><span data-stu-id="0f760-123">This interface is used by the [D3D12_VIDEO_MOTION_ESTIMATOR_OUTPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_output) structure returned from [ID3D12VideoEncodeCommandList::EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion).</span></span> <span data-ttu-id="0f760-124">Разрешаемая двухмерная текстура вывода — это [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) текстура, где R содержит горизонтальный компонент, а G содержит вертикальный компонент вектора движения.</span><span class="sxs-lookup"><span data-stu-id="0f760-124">The resolved output 2D texture is a [DXGI_FORMAT_R16G16_SINT](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) texture where R holds the horizontal component and G holds the vertical component of the motion vector.</span></span> <span data-ttu-id="0f760-125">Эта текстура имеет размер, чтобы вместить одну пару компонентов на блок.</span><span class="sxs-lookup"><span data-stu-id="0f760-125">This texture is sized to hold one pair of components per block.</span></span> <span data-ttu-id="0f760-126">Вызовите метод [ID3D12VideoEncodeCommandList:: ресолвемотионвекторхеап](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) , чтобы переводит выходные данные вектора движения **естиматемотион** из аппаратно зависимых форматов в единообразный формат, определенный API-интерфейсом оценки движения видео.</span><span class="sxs-lookup"><span data-stu-id="0f760-126">Call [ID3D12VideoEncodeCommandList::ResolveMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-resolvemotionvectorheap) to translates the motion vector output of **EstimateMotion** from hardware-dependent formats into a consistent format defined by the video motion estimation APIs.</span></span>

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

 <span data-ttu-id="0f760-127">**ID3D12VideoMotionVectorHeap** также используется для передачи векторов подсказок в структуре [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) .</span><span class="sxs-lookup"><span data-stu-id="0f760-127">**ID3D12VideoMotionVectorHeap** is also used to supply hint vectors in the [D3D12_VIDEO_MOTION_ESTIMATOR_INPUT](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_motion_estimator_input) structure.</span></span>



## <a name="estimate-motion-in-a-command-list"></a><span data-ttu-id="0f760-128">Оценка движения в списке команд</span><span class="sxs-lookup"><span data-stu-id="0f760-128">Estimate motion in a command list</span></span>

<span data-ttu-id="0f760-129">Вызовите [естиматемотион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) из [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) , чтобы вызвать операцию оценки движения.</span><span class="sxs-lookup"><span data-stu-id="0f760-129">Call the [EstimateMotion](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videoencodecommandlist-estimatemotion) from a [ID3D12VideoEncodeCommandList](/windows/win32/api/d3d12video/nn-d3d12video-id3d12videoencodecommandlist) to invoke the motion estimation operation.</span></span>

<span data-ttu-id="0f760-130">Приведенный ниже пример выполняет поиск движения и разрешает векторы движения к двухмерной текстуре с [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span><span class="sxs-lookup"><span data-stu-id="0f760-130">The example below executes the motion search and resolves the motion vectors to the 2D texture with [D3D12_COMMAND_LIST_TYPE_VIDEO_ENCODE](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).</span></span>  <span data-ttu-id="0f760-131">Ресурсы D3D12, используемые в качестве входных данных для **естиматемотион** , должны находиться в [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) состоянии, а ресурс, записанный **ресолвемотионвекторхеап** , должен находиться в состоянии [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) .</span><span class="sxs-lookup"><span data-stu-id="0f760-131">D3D12 Resources used as input to **EstimateMotion** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state and the resource written to by **ResolveMotionVectorHeap** must be in the [D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span>

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


## <a name="protected-resources"></a><span data-ttu-id="0f760-132">Защищенные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0f760-132">Protected resources</span></span>

<span data-ttu-id="0f760-133">Оценка вектора движения Direct3D 12 поддерживает чтение и запись в аппаратно защищенные ресурсы DRM, если поддерживается драйвером.</span><span class="sxs-lookup"><span data-stu-id="0f760-133">Direct3D 12 motion vector estimation supports reading from and writing to hardware DRM protected resources when supported by the driver.</span></span> <span data-ttu-id="0f760-134">Если входные ресурсы защищены аппаратным обеспечением DRM, то выходные данные также являются защищенным аппаратным ресурсом DRM. Методы, используемые для создания объекта контекста оценки движения и кучи векторов движения,  [ID3D12VideoDevice1:: креатевидеомотионестиматор](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) и [ID3D12VideoDevice1:: креатевидеомотионвекторхеап](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), оба принимают [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) , который используется для управления доступом к защищенным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="0f760-134">If the input resources are hardware DRM protected, the output is also a hardware DRM protected resource.The methods used to create the motion estimation context object and the motion vector heap,  [ID3D12VideoDevice1::CreateVideoMotionEstimator](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionestimator) and [ID3D12VideoDevice1::CreateVideoMotionVectorHeap](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodevice1-createvideomotionvectorheap), both accept a [ID3D12ProtectedResourceSession](/windows/win32/api/d3d12/nn-d3d12-id3d12protectedresourcesession) that is used to manage access to protected resources.</span></span> 

<span data-ttu-id="0f760-135">Используйте [ID3D12VideoMotionEstimator:: жетпротектедресаурцесессион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) и [ID3D12VideoMotionVectorHeap:: жетпротектедресаурцесессион](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) для получения объектов **ID3D12ProtectedResourceSession** , предоставленных при создании объектов.</span><span class="sxs-lookup"><span data-stu-id="0f760-135">Use [ID3D12VideoMotionEstimator::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionestimator-getprotectedresourcesession) and [ID3D12VideoMotionVectorHeap::GetProtectedResourceSession](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videomotionvectorheap-getprotectedresourcesession) to retrieve the **ID3D12ProtectedResourceSession** objects provided when the objects were created.</span></span>



## <a name="related-topics"></a><span data-ttu-id="0f760-136">См. также</span><span class="sxs-lookup"><span data-stu-id="0f760-136">Related topics</span></span>

* [<span data-ttu-id="0f760-137">API-интерфейсы видео Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0f760-137">Direct3D 12 Video APIs</span></span>](direct3d-12-video-apis.md)
* [<span data-ttu-id="0f760-138">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="0f760-138">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
