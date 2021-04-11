---
description: Сохраняет результаты анализа для определенной коллекции узлов контекста, связанной с Иинканализер.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Метод Иинканализер:: Савересултсфорнодес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145442"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a><span data-ttu-id="4ccc2-103">Метод Иинканализер:: Савересултсфорнодес</span><span class="sxs-lookup"><span data-stu-id="4ccc2-103">IInkAnalyzer::SaveResultsForNodes method</span></span>

<span data-ttu-id="4ccc2-104">Сохраняет результаты анализа для определенной коллекции узлов контекста, связанной с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="4ccc2-104">Saves analysis results for a specific context node collection associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ccc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ccc2-105">Syntax</span></span>


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="4ccc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ccc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ccc2-107">*пконтекстнодес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4ccc2-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc2-108">Коллекция [**иконтекстноде**](icontextnode.md) , для которой необходимо сохранить результаты анализа.</span><span class="sxs-lookup"><span data-stu-id="4ccc2-108">The [**IContextNode**](icontextnode.md) collection for which to save analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc2-109">*пулсериализеддатасизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4ccc2-109">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc2-110">Число байтов в *ппбсериализеддата*.</span><span class="sxs-lookup"><span data-stu-id="4ccc2-110">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="4ccc2-111">*ппбсериализеддата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4ccc2-111">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ccc2-112">Указатель на сериализованные данные анализа.</span><span class="sxs-lookup"><span data-stu-id="4ccc2-112">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ccc2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4ccc2-113">Return value</span></span>

<span data-ttu-id="4ccc2-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4ccc2-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4ccc2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4ccc2-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4ccc2-116">Чтобы избежать утечки памяти, вызовите [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) для \* *ппбсериализеддата* , когда информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="4ccc2-116">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="4ccc2-117">Этот метод сохраняет текущие результаты анализа для объектов [**иконтекстноде**](icontextnode.md) в *пконтекстнодес* и всех их предков и узлов контекста потомков.</span><span class="sxs-lookup"><span data-stu-id="4ccc2-117">This method saves the current analysis results for the [**IContextNode**](icontextnode.md) objects in *pContextNodes* and all of their ancestor and descendant context nodes.</span></span> <span data-ttu-id="4ccc2-118">Этот метод не сохраняет данные росчерка.</span><span class="sxs-lookup"><span data-stu-id="4ccc2-118">This method does not save any stroke data.</span></span> <span data-ttu-id="4ccc2-119">Приложение отвечает за синхронизацию результатов анализа и соответствующих данных штриха, если оно сохраняется.</span><span class="sxs-lookup"><span data-stu-id="4ccc2-119">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="4ccc2-120">Если объект [**иконтекстноде**](icontextnode.md) для сохранения заполняется только частично, этот метод возвращает код ошибки (см. [**Иконтекстноде:: жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="4ccc2-120">If the [**IContextNode**](icontextnode.md) object to be saved is only partially populated, this method returns an error code (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ccc2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4ccc2-121">Requirements</span></span>



| <span data-ttu-id="4ccc2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4ccc2-122">Requirement</span></span> | <span data-ttu-id="4ccc2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4ccc2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ccc2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4ccc2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4ccc2-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4ccc2-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4ccc2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4ccc2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4ccc2-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4ccc2-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4ccc2-128">Header</span><span class="sxs-lookup"><span data-stu-id="4ccc2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ccc2-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4ccc2-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4ccc2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4ccc2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ccc2-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ccc2-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4ccc2-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ccc2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ccc2-133">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="4ccc2-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4ccc2-134">**Метод Иинканализер:: Лоадресултс**</span><span class="sxs-lookup"><span data-stu-id="4ccc2-134">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="4ccc2-135">**Метод Иинканализер:: Савересултс**</span><span class="sxs-lookup"><span data-stu-id="4ccc2-135">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="4ccc2-136">**Метод Иинканализер:: Савересултсфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="4ccc2-136">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="4ccc2-137">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="4ccc2-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="4ccc2-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="4ccc2-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

