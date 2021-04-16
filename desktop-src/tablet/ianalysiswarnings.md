---
description: Содержит коллекцию объектов, реализующих интерфейс Ианалисисварнинг и являющихся результатом операции анализа рукописного ввода.
ms.assetid: 2118c18b-d316-4e91-8652-62969115e8b5
title: Интерфейс Ианалисисварнингс (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 938d406ea90d86cc05ac84b69304b7a85e0e54fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692448"
---
# <a name="ianalysiswarnings-interface"></a><span data-ttu-id="727e1-103">Интерфейс Ианалисисварнингс</span><span class="sxs-lookup"><span data-stu-id="727e1-103">IAnalysisWarnings interface</span></span>

<span data-ttu-id="727e1-104">Содержит коллекцию объектов, реализующих интерфейс [**ианалисисварнинг**](ianalysiswarning.md) и являющихся результатом операции анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="727e1-104">Contains a collection of objects that implement the [**IAnalysisWarning**](ianalysiswarning.md) interface and that are the result of an ink analysis operation.</span></span>

## <a name="members"></a><span data-ttu-id="727e1-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="727e1-105">Members</span></span>

<span data-ttu-id="727e1-106">Интерфейс **ианалисисварнингс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="727e1-106">The **IAnalysisWarnings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="727e1-107">**Ианалисисварнингс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="727e1-107">**IAnalysisWarnings** also has these types of members:</span></span>

-   [<span data-ttu-id="727e1-108">Методы</span><span class="sxs-lookup"><span data-stu-id="727e1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="727e1-109">Методы</span><span class="sxs-lookup"><span data-stu-id="727e1-109">Methods</span></span>

<span data-ttu-id="727e1-110">Интерфейс **ианалисисварнингс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="727e1-110">The **IAnalysisWarnings** interface has these methods.</span></span>



| <span data-ttu-id="727e1-111">Метод</span><span class="sxs-lookup"><span data-stu-id="727e1-111">Method</span></span>                                                             | <span data-ttu-id="727e1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="727e1-112">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="727e1-113">**жетаналисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="727e1-113">**GetAnalysisWarning**</span></span>](ianalysiswarnings-getanalysiswarning.md) | <span data-ttu-id="727e1-114">Извлекает объект [**ианалисисварнинг**](ianalysiswarning.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="727e1-114">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span><br/>                                       |
| [<span data-ttu-id="727e1-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="727e1-115">**GetCount**</span></span>](ianalysiswarnings-getcount.md)                     | <span data-ttu-id="727e1-116">Возвращает количество объектов [**ианалисисварнинг**](ianalysiswarning.md) , содержащихся в коллекции **ианалисисварнингс** .</span><span class="sxs-lookup"><span data-stu-id="727e1-116">Retrieves the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the **IAnalysisWarnings** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="727e1-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="727e1-117">Examples</span></span>

<span data-ttu-id="727e1-118">В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="727e1-118">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="727e1-119">Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="727e1-119">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="727e1-120">Если операция анализа создавала предупреждения, обработчик выполняет итерацию по коллекции объектов [**ианалисисварнинг**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="727e1-120">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="727e1-121">Требования</span><span class="sxs-lookup"><span data-stu-id="727e1-121">Requirements</span></span>



| <span data-ttu-id="727e1-122">Требование</span><span class="sxs-lookup"><span data-stu-id="727e1-122">Requirement</span></span> | <span data-ttu-id="727e1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="727e1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="727e1-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="727e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="727e1-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="727e1-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="727e1-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="727e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="727e1-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="727e1-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="727e1-128">Header</span><span class="sxs-lookup"><span data-stu-id="727e1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="727e1-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="727e1-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="727e1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="727e1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="727e1-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="727e1-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="727e1-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="727e1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727e1-133">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="727e1-133">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="727e1-134">**ианалисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="727e1-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="727e1-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="727e1-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

