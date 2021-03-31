---
title: Методы Сетклип Идкомпоситионвисуал (Дкомп. h)
description: Устанавливает свойство Clip этого визуального элемента в указанную прямоугольную область или объект Clip.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- Методы Сетклип DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803707"
---
# <a name="idcompositionvisualsetclip-methods"></a><span data-ttu-id="c50db-104">Методы Идкомпоситионвисуал:: Сетклип</span><span class="sxs-lookup"><span data-stu-id="c50db-104">IDCompositionVisual::SetClip methods</span></span>

<span data-ttu-id="c50db-105">Устанавливает свойство Clip этого визуального элемента в указанную прямоугольную область или объект Clip.</span><span class="sxs-lookup"><span data-stu-id="c50db-105">Sets the Clip property of this visual to the specified rectangular region or clip object.</span></span> <span data-ttu-id="c50db-106">Свойство Clip позволяет пререзать визуализацию визуального поддерева, которое находится в корне этого визуального элемента, до прямоугольной области.</span><span class="sxs-lookup"><span data-stu-id="c50db-106">The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region.</span></span>

### <a name="overload-list"></a><span data-ttu-id="c50db-107">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="c50db-107">Overload list</span></span>



| <span data-ttu-id="c50db-108">Метод</span><span class="sxs-lookup"><span data-stu-id="c50db-108">Method</span></span>                                                                                | <span data-ttu-id="c50db-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c50db-109">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="c50db-110">[**Сетклип (const D2D \_ Rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="c50db-110">[**SetClip(const D2D\_RECT\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span></span> | <span data-ttu-id="c50db-111">Устанавливает свойство Clip в указанную прямоугольную область.</span><span class="sxs-lookup"><span data-stu-id="c50db-111">Sets the Clip property to the specified rectangular region.</span></span><br/> |
| <span data-ttu-id="c50db-112">[**Сетклип (Идкомпоситионклип \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span><span class="sxs-lookup"><span data-stu-id="c50db-112">[**SetClip(IDCompositionClip\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span></span> | <span data-ttu-id="c50db-113">Устанавливает свойство Clip в указанный объект Clip.</span><span class="sxs-lookup"><span data-stu-id="c50db-113">Sets the Clip property to the specified clip object.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="c50db-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c50db-114">Requirements</span></span>



| <span data-ttu-id="c50db-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c50db-115">Requirement</span></span> | <span data-ttu-id="c50db-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c50db-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c50db-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c50db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c50db-118">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c50db-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c50db-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c50db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c50db-120">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c50db-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c50db-121">Header</span><span class="sxs-lookup"><span data-stu-id="c50db-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c50db-122"><dt>Дкомп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c50db-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c50db-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c50db-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c50db-124"><dt>Дкомп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c50db-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="c50db-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c50db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c50db-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50db-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c50db-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c50db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c50db-128">Вырезая</span><span class="sxs-lookup"><span data-stu-id="c50db-128">Clipping</span></span>](clipping.md)
</dt> <dt>

[<span data-ttu-id="c50db-129">**идкомпоситионвисуал**</span><span class="sxs-lookup"><span data-stu-id="c50db-129">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

<span data-ttu-id="c50db-130">�</span><span class="sxs-lookup"><span data-stu-id="c50db-130">�</span></span>

<span data-ttu-id="c50db-131">�</span><span class="sxs-lookup"><span data-stu-id="c50db-131">�</span></span>
