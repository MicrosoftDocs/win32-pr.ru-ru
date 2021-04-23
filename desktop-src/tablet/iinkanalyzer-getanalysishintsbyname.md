---
description: Извлекает все подсказку анализа, Иконтекстноде объекты, присоединенные к Иинканализер, с указанным именем.
ms.assetid: 15269ee0-055c-424e-be49-945f47e8a77e
title: 'Метод Иинканализер:: Жетаналисишинтсбинаме (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHintsByName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d86b18bfb8cf17097a36e35fc638dd9bd763d243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263141"
---
# <a name="iinkanalyzergetanalysishintsbyname-method"></a><span data-ttu-id="be61a-103">Метод Иинканализер:: Жетаналисишинтсбинаме</span><span class="sxs-lookup"><span data-stu-id="be61a-103">IInkAnalyzer::GetAnalysisHintsByName method</span></span>

<span data-ttu-id="be61a-104">Извлекает все подсказку анализа, [**иконтекстноде**](icontextnode.md) объекты, присоединенные к [**иинканализер**](iinkanalyzer.md) , с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="be61a-104">Retrieves all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md) and that have the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="be61a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be61a-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHintsByName(
  [in]  BSTR          hintName,
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="be61a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be61a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be61a-107">*хинтнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be61a-107">*hintName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be61a-108">Имя подсказки для поиска.</span><span class="sxs-lookup"><span data-stu-id="be61a-108">The hint name for which to search.</span></span>

</dd> <dt>

<span data-ttu-id="be61a-109">*ппаналисишинтс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be61a-109">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be61a-110">Подсказка анализа [**иконтекстноде**](icontextnode.md) объекты в [**иинканализер**](iinkanalyzer.md) с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="be61a-110">The analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) that have the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be61a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be61a-111">Return value</span></span>

<span data-ttu-id="be61a-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописных данных](classes-and-interfaces---ink-analysis.md) возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="be61a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="be61a-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be61a-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="be61a-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппаналисишинтс* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="be61a-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="be61a-115">Этот метод возвращает пустую коллекцию, если такие узлы подсказок по анализу не присоединены к [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="be61a-115">This method returns an empty collection if no such analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="be61a-116">Узел указания анализа — это [**иконтекстноде**](icontextnode.md) с типом узла контекста аналисишинт (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md) и [типы узлов контекста](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="be61a-116">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="be61a-117">Чтобы добавить сведения о контексте в указание, используйте [**иконтекстноде:: аддпропертидата**](icontextnode-addpropertydata.md) с параметром *ппропертидатаид* , равным одному из глобальных уникальных идентификаторов (GUID) в константах [свойств указания анализа](analysis-hint-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="be61a-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="be61a-118">Чтобы определить, какие значения свойств установлены в узле контекста, используйте [**иконтекстноде:: жетпропертидатаидс**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="be61a-118">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="be61a-119">Чтобы найти значение свойства, используйте [**иконтекстноде:: жетпропертидата**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="be61a-119">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be61a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="be61a-120">Requirements</span></span>



| <span data-ttu-id="be61a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="be61a-121">Requirement</span></span> | <span data-ttu-id="be61a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="be61a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be61a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be61a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be61a-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="be61a-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="be61a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be61a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be61a-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="be61a-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="be61a-127">Header</span><span class="sxs-lookup"><span data-stu-id="be61a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be61a-128"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="be61a-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="be61a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="be61a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be61a-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be61a-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="be61a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be61a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be61a-132">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="be61a-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="be61a-133">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="be61a-133">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="be61a-134">**Метод Иинканализер:: Креатеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="be61a-134">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="be61a-135">**Иинканализер: метод:D Елетеаналисишинт**</span><span class="sxs-lookup"><span data-stu-id="be61a-135">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="be61a-136">**Метод Иинканализер:: Жетаналисишинтс**</span><span class="sxs-lookup"><span data-stu-id="be61a-136">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="be61a-137">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="be61a-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

