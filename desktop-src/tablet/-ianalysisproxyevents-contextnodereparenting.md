---
description: Происходит перед тем, как Иинканализер перемещает объект Иконтекстноде, изменяя его родительский узел.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: 'Событие _IAnalysisProxyEvents:: Контекстнодерепарентинг (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703511"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a><span data-ttu-id="2a479-103">\_Событие Ианалисиспроксевентс:: Контекстнодерепарентинг</span><span class="sxs-lookup"><span data-stu-id="2a479-103">\_IAnalysisProxyEvents::ContextNodeReparenting event</span></span>

<span data-ttu-id="2a479-104">Происходит перед тем, как [**иинканализер**](iinkanalyzer.md) перемещает объект [**иконтекстноде**](icontextnode.md) , изменяя его родительский узел.</span><span class="sxs-lookup"><span data-stu-id="2a479-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a479-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a479-105">Syntax</span></span>


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a><span data-ttu-id="2a479-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a479-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a479-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a479-108">Объект [**иинканализер**](iinkanalyzer.md) , перемещающий объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="2a479-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2a479-109">*пневпарентконтекстноде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a479-109">*pNewParentContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a479-110">Новый родительский объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="2a479-110">The new parent [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2a479-111">*пконтекстнодетоберепарентед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2a479-111">*pContextNodeToBeReparented* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a479-112">Перемещаемый объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="2a479-112">The [**IContextNode**](icontextnode.md) object to be moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a479-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a479-113">Return value</span></span>

<span data-ttu-id="2a479-114">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2a479-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2a479-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a479-115">Remarks</span></span>

<span data-ttu-id="2a479-116">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="2a479-116">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="2a479-117">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод, который перемещает [**иконтекстноде**](icontextnode.md) из одной коллекции подузлов в другую (см. [**Иконтекстноде:: жетпарентноде**](icontextnode-getparentnode.md) и [**иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="2a479-117">This event occurs during the reconcile phase of ink analysis, or in response to a method that moves an [**IContextNode**](icontextnode.md) from one collection of subnodes to another (see [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) and [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span>

<span data-ttu-id="2a479-118">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2a479-118">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a479-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2a479-119">Requirements</span></span>



| <span data-ttu-id="2a479-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2a479-120">Requirement</span></span> | <span data-ttu-id="2a479-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2a479-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a479-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a479-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2a479-123">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2a479-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2a479-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a479-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2a479-125">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2a479-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2a479-126">Header</span><span class="sxs-lookup"><span data-stu-id="2a479-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a479-127"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2a479-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2a479-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2a479-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a479-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a479-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2a479-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a479-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a479-131">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="2a479-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="2a479-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="2a479-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="2a479-133">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="2a479-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2a479-134">**Иконтекстноде:: Жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="2a479-134">**IContextNode::GetParentNode**</span></span>](icontextnode-getparentnode.md)
</dt> <dt>

[<span data-ttu-id="2a479-135">**Иконтекстноде:: Жетсубнодес**</span><span class="sxs-lookup"><span data-stu-id="2a479-135">**IContextNode::GetSubNodes**</span></span>](icontextnode-getsubnodes.md)
</dt> <dt>

[<span data-ttu-id="2a479-136">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="2a479-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="2a479-137">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="2a479-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="2a479-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="2a479-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




