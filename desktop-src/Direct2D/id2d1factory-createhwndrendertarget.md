---
title: Методы Креатехвндрендертаржет ID2D1Factory (D2d1. h)
description: Создает ID2D1HwndRenderTarget, целевой объект отрисовки, который готовится к просмотру в окне.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Методы Креатехвндрендертаржет Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657603"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a><span data-ttu-id="a17e3-104">Методы ID2D1Factory:: Креатехвндрендертаржет</span><span class="sxs-lookup"><span data-stu-id="a17e3-104">ID2D1Factory::CreateHwndRenderTarget methods</span></span>

<span data-ttu-id="a17e3-105">Создает [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), целевой объект отрисовки, который готовится к просмотру в окне.</span><span class="sxs-lookup"><span data-stu-id="a17e3-105">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a17e3-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="a17e3-106">Overload list</span></span>



| <span data-ttu-id="a17e3-107">Метод</span><span class="sxs-lookup"><span data-stu-id="a17e3-107">Method</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="a17e3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a17e3-108">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a17e3-109">[**Креатехвндрендертаржет ( \_ \_ свойства целевого объекта прорисовки D2D1 \_ \* , \_ \_ свойства целевого объекта прорисовки D2D1 HWND \_ \_ \* , ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a17e3-109">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES\*,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES\*,ID2D1HwndRenderTarget\*\*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span> | <span data-ttu-id="a17e3-110">Создает [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), целевой объект отрисовки, который готовится к просмотру в окне.</span><span class="sxs-lookup"><span data-stu-id="a17e3-110">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |
| <span data-ttu-id="a17e3-111">[**Креатехвндрендертаржет ( \_ \_ свойства целевого объекта прорисовки D2D1 \_& \_ , \_ свойства целевого объекта прорисовки D2D1 HWND \_ \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span><span class="sxs-lookup"><span data-stu-id="a17e3-111">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES&,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES&,ID2D1HwndRenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span></span>   | <span data-ttu-id="a17e3-112">Создает [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), целевой объект отрисовки, который готовится к просмотру в окне.</span><span class="sxs-lookup"><span data-stu-id="a17e3-112">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a17e3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a17e3-113">Remarks</span></span>

<span data-ttu-id="a17e3-114">При создании целевого объекта рендеринга и возможности аппаратного ускорения выделяются ресурсы на GPU компьютера.</span><span class="sxs-lookup"><span data-stu-id="a17e3-114">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="a17e3-115">Создавая целевой объект рендеринга один раз и постоянно сохраняющий его, вы получаете выигрыш в производительности.</span><span class="sxs-lookup"><span data-stu-id="a17e3-115">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="a17e3-116">Приложение должно создавать целевые объекты рендеринга один раз и удерживать их на протяжении всего жизненного цикла приложения или до тех пор, пока не будет получено сообщение об ошибке [**\_ повторного создания \_ D2DERR**](direct2d-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a17e3-116">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="a17e3-117">При возникновении этой ошибки необходимо повторно создать целевой объект рендеринга (и все созданные им ресурсы).</span><span class="sxs-lookup"><span data-stu-id="a17e3-117">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="examples"></a><span data-ttu-id="a17e3-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="a17e3-118">Examples</span></span>

<span data-ttu-id="a17e3-119">В следующем примере создается [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a17e3-119">The following example creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a><span data-ttu-id="a17e3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a17e3-120">Requirements</span></span>



| <span data-ttu-id="a17e3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a17e3-121">Requirement</span></span> | <span data-ttu-id="a17e3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a17e3-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a17e3-123">Header</span><span class="sxs-lookup"><span data-stu-id="a17e3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a17e3-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="a17e3-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="a17e3-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a17e3-125">Library</span></span><br/> | <dl> <span data-ttu-id="a17e3-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a17e3-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="a17e3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a17e3-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="a17e3-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a17e3-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a17e3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a17e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a17e3-130">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="a17e3-130">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
