---
description: Содержит коллекцию объектов, реализующих интерфейс Иинканалисисрекогнизер и представляющих возможность распознавания рукописного текста, объектов или жестов.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Интерфейс Иинканалисисрекогнизерс (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343715"
---
# <a name="iinkanalysisrecognizers-interface"></a><span data-ttu-id="a8c4f-103">Интерфейс Иинканалисисрекогнизерс</span><span class="sxs-lookup"><span data-stu-id="a8c4f-103">IInkAnalysisRecognizers interface</span></span>

<span data-ttu-id="a8c4f-104">Содержит коллекцию объектов, реализующих интерфейс [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) и представляющих возможность распознавания рукописного текста, объектов или жестов.</span><span class="sxs-lookup"><span data-stu-id="a8c4f-104">Contains a collection of objects that implement the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) interface and that represent the ability to recognize handwriting, objects, or gestures.</span></span>

## <a name="members"></a><span data-ttu-id="a8c4f-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a8c4f-105">Members</span></span>

<span data-ttu-id="a8c4f-106">Интерфейс **иинканалисисрекогнизерс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a8c4f-106">The **IInkAnalysisRecognizers** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a8c4f-107">**Иинканалисисрекогнизерс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a8c4f-107">**IInkAnalysisRecognizers** also has these types of members:</span></span>

-   [<span data-ttu-id="a8c4f-108">Методы</span><span class="sxs-lookup"><span data-stu-id="a8c4f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a8c4f-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a8c4f-109">Methods</span></span>

<span data-ttu-id="a8c4f-110">Интерфейс **иинканалисисрекогнизерс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a8c4f-110">The **IInkAnalysisRecognizers** interface has these methods.</span></span>



| <span data-ttu-id="a8c4f-111">Метод</span><span class="sxs-lookup"><span data-stu-id="a8c4f-111">Method</span></span>                                                                               | <span data-ttu-id="a8c4f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a8c4f-112">Description</span></span>                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8c4f-113">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="a8c4f-113">**GetCount**</span></span>](iinkanalysisrecognizers-getcount.md)                                 | <span data-ttu-id="a8c4f-114">Возвращает число объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="a8c4f-114">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span><br/> |
| [<span data-ttu-id="a8c4f-115">**жетинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="a8c4f-115">**GetInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | <span data-ttu-id="a8c4f-116">Извлекает [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="a8c4f-116">Retrieves the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) at the specified index.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="a8c4f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8c4f-117">Remarks</span></span>

<span data-ttu-id="a8c4f-118">Метод [**иинканализер:: Жетинканалисисрекогнизерсбиприорити метода**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) [**Иинканализер**](iinkanalyzer.md) Возвращает коллекцию **иинканалисисрекогнизерс** , содержащую Распознаватели рукописного ввода, доступные на текущем планшетном ПК.</span><span class="sxs-lookup"><span data-stu-id="a8c4f-118">The [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method of [**IInkAnalyzer**](iinkanalyzer.md) returns an **IInkAnalysisRecognizers** collection containing the ink recognizers available on the current Tablet PC.</span></span>

<span data-ttu-id="a8c4f-119">Для распознавателя языка метод [**иинканалисисрекогнизер::**](iinkanalysisrecognizer-getlanguages.md) возвращает непустой массив.</span><span class="sxs-lookup"><span data-stu-id="a8c4f-119">For a language recognizer, the [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) method returns a non-empty array.</span></span> <span data-ttu-id="a8c4f-120">Для распознавателей жестов и распознавателей объектов метод **иинканалисисрекогнизер::** GetObject возвращает пустой массив.</span><span class="sxs-lookup"><span data-stu-id="a8c4f-120">For both gesture recognizers and object recognizers, the **IInkAnalysisRecognizer::GetLanguages** method returns an empty array.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8c4f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a8c4f-121">Requirements</span></span>



| <span data-ttu-id="a8c4f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a8c4f-122">Requirement</span></span> | <span data-ttu-id="a8c4f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a8c4f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8c4f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8c4f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8c4f-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a8c4f-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a8c4f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8c4f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8c4f-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a8c4f-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a8c4f-128">Header</span><span class="sxs-lookup"><span data-stu-id="a8c4f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8c4f-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a8c4f-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a8c4f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a8c4f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8c4f-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8c4f-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a8c4f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8c4f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c4f-133">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="a8c4f-133">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a8c4f-134">**Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити**</span><span class="sxs-lookup"><span data-stu-id="a8c4f-134">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="a8c4f-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="a8c4f-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

