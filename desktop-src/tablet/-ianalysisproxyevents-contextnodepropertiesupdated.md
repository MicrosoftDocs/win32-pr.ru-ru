---
description: Происходит после того, как Иинканализер обновляет одно или несколько свойств объекта Иконтекстноде.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: 'Событие _IAnalysisProxyEvents:: Контекстнодепропертиесупдатед (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105703493"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a><span data-ttu-id="34025-103">\_Событие Ианалисиспроксевентс:: Контекстнодепропертиесупдатед</span><span class="sxs-lookup"><span data-stu-id="34025-103">\_IAnalysisProxyEvents::ContextNodePropertiesUpdated event</span></span>

<span data-ttu-id="34025-104">Происходит после того, как [**иинканализер**](iinkanalyzer.md) обновляет одно или несколько свойств объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="34025-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="34025-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34025-105">Syntax</span></span>


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a><span data-ttu-id="34025-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="34025-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34025-107">*пинканализер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34025-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34025-108">Объект [**иинканализер**](iinkanalyzer.md) , обновляющий свойства.</span><span class="sxs-lookup"><span data-stu-id="34025-108">The [**IInkAnalyzer**](iinkanalyzer.md) object updating the properties.</span></span>

</dd> <dt>

<span data-ttu-id="34025-109">*пконтекстнодеупдатед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="34025-109">*pContextNodeUpdated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34025-110">Объект [**иконтекстноде**](icontextnode.md) , свойства которого обновляются.</span><span class="sxs-lookup"><span data-stu-id="34025-110">The [**IContextNode**](icontextnode.md) object whose properties are updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34025-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34025-111">Return value</span></span>

<span data-ttu-id="34025-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="34025-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="34025-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34025-113">Remarks</span></span>

<span data-ttu-id="34025-114">Это событие используется, когда приложение поддерживает собственную структуру данных, которая синхронизируется с [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="34025-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="34025-115">Это событие возникает на этапе выверки анализа рукописного текста или в ответ на метод анализатора рукописного ввода, который изменяет свойства [**иконтекстноде**](icontextnode.md) (см. [**Иконтекстноде:: жетпропертидата**](icontextnode-getpropertydata.md)).</span><span class="sxs-lookup"><span data-stu-id="34025-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that changes the properties of an [**IContextNode**](icontextnode.md) (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)).</span></span>

<span data-ttu-id="34025-116">Дополнительные сведения о синхронизации данных приложения с помощью [**иинканализер**](iinkanalyzer.md)см. в разделе [учетная запись-посредник данных с помощью анализа рукописного ввода](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="34025-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="34025-117">Требования</span><span class="sxs-lookup"><span data-stu-id="34025-117">Requirements</span></span>



| <span data-ttu-id="34025-118">Требование</span><span class="sxs-lookup"><span data-stu-id="34025-118">Requirement</span></span> | <span data-ttu-id="34025-119">Значение</span><span class="sxs-lookup"><span data-stu-id="34025-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34025-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34025-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34025-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="34025-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="34025-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34025-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34025-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="34025-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="34025-124">Header</span><span class="sxs-lookup"><span data-stu-id="34025-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34025-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="34025-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="34025-126">DLL</span><span class="sxs-lookup"><span data-stu-id="34025-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34025-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34025-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="34025-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34025-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34025-129">**\_ианалисиспроксевентс**</span><span class="sxs-lookup"><span data-stu-id="34025-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="34025-130">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="34025-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="34025-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="34025-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="34025-132">**Метод Иинканализер:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="34025-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="34025-133">**Метод Иинканализер:: Баккграунданализе**</span><span class="sxs-lookup"><span data-stu-id="34025-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="34025-134">Свойства узла контекста</span><span class="sxs-lookup"><span data-stu-id="34025-134">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="34025-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="34025-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




