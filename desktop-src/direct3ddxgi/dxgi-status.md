---
description: Коды состояния, которые могут возвращаться функциями DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703749"
---
# <a name="dxgi_status"></a><span data-ttu-id="5b5db-103">\_состояние DXGI</span><span class="sxs-lookup"><span data-stu-id="5b5db-103">DXGI\_STATUS</span></span>

<span data-ttu-id="5b5db-104">Коды состояния, которые могут возвращаться функциями DXGI.</span><span class="sxs-lookup"><span data-stu-id="5b5db-104">Status codes that can be returned by DXGI functions.</span></span>



| <span data-ttu-id="5b5db-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="5b5db-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="5b5db-106">Описание</span><span class="sxs-lookup"><span data-stu-id="5b5db-106">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <span data-ttu-id="5b5db-107"><dt>**DXGI \_ СОСТОЯНИЕ \_ перекрыто**</dt> <dt>0x087A0001</dt></span><span class="sxs-lookup"><span data-stu-id="5b5db-107"><dt>**DXGI\_STATUS\_OCCLUDED**</dt> <dt>0x087A0001</dt></span></span> </dl>                                                 | <span data-ttu-id="5b5db-108">Содержимое окна не отображается.</span><span class="sxs-lookup"><span data-stu-id="5b5db-108">The window content is not visible.</span></span> <span data-ttu-id="5b5db-109">При получении этого состояния приложение может прерывать отрисовку и использовать \_ тестовую презентацию DXGI \_ , чтобы определить, когда следует возобновить подготовку к просмотру.</span><span class="sxs-lookup"><span data-stu-id="5b5db-109">When receiving this status, an application can stop rendering and use DXGI\_PRESENT\_TEST to determine when to resume rendering.</span></span> <span data-ttu-id="5b5db-110">Вы не получите состояние DXGI \_ \_ перекрыто, если используете цепочку перелистывания моделей.</span><span class="sxs-lookup"><span data-stu-id="5b5db-110">You will not receive DXGI\_STATUS\_OCCLUDED if you're using a flip model swap chain.</span></span><br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <span data-ttu-id="5b5db-111"><dt>**DXGI \_ \_ \_ Изменен режим состояния**</dt> <dt>0x087A0007</dt></span><span class="sxs-lookup"><span data-stu-id="5b5db-111"><dt>**DXGI\_STATUS\_MODE\_CHANGED**</dt> <dt>0x087A0007</dt></span></span> </dl>                                    | <span data-ttu-id="5b5db-112">Изменен режим экрана рабочего стола, возможно, произошло преобразование или растяжение цвета.</span><span class="sxs-lookup"><span data-stu-id="5b5db-112">The desktop display mode has been changed, there might be color conversion/stretching.</span></span> <span data-ttu-id="5b5db-113">Приложение должно вызывать [**идксгисвапчаин:: ресизебуфферс**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) для сопоставления с новым режимом экрана.</span><span class="sxs-lookup"><span data-stu-id="5b5db-113">The application should call [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) to match the new display mode.</span></span><br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <span data-ttu-id="5b5db-114"><dt>**DXGI \_ \_Изменение режима \_ \_ \_ состояния**</dt> выполняется <dt>0x087A0008</dt></span><span class="sxs-lookup"><span data-stu-id="5b5db-114"><dt>**DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</dt> <dt>0x087A0008</dt></span></span> </dl> | <span data-ttu-id="5b5db-115">[**Идксгисвапчаин:: ресизетаржет**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) и [**Идксгисвапчаин:: сетфуллскринстате**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) будут возвращать \_ изменение режима отображения состояния DXGI, \_ \_ \_ \_ Если при вызове какого-либо API происходит переход в полноэкранный режим или в режиме окна.</span><span class="sxs-lookup"><span data-stu-id="5b5db-115">[**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) and [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) will return DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS if a fullscreen/windowed mode transition is occurring when either API is called.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5b5db-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b5db-116">Remarks</span></span>

<span data-ttu-id="5b5db-117">Значение **HRESULT** для каждого значения **\_ состояния DXGI** определяется на основе этого макроса, определенного в дксгитипе. h:</span><span class="sxs-lookup"><span data-stu-id="5b5db-117">The **HRESULT** value for each **DXGI\_STATUS** value is determined from this macro that is defined in DXGItype.h:</span></span>


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



<span data-ttu-id="5b5db-118">Например, **состояние DXGI \_ \_ перекрыто** определяется как **0x087A0001**:</span><span class="sxs-lookup"><span data-stu-id="5b5db-118">For example, **DXGI\_STATUS\_OCCLUDED** is defined as **0x087A0001**:</span></span>


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a><span data-ttu-id="5b5db-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5b5db-119">Requirements</span></span>



| <span data-ttu-id="5b5db-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5b5db-120">Requirement</span></span> | <span data-ttu-id="5b5db-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5b5db-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5b5db-122">Header</span><span class="sxs-lookup"><span data-stu-id="5b5db-122">Header</span></span><br/> | <dl> <span data-ttu-id="5b5db-123"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5db-123"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5db-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b5db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5db-125">Константы DXGI</span><span class="sxs-lookup"><span data-stu-id="5b5db-125">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




