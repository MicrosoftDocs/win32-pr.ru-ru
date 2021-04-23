---
description: Возвращает наиболее подходящую строку результатов операции распознавания для всего дерева узлов контекста в Иинканализер.
ms.assetid: 4aa57f41-3122-47a9-a60d-4a229e23f63c
title: 'Метод Иинканализер:: Жетрекогнизедстринг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67afe9909fcabb8df880706b2b077ea602ccade6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810006"
---
# <a name="iinkanalyzergetrecognizedstring-method"></a><span data-ttu-id="55fab-103">Метод Иинканализер:: Жетрекогнизедстринг</span><span class="sxs-lookup"><span data-stu-id="55fab-103">IInkAnalyzer::GetRecognizedString method</span></span>

<span data-ttu-id="55fab-104">Возвращает наиболее подходящую строку результатов операции распознавания для всего дерева узлов контекста в [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="55fab-104">Retrieves the best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="55fab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55fab-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="55fab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55fab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55fab-107">*пбстррекогнизедстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="55fab-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55fab-108">Наиболее подходящий результат операции распознавания для всего дерева узлов контекста в [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="55fab-108">The best-result string of the recognition operation for the entire context node tree in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55fab-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55fab-109">Return value</span></span>

<span data-ttu-id="55fab-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="55fab-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55fab-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55fab-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="55fab-112">Чтобы избежать утечки памяти, вызовите [**сисфристринг**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) для *пбстррекогнизедстринг* , когда больше не нужно использовать строку.</span><span class="sxs-lookup"><span data-stu-id="55fab-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) for *pbstrRecognizedString* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="55fab-113">Этот метод возвращает то же значение, что и данные свойства корневого узла для распознанной строки.</span><span class="sxs-lookup"><span data-stu-id="55fab-113">This method returns the same value as the root node's property data for the recognized string.</span></span> <span data-ttu-id="55fab-114">(См. раздел [**иинканализер:: Жетрутноде Method**](iinkanalyzer-getrootnode.md), [**Иконтекстноде:: Жетпропертидата**](icontextnode-getpropertydata.md)и [Свойства контекстного узла](context-node-properties.md).)</span><span class="sxs-lookup"><span data-stu-id="55fab-114">(See [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md), [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md), and [Context Node Properties](context-node-properties.md).)</span></span>

## <a name="examples"></a><span data-ttu-id="55fab-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="55fab-115">Examples</span></span>

<span data-ttu-id="55fab-116">В следующем примере показан метод, который просматривает дерево результатов [**иконтекстноде**](icontextnode.md) анализатора рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="55fab-116">The following example shows a method that walks the ink analyzer's [**IContextNode**](icontextnode.md) results tree.</span></span> <span data-ttu-id="55fab-117">Если Иинканлизер в настоящее время не выполняет анализ рукописного ввода, метод выполняет следующие операции.</span><span class="sxs-lookup"><span data-stu-id="55fab-117">If the IInkAnlyzer is not currently performing ink analysis, the method does the following.</span></span>

-   <span data-ttu-id="55fab-118">Возвращает верхнюю строку распознавания.</span><span class="sxs-lookup"><span data-stu-id="55fab-118">Gets the top recognition string.</span></span>
-   <span data-ttu-id="55fab-119">Возвращает корневой узел анализатора рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="55fab-119">Gets the ink analyzer's root node.</span></span>
-   <span data-ttu-id="55fab-120">Вызывает вспомогательный метод, `ExploreContextNode` для проверки корневого узла и его дочерних узлов.</span><span class="sxs-lookup"><span data-stu-id="55fab-120">Calls a helper method, `ExploreContextNode`, to examine the root node and its child nodes.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="55fab-121">Требования</span><span class="sxs-lookup"><span data-stu-id="55fab-121">Requirements</span></span>



| <span data-ttu-id="55fab-122">Требование</span><span class="sxs-lookup"><span data-stu-id="55fab-122">Requirement</span></span> | <span data-ttu-id="55fab-123">Значение</span><span class="sxs-lookup"><span data-stu-id="55fab-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55fab-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55fab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="55fab-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="55fab-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55fab-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55fab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="55fab-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="55fab-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="55fab-128">Header</span><span class="sxs-lookup"><span data-stu-id="55fab-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="55fab-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55fab-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55fab-130">DLL</span><span class="sxs-lookup"><span data-stu-id="55fab-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55fab-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55fab-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="55fab-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55fab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55fab-133">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="55fab-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="55fab-134">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="55fab-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

