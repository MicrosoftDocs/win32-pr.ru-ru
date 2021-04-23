---
description: Извлекает 10 альтернативных вариантов анализа для всех рукописных данных, связанных с Иинканализер.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: Метод Иинканализер::-alternate (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682738"
---
# <a name="iinkanalyzergetalternates-method"></a><span data-ttu-id="ef6b6-103">Метод Иинканализер:: Alternate</span><span class="sxs-lookup"><span data-stu-id="ef6b6-103">IInkAnalyzer::GetAlternates method</span></span>

<span data-ttu-id="ef6b6-104">Извлекает 10 альтернативных вариантов анализа для всех рукописных данных, связанных с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ef6b6-104">Retrieves 10 analysis alternates for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef6b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef6b6-105">Syntax</span></span>


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="ef6b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef6b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef6b6-107">*ппалтернатес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef6b6-107">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef6b6-108">Указатель на 10 лучших объектов [**ианалисисалтернате**](ianalysisalternate.md) для всех рукописных данных, связанных с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ef6b6-108">A pointer to the top 10 [**IAnalysisAlternate**](ianalysisalternate.md) objects for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef6b6-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef6b6-109">Return value</span></span>

<span data-ttu-id="ef6b6-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ef6b6-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef6b6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef6b6-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ef6b6-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппалтернатес* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="ef6b6-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="ef6b6-113">Верхний альтернативный вариант возвращается в качестве первого альтернативы коллекции.</span><span class="sxs-lookup"><span data-stu-id="ef6b6-113">The top alternate is returned as the first alternate of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef6b6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ef6b6-114">Requirements</span></span>



| <span data-ttu-id="ef6b6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ef6b6-115">Requirement</span></span> | <span data-ttu-id="ef6b6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ef6b6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b6-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef6b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ef6b6-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ef6b6-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ef6b6-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef6b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ef6b6-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ef6b6-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ef6b6-121">Header</span><span class="sxs-lookup"><span data-stu-id="ef6b6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef6b6-122"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ef6b6-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ef6b6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ef6b6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef6b6-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef6b6-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ef6b6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef6b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef6b6-126">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ef6b6-127">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-127">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="ef6b6-128">**ианалисисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-128">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="ef6b6-129">**Метод Иинканализер:: Жеталтернатесфорконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-129">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="ef6b6-130">**Метод Иинканализер:: Жеталтернатесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-130">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="ef6b6-131">**Метод Иинканализер:: Модифитопалтернате**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-131">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="ef6b6-132">**Метод Иинканализер:: Модифитопалтернатевисконфирматион**</span><span class="sxs-lookup"><span data-stu-id="ef6b6-132">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="ef6b6-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ef6b6-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

