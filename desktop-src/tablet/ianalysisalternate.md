---
description: Представляет возможные совпадения слов распознавания рукописного текста для объектов Иконтекстноде.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Интерфейс Ианалисисалтернате (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263162"
---
# <a name="ianalysisalternate-interface"></a><span data-ttu-id="7b956-103">Интерфейс Ианалисисалтернате</span><span class="sxs-lookup"><span data-stu-id="7b956-103">IAnalysisAlternate interface</span></span>

<span data-ttu-id="7b956-104">Представляет возможные совпадения слов распознавания рукописного текста для объектов [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="7b956-104">Represents the possible handwriting recognition word matches for [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="7b956-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="7b956-105">Members</span></span>

<span data-ttu-id="7b956-106">Интерфейс **ианалисисалтернате** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7b956-106">The **IAnalysisAlternate** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7b956-107">**Ианалисисалтернате** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7b956-107">**IAnalysisAlternate** also has these types of members:</span></span>

-   [<span data-ttu-id="7b956-108">Методы</span><span class="sxs-lookup"><span data-stu-id="7b956-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7b956-109">Методы</span><span class="sxs-lookup"><span data-stu-id="7b956-109">Methods</span></span>

<span data-ttu-id="7b956-110">Интерфейс **ианалисисалтернате** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7b956-110">The **IAnalysisAlternate** interface has these methods.</span></span>



| <span data-ttu-id="7b956-111">Метод</span><span class="sxs-lookup"><span data-stu-id="7b956-111">Method</span></span>                                                                          | <span data-ttu-id="7b956-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7b956-112">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b956-113">**жеталтернатенодес**</span><span class="sxs-lookup"><span data-stu-id="7b956-113">**GetAlternateNodes**</span></span>](ianalysisalternate-getalternatenodes.md)               | <span data-ttu-id="7b956-114">Извлекает объекты [**иконтекстноде**](icontextnode.md) , связанные с этим альтернативным.</span><span class="sxs-lookup"><span data-stu-id="7b956-114">Retrieves the [**IContextNode**](icontextnode.md) objects that are associated with this alternate.</span></span><br/>                                                       |
| [<span data-ttu-id="7b956-115">**жетрекогнитионконфиденце**</span><span class="sxs-lookup"><span data-stu-id="7b956-115">**GetRecognitionConfidence**</span></span>](ianalysisalternate-getrecognitionconfidence.md) | <span data-ttu-id="7b956-116">Извлекает значение, указывающее уровень достоверности, который [**иинканализер**](iinkanalyzer.md) имеет точность **ианалисисалтернате**.</span><span class="sxs-lookup"><span data-stu-id="7b956-116">Retrieves a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the **IAnalysisAlternate**.</span></span><br/> |
| [<span data-ttu-id="7b956-117">**жетрекогнизедстринг**</span><span class="sxs-lookup"><span data-stu-id="7b956-117">**GetRecognizedString**</span></span>](ianalysisalternate-getrecognizedstring.md)           | <span data-ttu-id="7b956-118">Извлекает распознанное строковое значение объекта **ианалисисалтернате** .</span><span class="sxs-lookup"><span data-stu-id="7b956-118">Retrieves the recognized string value of the **IAnalysisAlternate** object.</span></span><br/>                                                                               |
| [<span data-ttu-id="7b956-119">**жетстрокеидс**</span><span class="sxs-lookup"><span data-stu-id="7b956-119">**GetStrokeIds**</span></span>](ianalysisalternate-getstrokeids.md)                         | <span data-ttu-id="7b956-120">Получает идентификаторы штриха, связанные с этим **ианалисисалтернате**.</span><span class="sxs-lookup"><span data-stu-id="7b956-120">Retrieves the stroke identifiers that are associated with this **IAnalysisAlternate**.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="7b956-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b956-121">Remarks</span></span>

<span data-ttu-id="7b956-122">Существует множество вариантов рукописного ввода пользователей.</span><span class="sxs-lookup"><span data-stu-id="7b956-122">There are many variations in users' handwriting.</span></span> <span data-ttu-id="7b956-123">По этой причине Распознаватели рукописного ввода иногда могут преобразовывать рукописный ввод в текст, отличный от предполагаемого пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b956-123">For that reason, handwriting recognizers can sometimes convert handwriting into text that is different from what the user intended.</span></span> <span data-ttu-id="7b956-124">Когда [**иинканализер**](iinkanalyzer.md) выполняет анализ коллекции штрихов, **иинканализер** находит наиболее вероятный набор слов, которые представляет рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="7b956-124">When an [**IInkAnalyzer**](iinkanalyzer.md) performs analysis on a collection of strokes, the **IInkAnalyzer** finds the most likely set of words that the handwriting represents.</span></span> <span data-ttu-id="7b956-125">Кроме того, **иинканализер** находит наборы альтернативных совпадений распознавания, которые хранятся в коллекции [**ианалисисалтернатес**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="7b956-125">In addition, the **IInkAnalyzer** also finds sets of alternative recognition matches, which are stored in an [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span> <span data-ttu-id="7b956-126">Чтобы пользователь мог воспользоваться преимуществами распознавания, необходимо создать пользовательский интерфейс, позволяющий пользователю выбрать правильный **ианалисисалтернате**.</span><span class="sxs-lookup"><span data-stu-id="7b956-126">In order for a user to take advantage of recognition alternates, you must create a user interface that allows the user to select the correct **IAnalysisAlternate**.</span></span>

<span data-ttu-id="7b956-127">Объекты **ианалисисалтернате** обычно получаются с помощью [**метода иинканализер::-alternate**](iinkanalyzer-getalternates.md).</span><span class="sxs-lookup"><span data-stu-id="7b956-127">**IAnalysisAlternate** objects are generally obtained through [**IInkAnalyzer::GetAlternates Method**](iinkanalyzer-getalternates.md).</span></span> <span data-ttu-id="7b956-128">Первый объект **ианалисисалтернате** в коллекции — это то, что [**иинканализер**](iinkanalyzer.md) считает наиболее вероятной альтернативой.</span><span class="sxs-lookup"><span data-stu-id="7b956-128">The first **IAnalysisAlternate** object in the collection is what the [**IInkAnalyzer**](iinkanalyzer.md) considers to be the most likely alternate.</span></span>

<span data-ttu-id="7b956-129">Этот интерфейс эквивалентен [System. Windows. Ink. аналисискоре. аналисисалтернатебасе](/previous-versions/ms610092(v=vs.100)) в платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="7b956-129">This interface is equivalent to [System.Windows.Ink.AnalysisCore.AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b956-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7b956-130">Requirements</span></span>



| <span data-ttu-id="7b956-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7b956-131">Requirement</span></span> | <span data-ttu-id="7b956-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7b956-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b956-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b956-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b956-134">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7b956-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7b956-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b956-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b956-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7b956-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7b956-137">Header</span><span class="sxs-lookup"><span data-stu-id="7b956-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b956-138"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7b956-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7b956-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7b956-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b956-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b956-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7b956-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b956-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b956-142">**ианалисисалтернатес**</span><span class="sxs-lookup"><span data-stu-id="7b956-142">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="7b956-143">**Метод Иинканализер:: Жеталтернатесфорконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="7b956-143">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="7b956-144">**Метод Иинканализер:: Жеталтернатесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="7b956-144">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="7b956-145">**Метод Иинканализер:: Alternate**</span><span class="sxs-lookup"><span data-stu-id="7b956-145">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="7b956-146">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="7b956-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

