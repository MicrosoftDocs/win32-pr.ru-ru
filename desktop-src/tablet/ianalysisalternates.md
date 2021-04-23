---
description: Содержит коллекцию объектов, реализующих интерфейс Ианалисисалтернате и являющихся результатом анализа рукописного ввода.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Интерфейс Ианалисисалтернатес (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692454"
---
# <a name="ianalysisalternates-interface"></a><span data-ttu-id="54149-103">Интерфейс Ианалисисалтернатес</span><span class="sxs-lookup"><span data-stu-id="54149-103">IAnalysisAlternates interface</span></span>

<span data-ttu-id="54149-104">Содержит коллекцию объектов, реализующих интерфейс [**ианалисисалтернате**](ianalysisalternate.md) и являющихся результатом анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="54149-104">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="54149-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="54149-105">Members</span></span>

<span data-ttu-id="54149-106">Интерфейс **ианалисисалтернатес** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="54149-106">The **IAnalysisAlternates** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="54149-107">**Ианалисисалтернатес** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="54149-107">**IAnalysisAlternates** also has these types of members:</span></span>

-   [<span data-ttu-id="54149-108">Методы</span><span class="sxs-lookup"><span data-stu-id="54149-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54149-109">Методы</span><span class="sxs-lookup"><span data-stu-id="54149-109">Methods</span></span>

<span data-ttu-id="54149-110">Интерфейс **ианалисисалтернатес** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="54149-110">The **IAnalysisAlternates** interface has these methods.</span></span>



| <span data-ttu-id="54149-111">Метод</span><span class="sxs-lookup"><span data-stu-id="54149-111">Method</span></span>                                                                   | <span data-ttu-id="54149-112">Описание</span><span class="sxs-lookup"><span data-stu-id="54149-112">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54149-113">**жетаналисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="54149-113">**GetAnalysisAlternate**</span></span>](ianalysisalternates-getanalysisalternate.md) | <span data-ttu-id="54149-114">Извлекает объект [**ианалисисалтернате**](ianalysisalternate.md) по указанному индексу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="54149-114">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span><br/>                   |
| [<span data-ttu-id="54149-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="54149-115">**GetCount**</span></span>](ianalysisalternates-getcount.md)                         | <span data-ttu-id="54149-116">Возвращает количество объектов [**ианалисисалтернате**](ianalysisalternate.md) , содержащихся в коллекции **ианалисисалтернатес** .</span><span class="sxs-lookup"><span data-stu-id="54149-116">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the **IAnalysisAlternates** collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54149-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54149-117">Remarks</span></span>

<span data-ttu-id="54149-118">Этот интерфейс эквивалентен классу [**System. Windows. Ink. аналисискоре. аналисисалтернатебасеколлектион**](/previous-versions/ms610094(v=vs.100)) в платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="54149-118">This interface is equivalent to the [**System.Windows.Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="54149-119">Требования</span><span class="sxs-lookup"><span data-stu-id="54149-119">Requirements</span></span>



| <span data-ttu-id="54149-120">Требование</span><span class="sxs-lookup"><span data-stu-id="54149-120">Requirement</span></span> | <span data-ttu-id="54149-121">Значение</span><span class="sxs-lookup"><span data-stu-id="54149-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54149-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54149-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54149-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="54149-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="54149-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54149-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54149-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="54149-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="54149-126">Header</span><span class="sxs-lookup"><span data-stu-id="54149-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54149-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="54149-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="54149-128">DLL</span><span class="sxs-lookup"><span data-stu-id="54149-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54149-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54149-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="54149-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54149-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54149-131">**ианалисисалтернате**</span><span class="sxs-lookup"><span data-stu-id="54149-131">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="54149-132">**Метод Иинканализер:: Alternate**</span><span class="sxs-lookup"><span data-stu-id="54149-132">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="54149-133">**Метод Иинканализер:: Жеталтернатесфорконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="54149-133">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="54149-134">**Метод Иинканализер:: Жеталтернатесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="54149-134">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="54149-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="54149-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

