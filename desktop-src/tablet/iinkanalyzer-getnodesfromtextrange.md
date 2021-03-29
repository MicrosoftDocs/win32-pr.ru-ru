---
description: Извлекает коллекцию объектов Иконтекстноде, относящихся к указанному текстовому диапазону для указанных узлов контекста.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'Метод Иинканализер:: Жетнодесфромтекстранже (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810007"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a><span data-ttu-id="e381e-103">Метод Иинканализер:: Жетнодесфромтекстранже</span><span class="sxs-lookup"><span data-stu-id="e381e-103">IInkAnalyzer::GetNodesFromTextRange method</span></span>

<span data-ttu-id="e381e-104">Извлекает коллекцию объектов [**иконтекстноде**](icontextnode.md) , относящихся к указанному текстовому диапазону для указанных узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="e381e-104">Retrieves a collection of [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e381e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e381e-105">Syntax</span></span>


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a><span data-ttu-id="e381e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e381e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e381e-107">*плстарт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e381e-107">*plStart* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e381e-108">Ссылка на начало текстового диапазона в *пнодестосеарч* части распознанной строки.</span><span class="sxs-lookup"><span data-stu-id="e381e-108">A reference to the start of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="e381e-109">*плленгс* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="e381e-109">*plLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e381e-110">Ссылка на длину текстового диапазона в *пнодестосеарч* части распознанной строки.</span><span class="sxs-lookup"><span data-stu-id="e381e-110">A reference to the length of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="e381e-111">*ппконтекстнодес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e381e-111">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e381e-112">Указатель на объекты [**иконтекстноде**](icontextnode.md) , относящиеся к указанному текстовому диапазону для указанных узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="e381e-112">A pointer to the [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

</dd> <dt>

<span data-ttu-id="e381e-113">*пнодестосеарч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e381e-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e381e-114">Объекты [**иконтекстноде**](icontextnode.md) , для которых необходимо ограничить поиск.</span><span class="sxs-lookup"><span data-stu-id="e381e-114">The [**IContextNode**](icontextnode.md) objects to which to limit the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e381e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e381e-115">Return value</span></span>

<span data-ttu-id="e381e-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e381e-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e381e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e381e-117">Remarks</span></span>

<span data-ttu-id="e381e-118">Указанный диапазон текста должен относиться к *пнодестосеарч* части распознанной строки [**иинканализер**](iinkanalyzer.md), а не к распознанной строке всего **иинканализер**.</span><span class="sxs-lookup"><span data-stu-id="e381e-118">The specified text range should be relative to the *pNodesToSearch* portion of the recognized string of the [**IInkAnalyzer**](iinkanalyzer.md), rather than to the recognized string of the entire **IInkAnalyzer**.</span></span>

<span data-ttu-id="e381e-119">Этот метод изменяет значения параметров *плстарт* и *плленгс* , расширяя диапазон текста до ближайших границ слов.</span><span class="sxs-lookup"><span data-stu-id="e381e-119">This method modifies the values of the *plStart* and *plLength* parameters by expanding the text range to the nearest word boundaries.</span></span>

<span data-ttu-id="e381e-120">Например, если распознанная строка является "I-поздно", и этот метод вызывается с помощью значений параметра 6 для *плстарт* и 1 для *плленгс*, который соответствует букве "a" в "позднем", этот метод возвращает коллекцию, содержащую один [**иконтекстноде**](icontextnode.md), инкворд или текстворд, соответствующий слову "поздно".</span><span class="sxs-lookup"><span data-stu-id="e381e-120">For example, if the recognized string is "I am late" and you call this method using the parameter values of 6 for *plStart* and 1 for *plLength*, which corresponds to the letter "a" in "late", this method returns a collection containing a single [**IContextNode**](icontextnode.md), the InkWord or TextWord that corresponds to the word "late".</span></span> <span data-ttu-id="e381e-121">В этом примере этот метод также изменяет значение *плстарт* на 5, а значение *плленгс* — на 4, что соответствует слову "поздно".</span><span class="sxs-lookup"><span data-stu-id="e381e-121">For this example, this method also modifies the value of *plStart* to 5 and the value of *plLength* to 4, which corresponds to the word "late".</span></span>

> [!Note]  
> <span data-ttu-id="e381e-122">Параметр *плстарт* задается относительно распознанной строки параметра *пнодестосеарч* .</span><span class="sxs-lookup"><span data-stu-id="e381e-122">The *plStart* parameter is relative to the recognized string of the *pNodesToSearch* parameter.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e381e-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e381e-123">Requirements</span></span>



| <span data-ttu-id="e381e-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e381e-124">Requirement</span></span> | <span data-ttu-id="e381e-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e381e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e381e-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e381e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e381e-127">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e381e-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e381e-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e381e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e381e-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e381e-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e381e-130">Header</span><span class="sxs-lookup"><span data-stu-id="e381e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e381e-131"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e381e-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e381e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e381e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e381e-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e381e-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e381e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e381e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e381e-135">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="e381e-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




