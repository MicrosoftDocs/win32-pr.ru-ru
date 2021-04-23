---
description: Представляет предупреждение или ошибку, возникающую во время операции анализа рукописного ввода.
ms.assetid: a9b0564b-8a49-44bc-9dbc-60a2fd5b60f2
title: Интерфейс Ианалисисварнинг (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79e865ac909d6f9ee1862926ffab06f538661d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145550"
---
# <a name="ianalysiswarning-interface"></a><span data-ttu-id="4a54d-103">Интерфейс Ианалисисварнинг</span><span class="sxs-lookup"><span data-stu-id="4a54d-103">IAnalysisWarning interface</span></span>

<span data-ttu-id="4a54d-104">Представляет предупреждение или ошибку, возникающую во время операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="4a54d-104">Represents a warning or error that occurs during an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="4a54d-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="4a54d-105">Members</span></span>

<span data-ttu-id="4a54d-106">Интерфейс **ианалисисварнинг** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4a54d-106">The **IAnalysisWarning** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4a54d-107">**Ианалисисварнинг** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4a54d-107">**IAnalysisWarning** also has these types of members:</span></span>

-   [<span data-ttu-id="4a54d-108">Методы</span><span class="sxs-lookup"><span data-stu-id="4a54d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4a54d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="4a54d-109">Methods</span></span>

<span data-ttu-id="4a54d-110">Интерфейс **ианалисисварнинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4a54d-110">The **IAnalysisWarning** interface has these methods.</span></span>



| <span data-ttu-id="4a54d-111">Метод</span><span class="sxs-lookup"><span data-stu-id="4a54d-111">Method</span></span>                                                            | <span data-ttu-id="4a54d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4a54d-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a54d-113">**жетбаккграундеррор**</span><span class="sxs-lookup"><span data-stu-id="4a54d-113">**GetBackgroundError**</span></span>](ianalysiswarning-getbackgrounderror.md) | <span data-ttu-id="4a54d-114">Возвращает код ошибки для фоновой операции анализа рукописного ввода, если произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="4a54d-114">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span><br/>                                    |
| [<span data-ttu-id="4a54d-115">**Указание**</span><span class="sxs-lookup"><span data-stu-id="4a54d-115">**GetHint**</span></span>](ianalysiswarning-gethint.md)                       | <span data-ttu-id="4a54d-116">Извлекает подсказку анализа, вызвавшую это предупреждение</span><span class="sxs-lookup"><span data-stu-id="4a54d-116">Retrieves the analysis hint that caused this warning</span></span><br/>                                                                        |
| [<span data-ttu-id="4a54d-117">**жетнодеидс**</span><span class="sxs-lookup"><span data-stu-id="4a54d-117">**GetNodeIds**</span></span>](ianalysiswarning-getnodeids.md)                 | <span data-ttu-id="4a54d-118">Возвращает идентификаторы всех соответствующих узлов контекста, связанных с данным предупреждением.</span><span class="sxs-lookup"><span data-stu-id="4a54d-118">Retrieves the identifiers of any relevant context nodes that are associated with this warning.</span></span><br/>                              |
| [<span data-ttu-id="4a54d-119">**жетварнингкоде**</span><span class="sxs-lookup"><span data-stu-id="4a54d-119">**GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)         | <span data-ttu-id="4a54d-120">Извлекает тип предупреждения, произошедшего с помощью перечисления [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="4a54d-120">Retrieves the type of warning that occurred by using the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a54d-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a54d-121">Remarks</span></span>

<span data-ttu-id="4a54d-122">Типы предупреждений, которые могут возникнуть, описаны перечислением [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode) .</span><span class="sxs-lookup"><span data-stu-id="4a54d-122">The types of warnings that can occur are described by the [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) enumeration.</span></span> <span data-ttu-id="4a54d-123">Часто предупреждения возникают при попытке использовать функцию, которая не поддерживается [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , используемой [**иинканализер**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="4a54d-123">Often warnings occur when you try to use a feature that is not supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that the [**IInkAnalyzer**](iinkanalyzer.md) is using.</span></span>

<span data-ttu-id="4a54d-124">Некоторые предупреждения указывают на то, что [**иинканализер**](iinkanalyzer.md) не завершил операцию анализа.</span><span class="sxs-lookup"><span data-stu-id="4a54d-124">Some warnings indicate that the [**IInkAnalyzer**](iinkanalyzer.md) did not complete the analysis operation.</span></span> <span data-ttu-id="4a54d-125">Дополнительные сведения см. в разделе [**аналисисварнингкоде**](/windows/desktop/tablet/analysiswarningcode).</span><span class="sxs-lookup"><span data-stu-id="4a54d-125">For more information, see [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode).</span></span>

## <a name="examples"></a><span data-ttu-id="4a54d-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="4a54d-126">Examples</span></span>

<span data-ttu-id="4a54d-127">В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="4a54d-127">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="4a54d-128">Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="4a54d-128">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="4a54d-129">Если операция анализа создает предупреждения, обработчик выполняет итерацию по коллекции объектов **ианалисисварнинг** .</span><span class="sxs-lookup"><span data-stu-id="4a54d-129">If the analysis operation generates warnings, the handler iterates through the collection of **IAnalysisWarning** objects.</span></span>


```C++
// _IAnalysisEvents::Results event handler.
STDMETHODIMP CMyClass::Results(
    IInkAnalyzer *pInkAnalyzer,
    IAnalysisStatus *pAnalysisStatus)
{
    // Check the status of the analysis operation.
    VARIANT_BOOL bResult = VARIANT_FALSE;
    HRESULT hr = pAnalysisStatus->IsSuccessful(&bResult);

    if( SUCCEEDED(hr) )
    {
        if( bResult )
        {
            // Insert code that handles a successful result.
        }
        else
        {
            // Get the analysis warnings.
            IAnalysisWarnings* pAnalysisWarnings = NULL;
            hr = pAnalysisStatus->GetWarnings(&pAnalysisWarnings);
            if (SUCCEEDED(hr))
            {
                // Iterate through the warning collection.
                ULONG warningCount = 0;
                hr = pAnalysisWarnings->GetCount(&warningCount);
                if (SUCCEEDED(hr))
                {
                    IAnalysisWarning *pAnalysisWarning = NULL;
                    AnalysisWarningCode analysisWarningCode;
                    for (ULONG index=0; index<warningCount; index++)
                    {
                        // Get an analysis warning.
                        hr = pAnalysisWarnings->GetAnalysisWarning(
                            index, &pAnalysisWarning);

                        if (SUCCEEDED(hr))
                        {
                            // Get the warning code for the warning.
                            hr = pAnalysisWarning->GetWarningCode(
                                &analysisWarningCode);

                            if (SUCCEEDED(hr))
                            {
                                // Insert code that handles each
                                // analysis warning.
                            }
                        }

                        // Release this reference to the analysis warning.
                        if (pAnalysisWarning != NULL)
                        {
                            pAnalysisWarning->Release();
                            pAnalysisWarning = NULL;
                        }

                        if (FAILED(hr))
                        {
                            break;
                        }
                    }
                }
            }

            // Release this reference to the analysis warnings collection.
            if (pAnalysisWarnings != NULL)
            {
                pAnalysisWarnings->Release();
                pAnalysisWarnings = NULL;
            }
        }
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="4a54d-130">Требования</span><span class="sxs-lookup"><span data-stu-id="4a54d-130">Requirements</span></span>



| <span data-ttu-id="4a54d-131">Требование</span><span class="sxs-lookup"><span data-stu-id="4a54d-131">Requirement</span></span> | <span data-ttu-id="4a54d-132">Значение</span><span class="sxs-lookup"><span data-stu-id="4a54d-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a54d-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a54d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4a54d-134">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4a54d-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4a54d-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a54d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4a54d-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4a54d-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4a54d-137">Header</span><span class="sxs-lookup"><span data-stu-id="4a54d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a54d-138"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4a54d-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4a54d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4a54d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a54d-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a54d-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4a54d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a54d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a54d-142">**ианалисисварнингс**</span><span class="sxs-lookup"><span data-stu-id="4a54d-142">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="4a54d-143">**аналисисварнингкоде**</span><span class="sxs-lookup"><span data-stu-id="4a54d-143">**AnalysisWarningCode**</span></span>](analysiswarningcode.md)
</dt> <dt>

[<span data-ttu-id="4a54d-144">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="4a54d-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

