---
description: Извлекает объект Ианалисисварнинг по указанному индексу.
ms.assetid: 8f5d5642-73ec-496e-bad7-9f636fc00217
title: 'Метод Ианалисисварнингс:: Жетаналисисварнинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarnings.GetAnalysisWarning
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 88ed3686ecf3861a2b097ebfc005214ab0cdd1c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072785"
---
# <a name="ianalysiswarningsgetanalysiswarning-method"></a><span data-ttu-id="cf645-103">Метод Ианалисисварнингс:: Жетаналисисварнинг</span><span class="sxs-lookup"><span data-stu-id="cf645-103">IAnalysisWarnings::GetAnalysisWarning method</span></span>

<span data-ttu-id="cf645-104">Извлекает объект [**ианалисисварнинг**](ianalysiswarning.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="cf645-104">Retrieves the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf645-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf645-105">Syntax</span></span>


```C++
HRESULT GetAnalysisWarning(
  [in]  ULONG            ulIndex,
  [out] IAnalysisWarning **ppWarning
);
```



## <a name="parameters"></a><span data-ttu-id="cf645-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf645-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf645-107">*улиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf645-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf645-108">Отсчитываемый от нуля индекс объекта [**ианалисисварнинг**](ianalysiswarning.md) , который необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="cf645-108">The zero-based index of the [**IAnalysisWarning**](ianalysiswarning.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="cf645-109">*ппварнинг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cf645-109">*ppWarning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf645-110">Указатель на объект [**ианалисисварнинг**](ianalysiswarning.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="cf645-110">A pointer to the [**IAnalysisWarning**](ianalysiswarning.md) object at the specified index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf645-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf645-111">Return value</span></span>

<span data-ttu-id="cf645-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cf645-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf645-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf645-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cf645-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппварнинг* , когда больше не нужно использовать предупреждение.</span><span class="sxs-lookup"><span data-stu-id="cf645-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppWarning* when you no longer need to use the warning.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cf645-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="cf645-115">Examples</span></span>

<span data-ttu-id="cf645-116">В следующем примере показана структура обработчика событий для события [**\_ ианалисисевентс:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="cf645-116">The following example shows an outline of an event handler for the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span> <span data-ttu-id="cf645-117">Обработчик проверяет [**ианалисисстатус:: Success**](ianalysisstatus-issuccessful.md).</span><span class="sxs-lookup"><span data-stu-id="cf645-117">The handler checks [**IAnalysisStatus::IsSuccessful**](ianalysisstatus-issuccessful.md).</span></span> <span data-ttu-id="cf645-118">Если операция анализа создает предупреждения, обработчик выполняет итерацию по коллекции объектов [**ианалисисварнинг**](ianalysiswarning.md) .</span><span class="sxs-lookup"><span data-stu-id="cf645-118">If the analysis operation generates warnings, the handler iterates through the collection of [**IAnalysisWarning**](ianalysiswarning.md) objects.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cf645-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cf645-119">Requirements</span></span>



| <span data-ttu-id="cf645-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cf645-120">Requirement</span></span> | <span data-ttu-id="cf645-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cf645-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf645-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf645-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cf645-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cf645-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf645-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf645-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cf645-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cf645-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cf645-126">Header</span><span class="sxs-lookup"><span data-stu-id="cf645-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf645-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cf645-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cf645-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cf645-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf645-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf645-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cf645-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf645-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf645-131">**ианалисисварнингс**</span><span class="sxs-lookup"><span data-stu-id="cf645-131">**IAnalysisWarnings**</span></span>](ianalysiswarnings.md)
</dt> <dt>

[<span data-ttu-id="cf645-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="cf645-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

