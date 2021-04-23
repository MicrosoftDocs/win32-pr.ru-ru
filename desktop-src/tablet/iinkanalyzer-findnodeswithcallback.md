---
description: Извлекает все объекты Иконтекстноде, соответствующие указанным критериям.
ms.assetid: c0ba46f4-a286-454a-8de2-6663fd2dfed6
title: 'Метод Иинканализер:: Финднодесвискаллбакк (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b34501e33d637ca65f13e6e2e5ea0a9001b06198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810024"
---
# <a name="iinkanalyzerfindnodeswithcallback-method"></a><span data-ttu-id="56037-103">Метод Иинканализер:: Финднодесвискаллбакк</span><span class="sxs-lookup"><span data-stu-id="56037-103">IInkAnalyzer::FindNodesWithCallBack method</span></span>

<span data-ttu-id="56037-104">Извлекает все объекты [**иконтекстноде**](icontextnode.md) , соответствующие указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="56037-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="56037-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56037-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBack(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="56037-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="56037-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56037-107">*пкритериа* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56037-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56037-108">Объект [**иматческритериакаллбакк**](imatchescriteriacallback.md) , используемый для вычисления того, соответствует ли объект [**иконтекстноде**](icontextnode.md) заданным условиям или не завершается.</span><span class="sxs-lookup"><span data-stu-id="56037-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="56037-109">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="56037-109">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56037-110">Указатель на коллекцию [**иконтекстнодес**](icontextnodes.md) , содержащую все узлы, соответствующие указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="56037-110">A pointer to the [**IContextNodes**](icontextnodes.md) collection containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56037-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56037-111">Return value</span></span>

<span data-ttu-id="56037-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="56037-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="56037-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56037-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="56037-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="56037-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="56037-115">Если [**иинканализер**](iinkanalyzer.md) не содержит таких [**иконтекстноде**](icontextnode.md), возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="56037-115">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="56037-116">Требования</span><span class="sxs-lookup"><span data-stu-id="56037-116">Requirements</span></span>



| <span data-ttu-id="56037-117">Требование</span><span class="sxs-lookup"><span data-stu-id="56037-117">Requirement</span></span> | <span data-ttu-id="56037-118">Значение</span><span class="sxs-lookup"><span data-stu-id="56037-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56037-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56037-119">Minimum supported client</span></span><br/> | <span data-ttu-id="56037-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="56037-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="56037-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56037-121">Minimum supported server</span></span><br/> | <span data-ttu-id="56037-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="56037-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="56037-123">Header</span><span class="sxs-lookup"><span data-stu-id="56037-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56037-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="56037-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="56037-125">DLL</span><span class="sxs-lookup"><span data-stu-id="56037-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56037-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56037-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="56037-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56037-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56037-128">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="56037-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="56037-129">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="56037-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="56037-130">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="56037-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="56037-131">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="56037-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="56037-132">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="56037-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="56037-133">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="56037-133">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="56037-134">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="56037-134">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="56037-135">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="56037-135">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="56037-136">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="56037-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="56037-137">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="56037-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

