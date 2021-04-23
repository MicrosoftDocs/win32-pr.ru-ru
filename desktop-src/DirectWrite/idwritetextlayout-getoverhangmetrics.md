---
title: Идвритетекстлайаут Жетоверхангметрикс, метод
description: Возвращает перестает отвечать (в DIP) макета и всех содержащихся в нем объектов, включая текстовые глифы и встроенные объекты.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Непосредственная запись метода Жетоверхангметрикс
- Прямая запись метода Жетоверхангметрикс, интерфейс Идвритетекстлайаут
- Прямая запись интерфейса Идвритетекстлайаут, метод Жетоверхангметрикс
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668533"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a><span data-ttu-id="02231-106">Метод Идвритетекстлайаут:: Жетоверхангметрикс</span><span class="sxs-lookup"><span data-stu-id="02231-106">IDWriteTextLayout::GetOverhangMetrics method</span></span>

<span data-ttu-id="02231-107">Возвращает перестает отвечать (в DIP) макета и всех содержащихся в нем объектов, включая текстовые глифы и встроенные объекты.</span><span class="sxs-lookup"><span data-stu-id="02231-107">Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="02231-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02231-108">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="02231-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="02231-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02231-110">*перестает отвечать* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="02231-110">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02231-111">Тип: **[ **двритеные \_ \_ метрики выступа**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="02231-111">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="02231-112">Прокрутка видимых экстентов (в DIP) за пределами макета.</span><span class="sxs-lookup"><span data-stu-id="02231-112">Overshoots of visible extents (in DIPs) outside the layout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02231-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02231-113">Return value</span></span>

<span data-ttu-id="02231-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="02231-114">Type: **HRESULT**</span></span>

<span data-ttu-id="02231-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="02231-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02231-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02231-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="02231-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02231-117">Remarks</span></span>

<span data-ttu-id="02231-118">Подчеркивания и зачеркивание не влияют на определение черного прямоугольника, поскольку они на самом деле рисуются модулем подготовки отчетов, который может нарисовать их в различных стилях.</span><span class="sxs-lookup"><span data-stu-id="02231-118">Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="02231-119">Требования</span><span class="sxs-lookup"><span data-stu-id="02231-119">Requirements</span></span>



| <span data-ttu-id="02231-120">Требование</span><span class="sxs-lookup"><span data-stu-id="02231-120">Requirement</span></span> | <span data-ttu-id="02231-121">Значение</span><span class="sxs-lookup"><span data-stu-id="02231-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02231-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02231-122">Library</span></span><br/> | <dl> <span data-ttu-id="02231-123"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02231-123"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="02231-124">DLL</span><span class="sxs-lookup"><span data-stu-id="02231-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="02231-125"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02231-125"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02231-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02231-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02231-127">**идвритетекстлайаут**</span><span class="sxs-lookup"><span data-stu-id="02231-127">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="02231-128">**идвритетекстлайаут**</span><span class="sxs-lookup"><span data-stu-id="02231-128">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

