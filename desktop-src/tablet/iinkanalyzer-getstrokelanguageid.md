---
description: Возвращает идентификатор локали указанного штриха.
ms.assetid: a5fb9b7a-ed3e-4552-9412-39529203bd81
title: 'Метод Иинканализер:: Жетстрокелангуажеид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a231dde453467ad2973d729fa068cedcc35151c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810001"
---
# <a name="iinkanalyzergetstrokelanguageid-method"></a><span data-ttu-id="ca0d2-103">Метод Иинканализер:: Жетстрокелангуажеид</span><span class="sxs-lookup"><span data-stu-id="ca0d2-103">IInkAnalyzer::GetStrokeLanguageId method</span></span>

<span data-ttu-id="ca0d2-104">Возвращает идентификатор локали указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-104">Returns the locale identifier of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca0d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca0d2-105">Syntax</span></span>


```C++
HRESULT GetStrokeLanguageId(
  [in]  LONG lStrokeId,
  [out] LONG *lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="ca0d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca0d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca0d2-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca0d2-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0d2-108">Идентификатор штриха.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ca0d2-109">*лстрокелЦид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ca0d2-109">*lStrokeLCID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0d2-110">Идентификатор локали для указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-110">The locale identifier for the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca0d2-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca0d2-111">Return value</span></span>

<span data-ttu-id="ca0d2-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ca0d2-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca0d2-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca0d2-113">Remarks</span></span>

<span data-ttu-id="ca0d2-114">Язык штриха задается при добавлении штриха путем вызова метода [**иинканализер:: аддстроке**](iinkanalyzer-addstroke.md), метода [**Иинканализер:: аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md), [**Иинканализер:: аддстрокес**](iinkanalyzer-addstrokes.md)или [**метода IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="ca0d2-114">The stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="ca0d2-115">Чтобы изменить языковой стандарт обводки, используйте [**метод иинканализер:: сетстрокелангуажеид**](iinkanalyzer-setstrokelanguageid.md) или [**метод Иинканализер:: сетстрокеслангуажеид**](iinkanalyzer-setstrokeslanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="ca0d2-115">To change the stroke's locale, use [**IInkAnalyzer::SetStrokeLanguageId Method**](iinkanalyzer-setstrokelanguageid.md) or [**IInkAnalyzer::SetStrokesLanguageId Method**](iinkanalyzer-setstrokeslanguageid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca0d2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ca0d2-116">Requirements</span></span>



| <span data-ttu-id="ca0d2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ca0d2-117">Requirement</span></span> | <span data-ttu-id="ca0d2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ca0d2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0d2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca0d2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0d2-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ca0d2-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca0d2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca0d2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0d2-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ca0d2-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ca0d2-123">Header</span><span class="sxs-lookup"><span data-stu-id="ca0d2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca0d2-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ca0d2-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ca0d2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ca0d2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca0d2-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca0d2-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ca0d2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca0d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca0d2-128">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="ca0d2-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ca0d2-129">**Метод Иинканализер:: Сетстрокелангуажеид**</span><span class="sxs-lookup"><span data-stu-id="ca0d2-129">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="ca0d2-130">**Метод Иинканализер:: Сетстрокеслангуажеид**</span><span class="sxs-lookup"><span data-stu-id="ca0d2-130">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="ca0d2-131">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="ca0d2-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




