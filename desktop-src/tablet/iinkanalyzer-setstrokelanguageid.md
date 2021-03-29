---
description: Изменяет код локали для указанного штриха.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'Метод Иинканализер:: Сетстрокелангуажеид (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541991"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a><span data-ttu-id="af9c8-103">Метод Иинканализер:: Сетстрокелангуажеид</span><span class="sxs-lookup"><span data-stu-id="af9c8-103">IInkAnalyzer::SetStrokeLanguageId method</span></span>

<span data-ttu-id="af9c8-104">Изменяет код локали для указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="af9c8-104">Changes the locale identifier for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9c8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af9c8-105">Syntax</span></span>


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="af9c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af9c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9c8-107">*лстрокеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af9c8-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9c8-108">Идентификатор штриха, которому присваивается идентификатор локали.</span><span class="sxs-lookup"><span data-stu-id="af9c8-108">The identifier of the stroke to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="af9c8-109">*лстрокелЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af9c8-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9c8-110">Идентификатор локали, присваиваемый штриху.</span><span class="sxs-lookup"><span data-stu-id="af9c8-110">The locale identifier to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9c8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af9c8-111">Return value</span></span>

<span data-ttu-id="af9c8-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="af9c8-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af9c8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af9c8-113">Remarks</span></span>

<span data-ttu-id="af9c8-114">Языковой стандарт штриха задается при добавлении росчерка путем вызова метода [**иинканализер:: аддстроке**](iinkanalyzer-addstroke.md), метода [**Иинканализер:: аддстрокефорлангуаже**](iinkanalyzer-addstrokeforlanguage.md), [**Иинканализер:: аддстрокес**](iinkanalyzer-addstrokes.md)или [**метода IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="af9c8-114">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="af9c8-115">Чтобы получить языковой стандарт, назначенный для штриха, вызовите [**метод иинканализер:: жетстрокелангуажеид**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="af9c8-115">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="af9c8-116">Указанный росчерк перемещается в неклассифицированный узел рукописного ввода (см. раздел [**иконтекстноде:: GetType**](icontextnode-gettype.md)), содержащий штрихи того же языка.</span><span class="sxs-lookup"><span data-stu-id="af9c8-116">The specified stroke is moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="af9c8-117">Если такой [**иконтекстноде**](icontextnode.md) не существует, этот метод создает новый неклассифицированный узел рукописного ввода и перемещает в него штрих.</span><span class="sxs-lookup"><span data-stu-id="af9c8-117">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the stroke to it.</span></span> <span data-ttu-id="af9c8-118">Неклассифицированный узел рукописного ввода — это **иконтекстноде** с типом унклассифиединк.</span><span class="sxs-lookup"><span data-stu-id="af9c8-118">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="af9c8-119">Если этот метод перемещает росчерк из [**иконтекстноде**](icontextnode.md) , который не является неклассифицированным узлом рукописного ввода, этот метод также добавляет ограничивающий прямоугольник обводки в «грязную» область анализатора рукописного ввода (см. [**метод Иинканализер:: жетдиртирегион**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="af9c8-119">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="af9c8-120">Этот метод не перемещает штрих, если параметр *лстрокелЦид* соответствует текущему идентификатору языка Stroke.</span><span class="sxs-lookup"><span data-stu-id="af9c8-120">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="af9c8-121">Если указанный росчерк не связан с [**иинканализер**](iinkanalyzer.md), этот метод возвращает значение без обновления **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="af9c8-121">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="af9c8-122">Дополнительные сведения об идентификаторах языков см. в разделе [константы и строки идентификатора языка](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="af9c8-122">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="af9c8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="af9c8-123">Requirements</span></span>



| <span data-ttu-id="af9c8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="af9c8-124">Requirement</span></span> | <span data-ttu-id="af9c8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="af9c8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9c8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af9c8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="af9c8-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="af9c8-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="af9c8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af9c8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="af9c8-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="af9c8-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="af9c8-130">Header</span><span class="sxs-lookup"><span data-stu-id="af9c8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="af9c8-131"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="af9c8-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="af9c8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="af9c8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af9c8-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af9c8-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="af9c8-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af9c8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9c8-135">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="af9c8-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="af9c8-136">**Метод Иинканализер:: Аддстроке**</span><span class="sxs-lookup"><span data-stu-id="af9c8-136">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="af9c8-137">**Метод Иинканализер:: Аддстрокефорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="af9c8-137">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="af9c8-138">**Метод Иинканализер:: Аддстрокес**</span><span class="sxs-lookup"><span data-stu-id="af9c8-138">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="af9c8-139">**Метод Иинканализер:: Аддстрокесфорлангуаже**</span><span class="sxs-lookup"><span data-stu-id="af9c8-139">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="af9c8-140">**Метод Иинканализер:: Жетстрокелангуажеид**</span><span class="sxs-lookup"><span data-stu-id="af9c8-140">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="af9c8-141">**Метод Иинканализер:: Сетстрокеслангуажеид**</span><span class="sxs-lookup"><span data-stu-id="af9c8-141">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="af9c8-142">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="af9c8-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

