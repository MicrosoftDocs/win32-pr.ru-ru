---
description: Возвращает количество объектов Ианалисисварнинг, содержащихся в коллекции Ианалисисварнингс.
ms.assetid: a0ad46d5-fb1b-40f6-bfc1-28ea1bf4eb44
title: 'Метод Ианалисисварнингс:: NOCOUNT (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc795d310f4bc532a39e2c1a2b4d2ba68f0401f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692449"
---
# <a name="ianalysiswarningsgetcount-method"></a><span data-ttu-id="31ece-103">Метод Ианалисисварнингс:: NOCOUNT</span><span class="sxs-lookup"><span data-stu-id="31ece-103">IAnalysisWarnings::GetCount method</span></span>

<span data-ttu-id="31ece-104">Возвращает количество объектов [**ианалисисварнинг**](ianalysiswarning.md) , содержащихся в коллекции [**ианалисисварнингс**](ianalysiswarnings.md) .</span><span class="sxs-lookup"><span data-stu-id="31ece-104">Gets the number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ece-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31ece-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="31ece-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="31ece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ece-107">*пулкаунт* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="31ece-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="31ece-108">Количество объектов [**ианалисисварнинг**](ianalysiswarning.md) , содержащихся в коллекции [**ианалисисварнингс**](ianalysiswarnings.md) .</span><span class="sxs-lookup"><span data-stu-id="31ece-108">The number of [**IAnalysisWarning**](ianalysiswarning.md) objects contained in the [**IAnalysisWarnings**](ianalysiswarnings.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31ece-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="31ece-109">Return value</span></span>

<span data-ttu-id="31ece-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="31ece-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="31ece-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="31ece-111">Examples</span></span>

<span data-ttu-id="31ece-112">В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="31ece-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="31ece-113">Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="31ece-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="31ece-114">Если операция анализа создает предупреждения, обработчик выполняет итерацию по коллекции объектов [**ианалисисварнинг**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="31ece-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="31ece-115">Требования</span><span class="sxs-lookup"><span data-stu-id="31ece-115">Requirements</span></span>



| <span data-ttu-id="31ece-116">Требование</span><span class="sxs-lookup"><span data-stu-id="31ece-116">Requirement</span></span> | <span data-ttu-id="31ece-117">Значение</span><span class="sxs-lookup"><span data-stu-id="31ece-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ece-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31ece-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31ece-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="31ece-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="31ece-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31ece-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31ece-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="31ece-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="31ece-122">Header</span><span class="sxs-lookup"><span data-stu-id="31ece-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ece-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="31ece-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="31ece-124">DLL</span><span class="sxs-lookup"><span data-stu-id="31ece-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31ece-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31ece-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="31ece-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31ece-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ece-127">**ианалисисварнингс**</span><span class="sxs-lookup"><span data-stu-id="31ece-127">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="31ece-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="31ece-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




