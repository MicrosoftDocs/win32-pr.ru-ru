---
description: Возвращает все Иконтекстноденые в подсказках анализа объекты, присоединенные к Иинканализер.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'Метод Иинканализер:: Жетаналисишинтс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145460"
---
# <a name="iinkanalyzergetanalysishints-method"></a><span data-ttu-id="6f93a-103">Метод Иинканализер:: Жетаналисишинтс</span><span class="sxs-lookup"><span data-stu-id="6f93a-103">IInkAnalyzer::GetAnalysisHints method</span></span>

<span data-ttu-id="6f93a-104">Возвращает все [**иконтекстноденые**](icontextnode.md) в подсказках анализа объекты, присоединенные к [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="6f93a-104">Gets all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f93a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f93a-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="6f93a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6f93a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f93a-107">*ппаналисишинтс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6f93a-107">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f93a-108">Указатель на все подсказку анализа, [**иконтекстноде**](icontextnode.md) объекты в [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="6f93a-108">A pointer to all the analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f93a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6f93a-109">Return value</span></span>

<span data-ttu-id="6f93a-110">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6f93a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f93a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f93a-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="6f93a-112">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппаналисишинтс* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="6f93a-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="6f93a-113">Этот метод возвращает пустую коллекцию, если к [**иинканализер**](iinkanalyzer.md)не присоединены узлы подсказок анализа.</span><span class="sxs-lookup"><span data-stu-id="6f93a-113">This method returns an empty collection if no analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="6f93a-114">Узел указания анализа — это [**иконтекстноде**](icontextnode.md) с типом узла контекста аналисишинт (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md) и [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="6f93a-114">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="6f93a-115">Чтобы добавить сведения о контексте в указание, используйте [**иконтекстноде:: аддпропертидата**](icontextnode-addpropertydata.md) с параметром *ппропертидатаид* , равным одному из глобальных уникальных идентификаторов (GUID) в константах [свойств указания анализа](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6f93a-115">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="6f93a-116">Чтобы определить, какие значения свойств установлены в узле контекста, используйте [**иконтекстноде:: жетпропертидатаидс**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="6f93a-116">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="6f93a-117">Чтобы найти значение свойства, используйте [**иконтекстноде:: жетпропертидата**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="6f93a-117">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f93a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6f93a-118">Requirements</span></span>



| <span data-ttu-id="6f93a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6f93a-119">Requirement</span></span> | <span data-ttu-id="6f93a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6f93a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f93a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f93a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6f93a-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6f93a-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6f93a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f93a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6f93a-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6f93a-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6f93a-125">Header</span><span class="sxs-lookup"><span data-stu-id="6f93a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f93a-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6f93a-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6f93a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6f93a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f93a-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f93a-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6f93a-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f93a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f93a-130">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="6f93a-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="6f93a-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="6f93a-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="6f93a-132">**Метод Иинканализер:: Креатеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="6f93a-132">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="6f93a-133">**Иинканализер: метод:D Елетеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="6f93a-133">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="6f93a-134">**Метод Иинканализер:: Жетаналисишинтсбинаме**</span><span class="sxs-lookup"><span data-stu-id="6f93a-134">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="6f93a-135">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="6f93a-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

