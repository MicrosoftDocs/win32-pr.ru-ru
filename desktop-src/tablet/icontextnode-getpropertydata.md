---
description: Извлекает данные конкретного приложения или другие данные свойства для указанного идентификатора.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'Метод Иконтекстноде:: Жетпропертидата (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810036"
---
# <a name="icontextnodegetpropertydata-method"></a><span data-ttu-id="44e7e-103">Метод Иконтекстноде:: Жетпропертидата</span><span class="sxs-lookup"><span data-stu-id="44e7e-103">IContextNode::GetPropertyData method</span></span>

<span data-ttu-id="44e7e-104">Извлекает данные конкретного приложения или другие данные свойства для указанного идентификатора.</span><span class="sxs-lookup"><span data-stu-id="44e7e-104">Retrieves application-specific data or other property data for the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44e7e-105">Syntax</span></span>


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a><span data-ttu-id="44e7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44e7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44e7e-107">*ппропертидатаид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44e7e-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44e7e-108">Идентификатор данных.</span><span class="sxs-lookup"><span data-stu-id="44e7e-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="44e7e-109">*пулпропертидатасизе* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="44e7e-109">*pulPropertyDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="44e7e-110">Размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="44e7e-110">The size of the data in bytes.</span></span> <span data-ttu-id="44e7e-111">Передаваемое значение не используется.</span><span class="sxs-lookup"><span data-stu-id="44e7e-111">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="44e7e-112">*ппбпропертидата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="44e7e-112">*ppbPropertyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44e7e-113">Указатель на 8-разрядный массив целых чисел без знака, содержащий данные свойства.</span><span class="sxs-lookup"><span data-stu-id="44e7e-113">A pointer to an 8-bit unsigned integer array that contains the property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44e7e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44e7e-114">Return value</span></span>

<span data-ttu-id="44e7e-115">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="44e7e-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44e7e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44e7e-116">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="44e7e-117">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппбпропертидата* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="44e7e-117">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertyData* when you no longer need the information.</span></span>

 

