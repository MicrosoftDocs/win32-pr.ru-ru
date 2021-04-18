---
description: Находит текстовый диапазон в распознанной строке, соответствующей коллекции объектов Иконтекстноде.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'Метод Иинканализер:: Жеттекстранжефромнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711110"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a><span data-ttu-id="634d9-103">Метод Иинканализер:: Жеттекстранжефромнодес</span><span class="sxs-lookup"><span data-stu-id="634d9-103">IInkAnalyzer::GetTextRangeFromNodes method</span></span>

<span data-ttu-id="634d9-104">Находит текстовый диапазон в распознанной строке, соответствующей коллекции объектов [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="634d9-104">Finds the text range in the recognized string that corresponds to a collection of [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="634d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="634d9-105">Syntax</span></span>


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a><span data-ttu-id="634d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="634d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="634d9-107">*плстарт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="634d9-107">*plStart* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="634d9-108">32-битовое целое число со знаком, которое указывает начало текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="634d9-108">A 32-bit signed integer that indicates the start of the text range.</span></span> <span data-ttu-id="634d9-109">Этот параметр передается неинициализированным.</span><span class="sxs-lookup"><span data-stu-id="634d9-109">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="634d9-110">*плленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="634d9-110">*plLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="634d9-111">32-битовое целое число со знаком, которое указывает длину текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="634d9-111">A 32-bit signed integer that indicates the length of the text range.</span></span> <span data-ttu-id="634d9-112">Этот параметр передается неинициализированным.</span><span class="sxs-lookup"><span data-stu-id="634d9-112">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="634d9-113">*пнодестосеарч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="634d9-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="634d9-114">Коллекция объектов [**иконтекстноде**](icontextnode.md) , для которых необходимо найти текстовый диапазон.</span><span class="sxs-lookup"><span data-stu-id="634d9-114">The collection of [**IContextNode**](icontextnode.md) objects for which to find the text range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="634d9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="634d9-115">Return value</span></span>

<span data-ttu-id="634d9-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="634d9-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="634d9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="634d9-117">Remarks</span></span>

<span data-ttu-id="634d9-118">Если *пнодестосеарч* содержит несмежные объекты [**иконтекстноде**](icontextnode.md) , этот метод возвращает наименьший текстовый диапазон, охватывающий все объекты **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="634d9-118">If *pNodesToSearch* contains [**IContextNode**](icontextnode.md) objects that are not adjacent, this method returns the smallest text range that covers all of the **IContextNode** objects.</span></span>

<span data-ttu-id="634d9-119">Этот метод создает исключение E \_ INVALIDARG, когда *Пнодестосеарч* содержит [**иконтекстноде**](icontextnode.md) , не связанный с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="634d9-119">This method throws an E\_INVALIDARG exception when *pNodesToSearch* contains an [**IContextNode**](icontextnode.md) that is not associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="634d9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="634d9-120">Requirements</span></span>



| <span data-ttu-id="634d9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="634d9-121">Requirement</span></span> | <span data-ttu-id="634d9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="634d9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="634d9-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="634d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="634d9-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="634d9-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="634d9-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="634d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="634d9-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="634d9-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="634d9-127">Header</span><span class="sxs-lookup"><span data-stu-id="634d9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="634d9-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="634d9-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="634d9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="634d9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="634d9-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="634d9-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="634d9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="634d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="634d9-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="634d9-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




