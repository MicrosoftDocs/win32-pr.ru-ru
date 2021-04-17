---
title: Методы Сеттрансформ IDCompositionVisual3 (Дкомп. h)
description: Задает свойство Transform этого визуального элемента. Свойство Transform указывает трехмерное преобразование, используемое для изменения системы координат данного визуального элемента. Свойство может указывать либо матрицу преобразования размером 4 на 4, либо объект преобразования.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- Методы Сеттрансформ DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710497"
---
# <a name="idcompositionvisual3settransform-methods"></a><span data-ttu-id="57040-106">Методы IDCompositionVisual3:: Сеттрансформ</span><span class="sxs-lookup"><span data-stu-id="57040-106">IDCompositionVisual3::SetTransform methods</span></span>

<span data-ttu-id="57040-107">Задает свойство Transform этого визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="57040-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="57040-108">Свойство Transform указывает трехмерное преобразование, используемое для изменения системы координат данного визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="57040-108">The Transform property specifies a 3D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="57040-109">Свойство может указывать либо матрицу преобразования размером 4 на 4, либо объект преобразования.</span><span class="sxs-lookup"><span data-stu-id="57040-109">The property can specify either a 4-by-4 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="57040-110">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="57040-110">Overload list</span></span>



| <span data-ttu-id="57040-111">Метод</span><span class="sxs-lookup"><span data-stu-id="57040-111">Method</span></span>                                                                                  | <span data-ttu-id="57040-112">Описание</span><span class="sxs-lookup"><span data-stu-id="57040-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="57040-113">[**Сеттрансформ ( \_ Матрица D2D \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span><span class="sxs-lookup"><span data-stu-id="57040-113">[**SetTransform(D2D\_MATRIX\_4X4\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span></span>       | <span data-ttu-id="57040-114">Устанавливает свойство Transform в указанную матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="57040-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="57040-115">[**Сеттрансформ (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span><span class="sxs-lookup"><span data-stu-id="57040-115">[**SetTransform(IDCompositionTransform3D\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span></span> | <span data-ttu-id="57040-116">Задает для свойства Transform указанный объект преобразования.</span><span class="sxs-lookup"><span data-stu-id="57040-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="57040-117">Требования</span><span class="sxs-lookup"><span data-stu-id="57040-117">Requirements</span></span>



| <span data-ttu-id="57040-118">Требование</span><span class="sxs-lookup"><span data-stu-id="57040-118">Requirement</span></span> | <span data-ttu-id="57040-119">Значение</span><span class="sxs-lookup"><span data-stu-id="57040-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57040-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57040-120">Minimum supported client</span></span><br/> | <span data-ttu-id="57040-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57040-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="57040-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57040-122">Minimum supported server</span></span><br/> | <span data-ttu-id="57040-123">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57040-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="57040-124">Header</span><span class="sxs-lookup"><span data-stu-id="57040-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="57040-125"><dt>Дкомп. h</dt></span><span class="sxs-lookup"><span data-stu-id="57040-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="57040-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="57040-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="57040-127"><dt>Дкомп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57040-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="57040-128">DLL</span><span class="sxs-lookup"><span data-stu-id="57040-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57040-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57040-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57040-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57040-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57040-131">**IDCompositionVisual3**</span><span class="sxs-lookup"><span data-stu-id="57040-131">**IDCompositionVisual3**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[<span data-ttu-id="57040-132">**идкомпоситионматрикстрансформ**</span><span class="sxs-lookup"><span data-stu-id="57040-132">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="57040-133">**идкомпоситионротатетрансформ**</span><span class="sxs-lookup"><span data-stu-id="57040-133">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="57040-134">**идкомпоситионскалетрансформ**</span><span class="sxs-lookup"><span data-stu-id="57040-134">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="57040-135">**идкомпоситионскевтрансформ**</span><span class="sxs-lookup"><span data-stu-id="57040-135">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="57040-136">**идкомпоситионтрансформ**</span><span class="sxs-lookup"><span data-stu-id="57040-136">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="57040-137">**идкомпоситионтранслатетрансформ**</span><span class="sxs-lookup"><span data-stu-id="57040-137">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="57040-138">**идкомпоситионвисуал**</span><span class="sxs-lookup"><span data-stu-id="57040-138">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="57040-139">**Идкомпоситионвисуал:: Сетоффсеткс**</span><span class="sxs-lookup"><span data-stu-id="57040-139">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="57040-140">**Идкомпоситионвисуал:: Сетоффсети**</span><span class="sxs-lookup"><span data-stu-id="57040-140">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="57040-141">�</span><span class="sxs-lookup"><span data-stu-id="57040-141">�</span></span>

<span data-ttu-id="57040-142">�</span><span class="sxs-lookup"><span data-stu-id="57040-142">�</span></span>
