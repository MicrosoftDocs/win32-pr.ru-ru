---
description: Предоставляет метод для определения того, соответствует ли объект Иконтекстноде или завершается с указанными критериями.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Интерфейс Иматческритериакаллбакк (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540450"
---
# <a name="imatchescriteriacallback-interface"></a><span data-ttu-id="e4220-103">Интерфейс Иматческритериакаллбакк</span><span class="sxs-lookup"><span data-stu-id="e4220-103">IMatchesCriteriaCallBack interface</span></span>

<span data-ttu-id="e4220-104">Предоставляет метод для определения того, соответствует ли объект [**иконтекстноде**](icontextnode.md) или завершается с указанными критериями.</span><span class="sxs-lookup"><span data-stu-id="e4220-104">Exposes a method to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails a specified criteria.</span></span>

## <a name="members"></a><span data-ttu-id="e4220-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="e4220-105">Members</span></span>

<span data-ttu-id="e4220-106">Интерфейс **иматческритериакаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e4220-106">The **IMatchesCriteriaCallBack** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e4220-107">**Иматческритериакаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e4220-107">**IMatchesCriteriaCallBack** also has these types of members:</span></span>

-   [<span data-ttu-id="e4220-108">Методы</span><span class="sxs-lookup"><span data-stu-id="e4220-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e4220-109">Методы</span><span class="sxs-lookup"><span data-stu-id="e4220-109">Methods</span></span>

<span data-ttu-id="e4220-110">Интерфейс **иматческритериакаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e4220-110">The **IMatchesCriteriaCallBack** interface has these methods.</span></span>



| <span data-ttu-id="e4220-111">Метод</span><span class="sxs-lookup"><span data-stu-id="e4220-111">Method</span></span>                                                                      | <span data-ttu-id="e4220-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e4220-112">Description</span></span>                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4220-113">**евалуатеконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="e4220-113">**EvaluateContextNode**</span></span>](imatchescriteriacallback-evaluatecontextnode.md) | <span data-ttu-id="e4220-114">При переопределении в производном классе проверяет, соответствует ли указанный объект [**иконтекстноде**](icontextnode.md) критериям.</span><span class="sxs-lookup"><span data-stu-id="e4220-114">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4220-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4220-115">Remarks</span></span>

<span data-ttu-id="e4220-116">Чтобы использовать метод [**иинканализер:: финднодесвискаллбакк**](iinkanalyzer-findnodeswithcallback.md) или [**метод Иинканализер:: финднодесвискаллбаккинсубтри**](iinkanalyzer-findnodeswithcallbackinsubtree.md), создайте класс, реализующий **IMatchesCriteriaCallBack**.</span><span class="sxs-lookup"><span data-stu-id="e4220-116">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements **IMatchesCriteriaCallBack**.</span></span> <span data-ttu-id="e4220-117">Реализуйте [**иматческритериакаллбакк:: евалуатеконтекстноде**](imatchescriteriacallback-evaluatecontextnode.md) , чтобы вернуть **вариант \_ true** , если объект [**иконтекстноде**](icontextnode.md) соответствует Вашему критерию, и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e4220-117">Implement [**IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="e4220-118">Для некоторых критериев может потребоваться предоставить возможность инициализации или обслуживания состояния объекта **иматческритериакаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="e4220-118">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4220-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e4220-119">Requirements</span></span>



| <span data-ttu-id="e4220-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e4220-120">Requirement</span></span> | <span data-ttu-id="e4220-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e4220-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4220-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4220-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e4220-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e4220-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e4220-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4220-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e4220-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e4220-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e4220-126">Header</span><span class="sxs-lookup"><span data-stu-id="e4220-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4220-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e4220-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e4220-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e4220-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4220-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4220-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e4220-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4220-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4220-131">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e4220-131">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="e4220-132">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="e4220-132">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="e4220-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="e4220-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

