---
description: Изменяет код локали для указанных штрихов.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'Метод Иинканализер:: Сетстрокеслангуажеид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701600"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a><span data-ttu-id="b3129-103">Метод Иинканализер:: Сетстрокеслангуажеид</span><span class="sxs-lookup"><span data-stu-id="b3129-103">IInkAnalyzer::SetStrokesLanguageId method</span></span>

<span data-ttu-id="b3129-104">Изменяет код локали для указанных штрихов.</span><span class="sxs-lookup"><span data-stu-id="b3129-104">Changes the locale identifier for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3129-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3129-105">Syntax</span></span>


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a><span data-ttu-id="b3129-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3129-107">*улстрокеидкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3129-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3129-108">Число идентификаторов Stroke в *плстрокес*.</span><span class="sxs-lookup"><span data-stu-id="b3129-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="b3129-109">*плстрокес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3129-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3129-110">Массив идентификаторов для штрихов, которым назначается идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="b3129-110">The array of identifiers for the strokes to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b3129-111">*лстрокеслЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3129-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3129-112">Идентификатор локали, присваиваемый штрихам.</span><span class="sxs-lookup"><span data-stu-id="b3129-112">The locale identifier to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3129-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3129-113">Return value</span></span>

<span data-ttu-id="b3129-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b3129-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3129-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3129-115">Remarks</span></span>

<span data-ttu-id="b3129-116">Языковой стандарт штриха задается при добавлении росчерка путем вызова метода [**иинканализер:: аддстроке**](iinkanalyzer-addstroke.md), метода [**Иинканализер:: аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md), [**Иинканализер:: аддстрокес**](iinkanalyzer-addstrokes.md)или [**метода IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="b3129-116">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="b3129-117">Чтобы получить языковой стандарт, назначенный для штриха, вызовите [**метод иинканализер:: жетстрокелангуажеид**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="b3129-117">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="b3129-118">Указанные штрихи перемещаются в неклассифицированный узел рукописного ввода (см. [**иконтекстноде:: GetType**](icontextnode-gettype.md)), который содержит штрихи того же языка.</span><span class="sxs-lookup"><span data-stu-id="b3129-118">The specified strokes are moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="b3129-119">Если такой [**иконтекстноде**](icontextnode.md) не существует, этот метод создает новый неклассифицированный узел рукописного ввода и перемещает в него штрихи.</span><span class="sxs-lookup"><span data-stu-id="b3129-119">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the strokes to it.</span></span> <span data-ttu-id="b3129-120">Неклассифицированный узел рукописного ввода — это **иконтекстноде** с типом унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="b3129-120">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="b3129-121">Если этот метод перемещает штрихи из [**иконтекстноде**](icontextnode.md) , который не является неклассифицированным узлом рукописного ввода, этот метод также добавляет ограничивающие прямоугольники обводки в «грязную» область анализатора рукописного ввода (см. [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="b3129-121">If this method moves strokes from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the strokes' bounding boxes to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="b3129-122">Этот метод не перемещает штрих, если параметр *лстрокелЦид* соответствует текущему идентификатору языка Stroke.</span><span class="sxs-lookup"><span data-stu-id="b3129-122">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="b3129-123">Если указанный штрих не связан с [**иинканализер**](iinkanalyzer.md), этот метод игнорирует идентификатор.</span><span class="sxs-lookup"><span data-stu-id="b3129-123">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="b3129-124">Если ни один из указанных штрихов не определяет штрих, связанный с [**иинканализер**](iinkanalyzer.md), этот метод возвращает значение без обновления **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="b3129-124">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="b3129-125">Этот метод возвращает код ошибки, если Строкеидс имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b3129-125">This method returns an error code when strokeIds is **NULL**.</span></span>

<span data-ttu-id="b3129-126">Дополнительные сведения об идентификаторах языков см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="b3129-126">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3129-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b3129-127">Requirements</span></span>



| <span data-ttu-id="b3129-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b3129-128">Requirement</span></span> | <span data-ttu-id="b3129-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b3129-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3129-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3129-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b3129-131">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b3129-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b3129-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3129-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b3129-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b3129-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b3129-134">Header</span><span class="sxs-lookup"><span data-stu-id="b3129-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3129-135"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b3129-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b3129-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b3129-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3129-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3129-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b3129-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3129-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3129-139">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="b3129-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b3129-140">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="b3129-140">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="b3129-141">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="b3129-141">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="b3129-142">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="b3129-142">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="b3129-143">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="b3129-143">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="b3129-144">**Метод Иинканализер:: Жетстрокелангуажеид**</span><span class="sxs-lookup"><span data-stu-id="b3129-144">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="b3129-145">**Метод Иинканализер:: Сетстрокелангуажеид**</span><span class="sxs-lookup"><span data-stu-id="b3129-145">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="b3129-146">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b3129-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

