---
description: Возвращает идентификаторы всех соответствующих узлов контекста, связанных с данным предупреждением.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Метод Ианалисисварнинг:: Жетнодеидс (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542079"
---
# <a name="ianalysiswarninggetnodeids-method"></a><span data-ttu-id="8b461-103">Метод Ианалисисварнинг:: Жетнодеидс</span><span class="sxs-lookup"><span data-stu-id="8b461-103">IAnalysisWarning::GetNodeIds method</span></span>

<span data-ttu-id="8b461-104">Возвращает идентификаторы всех соответствующих узлов контекста, связанных с данным предупреждением.</span><span class="sxs-lookup"><span data-stu-id="8b461-104">Returns the identifiers of any relevant context nodes that are associated with this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b461-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b461-105">Syntax</span></span>


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a><span data-ttu-id="8b461-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b461-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b461-107">*пулкаунт* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8b461-107">*pulCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b461-108">Число глобально уникальных идентификаторов (GUID) в *ппнодеидс*.</span><span class="sxs-lookup"><span data-stu-id="8b461-108">The number of globally unique identifiers (GUIDs) in *ppNodeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="8b461-109">*ппнодеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8b461-109">*ppNodeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b461-110">Указатель на массив идентификаторов GUID, который определяет контекстные узлы, связанные с этим предупреждением анализа, или **значение NULL** , если с предупреждением не связаны контекстные узлы.</span><span class="sxs-lookup"><span data-stu-id="8b461-110">A pointer to an array of GUIDs that identifies the context nodes that are associated with this analysis warning, or **NULL** if no context nodes are associated with the warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b461-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b461-111">Return value</span></span>

<span data-ttu-id="8b461-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="8b461-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8b461-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b461-113">Remarks</span></span>

<span data-ttu-id="8b461-114">Если *ппнодеидс* передается как **null**, метод **жетнодеидс** возвращает значение **S \_ ОК** , а число прямоугольников возвращается в *пулкаунт*.</span><span class="sxs-lookup"><span data-stu-id="8b461-114">If *ppNodeIds* is passed as **NULL**, the **GetNodeIds** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="8b461-115">Чтобы избежать утечки памяти, используйте [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить память от \* *ппнодеидс* , если эта информация больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="8b461-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppNodeIds* when you no longer need the information.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8b461-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="8b461-116">Examples</span></span>

<span data-ttu-id="8b461-117">В следующем примере показано, как получить объекты [**иконтекстноде**](icontextnode.md) , которые находятся в [**ианалисисварнинг**](ianalysiswarning.md), `warning` и как получить только число объектов **иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="8b461-117">The following example shows how to get the [**IContextNode**](icontextnode.md) objects that are in the [**IAnalysisWarning**](ianalysiswarning.md), `warning`, and how to get only the number of **IContextNode** objects</span></span>


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="8b461-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8b461-118">Requirements</span></span>



| <span data-ttu-id="8b461-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8b461-119">Requirement</span></span> | <span data-ttu-id="8b461-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8b461-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b461-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b461-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b461-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8b461-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8b461-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b461-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b461-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8b461-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8b461-125">Header</span><span class="sxs-lookup"><span data-stu-id="8b461-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b461-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8b461-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8b461-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8b461-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b461-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b461-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8b461-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b461-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b461-130">**ианалисисварнинг**</span><span class="sxs-lookup"><span data-stu-id="8b461-130">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="8b461-131">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="8b461-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="8b461-132">**Метод Иинканализер:: Финдноде**</span><span class="sxs-lookup"><span data-stu-id="8b461-132">**IInkAnalyzer::FindNode Method**</span></span>](iinkanalyzer-findnode.md)
</dt> <dt>

[<span data-ttu-id="8b461-133">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="8b461-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

