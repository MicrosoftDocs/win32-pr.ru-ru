---
description: Извлекает массив диапазонов символов, представляющих поддерживаемые диапазоны символов Юникода.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Метод Иинканалисисрекогнизер:: Жетуникодеранжес (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897474"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a><span data-ttu-id="4f19e-103">Метод Иинканалисисрекогнизер:: Жетуникодеранжес</span><span class="sxs-lookup"><span data-stu-id="4f19e-103">IInkAnalysisRecognizer::GetUnicodeRanges method</span></span>

<span data-ttu-id="4f19e-104">Извлекает массив диапазонов символов, представляющих поддерживаемые диапазоны символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="4f19e-104">Retrieves an array of character ranges representing the supported Unicode character ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f19e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f19e-105">Syntax</span></span>


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a><span data-ttu-id="4f19e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f19e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f19e-107">*пулнумберофранжес* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4f19e-107">*pulNumberOfRanges* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f19e-108">Число диапазонов символов, на которые указывает *ппулловуникоде*.</span><span class="sxs-lookup"><span data-stu-id="4f19e-108">The number of character ranges pointed to by *ppulLowUnicode*.</span></span>

</dd> <dt>

<span data-ttu-id="4f19e-109">*ппулловуникоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f19e-109">*ppulLowUnicode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f19e-110">Указатель на массив диапазонов символов, представляющий поддерживаемые диапазоны символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="4f19e-110">Pointer to an array of character ranges representing the supported Unicode character ranges.</span></span>

</dd> <dt>

<span data-ttu-id="4f19e-111">*ппусуникодеранжеленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f19e-111">*ppusUnicodeRangeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f19e-112">Указатель на массив значений, указывающий длину каждой точки массива по *ппулловуникоде*.</span><span class="sxs-lookup"><span data-stu-id="4f19e-112">Pointer to an array of values indicating the length of each array point to by *ppulLowUnicode*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f19e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f19e-113">Return value</span></span>

<span data-ttu-id="4f19e-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4f19e-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f19e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4f19e-115">Requirements</span></span>



| <span data-ttu-id="4f19e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4f19e-116">Requirement</span></span> | <span data-ttu-id="4f19e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4f19e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f19e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f19e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4f19e-119">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4f19e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4f19e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f19e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4f19e-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4f19e-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4f19e-122">Header</span><span class="sxs-lookup"><span data-stu-id="4f19e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f19e-123"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4f19e-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4f19e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4f19e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f19e-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f19e-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4f19e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f19e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f19e-127">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="4f19e-127">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




