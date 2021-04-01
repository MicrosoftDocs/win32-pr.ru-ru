---
description: Обратные вызовы, используемые для просмотра текстур.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Интерфейс IPixEngine5Callbacks
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140134"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span data-ttu-id="a4b5d-103"><span id="vspixengine.ipixengine5callbacks"></span>Интерфейс IPixEngine5Callbacks</span><span class="sxs-lookup"><span data-stu-id="a4b5d-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks interface</span></span>

<span data-ttu-id="a4b5d-104">Обратные вызовы, используемые для просмотра текстур.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-104">Callbacks used for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="a4b5d-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a4b5d-105">Members</span></span>

<span data-ttu-id="a4b5d-106">Интерфейс **IPixEngine5Callbacks** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a4b5d-106">The **IPixEngine5Callbacks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a4b5d-107">**IPixEngine5Callbacks** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a4b5d-107">**IPixEngine5Callbacks** also has these types of members:</span></span>

-   [<span data-ttu-id="a4b5d-108">Методы</span><span class="sxs-lookup"><span data-stu-id="a4b5d-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="a4b5d-109"><span id="methods"></span>Методы</span><span class="sxs-lookup"><span data-stu-id="a4b5d-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="a4b5d-110">Интерфейс **IPixEngine5Callbacks** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-110">The **IPixEngine5Callbacks** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="a4b5d-111">Метод</span><span class="sxs-lookup"><span data-stu-id="a4b5d-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="a4b5d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a4b5d-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a4b5d-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>фритекстурекомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b5d-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a4b5d-114">Функция обратного вызова, используемая для уведомления узла при освобождении текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-114">A callback function used to notify the host when a texture has been freed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a4b5d-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>лоадхистограмкомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b5d-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a4b5d-116">Функция обратного вызова, используемая для уведомления узла о завершении загрузки гистограммы.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-116">A callback function used to notify the host when a histogram load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a4b5d-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>лоадтекстурефромфилекомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b5d-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a4b5d-118">Функция обратного вызова, используемая для уведомления узла о завершении загрузки текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-118">A callback function used to notify the host when a texture load has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a4b5d-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>лоадтекстуреслицекомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b5d-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a4b5d-120">Функция обратного вызова, используемая для уведомления узла о завершении загрузки среза текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-120">A callback function used to notify the host when a texture slice load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a4b5d-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>реадтекселвалуекомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b5d-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a4b5d-122">Функция обратного вызова, используемая для уведомления узла о завершении считывания значения шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-122">A callback function used to notify the host when a texel value read has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="a4b5d-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>рендертекстурекомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b5d-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a4b5d-124">Функция обратного вызова, используемая для уведомления узла о завершении прорисовки текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-124">A callback function used to notify the host when a texture render has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="a4b5d-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>саветекстурекомплете</strong></a></span><span class="sxs-lookup"><span data-stu-id="a4b5d-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="a4b5d-126">Функция обратного вызова, используемая для уведомления узла о завершении сохранения текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4b5d-126">A callback function used to notify the host when saving a texture has been completed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="a4b5d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="a4b5d-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="a4b5d-128">Header</span><span class="sxs-lookup"><span data-stu-id="a4b5d-128">Header</span></span></p></td><td><span data-ttu-id="a4b5d-129">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="a4b5d-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
