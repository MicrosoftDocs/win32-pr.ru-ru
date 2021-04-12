---
description: Указывает, следует ли анализировать штрих как часть рисунка или как часть записи.
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: Перечисление Строкетипе (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 3b59be130c6c7055bb7636760451dcadf5acf841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265679"
---
# <a name="stroketype-enumeration"></a><span data-ttu-id="9d5d5-103">Перечисление Строкетипе</span><span class="sxs-lookup"><span data-stu-id="9d5d5-103">StrokeType enumeration</span></span>

<span data-ttu-id="9d5d5-104">Указывает, следует ли анализировать штрих как часть рисунка или как часть записи.</span><span class="sxs-lookup"><span data-stu-id="9d5d5-104">Indicates whether a stroke should be analyzed as part of a drawing or as part of writing.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d5d5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d5d5-105">Syntax</span></span>


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a><span data-ttu-id="9d5d5-106">Константы</span><span class="sxs-lookup"><span data-stu-id="9d5d5-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9d5d5-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**Строкетипе не \_ классифицировано**</span><span class="sxs-lookup"><span data-stu-id="9d5d5-107"><span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType\_Unclassified**</span></span>
</dt> <dd>

<span data-ttu-id="9d5d5-108">Штрих может быть либо частью рисунка, либо частью записи.</span><span class="sxs-lookup"><span data-stu-id="9d5d5-108">The stroke might be either part of a drawing or part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="9d5d5-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**Строкетипе \_ запись**</span><span class="sxs-lookup"><span data-stu-id="9d5d5-109"><span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType\_Writing**</span></span>
</dt> <dd>

<span data-ttu-id="9d5d5-110">Штрих является частью записи.</span><span class="sxs-lookup"><span data-stu-id="9d5d5-110">The stroke is part of writing.</span></span>

</dd> <dt>

<span data-ttu-id="9d5d5-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**\_Рисование строкетипе**</span><span class="sxs-lookup"><span data-stu-id="9d5d5-111"><span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType\_Drawing**</span></span>
</dt> <dd>

<span data-ttu-id="9d5d5-112">Штрих является частью рисунка.</span><span class="sxs-lookup"><span data-stu-id="9d5d5-112">The stroke is part of a drawing.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9d5d5-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="9d5d5-113">Examples</span></span>

<span data-ttu-id="9d5d5-114">В следующем примере показана часть обработчика событий Stroke, реализованная аналогичным образом для [примера приемников событий C++](c---event-sinks-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9d5d5-114">The following example shows part of a stroke event handler, implemented in a similar fashion to the [C++ Event Sinks Sample](c---event-sinks-sample.md).</span></span> <span data-ttu-id="9d5d5-115">Добавленный росчерк проверяется, отображается ли верхняя граница ограничивающего прямоугольника под полем `drawingMargin` .</span><span class="sxs-lookup"><span data-stu-id="9d5d5-115">The added stroke is checked to see if the top of its bounding box has been drawn below a margin, `drawingMargin`.</span></span> <span data-ttu-id="9d5d5-116">Если это так, то объект [**иинканализер**](iinkanalyzer.md) , `m_spInkAnalyzer` , задается для анализа штриха в виде рисованной черты, а не в виде рукописного штриха.</span><span class="sxs-lookup"><span data-stu-id="9d5d5-116">If so, the [**IInkAnalyzer**](iinkanalyzer.md) object, `m_spInkAnalyzer`, is set to analyze the stroke as a drawing stroke, rather than as a handwriting stroke.</span></span> <span data-ttu-id="9d5d5-117">`CheckHResult` — Это функция, которая принимает `HRESULT` и получает строку и создает исключение, созданное со строкой, если `HRESULT` не **выполнено**.</span><span class="sxs-lookup"><span data-stu-id="9d5d5-117">`CheckHResult` is a function that takes an `HRESULT` and a string, and throws an exception created with the string if the `HRESULT` is not **SUCCESS**.</span></span>


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a><span data-ttu-id="9d5d5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9d5d5-118">Requirements</span></span>



| <span data-ttu-id="9d5d5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9d5d5-119">Requirement</span></span> | <span data-ttu-id="9d5d5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9d5d5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5d5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d5d5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5d5-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9d5d5-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9d5d5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d5d5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5d5-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9d5d5-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9d5d5-125">Header</span><span class="sxs-lookup"><span data-stu-id="9d5d5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5d5-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9d5d5-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d5d5-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d5d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d5d5-128">**Метод Иинканализер:: Сетстрокетипе**</span><span class="sxs-lookup"><span data-stu-id="9d5d5-128">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




