---
description: Извлекает значение, указывающее, выполняет ли Иинканализер анализ рукописного ввода.
ms.assetid: 3f3f6f29-0c90-47e1-938c-f1ce6ed8df47
title: 'Метод Иинканализер:: (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.IsAnalyzing
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94275d157b2936b7ad0ae16d4d70b62475f19af9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542010"
---
# <a name="iinkanalyzerisanalyzing-method"></a><span data-ttu-id="31ece-103">Метод Иинканализер::</span><span class="sxs-lookup"><span data-stu-id="31ece-103">IInkAnalyzer::IsAnalyzing method</span></span>

<span data-ttu-id="31ece-104">Извлекает значение, указывающее, выполняет ли [**иинканализер**](iinkanalyzer.md) анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="31ece-104">Retrieves a value indicating whether the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ece-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31ece-105">Syntax</span></span>


```C++
HRESULT IsAnalyzing(
  [out] VARIANT_BOOL *pbAnalyzing
);
```



## <a name="parameters"></a><span data-ttu-id="31ece-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31ece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ece-107">*пбанализинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="31ece-107">*pbAnalyzing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31ece-108">**Вариант \_ Значение TRUE** , если [**иинканализер**](iinkanalyzer.md) выполняет анализ рукописного ввода; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="31ece-108">**VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ece-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31ece-109">Return value</span></span>

<span data-ttu-id="31ece-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="31ece-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31ece-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31ece-111">Remarks</span></span>

<span data-ttu-id="31ece-112">Это свойство имеет **значение \_ true** , если [**иинканализер**](iinkanalyzer.md) выполняет синхронный или асинхронный анализ.</span><span class="sxs-lookup"><span data-stu-id="31ece-112">This property is **VARIANT\_TRUE** if the [**IInkAnalyzer**](iinkanalyzer.md) is performing synchronous or asynchronous analysis.</span></span>

## <a name="examples"></a><span data-ttu-id="31ece-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="31ece-113">Examples</span></span>

<span data-ttu-id="31ece-114">В следующем примере показан метод, который просматривает дерево результатов [**иконтекстноде**](icontextnode.md) анализатора рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="31ece-114">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="31ece-115">Если анализатор рукописного ввода в настоящее время не выполняет анализ рукописного ввода, метод выполняет следующие операции.</span><span class="sxs-lookup"><span data-stu-id="31ece-115">If the ink analyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="31ece-116">Возвращает верхнюю строку распознавания.</span><span class="sxs-lookup"><span data-stu-id="31ece-116">Gets the top recognition string.</span></span>
-   <span data-ttu-id="31ece-117">Возвращает корневой узел анализатора рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="31ece-117">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="31ece-118">Вызывает вспомогательный метод, `ExploreContextNode` для проверки корневого узла и его дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="31ece-118">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


```C++
// Helper method that explores the current analysis results of an ink analyzer.
HRESULT CMyClass::ExploreAnalysisResults(
    IInkAnalyzer *pInkAnalyzer)
{
    // Check that the ink analyzer is not currently analyzing ink.
    VARIANT_BOOL bIsAnalyzing;
    HRESULT hr = pInkAnalyzer->IsAnalyzing(&bIsAnalyzing);

    if (SUCCEEDED(hr))
    {
        if (bIsAnalyzing)
        {
            return E_PENDING;
        }

        // Get the ink analyzer's best-result string.
        BSTR recognizedString = NULL;
        hr = pInkAnalyzer->GetRecognizedString(&recognizedString);

        if (SUCCEEDED(hr))
        {
            // Insert code that records the ink analyzer's best-result string here.

            // Get the ink analyzer's root node.
            IContextNode *pRootNode = NULL;
            hr = pInkAnalyzer->GetRootNode(&pRootNode);

            if (SUCCEEDED(hr))
            {
                // Call a helper method that recursively explores context
                // nodes and their subnodes.
                hr = this->ExploreContextNode(pRootNode);
            }

            // Release this reference to the root node.
            if (pRootNode != NULL)
            {
                pRootNode->Release();
                pRootNode = NULL;
            }
        }

        // Free the system resources for the recognized string.
        SysFreeString(recognizedString);
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="31ece-119">Требования</span><span class="sxs-lookup"><span data-stu-id="31ece-119">Requirements</span></span>



| <span data-ttu-id="31ece-120">Требование</span><span class="sxs-lookup"><span data-stu-id="31ece-120">Requirement</span></span> | <span data-ttu-id="31ece-121">Значение</span><span class="sxs-lookup"><span data-stu-id="31ece-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ece-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31ece-122">Minimum supported client</span></span><br/> | <span data-ttu-id="31ece-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="31ece-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="31ece-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31ece-124">Minimum supported server</span></span><br/> | <span data-ttu-id="31ece-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="31ece-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="31ece-126">Header</span><span class="sxs-lookup"><span data-stu-id="31ece-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ece-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="31ece-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="31ece-128">DLL</span><span class="sxs-lookup"><span data-stu-id="31ece-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31ece-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31ece-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="31ece-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31ece-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ece-131">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="31ece-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="31ece-132">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="31ece-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="31ece-133">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="31ece-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="31ece-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="31ece-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




