---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Сохраняет упорядоченную пару целых чисел — обычно ширину и высоту прямоугольника.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135439"
---
# <a name="d2d1_size_u"></a><span data-ttu-id="99648-104">D2D1 \_ размер \_ U</span><span class="sxs-lookup"><span data-stu-id="99648-104">D2D1\_SIZE\_U</span></span>

<span data-ttu-id="99648-105">Сохраняет упорядоченную пару целых чисел — обычно ширину и высоту прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="99648-105">Stores an ordered pair of integers, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a><span data-ttu-id="99648-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99648-106">Remarks</span></span>

<span data-ttu-id="99648-107">Как и точки, размеры являются еще одной важной концепцией графики.</span><span class="sxs-lookup"><span data-stu-id="99648-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="99648-108">В Direct2D размеры представлены структурами D2D1 размера **\_ \_ U** или D2D1, [**\_ равными \_ F**](d2d1-size-f.md) .</span><span class="sxs-lookup"><span data-stu-id="99648-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_U** or [**D2D1\_SIZE\_F**](d2d1-size-f.md) structures.</span></span> <span data-ttu-id="99648-109">Они содержат упорядоченную пару чисел.</span><span class="sxs-lookup"><span data-stu-id="99648-109">They both contain an ordered pair of numbers.</span></span> <span data-ttu-id="99648-110">Структура **D2D1 \_ size \_ U** содержит упорядоченную пару значений **UINT32** , а структура **D2D1 \_ size \_ F** содержит упорядоченную пару значений **float** .</span><span class="sxs-lookup"><span data-stu-id="99648-110">The **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values, and the **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values.</span></span>

<span data-ttu-id="99648-111">Структура **D2D1 \_ size \_ U** предоставляет удобный способ хранения упорядоченной пары чисел, например ширины и высоты прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="99648-111">The **D2D1\_SIZE\_U** structure provides a convenient way for you to store an ordered pair of numbers, such as the width and height of a rectangle.</span></span>

<span data-ttu-id="99648-112">**D2D1 \_ РАЗМЕР \_ u** — это новое имя для уже определенного типа **D2D с \_ размером \_ U**.</span><span class="sxs-lookup"><span data-stu-id="99648-112">**D2D1\_SIZE\_U** is a new name for an already defined type **D2D\_SIZE\_U**.</span></span> <span data-ttu-id="99648-113">Для создания структуры **D2D1 \_ size \_ U** можно использовать функцию **D2D1:: сизеу** .</span><span class="sxs-lookup"><span data-stu-id="99648-113">You can use the **D2D1::SizeU** function to create a **D2D1\_SIZE\_U** structure.</span></span> <span data-ttu-id="99648-114">Как правило, эта структура используется для указания размера пикселя [**D2D1 \_ HWND \_ визуализации \_ целевой структуры \_ свойств**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) .</span><span class="sxs-lookup"><span data-stu-id="99648-114">A common use for this structure is to specify the pixel size of a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) structure.</span></span> <span data-ttu-id="99648-115">Ниже приведен пример использования этой структуры.</span><span class="sxs-lookup"><span data-stu-id="99648-115">The following provides an example of using this structure.</span></span>


```C++
    if (!m_pRenderTarget)
    {
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



## <a name="requirements"></a><span data-ttu-id="99648-116">Требования</span><span class="sxs-lookup"><span data-stu-id="99648-116">Requirements</span></span>



| <span data-ttu-id="99648-117">Требование</span><span class="sxs-lookup"><span data-stu-id="99648-117">Requirement</span></span> | <span data-ttu-id="99648-118">Значение</span><span class="sxs-lookup"><span data-stu-id="99648-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99648-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="99648-119">Minimum supported client</span></span><br/> | <span data-ttu-id="99648-120">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="99648-120">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="99648-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="99648-121">Minimum supported server</span></span><br/> | <span data-ttu-id="99648-122">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="99648-122">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="99648-123">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="99648-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="99648-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="99648-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="99648-125">Header</span><span class="sxs-lookup"><span data-stu-id="99648-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="99648-126"><dt>D2DBaseTypes. h (включение D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99648-126"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="99648-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99648-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99648-128">**\_Размер D2D \_ U**</span><span class="sxs-lookup"><span data-stu-id="99648-128">**D2D\_SIZE\_U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[<span data-ttu-id="99648-129">**D2D1 \_ размер \_ F**</span><span class="sxs-lookup"><span data-stu-id="99648-129">**D2D1\_SIZE\_F**</span></span>](d2d1-size-f.md)
</dt> <dt>

[<span data-ttu-id="99648-130">**D2D1:: Хвндрендертаржетпропертиес**</span><span class="sxs-lookup"><span data-stu-id="99648-130">**D2D1::HwndRenderTargetProperties**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

