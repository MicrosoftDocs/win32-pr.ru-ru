---
title: Методы изменения размера ID2D1HwndRenderTarget (D2d1. h)
description: Изменяет размер целевого объекта отрисовки на указанный размер в пикселях.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Методы изменения размера Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657637"
---
# <a name="id2d1hwndrendertargetresize-methods"></a><span data-ttu-id="db202-104">Методы ID2D1HwndRenderTarget:: resize</span><span class="sxs-lookup"><span data-stu-id="db202-104">ID2D1HwndRenderTarget::Resize methods</span></span>

<span data-ttu-id="db202-105">Изменяет размер целевого объекта отрисовки на указанный размер в пикселях.</span><span class="sxs-lookup"><span data-stu-id="db202-105">Changes the size of the render target to the specified pixel size.</span></span>

### <a name="overload-list"></a><span data-ttu-id="db202-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="db202-106">Overload list</span></span>



| <span data-ttu-id="db202-107">Метод</span><span class="sxs-lookup"><span data-stu-id="db202-107">Method</span></span>                                                                         | <span data-ttu-id="db202-108">Описание</span><span class="sxs-lookup"><span data-stu-id="db202-108">Description</span></span>                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="db202-109">[**Изменение размера (D2D1 \_ size \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span><span class="sxs-lookup"><span data-stu-id="db202-109">[**Resize(D2D1\_SIZE\_U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span></span>  | <span data-ttu-id="db202-110">Изменяет размер целевого объекта отрисовки на указанный размер в пикселях.</span><span class="sxs-lookup"><span data-stu-id="db202-110">Changes the size of the render target to the specified pixel size.</span></span> <br/> |
| <span data-ttu-id="db202-111">[**Изменить размер (D2D1 \_ размер \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span><span class="sxs-lookup"><span data-stu-id="db202-111">[**Resize(D2D1\_SIZE\_U\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span></span> | <span data-ttu-id="db202-112">Изменяет размер целевого объекта отрисовки на указанный размер в пикселях.</span><span class="sxs-lookup"><span data-stu-id="db202-112">Changes the size of the render target to the specified pixel size.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="db202-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db202-113">Remarks</span></span>

<span data-ttu-id="db202-114">После вызова этого метода содержимое заднего буфера целевого объекта прорисовки не определяется, даже если при создании целевого объекта отрисовки был указан параметр [**D2D1 \_ Present \_ Options ( \_ хранить \_ содержимое**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) ).</span><span class="sxs-lookup"><span data-stu-id="db202-114">After this method is called, the contents of the render target's back-buffer are not defined, even if the [**D2D1\_PRESENT\_OPTIONS\_RETAIN\_CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) option was specified when the render target was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="db202-115">Требования</span><span class="sxs-lookup"><span data-stu-id="db202-115">Requirements</span></span>



| <span data-ttu-id="db202-116">Требование</span><span class="sxs-lookup"><span data-stu-id="db202-116">Requirement</span></span> | <span data-ttu-id="db202-117">Значение</span><span class="sxs-lookup"><span data-stu-id="db202-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db202-118">Header</span><span class="sxs-lookup"><span data-stu-id="db202-118">Header</span></span><br/>  | <dl> <span data-ttu-id="db202-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="db202-119"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="db202-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="db202-120">Library</span></span><br/> | <dl> <span data-ttu-id="db202-121"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db202-121"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="db202-122">DLL</span><span class="sxs-lookup"><span data-stu-id="db202-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="db202-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db202-123"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db202-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db202-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="db202-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db202-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="db202-126">�</span><span class="sxs-lookup"><span data-stu-id="db202-126">�</span></span>

<span data-ttu-id="db202-127">�</span><span class="sxs-lookup"><span data-stu-id="db202-127">�</span></span>
