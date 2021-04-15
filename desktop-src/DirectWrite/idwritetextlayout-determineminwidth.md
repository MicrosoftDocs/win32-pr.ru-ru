---
title: Идвритетекстлайаут Детерминеминвидс, метод
description: Определяет минимальную возможную ширину, на которую можно установить макет без аварийного разрыва между символами целых слов.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Непосредственная запись метода Детерминеминвидс
- Прямая запись метода Детерминеминвидс, интерфейс Идвритетекстлайаут
- Прямая запись интерфейса Идвритетекстлайаут, метод Детерминеминвидс
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689024"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a><span data-ttu-id="fe17c-106">Идвритетекстлайаут: метод:D Етерминеминвидс</span><span class="sxs-lookup"><span data-stu-id="fe17c-106">IDWriteTextLayout::DetermineMinWidth method</span></span>

<span data-ttu-id="fe17c-107">Определяет минимальную возможную ширину, на которую можно установить макет без аварийного разрыва между символами целых слов.</span><span class="sxs-lookup"><span data-stu-id="fe17c-107">Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe17c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe17c-108">Syntax</span></span>


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="fe17c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe17c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe17c-110">*minWidth* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fe17c-110">*minWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe17c-111">Тип: **float \***</span><span class="sxs-lookup"><span data-stu-id="fe17c-111">Type: **FLOAT\***</span></span>

<span data-ttu-id="fe17c-112">Минимальная ширина.</span><span class="sxs-lookup"><span data-stu-id="fe17c-112">Minimum width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe17c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe17c-113">Return value</span></span>

<span data-ttu-id="fe17c-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fe17c-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fe17c-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="fe17c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe17c-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fe17c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe17c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="fe17c-117">Requirements</span></span>



| <span data-ttu-id="fe17c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="fe17c-118">Requirement</span></span> | <span data-ttu-id="fe17c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="fe17c-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe17c-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fe17c-120">Library</span></span><br/> | <dl> <span data-ttu-id="fe17c-121"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe17c-121"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe17c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="fe17c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe17c-123"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe17c-123"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe17c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe17c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe17c-125">**идвритетекстлайаут**</span><span class="sxs-lookup"><span data-stu-id="fe17c-125">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="fe17c-126">**идвритетекстлайаут**</span><span class="sxs-lookup"><span data-stu-id="fe17c-126">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

