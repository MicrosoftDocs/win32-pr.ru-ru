---
description: Возвращает тип предупреждения, произошедшего с помощью перечисления Аналисисварнингкоде.
ms.assetid: ec67a5ac-a7a2-4805-b9b5-915ea956d228
title: 'Метод Ианалисисварнинг:: Жетварнингкоде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetWarningCode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8e129b410de9e8ca9e3944b6a371fe0cac673fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711141"
---
# <a name="ianalysiswarninggetwarningcode-method"></a><span data-ttu-id="2d9d1-103">Метод Ианалисисварнинг:: Жетварнингкоде</span><span class="sxs-lookup"><span data-stu-id="2d9d1-103">IAnalysisWarning::GetWarningCode method</span></span>

<span data-ttu-id="2d9d1-104">Возвращает тип предупреждения, произошедшего с помощью перечисления [**аналисисварнингкоде**](analysiswarningcode.md) .</span><span class="sxs-lookup"><span data-stu-id="2d9d1-104">Returns the type of warning that occurred by using the [**AnalysisWarningCode**](analysiswarningcode.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d9d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d9d1-105">Syntax</span></span>


```C++
HRESULT GetWarningCode(
  [out] AnalysisWarningCode *pWarningCode
);
```



## <a name="parameters"></a><span data-ttu-id="2d9d1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d9d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d9d1-107">*пварнингкоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2d9d1-107">*pWarningCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d9d1-108">Тип произошедшего предупреждения.</span><span class="sxs-lookup"><span data-stu-id="2d9d1-108">The type of warning that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d9d1-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d9d1-109">Return value</span></span>

<span data-ttu-id="2d9d1-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2d9d1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2d9d1-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="2d9d1-111">Examples</span></span>

<span data-ttu-id="2d9d1-112">В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="2d9d1-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="2d9d1-113">Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="2d9d1-113">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="2d9d1-114">Если операция анализа создавала предупреждения, обработчик выполняет итерацию по коллекции объектов [**ианалисисварнинг**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="2d9d1-114">If the analysis operation generated warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2d9d1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="2d9d1-115">Requirements</span></span>



| <span data-ttu-id="2d9d1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="2d9d1-116">Requirement</span></span> | <span data-ttu-id="2d9d1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="2d9d1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d9d1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d9d1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d9d1-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2d9d1-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2d9d1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d9d1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d9d1-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2d9d1-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2d9d1-122">Header</span><span class="sxs-lookup"><span data-stu-id="2d9d1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d9d1-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2d9d1-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2d9d1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2d9d1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d9d1-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d9d1-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2d9d1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d9d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d9d1-127">**ианалисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="2d9d1-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="2d9d1-128">**аналисисварнингкоде**</span><span class="sxs-lookup"><span data-stu-id="2d9d1-128">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="2d9d1-129">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2d9d1-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

