---
description: Извлекает значение, указывающее, задан ли для этого Иконтекстноде Конфирматионтипе, переданный этому методу.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Метод Иконтекстноде:: Confirm (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542050"
---
# <a name="icontextnodeisconfirmed-method"></a><span data-ttu-id="15c72-103">Метод Иконтекстноде:: Confirm</span><span class="sxs-lookup"><span data-stu-id="15c72-103">IContextNode::IsConfirmed method</span></span>

<span data-ttu-id="15c72-104">Извлекает значение, указывающее, задан ли для этого Иконтекстноде Конфирматионтипе, переданный этому методу.</span><span class="sxs-lookup"><span data-stu-id="15c72-104">Retrieves a value that indicates whether the ConfirmationType passed in to this method has been set on this IContextNode.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c72-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15c72-105">Syntax</span></span>


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a><span data-ttu-id="15c72-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="15c72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c72-107">*конфирмедтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="15c72-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c72-108">Проверяемый тип подтверждения.</span><span class="sxs-lookup"><span data-stu-id="15c72-108">The confirmation type being tested for.</span></span>

</dd> <dt>

<span data-ttu-id="15c72-109">*пфтипеконфирмед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="15c72-109">*pfTypeConfirmed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c72-110">**Вариант \_ Значение TRUE** , если для этого объекта [**иконтекстноде**](icontextnode.md) был задан тип, переданный в конфирмедтипе; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="15c72-110">**VARIANT\_TRUE** if the type passed in confirmedType has been set on this [**IContextNode**](icontextnode.md) object; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c72-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15c72-111">Return value</span></span>

<span data-ttu-id="15c72-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="15c72-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15c72-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15c72-113">Remarks</span></span>

<span data-ttu-id="15c72-114">Это значение задается методом [**иконтекстноде:: Confirm**](icontextnode-confirm.md) .</span><span class="sxs-lookup"><span data-stu-id="15c72-114">This value is set by the [**IContextNode::Confirm**](icontextnode-confirm.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c72-115">Требования</span><span class="sxs-lookup"><span data-stu-id="15c72-115">Requirements</span></span>



| <span data-ttu-id="15c72-116">Требование</span><span class="sxs-lookup"><span data-stu-id="15c72-116">Requirement</span></span> | <span data-ttu-id="15c72-117">Значение</span><span class="sxs-lookup"><span data-stu-id="15c72-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c72-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15c72-118">Minimum supported client</span></span><br/> | <span data-ttu-id="15c72-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="15c72-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="15c72-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15c72-120">Minimum supported server</span></span><br/> | <span data-ttu-id="15c72-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="15c72-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="15c72-122">Header</span><span class="sxs-lookup"><span data-stu-id="15c72-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="15c72-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="15c72-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="15c72-124">DLL</span><span class="sxs-lookup"><span data-stu-id="15c72-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15c72-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15c72-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="15c72-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15c72-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c72-127">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="15c72-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="15c72-128">**Иконтекстноде:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="15c72-128">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="15c72-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="15c72-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




