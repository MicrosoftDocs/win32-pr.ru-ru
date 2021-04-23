---
description: Сохраняет все результаты анализа для Иинканализер.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'Метод Иинканализер:: Савересултс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343682"
---
# <a name="iinkanalyzersaveresults-method"></a><span data-ttu-id="20208-103">Метод Иинканализер:: Савересултс</span><span class="sxs-lookup"><span data-stu-id="20208-103">IInkAnalyzer::SaveResults method</span></span>

<span data-ttu-id="20208-104">Сохраняет все результаты анализа для [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="20208-104">Saves all analysis results for an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="20208-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20208-105">Syntax</span></span>


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="20208-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="20208-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20208-107">*пулсериализеддатасизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="20208-107">*pulSerializedDataSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20208-108">Число байтов в *ппбсериализеддата*.</span><span class="sxs-lookup"><span data-stu-id="20208-108">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="20208-109">*ппбсериализеддата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="20208-109">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20208-110">Массив, содержащий сохраненные результаты анализа.</span><span class="sxs-lookup"><span data-stu-id="20208-110">An array containing the saved analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20208-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20208-111">Return value</span></span>

<span data-ttu-id="20208-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="20208-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20208-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20208-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="20208-114">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппбсериализеддата* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="20208-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="20208-115">Этот метод сохраняет все текущие результаты анализа, включая текущую подсказку анализа и пользовательские узлы распознавателя (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="20208-115">This method saves all the current analysis results, which include current analysis hint and custom recognizer nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="20208-116">Этот метод не сохраняет данные росчерка.</span><span class="sxs-lookup"><span data-stu-id="20208-116">This method does not save any stroke data.</span></span> <span data-ttu-id="20208-117">При сохранении данных приложение отвечает за синхронизацию результатов анализа и соответствующих штрихов.</span><span class="sxs-lookup"><span data-stu-id="20208-117">It is the responsibility of your application to synchronize any analysis results and corresponding strokes if it persists data.</span></span>

<span data-ttu-id="20208-118">Этот метод возвращает код ошибки, когда объект [**иконтекстноде**](icontextnode.md) для сохранения частично заполняется (см. [**Иконтекстноде:: жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="20208-118">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="20208-119">Требования</span><span class="sxs-lookup"><span data-stu-id="20208-119">Requirements</span></span>



| <span data-ttu-id="20208-120">Требование</span><span class="sxs-lookup"><span data-stu-id="20208-120">Requirement</span></span> | <span data-ttu-id="20208-121">Значение</span><span class="sxs-lookup"><span data-stu-id="20208-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20208-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20208-122">Minimum supported client</span></span><br/> | <span data-ttu-id="20208-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="20208-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20208-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20208-124">Minimum supported server</span></span><br/> | <span data-ttu-id="20208-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="20208-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="20208-126">Header</span><span class="sxs-lookup"><span data-stu-id="20208-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="20208-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="20208-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="20208-128">DLL</span><span class="sxs-lookup"><span data-stu-id="20208-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20208-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20208-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="20208-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20208-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20208-131">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="20208-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="20208-132">**Метод Иинканализер:: Лоадресултс**</span><span class="sxs-lookup"><span data-stu-id="20208-132">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="20208-133">**Метод Иинканализер:: Савересултсфорнодес**</span><span class="sxs-lookup"><span data-stu-id="20208-133">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="20208-134">**Метод Иинканализер:: Савересултсфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="20208-134">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="20208-135">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="20208-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="20208-136">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="20208-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

