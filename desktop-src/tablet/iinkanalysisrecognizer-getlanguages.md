---
description: Получает идентификаторы для языковых стандартов, которые поддерживает эта Иинканалисисрекогнизер.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: Метод иинканалисисрекогнизер::-languageing (иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897477"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a><span data-ttu-id="55778-103">Метод Иинканалисисрекогнизер:: WebMethod</span><span class="sxs-lookup"><span data-stu-id="55778-103">IInkAnalysisRecognizer::GetLanguages method</span></span>

<span data-ttu-id="55778-104">Получает идентификаторы для языковых стандартов, которые поддерживает эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="55778-104">Retrieves the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="55778-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55778-105">Syntax</span></span>


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a><span data-ttu-id="55778-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="55778-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55778-107">*пуллангуажескаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="55778-107">*pulLanguagesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="55778-108">Число идентификаторов в *ппуллангуажес*.</span><span class="sxs-lookup"><span data-stu-id="55778-108">The number of identifiers in *ppulLanguages*.</span></span>

</dd> <dt>

<span data-ttu-id="55778-109">*ппуллангуажес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="55778-109">*ppulLanguages* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55778-110">Указатель на идентификаторы языковых стандартов, которые поддерживает эта [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="55778-110">A pointer to the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55778-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55778-111">Return value</span></span>

<span data-ttu-id="55778-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="55778-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55778-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55778-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="55778-114">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппуллангуажес* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="55778-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppulLanguages* when you no longer need the information.</span></span>

 

<span data-ttu-id="55778-115">Этот метод возвращает пустой массив для распознавателей объектов и жестов.</span><span class="sxs-lookup"><span data-stu-id="55778-115">This method returns an empty array for object and gesture recognizers.</span></span>

<span data-ttu-id="55778-116">Дополнительные сведения об идентификаторах языков см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="55778-116">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="55778-117">Требования</span><span class="sxs-lookup"><span data-stu-id="55778-117">Requirements</span></span>



| <span data-ttu-id="55778-118">Требование</span><span class="sxs-lookup"><span data-stu-id="55778-118">Requirement</span></span> | <span data-ttu-id="55778-119">Значение</span><span class="sxs-lookup"><span data-stu-id="55778-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55778-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55778-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55778-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="55778-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55778-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55778-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55778-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="55778-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="55778-124">Header</span><span class="sxs-lookup"><span data-stu-id="55778-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="55778-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55778-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55778-126">DLL</span><span class="sxs-lookup"><span data-stu-id="55778-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55778-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55778-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="55778-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55778-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55778-129">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="55778-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="55778-130">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="55778-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

