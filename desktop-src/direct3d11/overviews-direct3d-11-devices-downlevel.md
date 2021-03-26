---
title: Direct3D 11 на оборудовании нижнего уровня
description: В этом разделе обсуждается, как Direct3D 11 предназначен для поддержки как нового, так и существующего оборудования с версии DirectX 9 до DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104551516"
---
# <a name="direct3d-11-on-downlevel-hardware"></a><span data-ttu-id="dd6c7-103">Direct3D 11 на оборудовании нижнего уровня</span><span class="sxs-lookup"><span data-stu-id="dd6c7-103">Direct3D 11 on Downlevel Hardware</span></span>

<span data-ttu-id="dd6c7-104">В этом разделе обсуждается, как Direct3D 11 предназначен для поддержки как нового, так и существующего оборудования с версии DirectX 9 до DirectX 11.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-104">This section discusses how Direct3D 11 is designed to support both new and existing hardware, from DirectX 9 to DirectX 11.</span></span>

<span data-ttu-id="dd6c7-105">На этой схеме показано, как Direct3D 11 поддерживает новое и существующее оборудование.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-105">This diagram shows how Direct3D 11 supports new and existing hardware.</span></span>

![Схема оборудования, поддерживаемого Direct3D 11](images/d3d11-on-downlevel-hardware.png)

<span data-ttu-id="dd6c7-107">В Direct3D 11 появилась новая парадигма, называемая уровнями функций.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-107">With Direct3D 11, a new paradigm is introduced called feature levels.</span></span> <span data-ttu-id="dd6c7-108">Уровень функций — это хорошо определенный набор функций GPU.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-108">A feature level is a well defined set of GPU functionality.</span></span> <span data-ttu-id="dd6c7-109">Используя уровень функций, можно ориентироваться на приложение Direct3D для работы в низкоуровневых версиях аппаратных средств Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-109">Using a feature level, you can target a Direct3D application to run on a downlevel version of Direct3D hardware.</span></span>

<span data-ttu-id="dd6c7-110">В разделе [справочника 10Level9](d3d11-graphics-reference-10level9.md) перечислены различия между различными методами [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) и [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) на различных уровнях функций 10Level9.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-110">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="dd6c7-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="dd6c7-111">In this section</span></span>



| <span data-ttu-id="dd6c7-112">Раздел</span><span class="sxs-lookup"><span data-stu-id="dd6c7-112">Topic</span></span>                                                                                                                  | <span data-ttu-id="dd6c7-113">Описание</span><span class="sxs-lookup"><span data-stu-id="dd6c7-113">Description</span></span>                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd6c7-114">Уровни функций Direct3D </span><span class="sxs-lookup"><span data-stu-id="dd6c7-114">Direct3D feature levels</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | <span data-ttu-id="dd6c7-115">В этом разделе обсуждаются уровни функций Direct3D.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-115">This topic discusses Direct3D feature levels.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="dd6c7-116">Исключения</span><span class="sxs-lookup"><span data-stu-id="dd6c7-116">Exceptions</span></span>](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | <span data-ttu-id="dd6c7-117">В этом разделе описываются исключения при использовании Direct3D 11 на оборудовании нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-117">This topic describes exceptions when using Direct3D 11 on downlevel hardware.</span></span> <br/>                                                                                      |
| [<span data-ttu-id="dd6c7-118">Вычисление шейдеров на низкоуровневых устройствах</span><span class="sxs-lookup"><span data-stu-id="dd6c7-118">Compute Shaders on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | <span data-ttu-id="dd6c7-119">В этом разделе описывается использование [шейдеров вычислений](direct3d-11-advanced-stages-compute-shader.md) в приложении Direct3D 11 на оборудовании Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-119">This topic discusses how to make use of [compute shaders](direct3d-11-advanced-stages-compute-shader.md) in a Direct3D 11 app on Direct3D 10 hardware.</span></span><br/>             |
| [<span data-ttu-id="dd6c7-120">Предотвращение нежелательных СРВС шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="dd6c7-120">Preventing Unwanted NULL Pixel Shader SRVs</span></span>](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | <span data-ttu-id="dd6c7-121">В этом разделе обсуждается, как обойти драйвер, получая **пустые** представления ресурсов (СРВС), даже если СРВС, отличные от **null** , привязаны к этапу шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-121">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span><br/> |



 

## <a name="how-to-topics-about-feature-levels"></a><span data-ttu-id="dd6c7-122">Разделы, посвященные уровням функций</span><span class="sxs-lookup"><span data-stu-id="dd6c7-122">How to topics about feature levels</span></span>



| <span data-ttu-id="dd6c7-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="dd6c7-123">Topic</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="dd6c7-124">Описание</span><span class="sxs-lookup"><span data-stu-id="dd6c7-124">Description</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="dd6c7-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Как получить уровень функций устройства](overviews-direct3d-11-devices-downlevel-get.md)</span><span class="sxs-lookup"><span data-stu-id="dd6c7-125"><span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[How To: Get the Device Feature Level](overviews-direct3d-11-devices-downlevel-get.md)</span></span><br/> | <span data-ttu-id="dd6c7-126">Как получить уровень функций.</span><span class="sxs-lookup"><span data-stu-id="dd6c7-126">How to get a feature level.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="dd6c7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="dd6c7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd6c7-128">Устройства</span><span class="sxs-lookup"><span data-stu-id="dd6c7-128">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





