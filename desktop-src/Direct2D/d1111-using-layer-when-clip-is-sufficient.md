---
title: D1111 с использованием слоя, когда клип достаточно
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Слой используется с НУЛЕВой маской непрозрачности, непрозрачностью 1,0 и прямоугольной геометрической маской по оси. API-интерфейс обмена сообщениями Push/Pop должен добиться того же результата с более высокой производительностью.
keywords:
- D1111 с использованием слоя, когда Clip является достаточным Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8463cc3940b69e326f13df6be9602dd6073fec0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549909"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="b3d20-105">D1111: использование слоя при наличии клипа</span><span class="sxs-lookup"><span data-stu-id="b3d20-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="b3d20-106">Производительность — слой используется с **нулевой** маской непрозрачности, непрозрачностью 1,0 и прямоугольной геометрической маской по оси.</span><span class="sxs-lookup"><span data-stu-id="b3d20-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="b3d20-107">API-интерфейс обмена сообщениями Push/Pop должен добиться того же результата с более высокой производительностью.</span><span class="sxs-lookup"><span data-stu-id="b3d20-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="b3d20-108">Заполнители</span><span class="sxs-lookup"><span data-stu-id="b3d20-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="b3d20-109"><span id="interface"></span><span id="INTERFACE"></span>*взаимодействия*</span><span class="sxs-lookup"><span data-stu-id="b3d20-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="b3d20-110">Адрес интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b3d20-110">The address of the interface.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="b3d20-111">Уровень ошибки</span><span class="sxs-lookup"><span data-stu-id="b3d20-111">Error Level</span></span> | <span data-ttu-id="b3d20-112">Информация</span><span class="sxs-lookup"><span data-stu-id="b3d20-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="b3d20-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="b3d20-113">Examples</span></span>

<span data-ttu-id="b3d20-114">В следующем коде используется [**пушлайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) и [**поплайер**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , если слой содержит только один примитив (прямоугольник), а для полей структуры [**\_ \_ параметров слоя D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) задано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3d20-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="b3d20-115">Значения по умолчанию для структуры **\_ \_ параметров слоя D2D1** см. в разделе [**лайерпараметер**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="b3d20-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="b3d20-116">В этом примере создается следующее сообщение отладки:</span><span class="sxs-lookup"><span data-stu-id="b3d20-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="b3d20-117">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="b3d20-117">Possible Causes</span></span>

<span data-ttu-id="b3d20-118">Слой использовался, когда были бы достаточно методы [**пушаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) и [**попаксисалигнедклип**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) .</span><span class="sxs-lookup"><span data-stu-id="b3d20-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 