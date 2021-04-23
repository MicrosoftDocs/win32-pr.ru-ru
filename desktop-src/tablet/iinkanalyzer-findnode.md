---
description: Извлекает объект Иконтекстноде для указанного глобального уникального идентификатора (GUID).
ms.assetid: b8340666-98ab-4d8c-93c7-58ed05ef30d2
title: 'Метод Иинканализер:: Финдноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.FindNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 66771678253f1724653d87ad9c54d474a9ceceb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072777"
---
# <a name="iinkanalyzerfindnode-method"></a><span data-ttu-id="935ea-103">Метод Иинканализер:: Финдноде</span><span class="sxs-lookup"><span data-stu-id="935ea-103">IInkAnalyzer::FindNode method</span></span>

<span data-ttu-id="935ea-104">Извлекает объект [**иконтекстноде**](icontextnode.md) для указанного глобального уникального идентификатора (GUID).</span><span class="sxs-lookup"><span data-stu-id="935ea-104">Retrieves the [**IContextNode**](icontextnode.md) object for a specified globally unique identifier (GUID).</span></span>

## <a name="syntax"></a><span data-ttu-id="935ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="935ea-105">Syntax</span></span>


```C++
HRESULT FindNode(
  [in]  const GUID         *pId,
  [out]       IContextNode **ppContextNodeFound
);
```



## <a name="parameters"></a><span data-ttu-id="935ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="935ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="935ea-107">*идентификатор процесса* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="935ea-107">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="935ea-108">Идентификатор объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="935ea-108">The identifier for the [**IContextNode**](icontextnode.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="935ea-109">*ппконтекстнодефаунд* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="935ea-109">*ppContextNodeFound* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="935ea-110">Указатель на объект [**иконтекстноде**](icontextnode.md) с идентификатором *pId* .</span><span class="sxs-lookup"><span data-stu-id="935ea-110">A pointer to the [**IContextNode**](icontextnode.md) object with the *pId* identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="935ea-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="935ea-111">Return value</span></span>

<span data-ttu-id="935ea-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="935ea-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="935ea-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="935ea-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="935ea-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в *ппконтекстнодефаунд* , когда больше не нужно использовать объект.</span><span class="sxs-lookup"><span data-stu-id="935ea-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodeFound* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="935ea-115">Если такой объект [**иконтекстноде**](icontextnode.md) не существует в качестве потомка корневого узла [**Иинканализер**](iinkanalyzer.md) , возвращается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="935ea-115">If no such [**IContextNode**](icontextnode.md) object exists as a descendant of the [**IInkAnalyzer**](iinkanalyzer.md) root node, **NULL** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="935ea-116">Требования</span><span class="sxs-lookup"><span data-stu-id="935ea-116">Requirements</span></span>



| <span data-ttu-id="935ea-117">Требование</span><span class="sxs-lookup"><span data-stu-id="935ea-117">Requirement</span></span> | <span data-ttu-id="935ea-118">Значение</span><span class="sxs-lookup"><span data-stu-id="935ea-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="935ea-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="935ea-119">Minimum supported client</span></span><br/> | <span data-ttu-id="935ea-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="935ea-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="935ea-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="935ea-121">Minimum supported server</span></span><br/> | <span data-ttu-id="935ea-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="935ea-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="935ea-123">Header</span><span class="sxs-lookup"><span data-stu-id="935ea-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="935ea-124"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="935ea-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="935ea-125">DLL</span><span class="sxs-lookup"><span data-stu-id="935ea-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="935ea-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="935ea-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="935ea-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="935ea-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="935ea-128">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="935ea-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="935ea-129">**Метод Иинканализер:: Финдинклеафнодес**</span><span class="sxs-lookup"><span data-stu-id="935ea-129">**IInkAnalyzer::FindInkLeafNodes Method**</span></span>](iinkanalyzer-findinkleafnodes.md)
</dt> <dt>

[<span data-ttu-id="935ea-130">**Метод Иинканализер:: Финдинклеафнодесфорстрокес**</span><span class="sxs-lookup"><span data-stu-id="935ea-130">**IInkAnalyzer::FindInkLeafNodesForStrokes Method**</span></span>](iinkanalyzer-findinkleafnodesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="935ea-131">**Метод Иинканализер:: Финдлеафнодес**</span><span class="sxs-lookup"><span data-stu-id="935ea-131">**IInkAnalyzer::FindLeafNodes Method**</span></span>](iinkanalyzer-findleafnodes.md)
</dt> <dt>

[<span data-ttu-id="935ea-132">**Метод Иинканализер:: Финднодесофтипе**</span><span class="sxs-lookup"><span data-stu-id="935ea-132">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="935ea-133">**Метод Иинканализер:: Финднодесофтипефорстрокес**</span><span class="sxs-lookup"><span data-stu-id="935ea-133">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="935ea-134">**Метод Иинканализер:: Финднодесофтипеинсубтри**</span><span class="sxs-lookup"><span data-stu-id="935ea-134">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="935ea-135">**Метод Иинканализер:: Финднодесвискаллбакк**</span><span class="sxs-lookup"><span data-stu-id="935ea-135">**IInkAnalyzer::FindNodesWithCallBack Method**</span></span>](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[<span data-ttu-id="935ea-136">**Метод Иинканализер:: Финднодесвискаллбаккинсубтри**</span><span class="sxs-lookup"><span data-stu-id="935ea-136">**IInkAnalyzer::FindNodesWithCallBackInSubTree Method**</span></span>](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[<span data-ttu-id="935ea-137">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="935ea-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

