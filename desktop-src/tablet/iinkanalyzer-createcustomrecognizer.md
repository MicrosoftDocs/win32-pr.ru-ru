---
description: Создает новый пользовательский узел распознавателя для Иинканализер.
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'Метод Иинканализер:: Креатекустомрекогнизер (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263144"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a><span data-ttu-id="c0819-103">Метод Иинканализер:: Креатекустомрекогнизер</span><span class="sxs-lookup"><span data-stu-id="c0819-103">IInkAnalyzer::CreateCustomRecognizer method</span></span>

<span data-ttu-id="c0819-104">Создает новый пользовательский узел распознавателя для [**иинканализер**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="c0819-104">Creates a new custom recognizer node for the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0819-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0819-105">Syntax</span></span>


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a><span data-ttu-id="c0819-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0819-107">*пинканалисисрекогнизерид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c0819-107">*pInkAnalysisRecognizerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0819-108">Глобальный уникальный идентификатор (GUID) [**иинканалисисрекогнизер**](iinkanalysisrecognizer.md) , для которого создается узел.</span><span class="sxs-lookup"><span data-stu-id="c0819-108">The globally unique identifier (GUID) of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) for which to create a node.</span></span>

</dd> <dt>

<span data-ttu-id="c0819-109">*ппконтекстноде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c0819-109">*ppContextNode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0819-110">Указатель на объект [**иконтекстноде**](icontextnode.md) , представляющий новый пользовательский узел распознавателя.</span><span class="sxs-lookup"><span data-stu-id="c0819-110">A pointer to the [**IContextNode**](icontextnode.md) object representing the new custom recognizer node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0819-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0819-111">Return value</span></span>

<span data-ttu-id="c0819-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c0819-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c0819-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0819-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c0819-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в ппконтекстноде, когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="c0819-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on ppContextNode when you no longer need to use the object.</span></span>

 

<span data-ttu-id="c0819-115">Этот метод создает новый [**иконтекстноде**](icontextnode.md) с типом кустомрекогнизер (см. [**Иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="c0819-115">This method creates a new [**IContextNode**](icontextnode.md) with a type of CustomRecognizer (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="c0819-116">Затем он добавляет новый пользовательский узел распознавателя в коллекцию подузлов корневого узла объекта [**иинканализер**](iinkanalyzer.md) (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md) and [**иинканализер:: жетрутноде**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="c0819-116">It then adds the new custom recognizer node to the subnodes collection of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0819-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c0819-117">Requirements</span></span>



| <span data-ttu-id="c0819-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c0819-118">Requirement</span></span> | <span data-ttu-id="c0819-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c0819-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0819-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0819-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c0819-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c0819-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c0819-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0819-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c0819-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0819-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c0819-124">Header</span><span class="sxs-lookup"><span data-stu-id="c0819-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0819-125"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c0819-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c0819-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c0819-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0819-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0819-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c0819-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0819-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0819-129">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="c0819-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c0819-130">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="c0819-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c0819-131">**иинканалисисрекогнизер**</span><span class="sxs-lookup"><span data-stu-id="c0819-131">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c0819-132">**Метод Иинканализер:: Жетинканалисисрекогнизерсбиприорити**</span><span class="sxs-lookup"><span data-stu-id="c0819-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="c0819-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="c0819-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