<span data-ttu-id="44e7e-118">Помимо извлечения данных приложения, которые были добавлены с помощью [**иконтекстноде:: аддпропертидата**](icontextnode-addpropertydata.md), этот метод используется для получения общих свойств, описанных в константах [свойств узла контекста](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="44e7e-118">In addition to retrieving application-specific data that was added with [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md), this method is used to retrieve common properties that are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

<span data-ttu-id="44e7e-119">К свойствам строкового типа относятся:</span><span class="sxs-lookup"><span data-stu-id="44e7e-119">The string-type properties include:</span></span>

-   <span data-ttu-id="44e7e-120">GUID \_ КНП \_ рекогнизедстринг</span><span class="sxs-lookup"><span data-stu-id="44e7e-120">GUID\_CNP\_RECOGNIZEDSTRING</span></span>
-   <span data-ttu-id="44e7e-121">GUID \_ КНП \_ шапенаме</span><span class="sxs-lookup"><span data-stu-id="44e7e-121">GUID\_CNP\_SHAPENAME</span></span>
-   <span data-ttu-id="44e7e-122">GUID \_ ахп \_ аналисишинтнаме</span><span class="sxs-lookup"><span data-stu-id="44e7e-122">GUID\_AHP\_ANALYSISHINTNAME</span></span>
-   <span data-ttu-id="44e7e-123">GUID \_ ахп \_ префикстекст</span><span class="sxs-lookup"><span data-stu-id="44e7e-123">GUID\_AHP\_PREFIXTEXT</span></span>
-   <span data-ttu-id="44e7e-124">GUID \_ ахп \_ суффикстекст</span><span class="sxs-lookup"><span data-stu-id="44e7e-124">GUID\_AHP\_SUFFIXTEXT</span></span>
-   <span data-ttu-id="44e7e-125">GUID \_ ахп \_ фактоид</span><span class="sxs-lookup"><span data-stu-id="44e7e-125">GUID\_AHP\_FACTOID</span></span>

<span data-ttu-id="44e7e-126">Возвращаемое значение — \**WCHAR \**_. При приведении параметра \_ *ппбпропертидата* к \**WCHAR \**_ возвращаемая длина имеет значение `(length of the string + 1) _ sizeof(WCHAR)` .</span><span class="sxs-lookup"><span data-stu-id="44e7e-126">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `(length of the string + 1) _ sizeof(WCHAR)`.</span></span>

<span data-ttu-id="44e7e-127">Ниже перечислены свойства логического типа.</span><span class="sxs-lookup"><span data-stu-id="44e7e-127">The Boolean-type properties include:</span></span>

-   <span data-ttu-id="44e7e-128">GUID \_ ахп \_ оверриделангуажеид</span><span class="sxs-lookup"><span data-stu-id="44e7e-128">GUID\_AHP\_OVERRIDELANGUAGEID</span></span>
-   <span data-ttu-id="44e7e-129">GUID \_ ахп \_ коерцетофактоид</span><span class="sxs-lookup"><span data-stu-id="44e7e-129">GUID\_AHP\_COERCETOFACTOID</span></span>
-   <span data-ttu-id="44e7e-130">GUID \_ ахп \_ вордмоде</span><span class="sxs-lookup"><span data-stu-id="44e7e-130">GUID\_AHP\_WORDMODE</span></span>

<span data-ttu-id="44e7e-131">Возвращаемое значение является **вариантным \_ bool**.</span><span class="sxs-lookup"><span data-stu-id="44e7e-131">The return value is **VARIANT\_BOOL**.</span></span> <span data-ttu-id="44e7e-132">При приведении параметра \* *ппбпропертидата* к \**Variant \_ bool \** _ возвращаемая длина имеет значение `sizeof(VARIANT_BOOL)` .</span><span class="sxs-lookup"><span data-stu-id="44e7e-132">If you cast the \**ppbPropertyData* parameter to \**VARIANT\_BOOL\** _ its returned length is `sizeof(VARIANT_BOOL)`.</span></span>

<span data-ttu-id="44e7e-133">GUID \_ ахп \_ Guide — это свойство типа "руководство".</span><span class="sxs-lookup"><span data-stu-id="44e7e-133">GUID\_AHP\_GUIDE is a guide-type property.</span></span> <span data-ttu-id="44e7e-134">Возвращаемое значение — _*инканалисисрекогнитионгуиде \**_.</span><span class="sxs-lookup"><span data-stu-id="44e7e-134">The return value is _*InkAnalysisRecognitionGuide\**_.</span></span> <span data-ttu-id="44e7e-135">Если \_ параметр *ппбпропертидата* приведен в значение \**инканалисисрекогнитионгуиде \** _, его возвращаемая длина будет равна `sizeof(InkAnalysisRecognitionGuide)` .</span><span class="sxs-lookup"><span data-stu-id="44e7e-135">If you cast the \_*ppbPropertyData* parameter to \**InkAnalysisRecognitionGuide\** _ its returned length is `sizeof(InkAnalysisRecognitionGuide)`.</span></span>

<span data-ttu-id="44e7e-136">Свойства целочисленного типа включают:</span><span class="sxs-lookup"><span data-stu-id="44e7e-136">Integer-type properties include:</span></span>

-   <span data-ttu-id="44e7e-137">GUID \_ КНП \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="44e7e-137">GUID\_CNP\_LINENUMBER</span></span>
-   <span data-ttu-id="44e7e-138">GUID \_ КНП \_ поинтсперинч</span><span class="sxs-lookup"><span data-stu-id="44e7e-138">GUID\_CNP\_POINTSPERINCH</span></span>
-   <span data-ttu-id="44e7e-139">GUID \_ КНП \_ конфиденцелевел</span><span class="sxs-lookup"><span data-stu-id="44e7e-139">GUID\_CNP\_CONFIDENCELEVEL</span></span>
-   <span data-ttu-id="44e7e-140">\_Подтверждение GUID КНП \_</span><span class="sxs-lookup"><span data-stu-id="44e7e-140">GUID\_CNP\_CONFIRMATION</span></span>
-   <span data-ttu-id="44e7e-141">GUID \_ КНП \_ максимумстрокекаунт</span><span class="sxs-lookup"><span data-stu-id="44e7e-141">GUID\_CNP\_MAXIMUMSTROKECOUNT</span></span>
-   <span data-ttu-id="44e7e-142">\_ \_ сегментация КНП GUID</span><span class="sxs-lookup"><span data-stu-id="44e7e-142">GUID\_CNP\_SEGMENTATION</span></span>
-   <span data-ttu-id="44e7e-143">GUID \_ КНП \_ алигнментлевел</span><span class="sxs-lookup"><span data-stu-id="44e7e-143">GUID\_CNP\_ALIGNMENTLEVEL</span></span>

<span data-ttu-id="44e7e-144">Возвращаемое значение является _*длинным \**_.</span><span class="sxs-lookup"><span data-stu-id="44e7e-144">The return value is _*LONG\**_.</span></span> <span data-ttu-id="44e7e-145">Если \_ параметр *ппбпропертидата* приведен в значение \**Long \** _, его возвращаемая длина будет равна `sizeof(LONG)` .</span><span class="sxs-lookup"><span data-stu-id="44e7e-145">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)`.</span></span>

<span data-ttu-id="44e7e-146">Метрики линий — свойства типа включают:</span><span class="sxs-lookup"><span data-stu-id="44e7e-146">Line metrics-type properties include:</span></span>

-   <span data-ttu-id="44e7e-147">GUID \_ КНП \_ ascends</span><span class="sxs-lookup"><span data-stu-id="44e7e-147">GUID\_CNP\_ASCENDERS</span></span>
-   <span data-ttu-id="44e7e-148">GUID \_ КНП \_ нижние выносные</span><span class="sxs-lookup"><span data-stu-id="44e7e-148">GUID\_CNP\_DESCENDERS</span></span>
-   <span data-ttu-id="44e7e-149">Базовый идентификатор GUID \_ КНП \_</span><span class="sxs-lookup"><span data-stu-id="44e7e-149">GUID\_CNP\_BASELINE</span></span>
-   <span data-ttu-id="44e7e-150">GUID \_ КНП \_ заполнение нажатием клавиши</span><span class="sxs-lookup"><span data-stu-id="44e7e-150">GUID\_CNP\_MIDLINE</span></span>

<span data-ttu-id="44e7e-151">Возвращаемое значение является _*длинным \**_.</span><span class="sxs-lookup"><span data-stu-id="44e7e-151">The return value is _*LONG\**_.</span></span> <span data-ttu-id="44e7e-152">Если \_ параметр *ппбпропертидата* приведен в значение \**Long \** _, то его возвращаемая длина будет равна, что `sizeof(LONG)_4` означает значения (x, y) для начальных точек, за которыми следуют значения (x, y) для конечных точек.</span><span class="sxs-lookup"><span data-stu-id="44e7e-152">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_4`, signifying the (x, y) values for the starting points followed by the (x, y) values for the ending points.</span></span>

