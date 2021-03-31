---
description: Извлекает все объекты Иконтекстноде, соответствующие заданным критериям, и являются потомками указанного объекта Иконтекстноде.
ms.assetid: 48d0ae97-c4a5-458d-b4c0-fa82f5aed4e5
title: 'Метод Иинканализер:: Финднодесвискаллбаккинсубтри (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNodesWithCallBackInSubTree
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6b4ba64cd9271158d49ddd72270d4e6f25538672
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810019"
---
# <a name="iinkanalyzerfindnodeswithcallbackinsubtree-method"></a><span data-ttu-id="b1683-103">Метод Иинканализер:: Финднодесвискаллбаккинсубтри</span><span class="sxs-lookup"><span data-stu-id="b1683-103">IInkAnalyzer::FindNodesWithCallBackInSubTree method</span></span>

<span data-ttu-id="b1683-104">Извлекает все объекты [**иконтекстноде**](icontextnode.md) , соответствующие заданным критериям, и являются потомками указанного объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="b1683-104">Retrieves all of the [**IContextNode**](icontextnode.md) objects that match the specified criteria and are descendants of the specified **IContextNode** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1683-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1683-105">Syntax</span></span>


```C++
HRESULT FindNodesWithCallBackInSubTree(
  [in]  IMatchesCriteriaCallBack *pCriteria,
  [in]  IContextNode             *pContextNodeToSearchFrom,
  [out] IContextNodes            **ppContextNodesFound
);
```



## <a name="parameters"></a><span data-ttu-id="b1683-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1683-107">*пкритериа* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1683-107">*pCriteria* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1683-108">Объект [**иматческритериакаллбакк**](imatchescriteriacallback.md) , используемый для вычисления того, соответствует ли объект [**иконтекстноде**](icontextnode.md) заданным условиям или не завершается.</span><span class="sxs-lookup"><span data-stu-id="b1683-108">An [**IMatchesCriteriaCallBack**](imatchescriteriacallback.md) object that is used to evaluate whether an [**IContextNode**](icontextnode.md) object meets or fails its specified criteria.</span></span>

</dd> <dt>

<span data-ttu-id="b1683-109">*пконтекстнодетосеарчфром* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1683-109">*pContextNodeToSearchFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1683-110">Объект [**иконтекстноде**](icontextnode.md) , потомки которого ищутся.</span><span class="sxs-lookup"><span data-stu-id="b1683-110">The [**IContextNode**](icontextnode.md) object whose descendants are searched.</span></span>

</dd> <dt>

<span data-ttu-id="b1683-111">*ппконтекстнодесфаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b1683-111">*ppContextNodesFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1683-112">Указатель на [**иконтекстнодес**](icontextnodes.md) , содержащий все узлы, соответствующие заданным критериям.</span><span class="sxs-lookup"><span data-stu-id="b1683-112">A pointer to the [**IContextNodes**](icontextnodes.md) containing all nodes that meet the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1683-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1683-113">Return value</span></span>

<span data-ttu-id="b1683-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b1683-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1683-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1683-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="b1683-116">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодесфаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="b1683-116">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodesFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="b1683-117">Если [**иинканализер**](iinkanalyzer.md) не содержит узел *пконтекстнодетосеарчфром* , этот метод возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1683-117">If the [**IInkAnalyzer**](iinkanalyzer.md) does not contain the *pContextNodeToSearchFrom* node, this method returns an error code.</span></span>

<span data-ttu-id="b1683-118">Если [**иинканализер**](iinkanalyzer.md) не содержит таких [**иконтекстноде**](icontextnode.md), возвращается пустая коллекция [**иконтекстнодес**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="b1683-118">If the [**IInkAnalyzer**](iinkanalyzer.md) contains no such [**IContextNode**](icontextnode.md), an empty [**IContextNodes**](icontextnodes.md) collection is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1683-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b1683-119">Requirements</span></span>



| <span data-ttu-id="b1683-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b1683-120">Requirement</span></span> | <span data-ttu-id="b1683-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b1683-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1683-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1683-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1683-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b1683-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1683-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1683-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1683-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b1683-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b1683-126">Header</span><span class="sxs-lookup"><span data-stu-id="b1683-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1683-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b1683-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b1683-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b1683-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1683-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1683-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b1683-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1683-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1683-131">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="b1683-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b1683-132">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="b1683-132">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="b1683-133">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="b1683-133">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b1683-134">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="b1683-134">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="b1683-135">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="b1683-135">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="b1683-136">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="b1683-136">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="b1683-137">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="b1683-137">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b1683-138">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="b1683-138">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b1683-139">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="b1683-139">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="b1683-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="b1683-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

