---
description: Предоставляет доступ к распознавателям рукописного ввода для использования с анализом рукописного текста.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Интерфейс Иинканалисисрекогнизер (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692432"
---
# <a name="iinkanalysisrecognizer-interface"></a><span data-ttu-id="a2959-103">Интерфейс Иинканалисисрекогнизер</span><span class="sxs-lookup"><span data-stu-id="a2959-103">IInkAnalysisRecognizer interface</span></span>

<span data-ttu-id="a2959-104">Предоставляет доступ к распознавателям рукописного ввода для использования с анализом рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="a2959-104">Provides access to handwriting recognizers for use with ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="a2959-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="a2959-105">Members</span></span>

<span data-ttu-id="a2959-106">Интерфейс **иинканалисисрекогнизер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a2959-106">The **IInkAnalysisRecognizer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a2959-107">**Иинканалисисрекогнизер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a2959-107">**IInkAnalysisRecognizer** also has these types of members:</span></span>

-   [<span data-ttu-id="a2959-108">Методы</span><span class="sxs-lookup"><span data-stu-id="a2959-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a2959-109">Методы</span><span class="sxs-lookup"><span data-stu-id="a2959-109">Methods</span></span>

<span data-ttu-id="a2959-110">Интерфейс **иинканалисисрекогнизер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a2959-110">The **IInkAnalysisRecognizer** interface has these methods.</span></span>



| <span data-ttu-id="a2959-111">Метод</span><span class="sxs-lookup"><span data-stu-id="a2959-111">Method</span></span>                                                                          | <span data-ttu-id="a2959-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a2959-112">Description</span></span>                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2959-113">**Возможности**</span><span class="sxs-lookup"><span data-stu-id="a2959-113">**GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)               | <span data-ttu-id="a2959-114">Получает возможности распознавателя.</span><span class="sxs-lookup"><span data-stu-id="a2959-114">Retrieves the capabilities of the recognizer.</span></span><br/>                                                                       |
| [<span data-ttu-id="a2959-115">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="a2959-115">**GetGuid**</span></span>](iinkanalysisrecognizer-getguid.md)                               | <span data-ttu-id="a2959-116">Получает глобальный уникальный идентификатор (GUID) распознавателя.</span><span class="sxs-lookup"><span data-stu-id="a2959-116">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span><br/>                                                  |
| [<span data-ttu-id="a2959-117">**Языки**</span><span class="sxs-lookup"><span data-stu-id="a2959-117">**GetLanguages**</span></span>](iinkanalysisrecognizer-getlanguages.md)                     | <span data-ttu-id="a2959-118">Получает идентификаторы для языковых стандартов, которые поддерживает эта **иинканалисисрекогнизер** .</span><span class="sxs-lookup"><span data-stu-id="a2959-118">Retrieves the identifiers for the locales that this **IInkAnalysisRecognizer** supports.</span></span><br/>                            |
| [<span data-ttu-id="a2959-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="a2959-119">**GetName**</span></span>](iinkanalysisrecognizer-getname.md)                               | <span data-ttu-id="a2959-120">Возвращает имя распознавателя.</span><span class="sxs-lookup"><span data-stu-id="a2959-120">Retrieves the name of the recognizer.</span></span><br/>                                                                               |
| [<span data-ttu-id="a2959-121">**жетсуппортедпропертиес**</span><span class="sxs-lookup"><span data-stu-id="a2959-121">**GetSupportedProperties**</span></span>](iinkanalysisrecognizer-getsupportedproperties.md) | <span data-ttu-id="a2959-122">Получает идентификаторы GUID для свойств, которые поддерживает эта **иинканалисисрекогнизер** .</span><span class="sxs-lookup"><span data-stu-id="a2959-122">Retrieves the globally unique identifiers (GUIDs) for the properties that this **IInkAnalysisRecognizer** supports.</span></span><br/> |
| [<span data-ttu-id="a2959-123">**Поставщик**</span><span class="sxs-lookup"><span data-stu-id="a2959-123">**GetVendor**</span></span>](iinkanalysisrecognizer-getvendor.md)                           | <span data-ttu-id="a2959-124">Возвращает имя поставщика **иинканалисисрекогнизер**.</span><span class="sxs-lookup"><span data-stu-id="a2959-124">Retrieves the vendor name of the **IInkAnalysisRecognizer**.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="a2959-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2959-125">Remarks</span></span>

<span data-ttu-id="a2959-126">Распознаватель имеет определенные атрибуты и свойства, позволяющие ему выполнять распознавание.</span><span class="sxs-lookup"><span data-stu-id="a2959-126">A recognizer has specific attributes and properties that allow it to perform recognition.</span></span> <span data-ttu-id="a2959-127">Свойства распознавателя должны быть определены до того, как будет выполнено распознавание.</span><span class="sxs-lookup"><span data-stu-id="a2959-127">The properties of a recognizer must be determined before recognition can occur.</span></span> <span data-ttu-id="a2959-128">Типы свойств, поддерживаемых распознавателем, определяют типы распознавания, которые он может выполнять.</span><span class="sxs-lookup"><span data-stu-id="a2959-128">The types of properties that a recognizer supports determine the types of recognition that it can perform.</span></span> <span data-ttu-id="a2959-129">Например, если распознаватель не поддерживает письменный рукописный ввод, он возвращает неточные результаты, когда пользователь пишет письменно.</span><span class="sxs-lookup"><span data-stu-id="a2959-129">For instance, if a recognizer does not support cursive handwriting, it returns inaccurate results when a user writes in cursive.</span></span>

<span data-ttu-id="a2959-130">Распознаватель также имеет встроенные функции, которые автоматически управляют многими аспектами рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="a2959-130">A recognizer also has built-in functionality that automatically manages many aspects of handwriting.</span></span> <span data-ttu-id="a2959-131">Например, он определяет метрики линий, на которых рисуются штрихи.</span><span class="sxs-lookup"><span data-stu-id="a2959-131">For instance, it determines the metrics for the lines on which strokes are drawn.</span></span> <span data-ttu-id="a2959-132">Можно вернуть номер строки штриха, но не нужно указывать, как эти метрики линии определяются из-за встроенной функциональности распознавателя.</span><span class="sxs-lookup"><span data-stu-id="a2959-132">You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.</span></span>

<span data-ttu-id="a2959-133">[**Иинканализер**](iinkanalyzer.md) поддерживает список доступных распознавателей.</span><span class="sxs-lookup"><span data-stu-id="a2959-133">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a list of available recognizers.</span></span> <span data-ttu-id="a2959-134">Чтобы получить доступ к этому списку, используйте метод [**метода иинканализер:: жетинканалисисрекогнизерсбиприорити**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) .</span><span class="sxs-lookup"><span data-stu-id="a2959-134">To access this list, use the [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2959-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a2959-135">Requirements</span></span>



| <span data-ttu-id="a2959-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a2959-136">Requirement</span></span> | <span data-ttu-id="a2959-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a2959-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2959-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2959-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a2959-139">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a2959-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a2959-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2959-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a2959-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a2959-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a2959-142">Header</span><span class="sxs-lookup"><span data-stu-id="a2959-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2959-143"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a2959-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a2959-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a2959-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2959-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2959-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a2959-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2959-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2959-147">**иинканалисисрекогнизерс**</span><span class="sxs-lookup"><span data-stu-id="a2959-147">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="a2959-148">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="a2959-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a2959-149">**Метод Иинканализер:: Креатекустомрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="a2959-149">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="a2959-150">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="a2959-150">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="a2959-151">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="a2959-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

