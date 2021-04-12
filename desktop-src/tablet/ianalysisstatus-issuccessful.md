---
description: Извлекает логическую сводку результатов операции анализа.
ms.assetid: 9bc690f4-fb5f-449e-bde0-bd2277c4573b
title: 'Метод Ианалисисстатус:: Success (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.IsSuccessful
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: daf7ec801773d855f0ed85a795bc492ef673a74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343735"
---
# <a name="ianalysisstatusissuccessful-method"></a><span data-ttu-id="ec8cf-103">Метод Ианалисисстатус:: Success</span><span class="sxs-lookup"><span data-stu-id="ec8cf-103">IAnalysisStatus::IsSuccessful method</span></span>

<span data-ttu-id="ec8cf-104">Извлекает логическую сводку результатов операции анализа.</span><span class="sxs-lookup"><span data-stu-id="ec8cf-104">Retrieves a Boolean summary of the results of the analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec8cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec8cf-105">Syntax</span></span>


```C++
HRESULT IsSuccessful(
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a><span data-ttu-id="ec8cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec8cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec8cf-107">*пфсукцессфул* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ec8cf-107">*pfSuccessful* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec8cf-108">**Вариант \_ Значение TRUE** , если операция анализа завершилась без предупреждений, или **вариант \_ false** , если возникло хотя бы одно предупреждение.</span><span class="sxs-lookup"><span data-stu-id="ec8cf-108">**VARIANT\_TRUE** if the analysis operation completed without any warnings, or **VARIANT\_FALSE** if at least one warning occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec8cf-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec8cf-109">Return value</span></span>

<span data-ttu-id="ec8cf-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ec8cf-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ec8cf-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="ec8cf-111">Examples</span></span>

<span data-ttu-id="ec8cf-112">В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8cf-112">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="ec8cf-113">Обработчик проверяет **ианалисисстатус:: Success**.</span><span class="sxs-lookup"><span data-stu-id="ec8cf-113">The handler checks **IAnalysisStatus::IsSuccessful**.</span></span> <span data-ttu-id="ec8cf-114">Если операция анализа создает предупреждения, обработчик выполняет итерацию по коллекции объектов [**ианалисисварнинг**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8cf-114">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ec8cf-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ec8cf-115">Requirements</span></span>



| <span data-ttu-id="ec8cf-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ec8cf-116">Requirement</span></span> | <span data-ttu-id="ec8cf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ec8cf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8cf-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec8cf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ec8cf-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ec8cf-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ec8cf-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec8cf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ec8cf-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ec8cf-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ec8cf-122">Header</span><span class="sxs-lookup"><span data-stu-id="ec8cf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec8cf-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec8cf-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec8cf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ec8cf-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec8cf-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec8cf-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ec8cf-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec8cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8cf-127">**ианалисисстатус**</span><span class="sxs-lookup"><span data-stu-id="ec8cf-127">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="ec8cf-128">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ec8cf-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




