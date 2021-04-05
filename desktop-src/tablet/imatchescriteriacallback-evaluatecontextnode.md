---
description: При переопределении в производном классе проверяет, соответствует ли указанный объект Иконтекстноде критериям.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'Метод Иматческритериакаллбакк:: Евалуатеконтекстноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647159"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a><span data-ttu-id="224f4-103">Метод Иматческритериакаллбакк:: Евалуатеконтекстноде</span><span class="sxs-lookup"><span data-stu-id="224f4-103">IMatchesCriteriaCallBack::EvaluateContextNode method</span></span>

<span data-ttu-id="224f4-104">При переопределении в производном классе проверяет, соответствует ли указанный объект [**иконтекстноде**](icontextnode.md) критериям.</span><span class="sxs-lookup"><span data-stu-id="224f4-104">When overridden in a derived class, evaluates whether a specified [**IContextNode**](icontextnode.md) object meets the criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="224f4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="224f4-105">Syntax</span></span>


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a><span data-ttu-id="224f4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="224f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224f4-107">*пконтекстнодетоевалуате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="224f4-107">*pContextNodeToEvaluate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="224f4-108">Объект [**иконтекстноде**](icontextnode.md) для вычисления.</span><span class="sxs-lookup"><span data-stu-id="224f4-108">The [**IContextNode**](icontextnode.md) object to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="224f4-109">*пбресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="224f4-109">*pbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="224f4-110">**Вариант \_ Значение TRUE** , если *пконтекстнодетоевалуате* соответствует критериям; в противном случае — **\_ значение false**.</span><span class="sxs-lookup"><span data-stu-id="224f4-110">**VARIANT\_TRUE** if *pContextNodeToEvaluate* matches the criteria; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224f4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="224f4-111">Return value</span></span>

<span data-ttu-id="224f4-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="224f4-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="224f4-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="224f4-113">Remarks</span></span>

<span data-ttu-id="224f4-114">Чтобы использовать метод [**иинканализер:: финднодесвискаллбакк**](iinkanalyzer-findnodeswithcallback.md) или [**метод Иинканализер:: финднодесвискаллбаккинсубтри**](iinkanalyzer-findnodeswithcallbackinsubtree.md), создайте класс, реализующий [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span><span class="sxs-lookup"><span data-stu-id="224f4-114">To use [**IInkAnalyzer::FindNodesWithCallBack Method**](iinkanalyzer-findnodeswithcallback.md) or [**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**](iinkanalyzer-findnodeswithcallbackinsubtree.md), create a class that implements [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md).</span></span> <span data-ttu-id="224f4-115">Реализуйте **иматческритериакаллбакк:: евалуатеконтекстноде** , чтобы вернуть **вариант \_ true** , если объект [**иконтекстноде**](icontextnode.md) соответствует Вашему критерию, и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="224f4-115">Implement **IMatchesCriteriaCallBack::EvaluateContextNode** to return **VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object matches your criteria, and **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="224f4-116">Для некоторых критериев может потребоваться предоставить возможность инициализации или обслуживания состояния объекта **иматческритериакаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="224f4-116">For some criteria, you may need to provide a means of initializing or maintaining the state of your **IMatchesCriteriaCallBack** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="224f4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="224f4-117">Requirements</span></span>



| <span data-ttu-id="224f4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="224f4-118">Requirement</span></span> | <span data-ttu-id="224f4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="224f4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="224f4-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="224f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="224f4-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="224f4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="224f4-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="224f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="224f4-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="224f4-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="224f4-124">Header</span><span class="sxs-lookup"><span data-stu-id="224f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="224f4-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="224f4-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="224f4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="224f4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="224f4-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="224f4-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="224f4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="224f4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224f4-129">**иматческритериакаллбакк**</span><span class="sxs-lookup"><span data-stu-id="224f4-129">**IMatchesCriteriaCallBack**</span></span>](imatchescriteriacallback.md)
</dt> <dt>

[<span data-ttu-id="224f4-130">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="224f4-130">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="224f4-131">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="224f4-131">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="224f4-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="224f4-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




