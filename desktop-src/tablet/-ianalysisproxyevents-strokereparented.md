---
description: Происходит, когда Иинканализер перемещает штрих из одного объекта Иконтекстноде в другой.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: 'Событие _IAnalysisProxyEvents:: Строкерепарентед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703495"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a><span data-ttu-id="cf273-103">\_Событие Ианалисиспроксевентс:: Строкерепарентед</span><span class="sxs-lookup"><span data-stu-id="cf273-103">\_IAnalysisProxyEvents::StrokeReparented event</span></span>

<span data-ttu-id="cf273-104">Происходит, когда [**иинканализер**](iinkanalyzer.md) перемещает штрих из одного объекта [**иконтекстноде**](icontextnode.md) в другой.</span><span class="sxs-lookup"><span data-stu-id="cf273-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf273-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf273-105">Syntax</span></span>


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="cf273-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf273-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf273-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf273-108">Объект [**иинканализер**](iinkanalyzer.md) , который перемещает штрих.</span><span class="sxs-lookup"><span data-stu-id="cf273-108">The [**IInkAnalyzer**](iinkanalyzer.md) object moving the stroke.</span></span>

</dd> <dt>

<span data-ttu-id="cf273-109">*лстрокеидтомове* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf273-109">*lStrokeIdToMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf273-110">Идентификатор перемещаемого штриха.</span><span class="sxs-lookup"><span data-stu-id="cf273-110">The identifier of the stroke to move.</span></span>

</dd> <dt>

<span data-ttu-id="cf273-111">*псаурцеконтекстноде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf273-111">*pSourceContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf273-112">Объект [**иконтекстноде**](icontextnode.md) , из которого перемещается штрих.</span><span class="sxs-lookup"><span data-stu-id="cf273-112">The [**IContextNode**](icontextnode.md) object from which the stroke is moved.</span></span>

</dd> <dt>

<span data-ttu-id="cf273-113">*пдестинатионконтекстноде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf273-113">*pDestinationContextNode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf273-114">Объект [**иконтекстноде**](icontextnode.md) , в который перемещается штрих.</span><span class="sxs-lookup"><span data-stu-id="cf273-114">The [**IContextNode**](icontextnode.md) object to which the stroke is moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf273-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf273-115">Return value</span></span>

<span data-ttu-id="cf273-116">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cf273-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cf273-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf273-117">Remarks</span></span>

<span data-ttu-id="cf273-118">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="cf273-118">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="cf273-119">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод **иинканализер** , который перемещает данные штриха из одного [**иконтекстноде**](icontextnode.md) в другой.</span><span class="sxs-lookup"><span data-stu-id="cf273-119">This event occurs during the reconcile phase of ink analysis, or in response to an **IInkAnalyzer** method that moves stroke data from one [**IContextNode**](icontextnode.md) to another.</span></span>

<span data-ttu-id="cf273-120">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cf273-120">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf273-121">Требования</span><span class="sxs-lookup"><span data-stu-id="cf273-121">Requirements</span></span>



| <span data-ttu-id="cf273-122">Требование</span><span class="sxs-lookup"><span data-stu-id="cf273-122">Requirement</span></span> | <span data-ttu-id="cf273-123">Значение</span><span class="sxs-lookup"><span data-stu-id="cf273-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf273-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf273-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cf273-125">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cf273-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cf273-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf273-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cf273-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cf273-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cf273-128">Header</span><span class="sxs-lookup"><span data-stu-id="cf273-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf273-129"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cf273-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cf273-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cf273-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf273-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf273-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cf273-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf273-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf273-133">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="cf273-133">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="cf273-134">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="cf273-134">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cf273-135">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="cf273-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="cf273-136">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="cf273-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="cf273-137">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="cf273-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="cf273-138">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="cf273-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




