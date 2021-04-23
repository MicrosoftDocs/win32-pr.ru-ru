---
description: Происходит перед тем, как Иинканализер перемещает объект Иконтекстноде в новую точку в коллекции подузлов родительского узла.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: 'Событие _IAnalysisProxyEvents:: Контекстнодемовингтопоситион (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703497"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a><span data-ttu-id="70af2-103">\_Событие Ианалисиспроксевентс:: Контекстнодемовингтопоситион</span><span class="sxs-lookup"><span data-stu-id="70af2-103">\_IAnalysisProxyEvents::ContextNodeMovingToPosition event</span></span>

<span data-ttu-id="70af2-104">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) в новую точку в коллекции подузлов родительского узла.</span><span class="sxs-lookup"><span data-stu-id="70af2-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="70af2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70af2-105">Syntax</span></span>


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a><span data-ttu-id="70af2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="70af2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70af2-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70af2-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70af2-108">Объект [**иинканализер**](iinkanalyzer.md) , перемещающий объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="70af2-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="70af2-109">*писубнодетомове* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70af2-109">*pISubNodeToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70af2-110">Перемещаемый объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="70af2-110">The [**IContextNode**](icontextnode.md) object to move.</span></span>

</dd> <dt>

<span data-ttu-id="70af2-111">*ппарентконтекстноде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70af2-111">*pParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70af2-112">Родительский объект [**иконтекстноде**](icontextnode.md) объекта *писубнодетомове*.</span><span class="sxs-lookup"><span data-stu-id="70af2-112">The parent [**IContextNode**](icontextnode.md) object of *pISubNodeToMove*.</span></span>

</dd> <dt>

<span data-ttu-id="70af2-113">*улневиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="70af2-113">*ulNewIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70af2-114">Новое расположение *писубнодетомове* в коллекции подузлов родительского узла.</span><span class="sxs-lookup"><span data-stu-id="70af2-114">The new location of *pISubNodeToMove* in its parent node's collection of subnodes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70af2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70af2-115">Return value</span></span>

<span data-ttu-id="70af2-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="70af2-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70af2-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70af2-117">Remarks</span></span>

<span data-ttu-id="70af2-118">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="70af2-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="70af2-119">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализатора рукописного ввода, который перемещает [**иконтекстноде**](icontextnode.md) в коллекцию подузлов родительского узла (см. раздел [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) and [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="70af2-119">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that moves an [**IContextNode**](icontextnode.md) within its parent node's collection of subnodes (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="70af2-120">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="70af2-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70af2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="70af2-121">Requirements</span></span>



| <span data-ttu-id="70af2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="70af2-122">Requirement</span></span> | <span data-ttu-id="70af2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="70af2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70af2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70af2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70af2-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="70af2-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70af2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70af2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70af2-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="70af2-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="70af2-128">Header</span><span class="sxs-lookup"><span data-stu-id="70af2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="70af2-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="70af2-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="70af2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="70af2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70af2-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70af2-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="70af2-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70af2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70af2-133">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="70af2-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="70af2-134">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="70af2-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="70af2-135">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="70af2-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="70af2-136">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="70af2-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="70af2-137">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="70af2-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="70af2-138">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="70af2-138">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="70af2-139">**Иконтекстноде:: Жетсубнодес**</span><span class="sxs-lookup"><span data-stu-id="70af2-139">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="70af2-140">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="70af2-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




