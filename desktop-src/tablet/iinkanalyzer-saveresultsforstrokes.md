---
description: Сохраняет результаты анализа для указанных штрихов, связанных с Иинканализер.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Метод Иинканализер:: Савересултсфорстрокес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343675"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a><span data-ttu-id="dea19-103">Метод Иинканализер:: Савересултсфорстрокес</span><span class="sxs-lookup"><span data-stu-id="dea19-103">IInkAnalyzer::SaveResultsForStrokes method</span></span>

<span data-ttu-id="dea19-104">Сохраняет результаты анализа для указанных штрихов, связанных с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="dea19-104">Saves analysis results for the specified strokes associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dea19-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dea19-105">Syntax</span></span>


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="dea19-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dea19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dea19-107">*улстрокеидскаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dea19-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea19-108">Число идентификаторов Stroke в **плстрокеидс**.</span><span class="sxs-lookup"><span data-stu-id="dea19-108">The number of stroke identifiers in **plStrokeIds**.</span></span>

</dd> <dt>

<span data-ttu-id="dea19-109">*плстрокеидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dea19-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dea19-110">Массив идентификаторов Stroke.</span><span class="sxs-lookup"><span data-stu-id="dea19-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="dea19-111">*пулсериализеддатасизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dea19-111">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dea19-112">Число байтов в *ппбсериализеддата*.</span><span class="sxs-lookup"><span data-stu-id="dea19-112">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="dea19-113">*ппбсериализеддата* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="dea19-113">*ppbSerializedData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="dea19-114">Указатель на сериализованные данные анализа.</span><span class="sxs-lookup"><span data-stu-id="dea19-114">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dea19-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dea19-115">Return value</span></span>

<span data-ttu-id="dea19-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="dea19-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dea19-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dea19-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="dea19-118">Чтобы избежать утечки памяти, вызовите [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для \* *ппбсериализеддата* , когда информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="dea19-118">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="dea19-119">Этот метод сохраняет текущие результаты анализа для указанных штрихов.</span><span class="sxs-lookup"><span data-stu-id="dea19-119">This method saves the current analysis results for the specified strokes.</span></span> <span data-ttu-id="dea19-120">Этот метод сохраняет рукописные конечные объекты [**иконтекстноде**](icontextnode.md) , содержащие штрихи и все предки этих узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="dea19-120">This method saves the ink leaf [**IContextNode**](icontextnode.md) objects containing the strokes and all of the ancestors of those context nodes.</span></span> <span data-ttu-id="dea19-121">Этот метод не сохраняет никаких данных штриха или узлов указания анализа.</span><span class="sxs-lookup"><span data-stu-id="dea19-121">This method does not save any stroke data or analysis hint nodes.</span></span> <span data-ttu-id="dea19-122">Приложение отвечает за синхронизацию результатов анализа и соответствующих данных штриха, если оно сохраняется.</span><span class="sxs-lookup"><span data-stu-id="dea19-122">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="dea19-123">Этот метод возвращает код ошибки, когда объект [**иконтекстноде**](icontextnode.md) для сохранения частично заполняется (см. [**Иконтекстноде:: жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="dea19-123">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="dea19-124">Требования</span><span class="sxs-lookup"><span data-stu-id="dea19-124">Requirements</span></span>



| <span data-ttu-id="dea19-125">Требование</span><span class="sxs-lookup"><span data-stu-id="dea19-125">Requirement</span></span> | <span data-ttu-id="dea19-126">Значение</span><span class="sxs-lookup"><span data-stu-id="dea19-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea19-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dea19-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dea19-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dea19-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dea19-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dea19-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dea19-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dea19-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="dea19-131">Header</span><span class="sxs-lookup"><span data-stu-id="dea19-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea19-132"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dea19-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dea19-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dea19-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dea19-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dea19-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="dea19-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dea19-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea19-136">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="dea19-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="dea19-137">**Метод Иинканализер:: Лоадресултс**</span><span class="sxs-lookup"><span data-stu-id="dea19-137">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="dea19-138">**Метод Иинканализер:: Савересултс**</span><span class="sxs-lookup"><span data-stu-id="dea19-138">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="dea19-139">**Метод Иинканализер:: Савересултсфорнодес**</span><span class="sxs-lookup"><span data-stu-id="dea19-139">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="dea19-140">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="dea19-140">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="dea19-141">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="dea19-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

