---
description: Указывает расположение или область, в которой рукописный ввод отображается и распознается.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Структура Инканалисисрекогнизергуиде (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692244"
---
# <a name="inkanalysisrecognizerguide-structure"></a><span data-ttu-id="843b4-103">Структура Инканалисисрекогнизергуиде</span><span class="sxs-lookup"><span data-stu-id="843b4-103">InkAnalysisRecognizerGuide structure</span></span>

<span data-ttu-id="843b4-104">Указывает расположение или область, в которой рукописный ввод отображается и распознается.</span><span class="sxs-lookup"><span data-stu-id="843b4-104">Specifies the guide, or area where ink is drawn and recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="843b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="843b4-105">Syntax</span></span>


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a><span data-ttu-id="843b4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="843b4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="843b4-107">**ректвритингбокс**</span><span class="sxs-lookup"><span data-stu-id="843b4-107">**rectWritingBox**</span></span>
</dt> <dd>

<span data-ttu-id="843b4-108">Невидимая область письменности руководства по распознаванию, в которой запись может быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="843b4-108">The invisible writing area of the recognition guide in which writing can actually take place.</span></span>

</dd> <dt>

<span data-ttu-id="843b4-109">**ректдравнбокс**</span><span class="sxs-lookup"><span data-stu-id="843b4-109">**rectDrawnBox**</span></span>
</dt> <dd>

<span data-ttu-id="843b4-110">Прямоугольник, который рисуется на планшетном экране и в котором происходит запись.</span><span class="sxs-lookup"><span data-stu-id="843b4-110">The rectangle that is drawn on the tablet screen and in which writing takes place.</span></span>

</dd> <dt>

<span data-ttu-id="843b4-111">**cRows**</span><span class="sxs-lookup"><span data-stu-id="843b4-111">**cRows**</span></span>
</dt> <dd>

<span data-ttu-id="843b4-112">Число строк в поле "руководством по распознаванию".</span><span class="sxs-lookup"><span data-stu-id="843b4-112">The number of rows in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="843b4-113">**кколумнс**</span><span class="sxs-lookup"><span data-stu-id="843b4-113">**cColumns**</span></span>
</dt> <dd>

<span data-ttu-id="843b4-114">Число столбцов в поле "руководством по распознаванию".</span><span class="sxs-lookup"><span data-stu-id="843b4-114">The number of columns in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="843b4-115">**заполнение нажатием клавиши**</span><span class="sxs-lookup"><span data-stu-id="843b4-115">**midline**</span></span>
</dt> <dd>

<span data-ttu-id="843b4-116">Заполнение нажатием клавиши высота поля "руководством по распознаванию".</span><span class="sxs-lookup"><span data-stu-id="843b4-116">The midline height of the recognition guide box.</span></span> <span data-ttu-id="843b4-117">Высота заполнение нажатием клавиши — это расстояние от базовой линии до заполнение нажатием клавиши нарисованного бокса.</span><span class="sxs-lookup"><span data-stu-id="843b4-117">The midline height is the distance from the baseline to the midline, of the drawn box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="843b4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="843b4-118">Remarks</span></span>

<span data-ttu-id="843b4-119">**Инканалисисрекогнизергуиде** определяет ожидаемую область ввода, например линию или прямоугольники, для символов.</span><span class="sxs-lookup"><span data-stu-id="843b4-119">An **InkAnalysisRecognizerGuide** defines an expected area of input, such as a line or boxes, for characters.</span></span> <span data-ttu-id="843b4-120">Структуру **инканалисисрекогнизергуиде** можно задать только в узле контекста указания по анализу (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="843b4-120">An **InkAnalysisRecognizerGuide** structure can be set only on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="843b4-121">[**Иинканализер**](iinkanalyzer.md) использует расположение узла указания по анализу и расположения рукописных штрихов для связывания штриха с узлом указания по анализу.</span><span class="sxs-lookup"><span data-stu-id="843b4-121">The [**IInkAnalyzer**](iinkanalyzer.md) uses the location of the analysis hint node and the locations of the ink strokes to associate a stroke with the analysis hint node.</span></span> <span data-ttu-id="843b4-122">Любые штрихи с Ассоциацией к узлу указания анализа будут иметь указанную **инканалисисрекогнизергуиде** , используемую при распознавании **иинканализер**, при условии, что **иинканализер** поддерживает **инканалисисрекогнизергуиде**.</span><span class="sxs-lookup"><span data-stu-id="843b4-122">Any strokes with an association to the analysis hint node will have the specified **InkAnalysisRecognizerGuide** used when recognized by an **IInkAnalyzer**, provided the **IInkAnalyzer** supports the **InkAnalysisRecognizerGuide**.</span></span> <span data-ttu-id="843b4-123">Значения, выраженные в классе **инканалисисрекогнизергуиде** , всегда задаются относительно расположения узла указания по анализу и указываются в координатах пространства рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="843b4-123">The values expressed in the **InkAnalysisRecognizerGuide** class are always relative to the location of the analysis hint node and are specified in ink space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="843b4-124">Требования</span><span class="sxs-lookup"><span data-stu-id="843b4-124">Requirements</span></span>



| <span data-ttu-id="843b4-125">Требование</span><span class="sxs-lookup"><span data-stu-id="843b4-125">Requirement</span></span> | <span data-ttu-id="843b4-126">Значение</span><span class="sxs-lookup"><span data-stu-id="843b4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="843b4-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="843b4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="843b4-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="843b4-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="843b4-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="843b4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="843b4-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="843b4-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="843b4-131">Header</span><span class="sxs-lookup"><span data-stu-id="843b4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="843b4-132"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="843b4-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="843b4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="843b4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="843b4-134">Свойства указания по анализу</span><span class="sxs-lookup"><span data-stu-id="843b4-134">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="843b4-135">**Метод Иинканализер:: Креатеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="843b4-135">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="843b4-136">**Иконтекстноде:: Аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="843b4-136">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="843b4-137">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="843b4-137">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="843b4-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="843b4-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