<span data-ttu-id="44e7e-153">GUID \_ КНП \_ текстрекогнизерид является свойством **GUID** .</span><span class="sxs-lookup"><span data-stu-id="44e7e-153">GUID\_CNP\_TEXTRECOGNIZERID is a **GUID** property.</span></span> <span data-ttu-id="44e7e-154">Возвращаемое значение — \**GUID \**_. При приведении параметра \_ *ппбпропертидата* к \**GUID \**_ возвращаемой длины будет `sizeof(GUID)` .</span><span class="sxs-lookup"><span data-stu-id="44e7e-154">The return value is \**GUID\**_. If you cast the \_*ppbPropertyData* parameter to \**GUID\**_ its returned length is `sizeof(GUID)`.</span></span>

<span data-ttu-id="44e7e-155">GUID \_ КНП \_ ротатедбаундингбокс — это повернутое свойство ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="44e7e-155">GUID\_CNP\_ROTATEDBOUNDINGBOX is a rotated bounding box property.</span></span> <span data-ttu-id="44e7e-156">Возвращаемое значение является _*длинным \**_.</span><span class="sxs-lookup"><span data-stu-id="44e7e-156">The return value is _*LONG\**_.</span></span> <span data-ttu-id="44e7e-157">Если \_ параметр *ппбпропертидата* приведен в значение \**Long \** _, его возвращаемая длина равна, что `sizeof(LONG)_8` означает (x, y) для четырех углов прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="44e7e-157">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_8`, signifying the (x, y) values for the four corners of the box.</span></span>

<span data-ttu-id="44e7e-158">GUID \_ КНП \_ хотпоинт является свойством горячей точки.</span><span class="sxs-lookup"><span data-stu-id="44e7e-158">GUID\_CNP\_HOTPOINT is a hot point property.</span></span> <span data-ttu-id="44e7e-159">Возвращаемое значение — \**Long \**_. Если параметр ппбпропертидата приводится к значению \_  \**Long \**_ , его возвращаемая длина равна `sizeof(LONG)_2` , что означает (x, y) точки.</span><span class="sxs-lookup"><span data-stu-id="44e7e-159">The return value is \**LONG\**_. If you cast the \_*ppbPropertyData* parameter to \**LONG\**_ its returned length is `sizeof(LONG)_2`, signifying the (x, y) values for the point.</span></span>

<span data-ttu-id="44e7e-160">GUID \_ ахп \_ список слов — это свойство списка слов.</span><span class="sxs-lookup"><span data-stu-id="44e7e-160">GUID\_AHP\_WORDLIST is a word list property.</span></span> <span data-ttu-id="44e7e-161">Возвращаемое значение — \**WCHAR \**_. При приведении параметра \_ *ппбпропертидата* к значению \*\* \* WCHAR\*_ возвращаемой длины является `n _ sizeof(WCHAR)` , где `n` — сумма длины строк числа строк в списке плюс 1 для каждого завершающего символа **null** для каждой строки.</span><span class="sxs-lookup"><span data-stu-id="44e7e-161">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `n _ sizeof(WCHAR)`, where `n` is the sum of the string lengths of the number of strings in the list plus 1 for each **NULL** termination character for each string.</span></span>

## <a name="examples"></a><span data-ttu-id="44e7e-162">Примеры</span><span class="sxs-lookup"><span data-stu-id="44e7e-162">Examples</span></span>

<span data-ttu-id="44e7e-163">В этом примере показан метод, который обращается к свойству узла контекста Алигнментлевел типа узла контекста абзаца.</span><span class="sxs-lookup"><span data-stu-id="44e7e-163">This example shows a method that accesses the AlignmentLevel context node property of a Paragraph context node type.</span></span>


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="44e7e-164">Требования</span><span class="sxs-lookup"><span data-stu-id="44e7e-164">Requirements</span></span>



| <span data-ttu-id="44e7e-165">Требование</span><span class="sxs-lookup"><span data-stu-id="44e7e-165">Requirement</span></span> | <span data-ttu-id="44e7e-166">Значение</span><span class="sxs-lookup"><span data-stu-id="44e7e-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44e7e-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44e7e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="44e7e-168">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="44e7e-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="44e7e-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44e7e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="44e7e-170">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="44e7e-170">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="44e7e-171">Header</span><span class="sxs-lookup"><span data-stu-id="44e7e-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e7e-172"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="44e7e-172"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="44e7e-173">DLL</span><span class="sxs-lookup"><span data-stu-id="44e7e-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44e7e-174"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44e7e-174"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="44e7e-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44e7e-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e7e-176">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="44e7e-176">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="44e7e-177">**Иконтекстноде:: Аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="44e7e-177">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="44e7e-178">**Иконтекстноде:: Ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="44e7e-178">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="44e7e-179">**Иконтекстноде:: Жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="44e7e-179">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="44e7e-180">**Иконтекстноде:: Контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="44e7e-180">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="44e7e-181">**Иконтекстноде:: Лоадпропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="44e7e-181">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="44e7e-182">**Иконтекстноде:: Савепропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="44e7e-182">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="44e7e-183">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="44e7e-183">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

