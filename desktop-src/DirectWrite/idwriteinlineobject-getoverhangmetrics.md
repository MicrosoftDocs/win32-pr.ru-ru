---
title: Идвритеинлинеобжект Жетоверхангметрикс, метод
description: Идвритетекстлайаут вызывает эту функцию обратного вызова для получения видимых экстентов (в DIP) встроенного объекта. В случае с простым точечным рисунком без заполнения и без выступа все перевисает просто будут обнулены.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Непосредственная запись метода Жетоверхангметрикс
- Прямая запись метода Жетоверхангметрикс, интерфейс Идвритеинлинеобжект
- Прямая запись интерфейса Идвритеинлинеобжект, метод Жетоверхангметрикс
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668878"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a><span data-ttu-id="02326-107">Метод Идвритеинлинеобжект:: Жетоверхангметрикс</span><span class="sxs-lookup"><span data-stu-id="02326-107">IDWriteInlineObject::GetOverhangMetrics method</span></span>

<span data-ttu-id="02326-108">[**Идвритетекстлайаут**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) вызывает эту функцию обратного вызова для получения видимых экстентов (в DIP) встроенного объекта.</span><span class="sxs-lookup"><span data-stu-id="02326-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the visible extents (in DIPs) of the inline object.</span></span> <span data-ttu-id="02326-109">В случае с простым точечным рисунком без заполнения и без выступа все перевисает просто будут обнулены.</span><span class="sxs-lookup"><span data-stu-id="02326-109">In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.</span></span>

<span data-ttu-id="02326-110">Перестает возвращаться по отношению к сообщаемому размеру объекта (см. раздел [**ДВРИТЕ \_ inline \_ Object \_ метрики**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) и не должен быть скорректирован в базовом плане.</span><span class="sxs-lookup"><span data-stu-id="02326-110">The overhangs should be returned relative to the reported size of the object (see [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)), and should not be baseline adjusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="02326-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02326-111">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="02326-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="02326-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02326-113">*перестает отвечать* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="02326-113">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02326-114">Тип: **[ **двритеные \_ \_ метрики выступа**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="02326-114">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="02326-115">Отклонение видимых экстентов (в DIP-параметрах) за пределами объекта.</span><span class="sxs-lookup"><span data-stu-id="02326-115">Overshoot of visible extents (in DIPs) outside the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02326-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02326-116">Return value</span></span>

<span data-ttu-id="02326-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="02326-117">Type: **HRESULT**</span></span>

<span data-ttu-id="02326-118">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="02326-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02326-119">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02326-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="02326-120">Требования</span><span class="sxs-lookup"><span data-stu-id="02326-120">Requirements</span></span>



| <span data-ttu-id="02326-121">Требование</span><span class="sxs-lookup"><span data-stu-id="02326-121">Requirement</span></span> | <span data-ttu-id="02326-122">Значение</span><span class="sxs-lookup"><span data-stu-id="02326-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02326-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="02326-123">Library</span></span><br/> | <dl> <span data-ttu-id="02326-124"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02326-124"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="02326-125">DLL</span><span class="sxs-lookup"><span data-stu-id="02326-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="02326-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02326-126"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02326-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02326-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02326-128">**идвритеинлинеобжект**</span><span class="sxs-lookup"><span data-stu-id="02326-128">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[<span data-ttu-id="02326-129">**идвритеинлинеобжект**</span><span class="sxs-lookup"><span data-stu-id="02326-129">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

