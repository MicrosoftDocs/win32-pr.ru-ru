---
title: Методы Сеттрансформ Идкомпоситионвисуал (Дкомп. h)
description: Задает свойство Transform этого визуального элемента. Свойство Transform указывает 2D-преобразование, используемое для изменения системы координат данного визуального элемента. Свойство может задавать матрицу преобразования размером 3 на 2 или объект преобразования.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
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
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341165"
---
# <a name="idcompositionvisualsettransform-methods"></a><span data-ttu-id="8f2bd-106">Методы Идкомпоситионвисуал:: Сеттрансформ</span><span class="sxs-lookup"><span data-stu-id="8f2bd-106">IDCompositionVisual::SetTransform methods</span></span>

<span data-ttu-id="8f2bd-107">Задает свойство Transform этого визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="8f2bd-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="8f2bd-108">Свойство Transform указывает 2D-преобразование, используемое для изменения системы координат данного визуального элемента.</span><span class="sxs-lookup"><span data-stu-id="8f2bd-108">The Transform property specifies a 2D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="8f2bd-109">Свойство может задавать матрицу преобразования размером 3 на 2 или объект преобразования.</span><span class="sxs-lookup"><span data-stu-id="8f2bd-109">The property can specify either a 3-by-2 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="8f2bd-110">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="8f2bd-110">Overload list</span></span>



| <span data-ttu-id="8f2bd-111">Метод</span><span class="sxs-lookup"><span data-stu-id="8f2bd-111">Method</span></span>                                                                                                    | <span data-ttu-id="8f2bd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8f2bd-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-113">[**Сеттрансформ ( \_ Матрица D2D \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="8f2bd-113">[**SetTransform(D2D\_MATRIX\_3X2\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span></span>          | <span data-ttu-id="8f2bd-114">Устанавливает свойство Transform в указанную матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="8f2bd-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="8f2bd-115">[**Сеттрансформ (Идкомпоситионтрансформ \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span><span class="sxs-lookup"><span data-stu-id="8f2bd-115">[**SetTransform(IDCompositionTransform\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span></span> | <span data-ttu-id="8f2bd-116">Задает для свойства Transform указанный объект преобразования.</span><span class="sxs-lookup"><span data-stu-id="8f2bd-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8f2bd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8f2bd-117">Requirements</span></span>



| <span data-ttu-id="8f2bd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8f2bd-118">Requirement</span></span> | <span data-ttu-id="8f2bd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8f2bd-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2bd-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f2bd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8f2bd-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8f2bd-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8f2bd-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f2bd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8f2bd-123">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8f2bd-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8f2bd-124">Header</span><span class="sxs-lookup"><span data-stu-id="8f2bd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f2bd-125"><dt>Дкомп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f2bd-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f2bd-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8f2bd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f2bd-127"><dt>Дкомп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f2bd-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f2bd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8f2bd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f2bd-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f2bd-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f2bd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f2bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2bd-131">**идкомпоситионматрикстрансформ**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-131">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="8f2bd-132">**идкомпоситионротатетрансформ**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-132">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="8f2bd-133">**идкомпоситионскалетрансформ**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-133">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="8f2bd-134">**идкомпоситионскевтрансформ**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-134">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="8f2bd-135">**идкомпоситионтрансформ**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-135">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="8f2bd-136">**идкомпоситионтранслатетрансформ**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-136">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="8f2bd-137">**идкомпоситионвисуал**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-137">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="8f2bd-138">**Идкомпоситионвисуал:: Сетоффсеткс**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-138">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="8f2bd-139">**Идкомпоситионвисуал:: Сетоффсети**</span><span class="sxs-lookup"><span data-stu-id="8f2bd-139">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="8f2bd-140">�</span><span class="sxs-lookup"><span data-stu-id="8f2bd-140">�</span></span>

<span data-ttu-id="8f2bd-141">�</span><span class="sxs-lookup"><span data-stu-id="8f2bd-141">�</span></span>
