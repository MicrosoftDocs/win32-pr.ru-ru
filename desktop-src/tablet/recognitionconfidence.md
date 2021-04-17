---
description: Указывает уровень достоверности, в котором Иинканализер имеет точность результата распознавания.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Перечисление Рекогнитионконфиденце (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703203"
---
# <a name="recognitionconfidence-enumeration"></a><span data-ttu-id="f6fe6-103">Перечисление Рекогнитионконфиденце</span><span class="sxs-lookup"><span data-stu-id="f6fe6-103">RecognitionConfidence enumeration</span></span>

<span data-ttu-id="f6fe6-104">Указывает уровень достоверности, в котором [**иинканализер**](iinkanalyzer.md) имеет точность результата распознавания.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-104">Indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the recognition result.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fe6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6fe6-105">Syntax</span></span>


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a><span data-ttu-id="f6fe6-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f6fe6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f6fe6-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**Рекогнитионконфиденце \_ strong**</span><span class="sxs-lookup"><span data-stu-id="f6fe6-107"><span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence\_Strong**</span></span>
</dt> <dd>

<span data-ttu-id="f6fe6-108">Надежная уверенность в результатах или альтернативном варианте.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-108">Strong confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="f6fe6-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**\_Промежуточный рекогнитионконфиденце**</span><span class="sxs-lookup"><span data-stu-id="f6fe6-109"><span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence\_Intermediate**</span></span>
</dt> <dd>

<span data-ttu-id="f6fe6-110">Промежуточная уверенность в результате или в альтернативном варианте.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-110">Intermediate confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="f6fe6-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**Рекогнитионконфиденце \_ плохо**</span><span class="sxs-lookup"><span data-stu-id="f6fe6-111"><span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence\_Poor**</span></span>
</dt> <dd>

<span data-ttu-id="f6fe6-112">Низкая уверенность в результатах или альтернативе.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-112">Poor confidence in the result or alternate.</span></span>

</dd> <dt>

<span data-ttu-id="f6fe6-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**Рекогнитионконфиденце \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="f6fe6-113"><span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="f6fe6-114">[**Иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , создавший распознанный текст, не поддерживает уровни достоверности.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-114">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that generated the recognized text does not support confidence levels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6fe6-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f6fe6-115">Remarks</span></span>

<span data-ttu-id="f6fe6-116">[**Иинканализер**](iinkanalyzer.md) использует один или несколько объектов [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) для преобразования рукописного текста в текст.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-116">The [**IInkAnalyzer**](iinkanalyzer.md) uses one or more [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects to convert handwriting to text.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6fe6-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f6fe6-117">Requirements</span></span>



| <span data-ttu-id="f6fe6-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f6fe6-118">Requirement</span></span> | <span data-ttu-id="f6fe6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f6fe6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fe6-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6fe6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f6fe6-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f6fe6-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f6fe6-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6fe6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f6fe6-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f6fe6-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f6fe6-124">Header</span><span class="sxs-lookup"><span data-stu-id="f6fe6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6fe6-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f6fe6-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6fe6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6fe6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6fe6-127">**Метод Ианалисисалтернате:: Жетрекогнитионконфиденце**</span><span class="sxs-lookup"><span data-stu-id="f6fe6-127">**IAnalysisAlternate::GetRecognitionConfidence Method**</span></span>](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="f6fe6-128">**Иконтекстноде:: Жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="f6fe6-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="f6fe6-129">Свойства узла контекста</span><span class="sxs-lookup"><span data-stu-id="f6fe6-129">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="f6fe6-130">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="f6fe6-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




