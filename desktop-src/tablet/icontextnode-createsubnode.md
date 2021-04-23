---
description: Создает новый дочерний объект Иконтекстноде.
ms.assetid: 35d2b641-fada-418b-9374-0303c7d318e5
title: 'Метод Иконтекстноде:: Креатесубноде (Иаком. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.CreateSubNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 02c10cc50b90b96cc1ce4aadfa97f86a6c516ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897489"
---
# <a name="icontextnodecreatesubnode-method"></a><span data-ttu-id="361bc-103">Метод Иконтекстноде:: Креатесубноде</span><span class="sxs-lookup"><span data-stu-id="361bc-103">IContextNode::CreateSubNode method</span></span>

<span data-ttu-id="361bc-104">Создает новый дочерний объект [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="361bc-104">Creates a new child [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="361bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="361bc-105">Syntax</span></span>


```C++
HRESULT CreateSubNode(
  [in]  const GUID         *pNodeType,
  [out]       IContextNode **ppContextNodeCreated
);
```



## <a name="parameters"></a><span data-ttu-id="361bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="361bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="361bc-107">*пнодетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="361bc-107">*pNodeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="361bc-108">**Идентификатор GUID** , представляющий тип создаваемого [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="361bc-108">A **GUID** that represents the type of [**IContextNode**](icontextnode.md) to create.</span></span>

</dd> <dt>

<span data-ttu-id="361bc-109">*ппконтекстнодекреатед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="361bc-109">*ppContextNodeCreated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="361bc-110">Указатель на новый [**иконтекстноде**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="361bc-110">A pointer to the new [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="361bc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="361bc-111">Return value</span></span>

<span data-ttu-id="361bc-112">Описание возвращаемых значений см. в разделе [классы и интерфейсы — анализ рукописного ввода](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="361bc-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="361bc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="361bc-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="361bc-114">Чтобы избежать утечки памяти, вызовите метод [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) в \* *ппконтекстнодекреатед* , когда больше не нужно использовать контекстный узел.</span><span class="sxs-lookup"><span data-stu-id="361bc-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppContextNodeCreated* when you no longer need to use the context node.</span></span>

 

<span data-ttu-id="361bc-115">Новый [**иконтекстноде**](icontextnode.md) добавляется в коллекцию дочерних узлов этого узла контекста (см. раздел [**Иконтекстноде:: жетсубнодес**](icontextnode-getsubnodes.md)).</span><span class="sxs-lookup"><span data-stu-id="361bc-115">The new [**IContextNode**](icontextnode.md) is added to this context node's collection of child nodes (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).</span></span> <span data-ttu-id="361bc-116">При наличии существующих дочерних узлов вновь созданный **иконтекстноде** добавляется в качестве последнего дочернего узла.</span><span class="sxs-lookup"><span data-stu-id="361bc-116">When there are existing child nodes, the newly created **IContextNode** is added as the last child node.</span></span>

<span data-ttu-id="361bc-117">Список типов узлов контекста см. в разделе [типы узлов контекста](context-node-types.md).</span><span class="sxs-lookup"><span data-stu-id="361bc-117">For a list of context node types, see [Context Node Types](context-node-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="361bc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="361bc-118">Requirements</span></span>



| <span data-ttu-id="361bc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="361bc-119">Requirement</span></span> | <span data-ttu-id="361bc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="361bc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="361bc-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="361bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="361bc-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="361bc-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="361bc-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="361bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="361bc-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="361bc-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="361bc-125">Header</span><span class="sxs-lookup"><span data-stu-id="361bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="361bc-126"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="361bc-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="361bc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="361bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="361bc-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="361bc-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="361bc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="361bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="361bc-130">**иконтекстноде**</span><span class="sxs-lookup"><span data-stu-id="361bc-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="361bc-131">**Иконтекстноде::D Елетесубноде**</span><span class="sxs-lookup"><span data-stu-id="361bc-131">**IContextNode::DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)
</dt> <dt>

[<span data-ttu-id="361bc-132">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="361bc-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

